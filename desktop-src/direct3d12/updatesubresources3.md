---
title: Функция UpdateSubresources (выделение стека) (D3dx12. h)
description: Обновляет подресурсы с реализацией выделения стека.
ms.assetid: 2F30FDF1-4450-473E-AEA8-C5FF54260BCE
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
ms.openlocfilehash: 237e7df26b35b4cb5b1dba7b2a80c1baaac64e8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703711"
---
# <a name="updatesubresources-stack-allocating-function"></a><span data-ttu-id="a036f-104">Функция UpdateSubresources (выделение стека)</span><span class="sxs-lookup"><span data-stu-id="a036f-104">UpdateSubresources (stack-allocating) function</span></span>

<span data-ttu-id="a036f-105">Обновляет подресурсы с реализацией выделения стека.</span><span class="sxs-lookup"><span data-stu-id="a036f-105">Updates subresources with a stack-allocating implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a036f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a036f-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="a036f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a036f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a036f-108">*пкмдлист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a036f-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a036f-109">Тип: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="a036f-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="a036f-110">Список команд в виде указателя на [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="a036f-110">The command list, as a pointer to an [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

</dd> <dt>

<span data-ttu-id="a036f-111">*пдестинатионресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a036f-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a036f-112">Тип: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="a036f-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="a036f-113">Целевой ресурс в виде указателя на [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="a036f-113">The destination resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="a036f-114">*пинтермедиате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a036f-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a036f-115">Тип: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="a036f-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="a036f-116">Промежуточный ресурс в виде указателя на [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="a036f-116">The intermediate resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="a036f-117">*интермедиатеоффсет*</span><span class="sxs-lookup"><span data-stu-id="a036f-117">*IntermediateOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="a036f-118">Тип: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a036f-118">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a036f-119">Смещение в байтах для промежуточного ресурса.</span><span class="sxs-lookup"><span data-stu-id="a036f-119">The offset, in bytes, to the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="a036f-120">*Фирстсубресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a036f-120">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a036f-121">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a036f-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a036f-122">Индекс первого подресурса в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="a036f-122">The index of the first subresource in the resource.</span></span> <span data-ttu-id="a036f-123">Диапазон допустимых значений — от 0 до *макссубресаурцес*.</span><span class="sxs-lookup"><span data-stu-id="a036f-123">Valid values range from 0 to *MaxSubresources*.</span></span>

</dd> <dt>

<span data-ttu-id="a036f-124">*Нумсубресаурцес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a036f-124">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a036f-125">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a036f-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a036f-126">Число подресурсов в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="a036f-126">The number of subresources in the resource.</span></span> <span data-ttu-id="a036f-127">Допустимые значения находятся в диапазоне от 1 до (*макссубресаурцес*  -  *фирстсубресаурце*).</span><span class="sxs-lookup"><span data-stu-id="a036f-127">Valid values range from 1 to (*MaxSubresources* - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="a036f-128">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a036f-128">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a036f-129">Тип: **[ **\_ \_ данные о подресурсе D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span><span class="sxs-lookup"><span data-stu-id="a036f-129">Type: **[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="a036f-130">Указатель на массив (с длиной *нумсубресаурцес*) указателей на структуры [**\_ \_ данных**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) подресурсов D3D12, содержащие описания данных подресурсов, используемых для обновления.</span><span class="sxs-lookup"><span data-stu-id="a036f-130">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a036f-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a036f-131">Return value</span></span>

<span data-ttu-id="a036f-132">Тип: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a036f-132">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a036f-133">Размер (в байтах) буфера.</span><span class="sxs-lookup"><span data-stu-id="a036f-133">The size, in bytes, of the buffer.</span></span>

## <a name="remarks"></a><span data-ttu-id="a036f-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a036f-134">Remarks</span></span>

<span data-ttu-id="a036f-135">Объявление этой функции начинается с: `template <UINT MaxSubresources>`</span><span class="sxs-lookup"><span data-stu-id="a036f-135">The declaration of this function begins with: `template <UINT MaxSubresources>`</span></span>

## <a name="requirements"></a><span data-ttu-id="a036f-136">Требования</span><span class="sxs-lookup"><span data-stu-id="a036f-136">Requirements</span></span>



| <span data-ttu-id="a036f-137">Требование</span><span class="sxs-lookup"><span data-stu-id="a036f-137">Requirement</span></span> | <span data-ttu-id="a036f-138">Значение</span><span class="sxs-lookup"><span data-stu-id="a036f-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a036f-139">Header</span><span class="sxs-lookup"><span data-stu-id="a036f-139">Header</span></span><br/>  | <dl> <span data-ttu-id="a036f-140"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="a036f-140"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="a036f-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a036f-141">Library</span></span><br/> | <dl> <span data-ttu-id="a036f-142"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a036f-142"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="a036f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="a036f-143">DLL</span></span><br/>     | <dl> <span data-ttu-id="a036f-144"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a036f-144"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a036f-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a036f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a036f-146">Вспомогательные функции для D3D12</span><span class="sxs-lookup"><span data-stu-id="a036f-146">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="a036f-147">Подресурсы</span><span class="sxs-lookup"><span data-stu-id="a036f-147">Subresources</span></span>](subresources.md)
</dt> </dl>

 

