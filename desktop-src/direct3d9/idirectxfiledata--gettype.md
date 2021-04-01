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
ms.openlocfilehash: 463391c661b2d166a6fba773e3b01590daf0ebd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157223"
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
| Header<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[идиректксфиледата](idirectxfiledata.md)
</dt> </dl>

 

 




