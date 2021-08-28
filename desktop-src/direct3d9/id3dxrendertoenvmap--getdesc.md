---
description: Извлекает описание поверхности рендеринга.
ms.assetid: 3c2612fa-540d-4d7a-9821-bf37fa3b6da4
title: 'Метод ID3DXRenderToEnvMap:: desc (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7cfe9f3e8e857806895ec8be249d51f63ffe4818f24bbbf12d842754a885e855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847312"
---
# <a name="id3dxrendertoenvmapgetdesc-method"></a>Метод ID3DXRenderToEnvMap:: DESC

Извлекает описание поверхности рендеринга.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDesc(
  [out] D3DXRTE_DESC *pDesc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдеск* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXRTE \_ DESC**](d3dxrte-desc.md)\***

Указатель на структуру [**D3DXRTE \_ DESC**](d3dxrte-desc.md) , описывающую поверхность отрисовки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




