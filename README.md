# pushfeedback-react

Integrate PushFeedback feedback widget into your React project.

## Prerequisites

Before proceeding, ensure you have the following:

- A PushFeedback account ([Sign up for free](https://docs.pushfeedback.com/)).
- A project set up in your PushFeedback dashboard. Follow the Quickstart guide if you haven't done this yet.
- A React application with Node.js installed.

## Installation

1. Open your terminal or command prompt.
2. Navigate to your project's root directory:

    ```bash
    cd path/to/your/project
    ```

    Replace `path/to/your/project` with the actual path to your project directory.

3. Install PushFeedback by running:

    ```bash
    npm install pushfeedback-react
    ```

    > **INFO**: If you're using yarn, use `yarn add pushfeedback-react` instead.

## Embedding the Feedback Button

1. In the main component where you want the feedback button to appear (commonly `src/App.js`), import and embed the PushFeedback button:

    ```jsx
    import React, { useEffect } from 'react';
    import { FeedbackButton } from 'pushfeedback-react';
    import { defineCustomElements } from 'pushfeedback/loader';
    import 'pushfeedback/dist/pushfeedback/pushfeedback.css';

    function App() {
        
        useEffect(() => {
            if (typeof window !== 'undefined') {
            defineCustomElements(window);
            }
        }, []);

        return (
            <div className="App">
                {/* Other components and content */}
                <FeedbackButton project="<YOUR_PROJECT_ID>" button-position="bottom-right" modal-position="bottom-right" button-style="light">Feedback</FeedbackButton>
            </div>
        );
    }

    export default App;
    ```

    Replace `<YOUR_PROJECT_ID>` with your project's ID from the PushFeedback dashboard.

2. Start your React application:

    ```bash
    npm start
    ```

    Or if you're using yarn:

    ```bash
    yarn start
    ```

    After compiling successfully, the feedback button should be visible and functional on your site.

## Configuration

For further customization and to explore additional features, refer to the [Configuration section](https://docs.pushfeedback.com/category/configuration).

## Support

Need assistance? Contact [PushFeedback Support](https://docs.pushfeedback.com/support) for help.
