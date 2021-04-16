---
title: Ивмпклоседкаптион Самистиле, свойство
description: Свойство Самистиле получает или задает стиль закрытых субтитров.
ms.assetid: 0b1f92c6-b659-4ade-90c8-62a06e475f5c
keywords:
- Проигрыватель Windows Media для свойства Самистиле
- Самистиле свойство проигрывателя Windows Media Player, интерфейс Ивмпклоседкаптион
- Интерфейс Ивмпклоседкаптион Windows Media Player, свойство Самистиле
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIStyle
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd0b48fc1807d6ca1854651c7f222183a845be3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649061"
---
# <a name="iwmpclosedcaptionsamistyle-property"></a>Свойство Ивмпклоседкаптион:: Самистиле

Свойство **самистиле** получает или задает стиль закрытых субтитров.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String SAMIStyle {get; set;}
```


```VB

Public Property SAMIStyle As System.String
```





## <a name="property-value"></a>Значение свойства

**Строка System. String** , которая является именем, указанным в идентификаторе стиля файла Sami.

## <a name="remarks"></a>Комментарии

Файл SAMI может содержать несколько определений стиля формата. Стили SAMI определены между тегами <STYLE> и </STYLE> в файле Sami. Стиль определяется с помощью текстовой строки, предшествующей \# символу. Пример:


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}
```



Указывает стиль, создающий определенный шрифт.

Если параметр SAMI не указан, по умолчанию используется первый стиль, определенный в файле SAMI.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Добавление субтитров к цифровым носителям**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Интерфейс Ивмпклоседкаптион (VB и C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Интерфейс IWMPClosedCaption2 (VB и C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





