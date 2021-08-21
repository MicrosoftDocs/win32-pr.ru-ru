---
title: UI_PKEY_LabelDescription
description: Определяет свойство UI \_ PKEY \_ лабелдескриптион.
ms.assetid: e7dfbe7e-c9c9-44fe-9e2d-39e20f5f7062
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80a2db487988f66fcc393b3ba449dfda789248dabc3cd9e1d3e48acf9ba3473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438005"
---
# <a name="ui_pkey_labeldescription"></a>UI \_ PKEY \_ лабелдескриптион

Определяет свойство UI \_ PKEY \_ лабелдескриптион.

```
propertyDescription
   name = UI_PKEY_LabelDescription
   shellPKey = UI_PKEY_LabelDescription
   formatID = 00000002-7363-696e-8441798acf5aebb7
   propID = 2
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Remarks

UI \_ PKEY \_ лабелдескриптион используется приложением для запроса описания, связанного с [ \_ \_ меткой PKEY пользовательского интерфейса](windowsribbon-reference-properties-uipkey-label.md).

Значение свойства — это строка, ограниченная любой последовательностью символов, включая пробелы и символы разрыва строки.

> [!Note]  
> Используйте ссылку на символ XML универсальной кодировки (UCS) `&#xA;` для указания разрыва строки.

 

Максимальная длина не ограничена.

Выравнивание по правому краю не поддерживается.

На следующем снимке экрана показано использование метки и связанного описания метки в меню приложения.

![снимок экрана, отображающий метку и связанное с ним описание метки в меню приложения.](images/properties/ui-pkey-labeldescription.png)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства ресурса](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command. Лабелдескриптион**](windowsribbon-element-command-labeldescription.md)
</dt> <dt>

[\_Метка PKEY пользовательского интерфейса \_](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 




