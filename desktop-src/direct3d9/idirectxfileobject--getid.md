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
ms.openlocfilehash: 336dbde487ecd1b3af7b32d3743f037c235952f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105684992"
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
| Header<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[идиректксфилеобжект](idirectxfileobject.md)
</dt> </dl>

 

 




