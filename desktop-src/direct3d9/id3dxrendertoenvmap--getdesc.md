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
ms.openlocfilehash: d0b9faf5bdd4c57f7320749aef2010f457dd682e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821020"
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
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




