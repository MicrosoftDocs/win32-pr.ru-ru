---
title: Функция D3D12IsLayoutOpaque (D3dx12. h)
description: Указывает, является ли макет непрозрачным.
ms.assetid: 43B46A18-A725-4999-BD97-108032793A95
keywords:
- Функция D3D12IsLayoutOpaque
topic_type:
- apiref
api_name:
- D3D12IsLayoutOpaque
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971c44688e57dd1081d33a4a077a8dcadcb89abf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703662"
---
# <a name="d3d12islayoutopaque-function"></a><span data-ttu-id="c168a-104">Функция D3D12IsLayoutOpaque</span><span class="sxs-lookup"><span data-stu-id="c168a-104">D3D12IsLayoutOpaque function</span></span>

<span data-ttu-id="c168a-105">Указывает, является ли макет непрозрачным.</span><span class="sxs-lookup"><span data-stu-id="c168a-105">Indicates whether the layout is opaque.</span></span>

## <a name="syntax"></a><span data-ttu-id="c168a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c168a-106">Syntax</span></span>


```C++
bool inline D3D12IsLayoutOpaque(
   D3D12_TEXTURE_LAYOUT Layout
);
```



## <a name="parameters"></a><span data-ttu-id="c168a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c168a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c168a-108">*Макет*</span><span class="sxs-lookup"><span data-stu-id="c168a-108">*Layout*</span></span> 
</dt> <dd>

<span data-ttu-id="c168a-109">Тип: **[ **\_ \_ Макет текстуры D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**</span><span class="sxs-lookup"><span data-stu-id="c168a-109">Type: **[**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**</span></span>

<span data-ttu-id="c168a-110">Макет, который необходимо проверить, в [**виде \_ \_ макета текстуры D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).</span><span class="sxs-lookup"><span data-stu-id="c168a-110">The layout to check, as a [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c168a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c168a-111">Return value</span></span>

<span data-ttu-id="c168a-112">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="c168a-112">Type: **bool**</span></span>

<span data-ttu-id="c168a-113">**Логическое** значение, указывающее, является ли макет непрозрачным.</span><span class="sxs-lookup"><span data-stu-id="c168a-113">A **bool** that indicates whether the layout is opaque.</span></span> <span data-ttu-id="c168a-114">Макет является непрозрачным, если он \_ имеет \_ вид текстуры D3D12 \_ НЕизвестный или D3D12ный \_ \_ Макет текстуры \_ 64 КБ \_ неопределенный \_ свиззле.</span><span class="sxs-lookup"><span data-stu-id="c168a-114">A layout is opaque if it is D3D12\_TEXTURE\_LAYOUT\_UNKNOWN or D3D12\_TEXTURE\_LAYOUT\_64KB\_UNDEFINED\_SWIZZLE.</span></span>

## <a name="requirements"></a><span data-ttu-id="c168a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c168a-115">Requirements</span></span>



| <span data-ttu-id="c168a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c168a-116">Requirement</span></span> | <span data-ttu-id="c168a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c168a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c168a-118">Header</span><span class="sxs-lookup"><span data-stu-id="c168a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c168a-119"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c168a-119"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="c168a-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c168a-120">Library</span></span><br/> | <dl> <span data-ttu-id="c168a-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c168a-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="c168a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c168a-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="c168a-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c168a-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c168a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c168a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c168a-125">Вспомогательные функции для D3D12</span><span class="sxs-lookup"><span data-stu-id="c168a-125">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





