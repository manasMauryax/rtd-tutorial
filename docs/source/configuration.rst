Configuration
============

**EDIT docs/source/configuration.rst in order to make changes here**

Training config is defined in yaml formatted files. See data/config_lorem_ipsum.yaml. These configs are very explicit specifying all training parameters to keep model trainings as transparent and reproducible as possible. Each config setting is reflected in pydantic classes in src/llm_gym/config/*.py. In the config you need to define which config classes to load in field type_hint. This specifies the concrete class. A second parameter, config, then takes all the constructor arguments for that config class. This way it is easy to change i.e. DataLoaders while still having input validation in place.