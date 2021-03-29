---
description: Удаляет дочерний элемент Иконтекстноде.
ms.assetid: ed1d7b35-f6ba-4eff-888d-5cc492f02832
title: 'Иконтекстноде: метод:D Елетесубноде (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ffcec19e13a3ad885b3b497f80322caf9365c91a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542066"
---
# <a name="icontextnodedeletesubnode-method"></a><span data-ttu-id="b88ba-103">Иконтекстноде: метод:D Елетесубноде</span><span class="sxs-lookup"><span data-stu-id="b88ba-103">IContextNode::DeleteSubNode method</span></span>

<span data-ttu-id="b88ba-104">Удаляет дочерний элемент [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="b88ba-104">Removes a child [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b88ba-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b88ba-105">Syntax</span></span>


```C++
HRESULT DeleteSubNode(
  [in] IContextNode *pContextNodeToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="b88ba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b88ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b88ba-107">*пконтекстнодетоделете* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b88ba-107">*pContextNodeToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b88ba-108">Удаляемый [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="b88ba-108">The [**IContextNode**](icontextnode.md) to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b88ba-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b88ba-109">Return value</span></span>

<span data-ttu-id="b88ba-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b88ba-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b88ba-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b88ba-111">Remarks</span></span>

<span data-ttu-id="b88ba-112">E \_ INVALIDARG возвращается, если параметр *пконтекстнодетоделете* не является дочерним для этого объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="b88ba-112">E\_INVALIDARG is returned if the *pContextNodeToDelete* parameter is not a child of this [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="b88ba-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b88ba-113">Requirements</span></span>



| <span data-ttu-id="b88ba-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b88ba-114">Requirement</span></span> | <span data-ttu-id="b88ba-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b88ba-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b88ba-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b88ba-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b88ba-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b88ba-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b88ba-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b88ba-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b88ba-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b88ba-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b88ba-120">Header</span><span class="sxs-lookup"><span data-stu-id="b88ba-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b88ba-121"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b88ba-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b88ba-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b88ba-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b88ba-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b88ba-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b88ba-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b88ba-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b88ba-125">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="b88ba-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b88ba-126">**Иконтекстноде:: Креатесубноде**</span><span class="sxs-lookup"><span data-stu-id="b88ba-126">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="b88ba-127">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="b88ba-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




