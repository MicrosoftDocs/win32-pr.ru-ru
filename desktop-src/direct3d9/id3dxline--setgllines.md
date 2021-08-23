---
description: Переключает режим для отображения линий в стиле OpenGL.
ms.assetid: 298bf391-9f2b-4352-b9f8-3bc2ab661eee
title: 'Метод ID3DXLine:: Сетгллинес (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetGLLines
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bea46421cd259deb87bccaaf9e97073550467674491bba9e1983a7482686efd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748144"
---
# <a name="id3dxlinesetgllines-method"></a>Метод ID3DXLine:: Сетгллинес

Переключает режим для отображения линий в стиле OpenGL.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetGLLines(
  [in] BOOL bGLLines
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бгллинес* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Переключает рисование линий в стиле OpenGL. **True** включает линии в стиле OpenGL и **false** включает линии в стиле Direct3D.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
