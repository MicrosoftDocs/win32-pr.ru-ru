---
title: IWMPMedia2, свойство ошибки
description: Свойство Error получает интерфейс Ивмперроритем, если в элементе мультимедиа есть условие ошибки.
ms.assetid: 57dc8aef-5f22-43da-87bc-fdc0c8ebe49b
keywords:
- Проигрыватель Windows Media, свойство ошибки
- Свойство ошибки Windows Media Player, интерфейс IWMPMedia2
- Интерфейс IWMPMedia2 Windows Media Player, свойство Error
topic_type:
- apiref
api_name:
- IWMPMedia2.Error
- IWMPMedia2.get_Error
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2179b4604efd03574c78261575ce02311cd18a0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665108"
---
# <a name="iwmpmedia2error-property"></a>Свойство IWMPMedia2:: Error

Свойство **Error** получает интерфейс **ивмперроритем** , если в элементе мультимедиа есть условие ошибки.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPErrorItem Error {get;}
```


```VB

Public ReadOnly Property Error As IWMPErrorItem
```





## <a name="property-value"></a>Значение свойства

Интерфейс **вмплиб. ивмперроритем** , предоставляющий доступ к сведениям о состоянии ошибки.

## <a name="remarks"></a>Комментарии

Если не удается воспроизвести элемент мультимедиа, это свойство получает интерфейс **ивмперроритем** , содержащий сведения о возникшей проблеме.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ивмперроритем (VB и C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**Интерфейс IWMPMedia2 (VB и C#)**](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





