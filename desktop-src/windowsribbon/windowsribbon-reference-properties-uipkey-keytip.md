---
title: UI_PKEY_Keytip
description: Определяет свойство UI \_ PKEY \_ keytip.
ms.assetid: 7af4abcb-abb0-466a-bc58-274fa18b79af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550bfac9b341d14b495c73e4426e8143d91d8e19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986543"
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

## <a name="remarks"></a>Комментарии

UI \_ PKEY \_ KeyTip используется приложением для запроса сочетания клавиш для элемента управления ленты.

Это значение свойства является строкой, состоящей из любой последовательности символов, включая пробелы.

Значение UI \_ PKEY \_ KeyTip выступает в качестве сочетания клавиш для команды, если эта команда не предоставлена через пункт меню. В этом случае платформа игнорирует \_ \_ значение KeyTip UI PKEY и вместо этого использует символ, предшествующий амперсанду, как указано в [ \_ \_ метке](windowsribbon-reference-properties-uipkey-label.md) [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) или UI PKEY. Если амперсанд не указан с помощью **команды Command. лабелтитле** или \_ метки PKEY пользовательского интерфейса \_ , то KeyTip или сочетания клавиш не предоставляются.

Максимальная длина пользовательского интерфейса \_ PKEY \_ KeyTip не ограничена.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Свойства ресурса](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command. keytip**](windowsribbon-element-command-keytip.md)
</dt> </dl>

 

 




