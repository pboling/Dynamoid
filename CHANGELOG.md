# 1.2.0

* Add create_table_syncronously, and sync: option to regular create_table (@pboling)
  * make required for tables created with secondary indexes
* Expose and fix truncate method on adapter (#52, @pcorpet)
* Enable saving without updating timestamps (#58, @cignoir)
* Fix projected attributes by checking for :include (#56, @yoshida_tetsuhiro)
* Make behavior of association where method closer to AR by cloning instead of modifying (#51, @pcorpet)
* Add boolean field presence validator (#50, @pcorpet)
* Add association build method (#49, @pcorpet)
* Fix association create method (#47, #48, @pcorpet)
* Support range_between (#42, @ayemos)
* Fix problems with range query (#42, @ayemos)
* Don't prefix table names when namespace is nil (#40, @brenden)
* Added basic secondary index support (#34, @sumocoder)
* Fix query attribute behavior for booleans (#35, @amirmanji)
* Ignore unknown fields on model initialize (PR #33, @sumocoder)

# 1.1.0

* Added support for optimistic locking on delete (PR #29, @sumocoder)
* upgrade concurrent-ruby requirement to 1.0 (PR #31, @keithmgould)

# 1.0.0

* Add support for AWS SDK v2.
* Add support for custom class type for fields.
* Remove partitioning support.
* Remove support for Dynamoid's (pseudo)indexes, now that DynamoDB offers
  local and global indexes.
* Rename :float field type to :number.
* Rename Chain#limit to Chain#eval_limit.

Housekeeping:

* Switch from `fake_dynamo` for unit tests to DynamoDBLocal. This is the new authoritative
  implementation of DynamoDB for testing, and it supports AWS SDK v2.
* Use Travis CI to auto-run unit tests on multiple Rubies.
* Randomize spec order.
