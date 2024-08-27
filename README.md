# Solidity-Data-Type-Address
## Address Holds a 20-byte Ethereum address, 0xe688b84b23f322a994A53dbF8E15FA82CDB71127
it might be a smart contract that was not built to accept Ether.
## Address payable Cand send and recieve eth (transfer,send)
```solidity

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.25;
contract addressTest{
    address public myAddress = 0xAb8483F64d9C6d1EcF9b849Ae677dD3315835cb2;
    address payable  public myPayableAddress = payable(0xAb8483F64d9C6d1EcF9b849Ae677dD3315835cb2);


}
```
## Type Conversion
### In Solidity, type conversion refers to converting one data type to another when required
### Implicit conversions from address payable to address are allowed, whereas conversions from address to address payable must be explicit via payable(<address>).


## الفرق بين impilcit و expilcit
في البرمجة، التحويل الضمني (Implicit Conversion) و التحويل الصريح (Explicit Conversion) هما طريقتان لتحويل نوع البيانات من نوع إلى آخر. الاختلاف الرئيسي بينهما يعتمد على ما إذا كان التحويل يتم تلقائيًا بواسطة المترجم أو يتطلب تدخلًا مباشرًا من المبرمج.

 التحويل الضمني (Implicit Conversion)
التحويل الضمني يحدث تلقائيًا من قبل المترجم عندما يكون التحويل آمنًا، أي عندما لا يؤدي التحويل إلى فقدان البيانات أو مشاكل منطقية. يتم التحويل دون الحاجة إلى أن يقوم المبرمج بكتابة أي كود إضافي لتحويل النوع.

 التحويل الصريح (Explicit Conversion)
التحويل الصريح يتطلب تدخل المبرمج للإشارة بوضوح إلى أن التحويل مطلوب. يُستخدم هذا النوع من التحويل في الحالات التي قد تكون خطيرة أو قد تؤدي إلى فقدان بيانات، وبالتالي لا يتم إجراؤها تلقائيًا.

## Implicit conversions from address payable to address are allowed, whereas conversions from address to address payable must be explicit via payable(<address>).

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.25;
contract addressTest{
    
address payable payableAddr = payable(0xAb8483F64d9C6d1EcF9b849Ae677dD3315835cb2);
address addr = payableAddr;  // تحويل ضمني
}
```

```solidity

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.25;
contract addressTest{
    
address addr = 0xAb8483F64d9C6d1EcF9b849Ae677dD3315835cb2;
address payable payableAddr = payable(addr);  // تحويل صريح
}
```





