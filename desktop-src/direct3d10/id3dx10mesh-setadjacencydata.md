---
description: Задайте данные о смежности сетки.
ms.assetid: 67d51ce0-7fe2-484d-9874-f1fa59632d59
title: 'Метод ID3DX10Mesh:: Сетаджаценцидата (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAdjacencyData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6fabced002caf424fa1fcbcefcb3b326b0c71f7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713845"
---
# <a name="id3dx10meshsetadjacencydata-method"></a>Метод ID3DX10Mesh:: Сетаджаценцидата

Задайте данные о смежности сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetAdjacencyData(
  [in] const UINT *pAdjacency
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*паджаценци* \[ окне\]
</dt> <dd>

Тип: **const [**uint**](../winprog/windows-data-types.md) \***

Заданные соседства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
