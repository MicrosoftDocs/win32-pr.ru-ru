---
description: Извлекает идентификатор GUID шаблона объекта. Не рекомендуется.
ms.assetid: bb4a4a32-a9e7-4caa-869d-24cfb310d8d1
title: 'Метод Идиректксфиледата:: GetType (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 564d682c606d8b6bc0001f5d430d2d93f36c25210746169af4802512c330da08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292280"
---
# <a name="idirectxfiledatagettype-method"></a>Метод Идиректксфиледата:: GetType

Извлекает идентификатор GUID шаблона объекта. Не рекомендуется.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetType(
  [out, retval] const GUID **ppguid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппгуид* \[ out, retval\]
</dt> <dd>

Тип: **константа [**GUID**](guid.md) \* \***

Адрес указателя для получения идентификатора GUID шаблона объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК. В случае сбоя метода возвращаемое значение может быть ДКСФИЛИРР \_ бадвалуе.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[идиректксфиледата](idirectxfiledata.md)
</dt> </dl>

 

 




