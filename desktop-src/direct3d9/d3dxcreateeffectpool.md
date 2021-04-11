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
ms.openlocfilehash: 14753500ac15fb0ed30d46b1121431af78e1fe93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273932"
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

## <a name="remarks"></a>Комментарии

Для эффектов в пуле общие параметры с одинаковыми общими значениями имен.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции эффектов](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 




