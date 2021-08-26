---
description: Возвращает индекс анимации по ее имени.
ms.assetid: 6e91a4fe-3202-447b-b486-d29e8da64af2
title: 'Метод ID3DXAnimationSet:: Жетаниматиониндексбинаме (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetAnimationIndexByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cee98a1450d1ef10dffa9f8f2da232bc334ca77995e2fa0bcf985f014f7139c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069074"
---
# <a name="id3dxanimationsetgetanimationindexbyname-method"></a>Метод ID3DXAnimationSet:: Жетаниматиониндексбинаме

Возвращает индекс анимации по ее имени.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAnimationIndexByName(
  [in]  LPCSTR pName,
  [out] UINT   *pIndex
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pName* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Имя анимации.

</dd> <dt>

*Пиндекс* \[ заполняет\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Указатель на индекс анимации.

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

 

 
