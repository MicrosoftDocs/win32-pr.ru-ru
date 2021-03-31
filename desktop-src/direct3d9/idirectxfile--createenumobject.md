---
description: Создает объект перечислителя. Не рекомендуется.
ms.assetid: 9e72bb2f-143e-4690-baef-ccded21572ec
title: 'Метод Идиректксфиле:: Креатинумобжект (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3d15738b78299441fe08333a41f0652f1b4224d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821356"
---
# <a name="idirectxfilecreateenumobject-method"></a>Метод Идиректксфиле:: Креатинумобжект

Создает объект перечислителя. Не рекомендуется.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateEnumObject(
  [in]          LPVOID                  pvSource,
  [in]          DXFILELOADOPTIONS       dwLoadOptions,
  [out, retval] LPDIRECTXFILEENUMOBJECT *ppEnumObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвсаурце* \[ окне\]
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**

Указатель на данные, содержимое которых зависит от значения Двлоадоптионс

</dd> <dt>

*двлоадоптионс* \[ окне\]
</dt> <dd>

Тип: **[ **дксфилелоадоптионс**](dxfile.md)**

Значение, указывающее источник данных. Это значение может быть одним из \_ флагов дксфилелоад XXX в [константах дксфиле](dxfile.md).

</dd> <dt>

*ппенумобж* \[ out, retval\]
</dt> <dd>

Тип: **[ **лпдиректксфилинумобжект**](idirectxfileenumobject.md)\***

Адрес указателя на интерфейс [**идиректксфилинумобжект**](idirectxfileenumobject.md) , представляющий созданный объект перечислителя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадаллок, дксфилирр \_ БАДФИЛЕФЛОАТСИЗЕ, дксфилирр \_ бадфилетипе, ДКСФИЛИРР \_ бадфилеверсион, DXFILEERR \_ BADRESOURCE, DXFILEERR \_ BADVALUE, DXFILEERR \_ FILENOTFOUND, DXFILEERR \_ RESOURCENOTFOUND, DXFILEERR \_ URLNOTFOUND.

## <a name="remarks"></a>Комментарии

После использования этого метода используйте один из методов Идиректксфилинумобжект для получения объекта данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[идиректксфиле](idirectxfile.md)
</dt> </dl>

 

 
