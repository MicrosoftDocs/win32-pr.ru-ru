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
ms.openlocfilehash: f4d3e5fb39ebcfa5ce906d1f90c2c5c10bdd4b3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703687"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
