---
description: Добавляет спрайт в список пакетных спрайтов.
ms.assetid: 8f5c43a2-68dd-44a9-be2f-f76d9fa2d900
title: ID3DXSprite::D необработанный метод (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d453a2e03538b7601b5f73033a4749430e8812ef317a90816cac220e61695279
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747374"
---
# <a name="id3dxspritedraw-method"></a>ID3DXSprite::D необработанный метод

Добавляет спрайт в список пакетных спрайтов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Draw(
  [in]       LPDIRECT3DTEXTURE9 pTexture,
  [in] const RECT               *pSrcRect,
  [in] const D3DXVECTOR3        *pCenter,
  [in] const D3DXVECTOR3        *pPosition,
  [in]       D3DCOLOR           Color
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птекстуре* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Указатель на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий текстуру спрайта.

</dd> <dt>

*псркрект* \[ окне\]
</dt> <dd>

Тип: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , указывающую часть текстуры источника, используемую для спрайта. Если этот параметр имеет **значение NULL**, то для спрайта используется все исходное изображение.

</dd> <dt>

*пцентер* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на вектор [**D3DXVECTOR3**](d3dxvector3.md) , определяющий центр спрайта. Если этот аргумент имеет **значение NULL**, то используется точка (0, 0, 0), которая является верхним левым углом.

</dd> <dt>

*ппоситион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на вектор [**D3DXVECTOR3**](d3dxvector3.md) , определяющий расположение спрайта. Если этот аргумент имеет **значение NULL**, то используется точка (0, 0, 0), которая является верхним левым углом.

</dd> <dt>

*Цветовая палитра* \[ окне\]
</dt> <dd>

Тип: **[ **D3DCOLOR**](d3dcolor.md)**

Тип [**D3DCOLOR**](d3dcolor.md) . Этот параметр используется для связи цвета и альфа-каналов. Значение 0xFFFFFFFF сохраняет исходный цвет и альфа-данные. Чтобы создать этот цвет, используйте макрос [**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Remarks

Для масштабирования, вращения или перевода спрайта вызовите [**ID3DXSprite:: сеттрансформ**](id3dxsprite--settransform.md) с матрицей, которая содержит значения Scale, поверните и сдвига (SRT) перед вызовом ID3DXSprite::D RAW. Сведения о настройке значений SRT в матрице см. в разделе [преобразования матрицы](transforms.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite:: Transform**](id3dxsprite--gettransform.md)
</dt> </dl>

 

 
