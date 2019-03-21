# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ..

step1. Find all the test cases and try to put it in the alpaca_test.rb file where once the rails tests command is made to run we can do the testing for those test cases

And run the command rails teststest "#make_a_sweater" do
    nata = Alpaca.find_by(name: "Natalama")
    baldy = Alpaca.find_by(name: "Baldy")
    nata_starting_sweaters = nata.sweaters_made
    baldy_starting_sweaters = baldy.sweaters_made
    nata.make_a_sweater
    baldy.make_a_sweater
    assert nata.sheared
    assert_equal nata_starting_sweaters + 1, nata.sweaters_made
    assert_equal baldy_starting_sweaters, baldy.sweaters_made
  end
