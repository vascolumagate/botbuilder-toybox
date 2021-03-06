


#  botbuilder-toybox-prompts


## Index

### Enumerations

* [ListStyle](enums/botbuilder_toybox_prompts.liststyle.md)


### Interfaces

* [AttachmentPrompt](interfaces/botbuilder_toybox_prompts.attachmentprompt.md)
* [ChoicePrompt](interfaces/botbuilder_toybox_prompts.choiceprompt.md)
* [ConfirmChoices](interfaces/botbuilder_toybox_prompts.confirmchoices.md)
* [ConfirmPrompt](interfaces/botbuilder_toybox_prompts.confirmprompt.md)
* [DatetimePrompt](interfaces/botbuilder_toybox_prompts.datetimeprompt.md)
* [FoundDatetime](interfaces/botbuilder_toybox_prompts.founddatetime.md)
* [NumberPrompt](interfaces/botbuilder_toybox_prompts.numberprompt.md)
* [TextPrompt](interfaces/botbuilder_toybox_prompts.textprompt.md)


### Type aliases

* [ChoicePromptValidator](#choicepromptvalidator)
* [PromptValidator](#promptvalidator)


### Functions

* [createAttachmentPrompt](#createattachmentprompt)
* [createChoicePrompt](#createchoiceprompt)
* [createConfirmPrompt](#createconfirmprompt)
* [createDatetimePrompt](#createdatetimeprompt)
* [createNumberPrompt](#createnumberprompt)
* [createTextPrompt](#createtextprompt)



---
## Type aliases
<a id="choicepromptvalidator"></a>

###  ChoicePromptValidator

**Τ ChoicePromptValidator**:  *`function`* 

*Defined in [packages/botbuilder-toybox-prompts/lib/choicePrompt.d.ts:57](https://github.com/Stevenic/botbuilder-toybox/blob/848ed38/packages/botbuilder-toybox-prompts/lib/choicePrompt.d.ts#L57)*



Signature of a handler that can be passed to a prompt to provide additional validation logic or to customize the reply sent to the user when their response is invalid.
*__param__*: Type of output that will be returned by the validator. This can be changed from the input type by the validator.


#### Type declaration
►(context: *[BotContext]()*, value: *[FoundChoice]()⎮`undefined`*, choices: *(`string`⎮[Choice]())[]*): [Promiseable]()`O`⎮`undefined`



**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| context | [BotContext]()   |  Context for the current turn of conversation. |
| value | [FoundChoice]()⎮`undefined`   |  The value that was recognized or `undefined` if not recognized. |
| choices | (`string`⎮[Choice]())[]   |  Array of choices that should be prompted for. |





**Returns:** [Promiseable]()`O`⎮`undefined`






___

<a id="promptvalidator"></a>

###  PromptValidator

**Τ PromptValidator**:  *`function`* 

*Defined in [packages/botbuilder-toybox-prompts/lib/textPrompt.d.ts:29](https://github.com/Stevenic/botbuilder-toybox/blob/848ed38/packages/botbuilder-toybox-prompts/lib/textPrompt.d.ts#L29)*



Signature of a handler that can be passed to a prompt to provide additional validation logic or to customize the reply sent to the user when their response is invalid.
*__param__*: Type of value that will recognized and passed to the validator as input.

*__param__*: Type of output that will be returned by the validator. This can be changed from the input type by the validator.


#### Type declaration
►(context: *[BotContext]()*, value: *`R`⎮`undefined`*): [Promiseable]()`O`⎮`undefined`



**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| context | [BotContext]()   |  Context for the current turn of conversation. |
| value | `R`⎮`undefined`   |  The value that was recognized or `undefined` if not recognized. |





**Returns:** [Promiseable]()`O`⎮`undefined`






___


## Functions
<a id="createattachmentprompt"></a>

###  createAttachmentPrompt

► **createAttachmentPrompt**O(validator?: *[PromptValidator](#promptvalidator)[Attachment]()[], `O`*): [AttachmentPrompt](interfaces/botbuilder_toybox_prompts.attachmentprompt.md)`O`



*Defined in [packages/botbuilder-toybox-prompts/lib/attachmentPrompt.d.ts:26](https://github.com/Stevenic/botbuilder-toybox/blob/848ed38/packages/botbuilder-toybox-prompts/lib/attachmentPrompt.d.ts#L26)*



Creates a new prompt that asks the user to upload one or more attachments.


**Type parameters:**

#### O 
**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| validator | [PromptValidator](#promptvalidator)[Attachment]()[], `O`   |  (Optional) validator for providing additional validation logic or customizing the prompt sent to the user when invalid. |





**Returns:** [AttachmentPrompt](interfaces/botbuilder_toybox_prompts.attachmentprompt.md)`O`





___

<a id="createchoiceprompt"></a>

###  createChoicePrompt

► **createChoicePrompt**O(validator?: *[ChoicePromptValidator](#choicepromptvalidator)`O`*): [ChoicePrompt](interfaces/botbuilder_toybox_prompts.choiceprompt.md)`O`



*Defined in [packages/botbuilder-toybox-prompts/lib/choicePrompt.d.ts:62](https://github.com/Stevenic/botbuilder-toybox/blob/848ed38/packages/botbuilder-toybox-prompts/lib/choicePrompt.d.ts#L62)*



Creates a new prompt that asks the user to select from a list of choices.


**Type parameters:**

#### O 
**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| validator | [ChoicePromptValidator](#choicepromptvalidator)`O`   |  (Optional) validator for providing additional validation logic or customizing the prompt sent to the user when invalid. |





**Returns:** [ChoicePrompt](interfaces/botbuilder_toybox_prompts.choiceprompt.md)`O`





___

<a id="createconfirmprompt"></a>

###  createConfirmPrompt

► **createConfirmPrompt**O(validator?: *[PromptValidator](#promptvalidator)`O`*): [ConfirmPrompt](interfaces/botbuilder_toybox_prompts.confirmprompt.md)`O`



*Defined in [packages/botbuilder-toybox-prompts/lib/confirmPrompt.d.ts:54](https://github.com/Stevenic/botbuilder-toybox/blob/848ed38/packages/botbuilder-toybox-prompts/lib/confirmPrompt.d.ts#L54)*



Creates a new prompt that asks the user to answer a yes/no question.


**Type parameters:**

#### O 
**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| validator | [PromptValidator](#promptvalidator)`O`   |  (Optional) validator for providing additional validation logic or customizing the prompt sent to the user when invalid. |





**Returns:** [ConfirmPrompt](interfaces/botbuilder_toybox_prompts.confirmprompt.md)`O`





___

<a id="createdatetimeprompt"></a>

###  createDatetimePrompt

► **createDatetimePrompt**O(validator?: *[PromptValidator](#promptvalidator)[FoundDatetime](interfaces/botbuilder_toybox_prompts.founddatetime.md)[], `O`*): [DatetimePrompt](interfaces/botbuilder_toybox_prompts.datetimeprompt.md)`O`



*Defined in [packages/botbuilder-toybox-prompts/lib/datetimePrompt.d.ts:46](https://github.com/Stevenic/botbuilder-toybox/blob/848ed38/packages/botbuilder-toybox-prompts/lib/datetimePrompt.d.ts#L46)*



Creates a new prompt that asks the user to reply with a date or time.


**Type parameters:**

#### O 
**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| validator | [PromptValidator](#promptvalidator)[FoundDatetime](interfaces/botbuilder_toybox_prompts.founddatetime.md)[], `O`   |  (Optional) validator for providing additional validation logic or customizing the prompt sent to the user when invalid. |





**Returns:** [DatetimePrompt](interfaces/botbuilder_toybox_prompts.datetimeprompt.md)`O`





___

<a id="createnumberprompt"></a>

###  createNumberPrompt

► **createNumberPrompt**O(validator?: *[PromptValidator](#promptvalidator)`number`, `O`*): [NumberPrompt](interfaces/botbuilder_toybox_prompts.numberprompt.md)`O`



*Defined in [packages/botbuilder-toybox-prompts/lib/numberPrompt.d.ts:26](https://github.com/Stevenic/botbuilder-toybox/blob/848ed38/packages/botbuilder-toybox-prompts/lib/numberPrompt.d.ts#L26)*



Creates a new prompt that asks the user to reply with a number.


**Type parameters:**

#### O 
**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| validator | [PromptValidator](#promptvalidator)`number`, `O`   |  (Optional) validator for providing additional validation logic or customizing the prompt sent to the user when invalid. |





**Returns:** [NumberPrompt](interfaces/botbuilder_toybox_prompts.numberprompt.md)`O`





___

<a id="createtextprompt"></a>

###  createTextPrompt

► **createTextPrompt**O(validator?: *[PromptValidator](#promptvalidator)`string`, `O`*): [TextPrompt](interfaces/botbuilder_toybox_prompts.textprompt.md)`O`



*Defined in [packages/botbuilder-toybox-prompts/lib/textPrompt.d.ts:34](https://github.com/Stevenic/botbuilder-toybox/blob/848ed38/packages/botbuilder-toybox-prompts/lib/textPrompt.d.ts#L34)*



Creates a new prompt that asks the user to enter some text.


**Type parameters:**

#### O 
**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| validator | [PromptValidator](#promptvalidator)`string`, `O`   |  (Optional) validator for providing additional validation logic or customizing the prompt sent to the user when invalid. |





**Returns:** [TextPrompt](interfaces/botbuilder_toybox_prompts.textprompt.md)`O`





___


