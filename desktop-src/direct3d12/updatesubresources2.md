---
title: Функция UpdateSubresources (выделение кучи) (D3dx12. h)
description: Обновляет подресурсы с реализацией выделения кучи.
ms.assetid: 328D8755-D328-471D-AAF4-9771CBFF7539
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
ms.openlocfilehash: c97abe59bdd0334fe4b7badf03e44ddc03b85495
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703827"
---
# <a name="updatesubresources-heap-allocating-function"></a>Функция UpdateSubresources (выделение кучи)

Обновляет подресурсы с реализацией выделения кучи.

## <a name="syntax"></a>Синтаксис


```C++
UINT64 inline UpdateSubresources(
  _In_ ID3D12GraphicsCommandList *pCmdList,
  _In_ ID3D12Resource            *pDestinationResource,
  _In_ ID3D12Resource            *pIntermediate,
       UINT64                    IntermediateOffset,
  _In_ UINT                      FirstSubresource,
  _In_ UINT                      NumSubresources,
  _In_ D3D12_SUBRESOURCE_DATA    *pSrcData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкмдлист* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

Указатель на интерфейс [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) для списка команд.

</dd> <dt>

*пдестинатионресаурце* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Указатель на интерфейс [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) , представляющий целевой ресурс.

</dd> <dt>

*пинтермедиате* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Указатель на интерфейс [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) , представляющий промежуточный ресурс.

</dd> <dt>

*интермедиатеоффсет* 
</dt> <dd>

Тип: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Смещение в байтах для промежуточного ресурса.

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

*псркдата* \[ окне\]
</dt> <dd>

Тип: **[ **\_ \_ данные о подресурсе D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***

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

 

