---
title: Функция UpdateSubresources (D3dx12. h)
description: Обновляет подресурсы, все массивы подресурсов должны быть заполнены, обычно путем вызова ID3D12Device GetCopyableFootprints.
ms.assetid: D6885165-095E-452D-8D93-A2C43A215F48
keywords:
- Функция UpdateSubresources
topic_type:
- apiref
api_name:
- UpdateSubresources
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885ee058aacbfca238448830f2b7b1b54a298f89
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703989"
---
# <a name="updatesubresources-function"></a>Функция UpdateSubresources

Обновляет подресурсы, все массивы подресурсов должны быть заполнены, обычно путем вызова [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).

## <a name="syntax"></a>Синтаксис


```C++
UINT64 inline UpdateSubresources(
  _In_       ID3D12GraphicsCommandList          *pCmdList,
  _In_       ID3D12Resource                     *pDestinationResource,
  _In_       ID3D12Resource                     *pIntermediate,
  _In_       UINT                               FirstSubresource,
  _In_       UINT                               NumSubresources,
             UINT64                             RequiredSize,
  _In_ const D3D12_PLACED_SUBRESOURCE_FOOTPRINT *pLayouts,
  _In_ const UINT                               *pNumRows,
  _In_ const UINT64                             *pRowSizesInBytes,
  _In_ const D3D12_SUBRESOURCE_DATA             *pSrcData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкмдлист* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

Список команд в виде указателя на [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).

</dd> <dt>

*пдестинатионресаурце* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Целевой ресурс в виде указателя на [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).

</dd> <dt>

*пинтермедиате* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Промежуточный ресурс в виде указателя на [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).

</dd> <dt>

*Фирстсубресаурце* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Индекс первого подресурса в ресурсе. Диапазон допустимых значений — от 0 до D3D12 \_ требований к \_ подресурсам.

</dd> <dt>

*Нумсубресаурцес* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Число подресурсов в ресурсе. Диапазон допустимых значений — от 0 до (D3D12 \_ req \_ Resources- *фирстсубресаурце*).

</dd> <dt>

*рекуиредсизе* 
</dt> <dd>

Тип: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Требуемый размер обновления (в байтах).

</dd> <dt>

*плайаутс* \[ окне\]
</dt> <dd>

Тип: **константа \* [**D3D12 \_ размещенных \_ подресурсов \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)** .

Указатель на массив (с длиной *нумсубресаурцес*) указателей на структуры, содержащие описание и размещение подресурсов ресурса.

</dd> <dt>

*пнумровс* \[ окне\]
</dt> <dd>

Тип: **const [**uint**](/windows/desktop/WinProg/windows-data-types) \***

Указатель на массив (с длиной *нумсубресаурцес*) uint, содержащий количество строк для каждого подресурса.

</dd> <dt>

*провсизесинбитес* \[ окне\]
</dt> <dd>

Тип: **константа [**UINT64**](/windows/desktop/WinProg/windows-data-types) \***

Указатель на массив (с длиной *нумсубресаурцес*) uint, содержащий размер (в байтах) каждой строки.

</dd> <dt>

*псркдата* \[ окне\]
</dt> <dd>

Тип: **\* const [**D3D12 \_ \_ данные о подресурсе**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)**

Указатель на массив (с длиной *нумсубресаурцес*) указателей на структуры [**\_ \_ данных**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) подресурсов D3D12, содержащие описания данных подресурсов, используемых для обновления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Размер (в байтах) буфера.

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

 

