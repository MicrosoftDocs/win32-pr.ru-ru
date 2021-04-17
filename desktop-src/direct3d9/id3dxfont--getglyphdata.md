---
description: Возвращает сведения о размещении и ориентации глифа в ячейке символов.
ms.assetid: 80a78e68-6f88-4cd2-bb7b-0c608ae700aa
title: 'Метод ID3DXFont:: Жетглифдата (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetGlyphData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31f8d2e9d61cd7a8d6bd96fbdd3f6f6a7d895568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105685000"
---
# <a name="id3dxfontgetglyphdata-method"></a>Метод ID3DXFont:: Жетглифдата

Возвращает сведения о размещении и ориентации глифа в ячейке символов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetGlyphData(
  [in]  UINT               Glyph,
  [out] LPDIRECT3DTEXTURE9 *ppTexture,
  [out] RECT               *pBlackBox,
  [out] POINT              *pCellInc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Глиф* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор глифа.

</dd> <dt>

*пптекстуре* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Адрес указателя на объект [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , который содержит глиф.

</dd> <dt>

*пблаккбокс* \[ заполняет\]
</dt> <dd>

Тип: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***

Указатель на самый маленький объект Rectangle, полностью охватывающий глиф.

</dd> <dt>

*пцеллинк* \[ заполняет\]
</dt> <dd>

Тип: **[ **точка**](../winprog/windows-data-types.md)\***

Указатель на двухмерный вектор, соединяющий источник текущей ячейки символов с источником следующей ячейки символа. См. раздел [**Point**](../winprog/windows-data-types.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
