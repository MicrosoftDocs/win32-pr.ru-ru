---
title: UI_PKEY_TooltipTitle
description: Определяет свойство UI \_ PKEY \_ тултиптитле.
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6a9e479d2f963acd4041d23e2b1ca075db609f9d45b556cd2aab34e6b2c6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437789"
---
# <a name="ui_pkey_tooltiptitle"></a>UI \_ PKEY \_ тултиптитле

Определяет свойство UI \_ PKEY \_ тултиптитле.

```
propertyDescription
   name = UI_PKEY_TooltipTitle
   shellPKey = UI_PKEY_TooltipTitle
   formatID = 00000006-7363-696e-8441798acf5aebb7
   propID = 6
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Remarks

UI \_ PKEY \_ тултиптитле используется приложением для запроса подсказки вкладок, групп, кнопок, элементов коллекции и других элементов управления ленты.

Значение свойства — это строка, ограниченная любой последовательностью символов, включая пробелы и символы разрыва строки.

> [!Note]  
> Используйте ссылку на символ XML универсальной кодировки (UCS) `&#xA;` для указания разрыва строки.

 

Выравнивание по правому краю не поддерживается.

Максимальная длина пользовательского интерфейса \_ PKEY \_ тултиптитле не ограничена.

Чтобы отобразить амперсанд во всплывающей подсказке, необходимо экранировать Специальный символ с двойным амперсандом ( `&&` ), как показано в следующем примере.


```XML
<Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства ресурса](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command. Тултиптитле**](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[UI \_ PKEY \_ тултипдескриптион](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 




