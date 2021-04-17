---
title: Ивмпсеттингс, свойство тома
description: Свойство Volume получает или задает текущий том воспроизведения.
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- Проигрыватель Windows Media, свойство тома
- Свойство тома проигрыватель Windows Media Player, интерфейс Ивмпсеттингс
- Интерфейс Ивмпсеттингс Windows Media Player, свойство Volume
topic_type:
- apiref
api_name:
- IWMPSettings.volume
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b21e50c9d3c52b7ce117d6c2ab681e592571c0f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685270"
---
# <a name="iwmpsettingsvolume-property"></a>Свойство Ивмпсеттингс:: Volume

Свойство **Volume** получает или задает текущий том воспроизведения.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 volume {get; set;}
```


```VB

Public Property volume As System.Int32
```





## <a name="property-value"></a>Значение свойства

Объект **System. Int32** , который является уровнем громкости в диапазоне от 0 до 100.

## <a name="remarks"></a>Комментарии

Нулевое значение указывает на отсутствие тома (без звука). Значение 100 указывает полный том. Если для этого свойства не указано значение, по умолчанию используется последний параметр тома, установленный для проигрывателя Windows Media.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпсеттингс (VB и C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





