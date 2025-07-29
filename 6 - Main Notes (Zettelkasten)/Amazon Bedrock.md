2025-07-29 14:58

### Status: #baby

### Tags: [[machine-learning]] [[AWS]]

# What is Amazon Bedrock

According to Amazon, it is a comprehensive, secure and flexible AWS service to create and building genAI apps and agents. It connects to leading foundation models (FMs), services for deploy and operate and tools for fine-tuning, safeguard and optimizing models.

So basically, is a built-in, all-in-one AI platform that gives you access to pre-built models and data and allow faster deployment due to this nature.

It also provides it's built-in orchestration called [Amazon Bedrock Flows] that is a visual builder to connect the prompts, agents, the guardrails you requested for your app, etc.

## Bedrock capabilities

### Model choice

Bedrock provies access to more than 100 foundational models from leading AI companies, all with evaluation tools to pick the best model given the perfomance and cost needs.

Allows the usage of many models from most AI companies such as Anthropic, Amaozn, DeepSeek, Meta, MistralAI etc.
#### Foundational Model
A [[Foundational Model]] is an AI model with many number of parameters and it is trained on a massive amount of data. A FM can generate from text to image data, and can convert inputs into [[embeddings]]. This [Amazon](https://docs.aws.amazon.com/bedrock/latest/userguide/foundation-models-reference.html) doc page provides more information on FM.

To start using a FM, you must request access to a model before using it. After that, you can use the FM in the following way:
 - Run inference by sending prompts and generating responses;
 - Evaluate the models to compare outputs and determine which models is the best for your use-case
 - Set up a knowledge base that can query and evaluate your own data and text to then use it to generate responses to queries
 - Create agents by using a model to run the inference and make the orchestration work
 - Customize a model by feeding training and validation data to adjust to parameters for your use-case.
 - 






# References

[Amazon Bedrock documentation](https://docs.aws.amazon.com/bedrock/latest/userguide/foundation-models-reference.html)

[Amazon Bedrock page](https://aws.amazon.com/bedrock/)






