## Json Schema and Json Validation

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1647930168419/XI55BhfeM.png)A sample json schema
A discussion in one of my office meetings, led me to think and write about Json Schema. Every post I write is an attempt to get a better understanding of the topic and keep that as a reference for my future projects.

> How do you validate the complex nested Json data files?

One approach, I can think of is defining a schema and validating the JSON data against it. I had used this approach to validate a avro schema.

Define JSON Schema:
-------------------

This is the most time consuming part but if done right, the JSON validation is cakewalk. Json Schema came to my rescue. After reading, I was able to understand most of the concepts and write my own [schema](https://github.com/anilkulkarni87/JsonSchema/blob/master/src/main/resources/customer_schema.json) and also validate a couple of data files. Below are some of the things you can define/achieve:

- Mandatory values.
- Nested objects and fields.
- Data type and additional criteria: 
  - String can be of format:email/uuid etc.
  - String can match with pattern.
  - Integer – Can have max , multipleOf.

JSON Validation
---------------

I leveraged a gradle plugin to implement the validation as part of the build. So that our next steps of the build are executed only if the Validation task is successful. The errors printed are very precise and easy to understand. You can find this sample project on my [github](https://github.com/anilkulkarni87/JsonSchema).

![Output from the gradle plugin.](https://cdn.hashnode.com/res/hashnode/image/upload/v1647930170978/vVg-SUnGPN.png)Validation Output
#### Next steps and other thoughts:

- To add examples of different schemas Eg: Use definition and references.
- One can also generate schema from a json and then improvise it.
- For the first time, I used github actions to build the project.
- I should write more about some of my other [learnings](https://anilkulkarni.com/2019/12/learnings-from-my-last-assignment/).

The post [Json Schema and Json Validation](https://anilkulkarni.com/2020/02/json-schema-and-json-validation/) appeared first on [Anil Kulkarni | Blog](https://anilkulkarni.com).