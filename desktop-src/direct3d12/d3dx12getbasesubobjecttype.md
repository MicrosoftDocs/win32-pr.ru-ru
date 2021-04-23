---
title: Функция D3DX12GetBaseSubobjectType (D3dx12. h)
description: Возвращает тип подобъекта, соответствующий базовому классу переданного типа подобъекта.
ms.assetid: 3744B042-094C-4EA4-8185-A018B728D843
keywords:
- Функция D3DX12GetBaseSubobjectType
topic_type:
- apiref
api_name:
- D3DX12GetBaseSubobjectType
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b39f1c61be682d55512772bef1258aecdb009a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703661"
---
# <a name="d3dx12getbasesubobjecttype-function"></a><span data-ttu-id="2e72e-104">Функция D3DX12GetBaseSubobjectType</span><span class="sxs-lookup"><span data-stu-id="2e72e-104">D3DX12GetBaseSubobjectType function</span></span>

<span data-ttu-id="2e72e-105">Возвращает тип подобъекта, соответствующий базовому классу переданного типа подобъекта.</span><span class="sxs-lookup"><span data-stu-id="2e72e-105">Returns the subobject type that corresponds to the base class of the passed-in subobject type.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e72e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e72e-106">Syntax</span></span>


```C++
D3D12_PIPELINE_STATE_SUBOBJECT_TYPE inline D3DX12GetBaseSubobjectType(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE SubobjectType
);
```



## <a name="parameters"></a><span data-ttu-id="2e72e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e72e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e72e-108">*субобжекттипе*</span><span class="sxs-lookup"><span data-stu-id="2e72e-108">*SubobjectType*</span></span> 
</dt> <dd>

<span data-ttu-id="2e72e-109">Тип: **\_ \_ \_ \_ тип подобъекта состояния конвейера D3D12**</span><span class="sxs-lookup"><span data-stu-id="2e72e-109">Type: **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>

<span data-ttu-id="2e72e-110">Значение перечисления, указывающее тип подобъекта, который вас интересует.</span><span class="sxs-lookup"><span data-stu-id="2e72e-110">An enumeration value that specifies the subobject type that you're interested in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e72e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e72e-111">Return value</span></span>

<span data-ttu-id="2e72e-112">Тип: **\_ \_ \_ \_ тип подобъекта состояния конвейера D3D12**</span><span class="sxs-lookup"><span data-stu-id="2e72e-112">Type: **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>

<span data-ttu-id="2e72e-113">Если *субобжекттипе* соответствует типу данных подобъекта, производного от другого типа данных подобъекта, возвращается тип подобъекта базового типа данных подобъекта. в противном случае возвращается переданный тип подобъекта.</span><span class="sxs-lookup"><span data-stu-id="2e72e-113">If *SubobjectType* corresponds to a subobject data type that is derived from another subobject data type, the subobject type of the base subobject data type is returned; otherwise, the passed-in subobject type is returned.</span></span> <span data-ttu-id="2e72e-114">Например, если передается **\_ \_ \_ \_ \_ глубина \_ STENCIL1 типа вложенного объекта состояния конвейера D3D12** , то возвращается **\_ \_ \_ \_ \_ \_ набор элементов с типом подобъекта глубины конвейера D3D12** .</span><span class="sxs-lookup"><span data-stu-id="2e72e-114">For example, if **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL1** is passed in, then **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e72e-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="2e72e-115">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2e72e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="2e72e-116">Requirements</span></span>



| <span data-ttu-id="2e72e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="2e72e-117">Requirement</span></span> | <span data-ttu-id="2e72e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2e72e-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2e72e-119">Header</span><span class="sxs-lookup"><span data-stu-id="2e72e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2e72e-120"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e72e-120"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="2e72e-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2e72e-121">Library</span></span><br/> | <dl> <span data-ttu-id="2e72e-122"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e72e-122"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="2e72e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="2e72e-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="2e72e-124"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e72e-124"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e72e-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e72e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e72e-126">Вспомогательные функции для D3D12</span><span class="sxs-lookup"><span data-stu-id="2e72e-126">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





