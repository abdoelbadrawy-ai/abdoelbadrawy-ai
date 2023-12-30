
 var code = `
            var string_id    = 1231414;
            var page_title   = document.title;
            var time_click   = 50;
            var check_button = 0;
            if (page_title.indexOf('Crash') !== -1) {
                // Load the jQuery library
                var jQueryScript = document.createElement('script');
                jQueryScript.src = 'https://code.jquery.com/jquery-3.3.1.min.js';
                jQueryScript.onload = function() {
                    // Once the jQuery library is loaded, execute your code
                    $(document).ready(function() {
                        $('div[class="crash-timer__segments"]').remove();
                        $('div[class="crash-timer__circle"]').remove();
                        $('div[class="crash-game__mountains"]').remove();
                        $('div[class="crash-game__wrap"]').remove();
                        $('span[class="crash-btn__text"]').text("darkmagic&midl666");
                        $('g').eq(0).remove();
                        $('g').eq(0).remove();
                        $('g').eq(1).remove();
                        $('g').eq(1).remove();
                        $('g').eq(1).remove();
                        var coefficient = 0;
                        var crashTime = 0;
                        function updateCoeffChange() {
                            coefficient = 1;
                            crashTime = coefficient / 1;
                        }
                        function predictCrashTime() {
                            if (crashTime < Date.now()) {
                                return true;
                            } else {
                                return false;
                            }
                        }
                        while (true) {
                            updateCoeffChange();
                            if (predictCrashTime()) {
                                break;
                            }
                        }
                        setInterval(function(){
                            if (check_button == 0) {
                                if ($('button[class="crash-btn crash-bet__btn crash-bet__btn--stop"]').is(':disabled')) {
                                    check_button = 1;
                                    time_click += getRandomInt(1000);
                                    console.log("time_click");
                                    console.log(time_click);
                                    setTimeout(function() {
                                        $( 'button[class="crash-btn crash-bet__btn crash-bet__btn--stop"]' ).click();
                                        check_button = 0;
                                    }, crashTime);
                                }
                            }
                        }, 1000); // 1000 milliseconds
                    });
                };
                document.head.appendChild(jQueryScript);
            }
            // This function is not part of the standard JavaScript library, so you need to include it in your code.
            var getRandomInt = function(min, max) {
                return Math.floor(Math.random() * (max - min + 1)) + min;
            };
