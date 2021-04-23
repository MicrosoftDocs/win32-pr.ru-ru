---
title: Функция Жетрекуирединтермедиатесизе (D3dx12. h)
description: Возвращает требуемый размер буфера, используемый для передачи данных.
ms.assetid: 424B52E9-DE52-40D2-B8B0-C27FD3D3C298
keywords:
- Функция Жетрекуирединтермедиатесизе
topic_type:
- apiref
api_name:
- GetRequiredIntermediateSize
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15293ce1588704d55f41c364c35db57cbf4c869d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647863"
---
# <a name="getrequiredintermediatesize-function"></a><span data-ttu-id="7919f-104">Функция Жетрекуирединтермедиатесизе</span><span class="sxs-lookup"><span data-stu-id="7919f-104">GetRequiredIntermediateSize function</span></span>

<span data-ttu-id="7919f-105">Возвращает требуемый размер буфера, используемый для передачи данных.</span><span class="sxs-lookup"><span data-stu-id="7919f-105">Returns the required size of a buffer to be used for data upload.</span></span>

## <a name="syntax"></a><span data-ttu-id="7919f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7919f-106">Syntax</span></span>


```C++
UINT64 inline GetRequiredIntermediateSize(
  _In_ ID3D12Resource *pDestinationResource,
  _In_ UINT           FirstSubresource,
  _In_ UINT           NumSubresources
);
```



## <a name="parameters"></a><span data-ttu-id="7919f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7919f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7919f-108">*пдестинатионресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7919f-108">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7919f-109">Тип: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="7919f-109">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="7919f-110">Указатель на интерфейс [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) , представляющий целевой ресурс.</span><span class="sxs-lookup"><span data-stu-id="7919f-110">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the destination resource.</span></span>

</dd> <dt>

<span data-ttu-id="7919f-111">*Фирстсубресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7919f-111">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7919f-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7919f-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7919f-113">Индекс первого подресурса в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="7919f-113">The index of the first subresource in the resource.</span></span> <span data-ttu-id="7919f-114">Диапазон допустимых значений — от 0 до D3D12 \_ требований к \_ подресурсам.</span><span class="sxs-lookup"><span data-stu-id="7919f-114">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="7919f-115">*Нумсубресаурцес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7919f-115">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7919f-116">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7919f-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7919f-117">Число подресурсов в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="7919f-117">The number of subresources in the resource.</span></span> <span data-ttu-id="7919f-118">Диапазон допустимых значений — от 0 до (D3D12 \_ req \_ Resources- *фирстсубресаурце*).</span><span class="sxs-lookup"><span data-stu-id="7919f-118">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7919f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7919f-119">Return value</span></span>

<span data-ttu-id="7919f-120">Тип: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7919f-120">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7919f-121">Размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="7919f-121">The size of the buffer, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="7919f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="7919f-122">Requirements</span></span>



| <span data-ttu-id="7919f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="7919f-123">Requirement</span></span> | <span data-ttu-id="7919f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7919f-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7919f-125">Header</span><span class="sxs-lookup"><span data-stu-id="7919f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7919f-126"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7919f-126"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="7919f-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7919f-127">Library</span></span><br/> | <dl> <span data-ttu-id="7919f-128"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7919f-128"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="7919f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7919f-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="7919f-130"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7919f-130"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7919f-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7919f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7919f-132">Вспомогательные функции для D3D12</span><span class="sxs-lookup"><span data-stu-id="7919f-132">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

