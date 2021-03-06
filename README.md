# Google Assistant Ruby

Write Google Assistant actions in Ruby.

## Installation

```rb
gem "google_assistant"
```

## Usage

Details to come. Basically, you can use this in rails like so:

```rb
class GoogleAssistantController < ApplicationController

  def conversation
    assistant_response = GoogleAssistant.new(params, response).respond_to do |assistant|
      assistant.intent.main do
        assistant.ask("<speak>I can speak! Can you hear me?</speak>")
      end

      assistant.intent.text do
        assistant.tell("<speak>I can respond, too!</speak>")
      end
    end

    render assistant_response
  end
end
```

Check out Google's instructions at https://developers.google.com/actions/develop/sdk/getting-started. You'll need to add an `actions.json` file, but Google's instructions pretty much cover deploying a Google Assistant action.

Check out https://github.com/armilam/google_assistant_example for a simple example of this gem in action.
