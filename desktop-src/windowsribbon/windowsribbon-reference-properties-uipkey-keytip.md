---
title: UI_PKEY_Keytip
description: Определяет свойство UI \_ PKEY \_ keytip.
ms.assetid: 7af4abcb-abb0-466a-bc58-274fa18b79af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940a855561dfd30dfbf063323f4b86b03561163c4fbf34f9db08be4eb3e1ece3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028612"
---
# <a name="ui_pkey_keytip"></a>UI \_ PKEY \_ keytip

Определяет свойство UI \_ PKEY \_ keytip.

```
propertyDescription
   name = UI_PKEY_Keytip
   shellPKey = UI_PKEY_Keytip
   formatID = 00000003-7363-696e-8441798acf5aebb7
   propID = 3
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Remarks

UI \_ PKEY \_ KeyTip используется приложением для запроса сочетания клавиш для элемента управления ленты.

Это значение свойства является строкой, состоящей из любой последовательности символов, включая пробелы.

Значение UI \_ PKEY \_ KeyTip выступает в качестве сочетания клавиш для команды, если эта команда не предоставлена через пункт меню. В этом случае платформа игнорирует \_ \_ значение KeyTip UI PKEY и вместо этого использует символ, предшествующий амперсанду, как указано в [ \_ \_ метке](windowsribbon-reference-properties-uipkey-label.md) [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) или UI PKEY. Если амперсанд не указан с помощью **команды Command. лабелтитле** или \_ метки PKEY пользовательского интерфейса \_ , то KeyTip или сочетания клавиш не предоставляются.

Максимальная длина пользовательского интерфейса \_ PKEY \_ KeyTip не ограничена.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства ресурса](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command. keytip**](windowsribbon-element-command-keytip.md)
</dt> </dl>

 

 




