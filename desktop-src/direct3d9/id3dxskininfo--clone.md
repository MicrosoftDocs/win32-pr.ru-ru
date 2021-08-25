---
description: Создает точную копию объекта сведений об обложке.
ms.assetid: 82d0a78a-95f3-4b09-bc1a-b4bc663e0850
title: 'Метод ID3DXSkinInfo:: Clone (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Clone
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 19a07c3d29c4c73b423ec5d93e2eda549243a00ff7ee3570cca9b9699fbd1be2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893304"
---
# <a name="id3dxskininfoclone-method"></a>Метод ID3DXSkinInfo:: Clone

Создает точную копию объекта сведений об обложке.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Clone(
  [in, out] LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппскининфо* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Адрес указателя на объект [**ID3DXSkinInfo**](id3dxskininfo.md) , который будет содержать клонированный объект, если метод выполнен успешно.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 




