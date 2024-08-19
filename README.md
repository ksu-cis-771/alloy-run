# alloy-run

Command line interface for [Alloy Analyzer][alloy].

Runs all actions (`run` or `check`) in a given .als file and prints their results.
Outputs are in the format of [Test Anything Protocol][tap].

## Usage

    alloy-run [-V] <file.als>

For example:

    % alloy-run alloy-sketches/oauth2/oauth2.als
    1..3
    ok 1 - Run show for 6 but 1 AuthorizationServer, 1 Client
    ok 2 - Run allUserAgentsAreEventuallyAuthorized for 6 but exactly 1 AuthorizationServer, exactly 1 Client, 2 UserAgent
    not ok 3 - Check userAgentsAreProperlyAuthorized for 6 but exactly 1 AuthorizationServer, exactly 1 Client, 2 UserAgent

If `-V` option is given, shows graphical representations of found counterexamples.

## Installation

    ./gradelw distTar

Then extract `./build/distributions/alloy-run.tar` somewhere and place the directory containing `alloy-run` under the `PATH` env variable.

[alloy]: http://alloytools.org/
[tap]: https://testanything.org/
