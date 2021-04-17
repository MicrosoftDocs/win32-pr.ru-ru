---
title: Функция D3D12GetFormatPlaneCount (D3dx12. h)
description: Возвращает число плоскостей для указанного формата DXGI для указанного виртуального адаптера (ID3D12Device).
ms.assetid: CD21F6F9-A9AA-4CE8-A430-57C70326CB4B
keywords:
- Функция D3D12GetFormatPlaneCount
topic_type:
- apiref
api_name:
- D3D12GetFormatPlaneCount
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfc2e88c162068de2b97c9df5071398e2fab068
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703663"
---
# <a name="d3d12getformatplanecount-function"></a><span data-ttu-id="53565-104">Функция D3D12GetFormatPlaneCount</span><span class="sxs-lookup"><span data-stu-id="53565-104">D3D12GetFormatPlaneCount function</span></span>

<span data-ttu-id="53565-105">Возвращает число плоскостей для указанного формата DXGI для указанного виртуального адаптера ( **ID3D12Device**).</span><span class="sxs-lookup"><span data-stu-id="53565-105">Gets the number of planes for the specified DXGI format for the specified virtual adapter (an **ID3D12Device**).</span></span>

## <a name="syntax"></a><span data-ttu-id="53565-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53565-106">Syntax</span></span>


```C++
UINT8 inline D3D12GetFormatPlaneCount(
  _In_ ID3D12Device *pDevice,
       DXGI_FORMAT  Format
);
```



## <a name="parameters"></a><span data-ttu-id="53565-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="53565-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53565-108">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53565-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53565-109">Тип: **[ **ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***</span><span class="sxs-lookup"><span data-stu-id="53565-109">Type: **[**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***</span></span>

<span data-ttu-id="53565-110">Виртуальный адаптер ( [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)), для которого необходимо получить число плоскостей.</span><span class="sxs-lookup"><span data-stu-id="53565-110">The virtual adapter (an [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)) for which to get the plane count.</span></span>

</dd> <dt>

<span data-ttu-id="53565-111">*Формат*</span><span class="sxs-lookup"><span data-stu-id="53565-111">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="53565-112">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="53565-112">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="53565-113">[**\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , для которого необходимо получить число плоскостей.</span><span class="sxs-lookup"><span data-stu-id="53565-113">The [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) for which to get the plane count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53565-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53565-114">Return value</span></span>

<span data-ttu-id="53565-115">Тип: **UINT8**</span><span class="sxs-lookup"><span data-stu-id="53565-115">Type: **UINT8**</span></span>

<span data-ttu-id="53565-116">Количество плоскостей для указанного формата на указанном виртуальном адаптере.</span><span class="sxs-lookup"><span data-stu-id="53565-116">The plane count for the specified format on the specified virtual adapter.</span></span>

## <a name="requirements"></a><span data-ttu-id="53565-117">Требования</span><span class="sxs-lookup"><span data-stu-id="53565-117">Requirements</span></span>



| <span data-ttu-id="53565-118">Требование</span><span class="sxs-lookup"><span data-stu-id="53565-118">Requirement</span></span> | <span data-ttu-id="53565-119">Значение</span><span class="sxs-lookup"><span data-stu-id="53565-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="53565-120">Header</span><span class="sxs-lookup"><span data-stu-id="53565-120">Header</span></span><br/>  | <dl> <span data-ttu-id="53565-121"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="53565-121"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="53565-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="53565-122">Library</span></span><br/> | <dl> <span data-ttu-id="53565-123"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53565-123"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="53565-124">DLL</span><span class="sxs-lookup"><span data-stu-id="53565-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="53565-125"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53565-125"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53565-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53565-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53565-127">**\_ \_ \_ Сведения о формате данных компонента D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="53565-127">**D3D12\_FEATURE\_DATA\_FORMAT\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info)
</dt> <dt>

[<span data-ttu-id="53565-128">**CheckFeatureSupport**</span><span class="sxs-lookup"><span data-stu-id="53565-128">**CheckFeatureSupport**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
</dt> <dt>

[<span data-ttu-id="53565-129">Вспомогательные функции для D3D12</span><span class="sxs-lookup"><span data-stu-id="53565-129">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

