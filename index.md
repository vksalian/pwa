<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
	<meta name="theme-color" content="#3f51b5"/>
    <title>HH2 Programmer / Debugger</title>
    <base href="/">
    <link href="https://fonts.googleapis.com/css?family=Roboto:400,700" rel="stylesheet">
    <link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">
    <link rel="stylesheet" href="https://code.getmdl.io/1.3.0/material.indigo-deep_orange.min.css"/>
    <link rel="stylesheet" href="src/css/app.css">
    <link rel="stylesheet" href="src/css/feed.css">
    <link rel="manifest" href="manifest.json">
    <link rel="apple-touch-icon" href="/src/images/icons/apple-icon-180x180.png">
    <link rel="shortcut icon" href="favicon.ico" type="image/x-icon"/>

</head>
<body>

<div id="app">
    <div class="mdl-layout mdl-js-layout mdl-layout--fixed-header">
        <header class="mdl-layout__header">
            <div class="mdl-layout__header-row">
                <!-- Title -->
                <span class="mdl-layout-title">HH2 Programmer / Debugger</span>
                <!-- Add spacer, to align navigation to the right -->
                <div class="mdl-layout-spacer"></div>
                <!-- Navigation. We hide it in small screens. -->
                <nav class="mdl-navigation mdl-layout--large-screen-only">
                    <a class="mdl-navigation__link" href="/">Program</a>
                    <a class="mdl-navigation__link" href="/">Debug</a>
                    <a class="mdl-navigation__link" href="/">Configuration</a>
                    <div class="drawer-option">
                        <button
                            class="enable-notifications mdl-button mdl-js-button mdl-button--raised mdl-button--colored mdl-color--accent">
                            Enable Notifications
                        </button>
                    </div>
                </nav>
            </div>
        </header>
        <div class="mdl-layout__drawer">
            <span class="mdl-layout-title">HH2 Programmer / Debugger</span>
            <nav class="mdl-navigation">
                <a class="mdl-navigation__link" href="/">Program</a>
                <a class="mdl-navigation__link" href="/">Debug</a>
                <a class="mdl-navigation__link" href="/">Configuration</a>
                <div class="drawer-option">
                    <button
                        class="enable-notifications mdl-button mdl-js-button mdl-button--raised mdl-button--colored mdl-color--accent">
                        Enable Notifications
                    </button>
                </div>
            </nav>
        </div>
        <main class="mdl-layout__content mat-typography">
            <div id="create-post">
                <form>
                    <div class="input-section mdl-textfield mdl-js-textfield mdl-textfield--floating-label">
                        <input class="mdl-textfield__input" type="text" id="title">
                        <label class="mdl-textfield__label" for="title" name="title">Title</label>
                    </div>
                    <div class="input-section mdl-textfield mdl-js-textfield mdl-textfield--floating-label"
                         id="manual-location">
                        <input class="mdl-textfield__input" type="text" id="location">
                        <label class="mdl-textfield__label" for="location" name="location">Location</label>
                    </div>
                    <br>
                    <div>
                        <button
                            class="mdl-button mdl-js-button mdl-button--raised mdl-button--colored mdl-color--accent"
                            type="submit" id="post-btn">Post!
                        </button>
                    </div>
                    <br>
                    <div>
                        <button class="mdl-button mdl-js-button mdl-button--fab" id="close-create-post-modal-btn"
                                type="button">
                            <i class="material-icons">close</i>
                        </button>
                    </div>
                </form>
            </div>
            <button style="margin:5px" id="connectButton">Connect Serialport</button>
            <button style="margin:5px" id="sendI2C">Send HH2 I2C packet</button>
            <div>
                <h1>
                    <textarea style="left: 30px;
                    right: 30px;
                    top: 30px;
                    bottom: 30px;" class="mdl-textfield__label" id="target" name="logwindow" rows="10" cols="50">Application log goes here...</textarea>
                </h1>
            </div>

            <!-- <p>
                <small class="mdl-textfield__label">Serialport Connection detection</small>
            </p> -->

            <img src="src/images/main-image.jpg"
                 srcset="src/images/main-image-lg.jpg 1200w,
                         src/images/main-image.jpg 900w,
                         src/images/main-image-sm.jpg 480w"
                 alt="Ducks everywhere"
                 class="main-image">
            <div class="page-content">
                <h5 class="text-center mdl-color-text--primary">SiliConch Systems</h5>
                <div class="text-center mdl-color-text--primary" id="shared-moments"></div>
            </div>
            <div class="floating-button">
                <button class="mdl-button mdl-js-button mdl-button--fab mdl-button--colored"
                        id="share-image-button">
                    <i class="material-icons">add</i>
                </button>
            </div>
            <div id="confirmation-toast" aria-live="assertive" aria-atomic="true" aria-relevant="text"
                 class="mdl-snackbar mdl-js-snackbar">
                <div class="mdl-snackbar__text"></div>
                <button type="button" class="mdl-snackbar__action"></button>
            </div>
        </main>
    </div>
</div>
<script defer src="src/lib/material.min.js"></script>
<script src="src/js/app.js"></script>
<script src="src/js/feed.js"></script>
</body>
</html>
