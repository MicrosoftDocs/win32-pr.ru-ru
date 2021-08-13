---
title: UI_PKEY_Label
description: Определяет \_ свойство метки PKEY пользовательского интерфейса \_ .
ms.assetid: 4d704133-bba7-4c32-a552-d748b66455eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13506d1609f915c2eab9824a3f5256383c5f2aecf73ed5787e3372f17b44b435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706435"
---
# <a name="ui_pkey_label"></a>\_Метка PKEY пользовательского интерфейса \_

Определяет \_ свойство метки PKEY пользовательского интерфейса \_ .

```
propertyDescription
   name = UI_PKEY_Label
   shellPKey = UI_PKEY_Label
   formatID = 00000004-7363-696e-8441798acf5aebb7
   propID = 4
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Remarks

\_Метка PKEY пользовательского интерфейса \_ используется приложением для запроса текста метки вкладок, групп, кнопок, элементов коллекции и других элементов управления ленты.

> [!Note]  
> Windows 8 и более новые: изображение кнопки [меню приложения](windowsribbon-controls-applicationmenu.md) изменилось на метка: **файл**. Не рекомендуется использовать файл в качестве метки для любой из вкладок.

 

Значение свойства — это строка, ограниченная любой последовательностью символов, включая пробелы и символы разрыва строки.

> [!Note]  
> Используйте ссылку на символ XML универсальной кодировки (UCS) `&#xA;` для указания разрыва строки.

 

Выравнивание по правому краю не поддерживается.

Максимальная длина \_ метки PKEY пользовательского интерфейса \_ не ограничена.

Если команда предоставляется через пункт меню, а значение [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) или \_ подпись PKEY пользовательского интерфейса \_ содержит букву, предшествующую амперсанду, как показано в следующем примере, эта буква рассматривается как KeyTip и сочетание клавиш для этой команды в инфраструктуре Ribbon.


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



Чтобы отобразить знак амперсанда в метке, необходимо экранировать Специальный символ с двойным амперсандом ( `&&` ), как показано в следующем примере.


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства ресурса](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command. Лабелтитле**](windowsribbon-element-command-labeltitle.md)
</dt> <dt>

[UI \_ PKEY \_ лабелдескриптион](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 




