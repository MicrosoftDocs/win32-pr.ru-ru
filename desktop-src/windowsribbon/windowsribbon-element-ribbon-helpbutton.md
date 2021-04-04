---
title: Свойство Ribbon. Хелпбуттон
description: Представляет контейнер для кнопки "Справка".
ms.assetid: a64239b2-2440-4bcf-8fd7-079003de6d8c
keywords:
- Лента Windows свойства Ribbon. Хелпбуттон
topic_type:
- apiref
api_name:
- Ribbon.HelpButton
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49e343a5181479ede5d428937908ed4bf37764f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802872"
---
# <a name="ribbonhelpbutton-property"></a>Свойство Ribbon. Хелпбуттон

Представляет контейнер для [кнопки "Справка"](windowsribbon-controls-helpbutton.md).

## <a name="usage"></a>Использование

``` syntax
<Ribbon.HelpButton>
  child elements
</Ribbon.HelpButton>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                           | Описание                                   |
|-------------------------------------------------------------------|-----------------------------------------------|
| [**хелпбуттон**](windowsribbon-element-helpbutton.md)<br/> | Может выполняться не более одного раза<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                   |
|-----------------------------------------------------------|
| [**Лента**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Комментарии

Необязательный элемент.

Может встречаться не более одного раза для каждой [**ленты**](windowsribbon-element-ribbon.md).

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка, необходимая для реализации кнопки справки на ленте.

В этом разделе кода показано объявление команды **Ribbon. хелпбуттон** .


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



В этом разделе кода показано объявление элемента управления **Ribbon. хелпбуттон** .


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



 

 





