---
title: Ивмпклоседкаптион Каптионингид, свойство
description: Свойство Ивмпклоседкаптион Возвращает или задает имя HTML-элемента, отображающего субтитры.
ms.assetid: b09bb7c7-c3b6-4e0d-962f-24b06a04f6d1
keywords:
- Проигрыватель Windows Media для свойства Каптионингид
- Каптионингид свойство проигрывателя Windows Media Player, интерфейс Ивмпклоседкаптион
- Интерфейс Ивмпклоседкаптион Windows Media Player, свойство Каптионингид
topic_type:
- apiref
api_name:
- IWMPClosedCaption.captioningId
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343234fce2b93ac02255731a38025f6d7b9fac6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648824"
---
# <a name="iwmpclosedcaptioncaptioningid-property"></a>Свойство Ивмпклоседкаптион:: Каптионингид

Свойство **ивмпклоседкаптион** Возвращает или задает имя HTML-элемента, отображающего субтитры.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String captioningId {get; set;}
```


```VB

Public Property captioningId As System.String
```





## <a name="property-value"></a>Значение свойства

**Строка System. String** , которая является идентификатором HTML-элемента.

## <a name="remarks"></a>Комментарии

Указанное имя элемента может быть любым HTML-элементом на веб-странице, если он поддерживает атрибут **InnerHtml** . Если веб-страница содержит несколько кадров, имя элемента может ссылаться только на элемент в том же кадре, что и элемент управления проигрывателя Windows Media.

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

 

 





