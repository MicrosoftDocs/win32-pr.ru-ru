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
# <a name="updatesubresources-heap-allocating-function"></a><span data-ttu-id="6d5b3-104">Функция UpdateSubresources (выделение кучи)</span><span class="sxs-lookup"><span data-stu-id="6d5b3-104">UpdateSubresources (heap-allocating) function</span></span>

<span data-ttu-id="6d5b3-105">Обновляет подресурсы с реализацией выделения кучи.</span><span class="sxs-lookup"><span data-stu-id="6d5b3-105">Updates subresources with a heap-allocating implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d5b3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d5b3-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="6d5b3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d5b3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d5b3-108">*пкмдлист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d5b3-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5b3-109">Тип: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="6d5b3-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="6d5b3-110">Указатель на интерфейс [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) для списка команд.</span><span class="sxs-lookup"><span data-stu-id="6d5b3-110">A pointer to the [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface for the command list.</span></span>

</dd> <dt>

<span data-ttu-id="6d5b3-111">*пдестинатионресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d5b3-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5b3-112">Тип: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="6d5b3-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="6d5b3-113">Указатель на интерфейс [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) , представляющий целевой ресурс.</span><span class="sxs-lookup"><span data-stu-id="6d5b3-113">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the destination resource.</span></span>

</dd> <dt>

<span data-ttu-id="6d5b3-114">*пинтермедиате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d5b3-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5b3-115">Тип: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="6d5b3-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="6d5b3-116">Указатель на интерфейс [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) , представляющий промежуточный ресурс.</span><span class="sxs-lookup"><span data-stu-id="6d5b3-116">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="6d5b3-117">*интермедиатеоффсет*</span><span class="sxs-lookup"><span data-stu-id="6d5b3-117">*IntermediateOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="6d5b3-118">Тип: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6d5b3-118">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6d5b3-119">Смещение в байтах для промежуточного ресурса.</span><span class="sxs-lookup"><span data-stu-id="6d5b3-119">The offset, in bytes, to the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="6d5b3-120">*Фирстсубресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d5b3-120">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5b3-121">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6d5b3-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6d5b3-122">Индекс первого подресурса в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="6d5b3-122">The index of the first subresource in the resource.</span></span> <span data-ttu-id="6d5b3-123">Диапазон допустимых значений — от 0 до D3D12 \_ требований к \_ подресурсам.</span><span class="sxs-lookup"><span data-stu-id="6d5b3-123">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="6d5b3-124">*Нумсубресаурцес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d5b3-124">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5b3-125">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6d5b3-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6d5b3-126">Число подресурсов в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="6d5b3-126">The number of subresources in the resource.</span></span> <span data-ttu-id="6d5b3-127">Диапазон допустимых значений — от 0 до (D3D12 \_ req \_ Resources- *фирстсубресаурце*).</span><span class="sxs-lookup"><span data-stu-id="6d5b3-127">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="6d5b3-128">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d5b3-128">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5b3-129">Тип: **[ **\_ \_ данные о подресурсе D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span><span class="sxs-lookup"><span data-stu-id="6d5b3-129">Type: **[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="6d5b3-130">Указатель на массив (с длиной *нумсубресаурцес*) указателей на структуры [**\_ \_ данных**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) подресурсов D3D12, содержащие описания данных подресурсов, используемых для обновления.</span><span class="sxs-lookup"><span data-stu-id="6d5b3-130">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d5b3-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d5b3-131">Return value</span></span>

<span data-ttu-id="6d5b3-132">Тип: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6d5b3-132">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6d5b3-133">Размер (в байтах) буфера.</span><span class="sxs-lookup"><span data-stu-id="6d5b3-133">The size, in bytes, of the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d5b3-134">Требования</span><span class="sxs-lookup"><span data-stu-id="6d5b3-134">Requirements</span></span>



| <span data-ttu-id="6d5b3-135">Требование</span><span class="sxs-lookup"><span data-stu-id="6d5b3-135">Requirement</span></span> | <span data-ttu-id="6d5b3-136">Значение</span><span class="sxs-lookup"><span data-stu-id="6d5b3-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6d5b3-137">Header</span><span class="sxs-lookup"><span data-stu-id="6d5b3-137">Header</span></span><br/>  | <dl> <span data-ttu-id="6d5b3-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d5b3-138"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="6d5b3-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6d5b3-139">Library</span></span><br/> | <dl> <span data-ttu-id="6d5b3-140"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d5b3-140"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="6d5b3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6d5b3-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="6d5b3-142"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d5b3-142"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d5b3-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d5b3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d5b3-144">Вспомогательные функции для D3D12</span><span class="sxs-lookup"><span data-stu-id="6d5b3-144">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="6d5b3-145">Подресурсы</span><span class="sxs-lookup"><span data-stu-id="6d5b3-145">Subresources</span></span>](subresources.md)
</dt> </dl>

 

