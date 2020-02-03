# mqtt-async-client-rs

An MQTT 3.1.1 client written in Rust, using async functions and tokio.

* Repository: <https://github.com/fluffysquirrels/mqtt-async-client-rs>
* Documentation: <https://docs.rs/mqtt-async-client>
* Cargo crate: <https://crates.io/crates/mqtt-async-client>
* CI builds on Travis CI: <https://travis-ci.com/fluffysquirrels/mqtt-async-client-rs>

Pull requests and Github issues welcome!

## To run automated tests

Simply run `cargo test`.

The integration tests require an MQTT broker to run against, see the
instructions in `${REPO}/tests/integration_test.rs`.

## Run the test command-line app

Run `cargo run --bin mqttc` to print usage.

The test app requires an MQTT broker to run against, see the
instructions in `${REPO}/tests/integration_test.rs`.

Run `cargo run --bin mqttc -- --host localhost publish topic payload`
to publish payload `payload` to topic `topic`.

Run `RUST_LOG="info" cargo run --bin mqttc -- --host localhost subscribe topic`
to subscribe to topic `topic` and print any messages that are published to it.
