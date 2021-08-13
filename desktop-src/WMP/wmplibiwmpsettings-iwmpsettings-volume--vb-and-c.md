---
title: Ивмпсеттингс, свойство тома
description: Свойство Volume получает или задает текущий том воспроизведения.
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- проигрыватель Windows Media свойств тома
- свойство volume проигрыватель Windows Media, интерфейс ивмпсеттингс
- проигрыватель Windows Media интерфейса ивмпсеттингс, свойство volume
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
ms.openlocfilehash: a2077547dd00b5c75b6ca77a966190db2bb3bb1bcde61d1f5c5b84c794af84e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568401"
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

## <a name="remarks"></a>Remarks

Нулевое значение указывает на отсутствие тома (без звука). Значение 100 указывает полный том. если для этого свойства не указано значение, по умолчанию используется последний параметр тома, установленный для проигрыватель Windows Media.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпсеттингс (VB и C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





