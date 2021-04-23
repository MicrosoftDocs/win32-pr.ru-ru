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
# <a name="updatesubresources-function"></a><span data-ttu-id="cc80f-104">Функция UpdateSubresources</span><span class="sxs-lookup"><span data-stu-id="cc80f-104">UpdateSubresources function</span></span>

<span data-ttu-id="cc80f-105">Обновляет подресурсы, все массивы подресурсов должны быть заполнены, обычно путем вызова [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span><span class="sxs-lookup"><span data-stu-id="cc80f-105">Updates subresources, all the subresource arrays should be populated, typically by calling [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span></span>

## <a name="syntax"></a><span data-ttu-id="cc80f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc80f-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="cc80f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc80f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc80f-108">*пкмдлист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc80f-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc80f-109">Тип: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="cc80f-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="cc80f-110">Список команд в виде указателя на [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="cc80f-110">The command list, as a pointer to an [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

</dd> <dt>

<span data-ttu-id="cc80f-111">*пдестинатионресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc80f-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc80f-112">Тип: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="cc80f-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="cc80f-113">Целевой ресурс в виде указателя на [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="cc80f-113">The destination resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="cc80f-114">*пинтермедиате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc80f-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc80f-115">Тип: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="cc80f-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="cc80f-116">Промежуточный ресурс в виде указателя на [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="cc80f-116">The intermediate resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="cc80f-117">*Фирстсубресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc80f-117">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc80f-118">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc80f-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cc80f-119">Индекс первого подресурса в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="cc80f-119">The index of the first subresource in the resource.</span></span> <span data-ttu-id="cc80f-120">Диапазон допустимых значений — от 0 до D3D12 \_ требований к \_ подресурсам.</span><span class="sxs-lookup"><span data-stu-id="cc80f-120">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="cc80f-121">*Нумсубресаурцес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc80f-121">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc80f-122">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc80f-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cc80f-123">Число подресурсов в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="cc80f-123">The number of subresources in the resource.</span></span> <span data-ttu-id="cc80f-124">Диапазон допустимых значений — от 0 до (D3D12 \_ req \_ Resources- *фирстсубресаурце*).</span><span class="sxs-lookup"><span data-stu-id="cc80f-124">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="cc80f-125">*рекуиредсизе*</span><span class="sxs-lookup"><span data-stu-id="cc80f-125">*RequiredSize*</span></span> 
</dt> <dd>

<span data-ttu-id="cc80f-126">Тип: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc80f-126">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cc80f-127">Требуемый размер обновления (в байтах).</span><span class="sxs-lookup"><span data-stu-id="cc80f-127">The required size, in bytes, for the update.</span></span>

</dd> <dt>

<span data-ttu-id="cc80f-128">*плайаутс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc80f-128">*pLayouts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc80f-129">Тип: **константа \* [**D3D12 \_ размещенных \_ подресурсов \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)** .</span><span class="sxs-lookup"><span data-stu-id="cc80f-129">Type: **const [**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)\***</span></span>

<span data-ttu-id="cc80f-130">Указатель на массив (с длиной *нумсубресаурцес*) указателей на структуры, содержащие описание и размещение подресурсов ресурса.</span><span class="sxs-lookup"><span data-stu-id="cc80f-130">Pointer to an array (of length *NumSubresources*) of pointers to the structures that contains the description and placement of the resource's subresources.</span></span>

</dd> <dt>

<span data-ttu-id="cc80f-131">*пнумровс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc80f-131">*pNumRows* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc80f-132">Тип: **const [**uint**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="cc80f-132">Type: **const [**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="cc80f-133">Указатель на массив (с длиной *нумсубресаурцес*) uint, содержащий количество строк для каждого подресурса.</span><span class="sxs-lookup"><span data-stu-id="cc80f-133">Pointer to an array (of length *NumSubresources*) of UINTS containing the number of rows for each subresource.</span></span>

</dd> <dt>

<span data-ttu-id="cc80f-134">*провсизесинбитес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc80f-134">*pRowSizesInBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc80f-135">Тип: **константа [**UINT64**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="cc80f-135">Type: **const [**UINT64**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="cc80f-136">Указатель на массив (с длиной *нумсубресаурцес*) uint, содержащий размер (в байтах) каждой строки.</span><span class="sxs-lookup"><span data-stu-id="cc80f-136">Pointer to an array (of length *NumSubresources*) of UINTS containing the size, in bytes, of each row.</span></span>

</dd> <dt>

<span data-ttu-id="cc80f-137">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc80f-137">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc80f-138">Тип: **\* const [**D3D12 \_ \_ данные о подресурсе**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)**</span><span class="sxs-lookup"><span data-stu-id="cc80f-138">Type: **const [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="cc80f-139">Указатель на массив (с длиной *нумсубресаурцес*) указателей на структуры [**\_ \_ данных**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) подресурсов D3D12, содержащие описания данных подресурсов, используемых для обновления.</span><span class="sxs-lookup"><span data-stu-id="cc80f-139">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc80f-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc80f-140">Return value</span></span>

<span data-ttu-id="cc80f-141">Тип: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc80f-141">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cc80f-142">Размер (в байтах) буфера.</span><span class="sxs-lookup"><span data-stu-id="cc80f-142">The size, in bytes, of the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc80f-143">Требования</span><span class="sxs-lookup"><span data-stu-id="cc80f-143">Requirements</span></span>



| <span data-ttu-id="cc80f-144">Требование</span><span class="sxs-lookup"><span data-stu-id="cc80f-144">Requirement</span></span> | <span data-ttu-id="cc80f-145">Значение</span><span class="sxs-lookup"><span data-stu-id="cc80f-145">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80f-146">Header</span><span class="sxs-lookup"><span data-stu-id="cc80f-146">Header</span></span><br/>  | <dl> <span data-ttu-id="cc80f-147"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc80f-147"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="cc80f-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cc80f-148">Library</span></span><br/> | <dl> <span data-ttu-id="cc80f-149"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc80f-149"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="cc80f-150">DLL</span><span class="sxs-lookup"><span data-stu-id="cc80f-150">DLL</span></span><br/>     | <dl> <span data-ttu-id="cc80f-151"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc80f-151"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc80f-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc80f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc80f-153">Вспомогательные функции для D3D12</span><span class="sxs-lookup"><span data-stu-id="cc80f-153">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="cc80f-154">Подресурсы</span><span class="sxs-lookup"><span data-stu-id="cc80f-154">Subresources</span></span>](subresources.md)
</dt> </dl>

 

