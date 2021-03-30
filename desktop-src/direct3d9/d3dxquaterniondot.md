---
description: Возвращает скалярное произведение двух кватернионов.
ms.assetid: 2ed9aca9-0526-4b92-bd66-b09dcf4f474a
title: Функция D3DXQuaternionDot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e893ed9260c0d843e8454d96ab5b634741ee60d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355520"
---
# <a name="d3dxquaterniondot-function"></a>Функция D3DXQuaternionDot

Возвращает скалярное произведение двух кватернионов.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT D3DXQuaternionDot(
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pQ1* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .

</dd> <dt>

*pQ2* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **float**](../winprog/windows-data-types.md)**

Скалярное произведение двух кватернионов.

## <a name="remarks"></a>Комментарии

Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
