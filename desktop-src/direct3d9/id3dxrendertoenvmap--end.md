---
description: Восстановите все целевые объекты отрисовки и при необходимости сформируйте все отрисованные лица в области схемы среды.
ms.assetid: 57c73787-36e7-4088-b5ff-78894e3a5d90
title: 'Метод ID3DXRenderToEnvMap:: end (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: efaf32eb421f6bda38fb922c4a89b1dbbe871842c3b4f07a87ff30c2e6b4dc40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095794"
---
# <a name="id3dxrendertoenvmapend-method"></a>Метод ID3DXRenderToEnvMap:: end

Восстановите все целевые объекты отрисовки и при необходимости сформируйте все отрисованные лица в области схемы среды.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT End(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Мипфилтер* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Допустимое сочетание одного или нескольких флагов [ \_ фильтра D3DX](d3dx-filter.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md)
</dt> </dl>

 

 
