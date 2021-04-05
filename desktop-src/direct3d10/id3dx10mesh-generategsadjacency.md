---
description: Добавляет смежные данные в буфер индекса сетки. Когда сеть должна быть отправлена в шейдер Geometry, который принимает данные из соседей по смежным связям, необходимо, чтобы буфер индексов сетки содержал смежные данные.
ms.assetid: 8e587620-a4b6-4415-8fe7-9ec22f253b16
title: 'Метод ID3DX10Mesh:: Женератегсаджаценци (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateGSAdjacency
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d47747acfa97fbe843dabf527c8f94742db78d6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081898"
---
# <a name="id3dx10meshgenerategsadjacency-method"></a>Метод ID3DX10Mesh:: Женератегсаджаценци

Добавляет смежные данные в буфер индекса сетки. Когда сеть должна быть отправлена в шейдер Geometry, который принимает данные из соседей по смежным связям, необходимо, чтобы буфер индексов сетки содержал смежные данные.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GenerateGSAdjacency();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

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

 

 




