---
title: Функция Мемкписубресаурце (D3dx12. h)
description: Копирует подресурс по строкам.
ms.assetid: 33A9F99D-FD85-4FD6-AFD6-7A10F16C3D9B
keywords:
- Функция Мемкписубресаурце
topic_type:
- apiref
api_name:
- MemcpySubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955211a490927033186442480b3449773b4ebcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694230"
---
# <a name="memcpysubresource-function"></a>Функция Мемкписубресаурце

Копирует подресурс по строкам.

## <a name="syntax"></a>Синтаксис


```C++
void inline MemcpySubresource(
  _In_ const D3D12_MEMCPY_DEST      *pDest,
  _In_ const D3D12_SUBRESOURCE_DATA *pSrc,
             SIZE_T                 RowSizeInBytes,
             UINT                   NumRows,
             UINT                   NumSlices
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдест* \[ окне\]
</dt> <dd>

Тип: **const [**D3D12 \_ MEMCPY \_ dest**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) \***

Указатель на структуру [**D3D12 \_ MEMCPY \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) , описывающую назначение операции копирования в память.

</dd> <dt>

*pSrc* \[ окне\]
</dt> <dd>

Тип: **\* const [**D3D12 \_ \_ данные о подресурсе**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)**

Указатель на структуру [**\_ \_ данных подресурса D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) , которая описывает источник операции копирования в память.

</dd> <dt>

*ровсизеинбитес* 
</dt> <dd>

Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**

Размер каждой строки в байтах.

</dd> <dt>

*нумровс* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Количество строк.

</dd> <dt>

*нумслицес* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Количество срезов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Также рассмотрим следующие методы.

-   [**ID3D12Resource:: Вритетосубресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)
-   [**ID3D12Resource:: Реадфромсубресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource)
-   [**ID3D12GraphicsCommandList:: Копиресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Библиотека<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вспомогательные функции для D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Подресурсы](subresources.md)
</dt> </dl>

 

