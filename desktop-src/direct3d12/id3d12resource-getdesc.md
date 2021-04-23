---
title: ID3D12Resource, метод
description: Возвращает описание ресурса.
ms.assetid: B8D84D69-6B13-4E86-8EF6-A841354B1E5C
keywords:
- Метод DESC
- Метод DESC, интерфейс ID3D12Resource
- Интерфейс ID3D12Resource, метод DESC
topic_type:
- apiref
api_name:
- ID3D12Resource.GetDesc
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
api_location:
- d3d12.h
ms.openlocfilehash: 5be3f6f825370c467388805c84096240441d09a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105700757"
---
# <a name="id3d12resourcegetdesc-method"></a><span data-ttu-id="24c45-106">Метод ID3D12Resource:: DESC</span><span class="sxs-lookup"><span data-stu-id="24c45-106">ID3D12Resource::GetDesc method</span></span>

<span data-ttu-id="24c45-107">Возвращает описание ресурса.</span><span class="sxs-lookup"><span data-stu-id="24c45-107">Gets the resource description.</span></span>

## <a name="syntax"></a><span data-ttu-id="24c45-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24c45-108">Syntax</span></span>


```C++
D3D12_RESOURCE_DESC GetDesc();
```



## <a name="parameters"></a><span data-ttu-id="24c45-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="24c45-109">Parameters</span></span>

<span data-ttu-id="24c45-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="24c45-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="24c45-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24c45-111">Return value</span></span>

<span data-ttu-id="24c45-112">Тип: **[ **D3D12 \_ ресурс \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)**</span><span class="sxs-lookup"><span data-stu-id="24c45-112">Type: **[**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)**</span></span>

<span data-ttu-id="24c45-113">Структура описания ресурсов Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="24c45-113">A Direct3D 12 resource description structure.</span></span>

## <a name="examples"></a><span data-ttu-id="24c45-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="24c45-114">Examples</span></span>

<span data-ttu-id="24c45-115">Возвращает требуемый размер буфера, используемый для передачи данных.</span><span class="sxs-lookup"><span data-stu-id="24c45-115">Returns required size of a buffer to be used for data upload.</span></span>


```C++
// Returns required size of a buffer to be used for data upload
inline UINT64 GetRequiredIntermediateSize(
    _In_ ID3D12Resource* pDestinationResource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES) UINT FirstSubresource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES-FirstSubresource) UINT NumSubresources)
{
    D3D12_RESOURCE_DESC Desc = pDestinationResource->GetDesc();
    UINT64 RequiredSize = 0;
    
    ID3D12Device* pDevice;
    pDestinationResource->GetDevice(__uuidof(*pDevice), reinterpret_cast<void**>(&pDevice));
    pDevice->GetCopyableFootprints(&Desc, FirstSubresource, NumSubresources, 0, nullptr, nullptr, nullptr, &RequiredSize);
    pDevice->Release();
    
    return RequiredSize;
}
```



<span data-ttu-id="24c45-116">См. [пример кода в справочнике по D3D12](notes-on-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="24c45-116">Refer to the [Example Code in the D3D12 Reference](notes-on-example-code.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="24c45-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24c45-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24c45-118">**ID3D12Resource**</span><span class="sxs-lookup"><span data-stu-id="24c45-118">**ID3D12Resource**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)
</dt> </dl>

 

 




