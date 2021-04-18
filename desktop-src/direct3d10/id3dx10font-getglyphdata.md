---
description: Возвращает сведения о размещении и ориентации глифа в символьной ячейке.
ms.assetid: 1114b06a-c0f0-4c2a-86ad-2ed72bee4049
title: 'Метод ID3DX10Font:: Жетглифдата (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetGlyphData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 530206c4f351cb1ef073639a21dfa37e43af5bae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703901"
---
# <a name="id3dx10fontgetglyphdata-method"></a>Метод ID3DX10Font:: Жетглифдата

Возвращает сведения о размещении и ориентации глифа в символьной ячейке.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetGlyphData(
  [in]  UINT                     Glyph,
  [out] ID3D10ShaderResourceView **ppTexture,
  [in]  RECT                     *pBlackBox,
  [in]  POINT                    *pCellInc
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

Тип: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***

Адрес указателя на объект ID3D10Texture, который содержит глиф.

</dd> <dt>

*пблаккбокс* \[ окне\]
</dt> <dd>

Тип: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***

Указатель на самый маленький объект Rectangle, полностью охватывающий глиф. См. раздел [Rect](/previous-versions//ms536136(v=vs.85)).

</dd> <dt>

*пцеллинк* \[ окне\]
</dt> <dd>

Тип: **точка \***

Указатель на двухмерный вектор, соединяющий источник текущей ячейки символов с источником следующей ячейки символа. См. раздел [Point](/previous-versions//ms536119(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
