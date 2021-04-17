---
description: Определяет, является ли кватернион единичным кватернион.
ms.assetid: 1cd39e1b-9b68-434d-b7b0-3ec6cddb8757
title: Функция D3DXQuaternionIsIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b2b02bdddb4b7a2d31a685f576434e34952c0a22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703927"
---
# <a name="d3dxquaternionisidentity-function"></a>Функция D3DXQuaternionIsIdentity

Определяет, является ли кватернион единичным кватернион.

## <a name="syntax"></a>Синтаксис


```C++
BOOL D3DXQuaternionIsIdentity(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pQ* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая будет протестирована для идентификации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Если кватернион является единичным кватернион, эта функция возвращает **значение true**. В противном случае эта функция возвращает **значение false**.

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
</dt> <dt>

[**D3DXQuaternionIdentity**](d3dxquaternionidentity.md)
</dt> </dl>

 

 
