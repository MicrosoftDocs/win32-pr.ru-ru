---
description: Применяет переплет к объекту текстуры IDirect3DTexture9.
ms.assetid: e8f4a4cf-4d3b-419b-9486-08aa3bd3d8a4
title: 'Метод ID3DXTextureGutterHelper:: Апплигуттерстекс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersTex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a289eede9b55a3560408caf71a20aaf1811bb82780488b886cade8aaa5e96d75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893244"
---
# <a name="id3dxtexturegutterhelperapplygutterstex-method"></a>Метод ID3DXTextureGutterHelper:: Апплигуттерстекс

Применяет переплет к объекту текстуры [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ApplyGuttersTex(
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птекстуре* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Указатель на объект текстуры [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ NOTAVAILABLE, D3DERR \_ аутофвидеомемори, D3DERR \_ васстиллдравинг, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

[**Класс 2 пикселей текстуры**](id3dxtexturegutterhelper.md) создается путем повторной выборки класса 1 и 4 пикселей текстуры.

Ширина и высота текстуры должны совпадать с шириной и высотой, возвращаемой [**ID3DXTextureGutterHelper:: полуширинные**](id3dxtexturegutterhelper--getwidth.md) и [**ID3DXTextureGutterHelper:: Height**](id3dxtexturegutterhelper--getheight.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
