---
title: Функция Коммандлисткаст (D3dx12. h)
description: Этот шаблон функции приводит указатель константы к любому списку команд в указатель const на ID3D12CommandList.
ms.assetid: 63719AA1-2119-456C-9D23-13933D38AFA9
keywords:
- Функция Коммандлисткаст
topic_type:
- apiref
api_name:
- CommandListCast
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a740258f74975fecac3e1a4df2412f1fae92f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713927"
---
# <a name="commandlistcast-function"></a><span data-ttu-id="fe14d-104">Функция Коммандлисткаст</span><span class="sxs-lookup"><span data-stu-id="fe14d-104">CommandListCast function</span></span>

<span data-ttu-id="fe14d-105">Этот шаблон функции приводит указатель константы к любому списку команд в указатель const на ID3D12CommandList.</span><span class="sxs-lookup"><span data-stu-id="fe14d-105">This function template casts a constant pointer to any command list into a const pointer to an ID3D12CommandList.</span></span>

<span data-ttu-id="fe14d-106">Это приведение полезно для передачи строго типизированных указателей списка команд в [**ексекутекоммандлистс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span><span class="sxs-lookup"><span data-stu-id="fe14d-106">This cast is useful for passing strongly-typed command list pointers into [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span></span>

## <a name="syntax"></a><span data-ttu-id="fe14d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe14d-107">Syntax</span></span>


```C++
ID3D12CommandList * const * inline CommandListCast(
   t_CommandListType * const * pp
);
```



## <a name="parameters"></a><span data-ttu-id="fe14d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe14d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe14d-109">*PP*</span><span class="sxs-lookup"><span data-stu-id="fe14d-109">*pp*</span></span> 
</dt> <dd>

<span data-ttu-id="fe14d-110">Тип: **t \_ коммандлисттипе \* const \***</span><span class="sxs-lookup"><span data-stu-id="fe14d-110">Type: **t\_CommandListType \* const \***</span></span>

<span data-ttu-id="fe14d-111">Строго типизированный список команд для приведения.</span><span class="sxs-lookup"><span data-stu-id="fe14d-111">The strongly-typed command list to cast.</span></span>

<span data-ttu-id="fe14d-112">Аргумент шаблона **t \_ коммандлисттипе** указывает любой строго типизированный объект списка команд.</span><span class="sxs-lookup"><span data-stu-id="fe14d-112">The template argument **t\_CommandListType** specifies any strongly-typed command list object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe14d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe14d-113">Return value</span></span>

<span data-ttu-id="fe14d-114">Тип: **ID3D12CommandList \* const \***</span><span class="sxs-lookup"><span data-stu-id="fe14d-114">Type: **ID3D12CommandList \* const \***</span></span>

<span data-ttu-id="fe14d-115">Строго типизированный список команд, повторно интерпретируемый как [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist).</span><span class="sxs-lookup"><span data-stu-id="fe14d-115">The strongly-typed command list, reinterpreted as an [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe14d-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe14d-116">Remarks</span></span>

<span data-ttu-id="fe14d-117">Коммандлисткаст выполняет **переинтерпретируемое \_ приведение**.</span><span class="sxs-lookup"><span data-stu-id="fe14d-117">CommandListCast performs a **reinterpret\_cast**.</span></span> <span data-ttu-id="fe14d-118">Приведение допустимо, пока учитывается константа-rvalue характеристики списка команд.</span><span class="sxs-lookup"><span data-stu-id="fe14d-118">The cast is valid as long as the const-ness of the command list is respected.</span></span>

<span data-ttu-id="fe14d-119">Функция Коммандлисткаст определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="fe14d-119">The CommandListCast function is defined as the following:</span></span>


```C++
template <typename t_CommandListType>
inline ID3D12CommandList * const * CommandListCast(t_CommandListType * const * pp)
{
    return reinterpret_cast<ID3D12CommandList * const *>(pp);
}
          
```



## <a name="requirements"></a><span data-ttu-id="fe14d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="fe14d-120">Requirements</span></span>



| <span data-ttu-id="fe14d-121">Требование</span><span class="sxs-lookup"><span data-stu-id="fe14d-121">Requirement</span></span> | <span data-ttu-id="fe14d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="fe14d-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fe14d-123">Header</span><span class="sxs-lookup"><span data-stu-id="fe14d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fe14d-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe14d-124"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="fe14d-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fe14d-125">Library</span></span><br/> | <dl> <span data-ttu-id="fe14d-126"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe14d-126"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="fe14d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fe14d-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="fe14d-128"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe14d-128"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe14d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe14d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe14d-130">Вспомогательные функции для D3D12</span><span class="sxs-lookup"><span data-stu-id="fe14d-130">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





