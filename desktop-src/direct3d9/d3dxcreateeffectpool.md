---
description: Создайте пул эффектов. Пул используется для совместного использования параметров различными эффектами.
ms.assetid: 5b202f85-b32b-4041-8873-0de535c2f59f
title: Функция D3DXCreateEffectPool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectPool
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 55df5e579b724a26e30223a0a0df7ffa815bda5a64b6f7d7e7e2c2c7f02f2fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804580"
---
# <a name="d3dxcreateeffectpool-function"></a>Функция D3DXCreateEffectPool

Создайте пул эффектов. Пул используется для совместного использования параметров различными эффектами.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateEffectPool(
  _Out_ LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пппул* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***

Возвращает указатель на созданный пул.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ .

Если аргументы недопустимы, метод возвратит D3DERR \_ инвалидкалл.

Если метод завершается с ошибкой, возвращается значение E \_ Failed.

## <a name="remarks"></a>Remarks

Для эффектов в пуле общие параметры с одинаковыми общими значениями имен.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции эффектов](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 




