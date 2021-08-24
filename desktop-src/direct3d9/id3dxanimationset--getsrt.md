---
description: Возвращает значения масштаба, вращения и перевода набора анимации.
ms.assetid: 84fc56f3-15bf-4e27-ad06-57fab94f3a33
title: 'Метод ID3DXAnimationSet:: Жетсрт (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetSRT
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: baa1b882972a91626b19194f83655ea1839877943f7463be8991167eb72d17fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791074"
---
# <a name="id3dxanimationsetgetsrt-method"></a>Метод ID3DXAnimationSet:: Жетсрт

Возвращает значения масштаба, вращения и перевода набора анимации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSRT(
  [in]  DOUBLE         PeriodicPosition,
  [in]  UINT           Animation,
  [out] D3DXVECTOR3    *pScale,
  [out] D3DXQUATERNION *pRotation,
  [out] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Периодикпоситион* \[ окне\]
</dt> <dd>

Тип: **[ **Double**](../winprog/windows-data-types.md)**

Расположение набора анимации. Эту точку можно получить путем вызова [**ID3DXAnimationSet:: жетпериодикпоситион**](id3dxanimationset--getperiodicposition.md).

</dd> <dt>

*Анимация* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Индекс анимации.

</dd> <dt>

*пскале* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Указатель на вектор [**D3DXVECTOR3**](d3dxvector3.md) , описывающий масштаб набора анимации.

</dd> <dt>

 \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Указатель на кватернион [**D3DXQUATERNION**](d3dxquaternion.md) , описывающий поворот набора анимации.

</dd> <dt>

*птранслатион* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Указатель на вектор [**D3DXVECTOR3**](d3dxvector3.md) , описывающий перевод набора анимации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемые значения этого метода реализуются программистом приложения. Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК. В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке из [D3DERR](d3derr.md) или [**D3DXERR**](./d3dxerr.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
