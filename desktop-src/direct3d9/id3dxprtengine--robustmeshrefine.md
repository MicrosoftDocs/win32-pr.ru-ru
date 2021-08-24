---
description: Делит лиц на сетку, обеспечивая консервативную адаптивную выборку, которая не будет устранять функции в сети.
ms.assetid: 0d74a01a-de67-4607-99eb-ed98e239f199
title: 'Метод ID3DXPRTEngine:: Робустмешрефине (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.RobustMeshRefine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 280e4552af6de13995ed81afab4d743232485e92446c72b61fd10ae17fea7b07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790564"
---
# <a name="id3dxprtenginerobustmeshrefine-method"></a>Метод ID3DXPRTEngine:: Робустмешрефине

Делит лиц на сетку, обеспечивая консервативную адаптивную выборку, которая не будет устранять функции в сети.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RobustMeshRefine(
  [in] FLOAT MinEdgeLength,
  [in] UINT  MaxSubdiv
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Минеджеленгс* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Минимальная длина грани, которая будет создана при адаптивной выборки. При нулевом значении будет заменено разумное значение по умолчанию.

</dd> <dt>

*Макссубдив* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Максимальный уровень подраздела лица, который будет использоваться в адаптивной выборки. Если значение равно нулю, заменяется значением по умолчанию, равным 5.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: Компутебаунцеадаптиве**](id3dxprtengine--computebounceadaptive.md)
</dt> <dt>

[**ID3DXPRTEngine:: Компутедиректлигхтингшадаптиве**](id3dxprtengine--computedirectlightingshadaptive.md)
</dt> </dl>

 

 
