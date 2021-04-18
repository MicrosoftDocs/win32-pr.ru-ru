---
description: Разрешает ссылки на данные. Не рекомендуется.
ms.assetid: e8cf6e5d-c9b2-4a47-b058-24282dc65e74
title: 'Метод Идиректксфиледатареференце:: Resolve (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference.Resolve
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1b047245e3f89a618cde83e5c18a323f9364f3ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713865"
---
# <a name="idirectxfiledatareferenceresolve-method"></a>Метод Идиректксфиледатареференце:: Resolve

Разрешает ссылки на данные. Не рекомендуется.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Resolve(
  [out, retval] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдатаобж* \[ out, retval\]
</dt> <dd>

Тип: **[ **лпдиректксфиледата**](idirectxfiledata.md)\***

Адрес указателя на интерфейс [**идиректксфиледата**](idirectxfiledata.md) , представляющий возвращаемый объект данных файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК. Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадвалуе, дксфилирр \_ NotFound.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[идиректксфиледатареференце](idirectxfiledatareference.md)
</dt> </dl>

 

 




