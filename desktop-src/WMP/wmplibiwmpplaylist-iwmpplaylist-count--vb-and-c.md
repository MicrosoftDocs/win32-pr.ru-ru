---
title: Ивмпплайлист Count, свойство
description: Свойство Count возвращает количество элементов мультимедиа в списке воспроизведения.
ms.assetid: dbff3c86-2d42-4d47-a5cb-b8199efac728
keywords:
- проигрыватель Windows Media свойства count
- свойство count проигрыватель Windows Media, интерфейс ивмпплайлист
- интерфейс ивмпплайлист проигрыватель Windows Media, свойство count
topic_type:
- apiref
api_name:
- IWMPPlaylist.count
- IWMPPlaylist.get_count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad690278b45563395c926adb4d0329bff8a01c7e8ace2f25ff3fefdb9c39cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568699"
---
# <a name="iwmpplaylistcount-property"></a>Свойство Ивмпплайлист:: count

Свойство **Count** возвращает количество элементов мультимедиа в списке воспроизведения.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 count {get;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a>Значение свойства

Объект **System. Int32** , который является числом элементов мультимедиа в списке воспроизведения.

## <a name="remarks"></a>Remarks

Перед использованием этого свойства необходимо иметь доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

Пример кода, в котором используется это свойство, см. в свойстве [аттрибутекаунт](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпплайлист (VB и C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





