---
description: Задает объявление вершины.
ms.assetid: cbb802ac-f0ba-41e6-8c67-a787982f975f
title: 'Метод ID3DXSkinInfo:: Сетдекларатион (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 821801647ca1aee3deabe69d911bd1cab5f7eb4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354050"
---
# <a name="id3dxskininfosetdeclaration-method"></a>Метод ID3DXSkinInfo:: Сетдекларатион

Задает объявление вершины.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetDeclaration(
  [in] const D3DVERTEXELEMENT9 *pDeclaration
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдекларатион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Указатель на массив элементов [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo:: onдекларация**](id3dxskininfo--getdeclaration.md)
</dt> </dl>

 

 




