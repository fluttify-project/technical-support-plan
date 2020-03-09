Technical Support Plan for Fluttify Project
V0.0.1-pre3 by [yohom] (https://github.com/yohom)

## Basic instructions
- Settle first, charge later.
- No settlement, no charge.
- Resolved, no charge, blocked.
- Confirmed work orders (bugs, new features, etc.) will be processed according to the highest priority, paid work order internal priority in chronological order.

## How do I initiate a technical support request?
- Please file a new issue in the [technical-support-plan]((https://github.com/fluttify-project/technical-support-plan/issues/new?assignees=yohom&labels=&template=------.md&title=)) repository according to the template to initiate the technical support request.
- Contact [yohom] (https://github.com/yohom), email yohombao@qq.com, or add qq group 938842596.
- After the technical support request is approved, the issue is moved to the corresponding plug-in repository and progress is tracked under this issue.

## Plans
### Consultation ¥50
- The package is valid from the consultation time on the first day to the same time on the next day.

### Bug fixed ¥100+
- Confirm different costs according to the difficulty of bug repair.

### New features
The new function differentiates the price according to the implementation complexity, and the complexity calculation formula is as follows:

> Can be directly in the method of channel transmission type called *simple type*, the other is called *complex type*, a specific definition see [Flutter official document](https://flutter.dev/docs/development/platform-integration/platform-channels#codec).
>
> final price = ¥50 + (number of simple parameters × ¥20 / unit) + (number of simple return values × ¥20 / unit) + (number of compound parameters × ¥50 / unit) + (number of compound return values × ¥50 / unit)
>
For example, the existing Dart method to be implemented is signed as follows:

```
(simple return value) (complex parameter) (simple parameter)
          ↓                      ↓                ↓
        String exampleMethod(SomeClass object, String String);
```

Then you need:

Basic ¥50 + (number of simple parameters 1 × 20¥/) + (number of simple return values 1 × 20¥/) + (number of complex parameters 1 × 50¥/) + (number of complex return values 0 × 50¥/) = ¥50 + ¥20 + ¥20 + ¥50 = ¥140

Other types of methods and so on.

### Business function reference implementation ¥200+
- Business function implementation refers to the combination of functions under specific business scenarios, such as the sending location function of WeChat, which needs to be realized with search plug-in and map plug-in. This scheme provides reference implementation.

### New plugin development
- New plug-in development needs into plug-in, plug-in generated after the completion of the uploaded to [organization](https://github.com/fluttify-project). The subsequent new feature request can go `new features` scheme.
- the cost of plug-in generation is calculated according to the number of interfaces, and the unit price is to be determined.

### Reward mode
Later conditions allow the reward model to be opened, that is, all the above technical support programs can participate as the support party.

Users solve problems quickly, contributors get paid, and owners continue to iterate on projects. This is my vision for the health of the open source community :).