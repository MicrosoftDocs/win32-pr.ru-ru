---
title: UI_PKEY_TooltipTitle
description: Определяет свойство UI \_ PKEY \_ тултиптитле.
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e62fe9ebdb6418f5790e0073e32e81d7f7aba75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700635"
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

## <a name="remarks"></a>Комментарии

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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Свойства ресурса](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command. Тултиптитле**](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[UI \_ PKEY \_ тултипдескриптион](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 




