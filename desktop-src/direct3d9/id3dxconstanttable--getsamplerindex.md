---
description: Возвращает индекс образца.
ms.assetid: vs|directx_sdk|~\id3dxconstanttable__getsamplerindex.htm
title: 'Метод ID3DXConstantTable:: Жетсамплериндекс (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetSamplerIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f803b6e129ac20b8a22ed2393ab941698c02d3d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713735"
---
# <a name="id3dxconstanttablegetsamplerindex-method"></a>Метод ID3DXConstantTable:: Жетсамплериндекс

Возвращает индекс образца.

## <a name="syntax"></a>Синтаксис


```C++
UINT GetSamplerIndex(
  [out] D3DXHANDLE hConstant
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хконстант* \[ заполняет\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Маркер образца.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Возвращает номер индекса образца выборки из таблицы констант.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
