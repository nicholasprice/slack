% SEND2SLACK Send text message and optional file to slack from Matlab.
%
% USAGE
% send2slack('Hello, world!')
% send2slack('Hello, world!', 'file', 'pics/theworld.jpg')
% send2slack('Hello, world!', 'file', 'pics/theworld.jpg','url',mySecretURL,'token',mySecretToken','channel',myChannelID)
%
% - messages are handled by webwrite
% - files are handled by operating system call to curl
%
% NOTES ON SLACK SETUP
% We need to create a channel and App in Slack, and either pass the
% relevant (private) tokens as inputs to this function, or put them in the
% function "getSlackParam"
% 1. make a new channel to receive your messages (or use an existing
% channel). You need the channel ID - it's an alphanumeric code that you
% can get in the Channel Details section - Right-click, or hit the drop-down
% next to the channel name. Code is at the bottom of the "About" section
% 2. Make a new App - follow the instructions here - https://api.slack.com/apps
% 3. get the URL for the Incoming Webhook (under Features) and put it in
% the file "getSlackParam"
% 4. Edit Features > OAuth and Permissions
%   Add a Bot Token Scope "files:write"
% 5. Install your App (the website should prompt you to do this)
% 6. In your new slack channel, invite the app: /invite @yourAppName
% You should now be in business
%
% Nicholas Price 20210909
