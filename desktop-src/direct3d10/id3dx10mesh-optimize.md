---
description: 'Метод ID3DX10Mesh:: optimize — создает новую сетку с переупорядоченными лицами и вершинами для оптимизации производительности рисования.'
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: 'Метод ID3DX10Mesh:: optimize (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Optimize
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f530995a2388d3ec2627ac5ce128271ed085a779
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108052"
---
# <a name="id3dx10meshoptimize-method"></a>Метод ID3DX10Mesh:: OPTIMIZE

Создает новую сетку с переупорядоченными лицами и вершинами для оптимизации производительности рисования.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Optimize(
  [in]  UINT        Flags,
  [in]  UINT        *pFaceRemap,
  [out] LPD3D10BLOB *ppVertexRemap
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Указывает тип выполняемой оптимизации. Этому параметру можно присвоить сочетание из одного или нескольких флагов из D3DXMESHOPT и D3DXMESH (за исключением D3DXMESH \_ 32-разрядной версии, D3DXMESH с помощью \_ \_ WriteOnly и D3DXMESH \_ WRITEONLY).

</dd> <dt>

*пфацеремап* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Массив UINT, по одному на каждое лицо, определяющий исходную сетку, которая соответствует каждой грани в оптимизированной сетке. Если значение, заданное для этого аргумента, равно **null**, данные сопоставления лиц не возвращаются.

</dd> <dt>

*ппвертексремап* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***

Адрес указателя на [**интерфейс ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), который содержит DWORD для каждой вершины, указывающий, как новые вершины сопоставляются со старыми вершинами. Такое перераспределение полезно, если необходимо изменить внешние данные на основе нового сопоставления вершин.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

Этот метод создает новую сетку. Перед запуском optimize приложение должно создать буфер соседей путем вызова [**ID3DX10Mesh:: женератеаджаценциандпоинтрепс**](id3dx10mesh-generateadjacencyandpointreps.md). В буфере соседка содержатся смежные данные, например список краев и сторон, расположенных рядом друг с другом.

Этот метод очень похож на метод [**ID3DX10Mesh:: клонемеш**](id3dx10mesh-clonemesh.md) , за исключением того, что он может выполнять оптимизацию при формировании нового клона сетки. Выходная сетка наследует все параметры создания входной сетки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
