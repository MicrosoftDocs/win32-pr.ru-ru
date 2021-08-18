---
description: Получает указатель на идентификатор GUID, определяющий объект файла DirectX. Не рекомендуется.
ms.assetid: 74c7a1d9-85e4-43eb-bcd8-1f3ddd713e9f
title: 'Метод Идиректксфилеобжект:: GetId (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetId
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 5cb6788afe0b937822b8895790584f6928a7b5aecb564a31540337935763b2f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800185"
---
# <a name="idirectxfileobjectgetid-method"></a>Метод Идиректксфилеобжект:: GetId

Получает указатель на идентификатор GUID, определяющий объект файла DirectX. Не рекомендуется.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetId(
  [out, retval] 
            LPGUID pGuid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пгуид* \[ out, retval\]
</dt> <dd>

Тип: **лпгуид**

Указатель на идентификатор GUID для получения идентификатора объекта. Функция присвойте идентификатору GUID **значение NULL** , если у объекта нет идентификатора.

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

[идиректксфилеобжект](idirectxfileobject.md)
</dt> </dl>

 

 




