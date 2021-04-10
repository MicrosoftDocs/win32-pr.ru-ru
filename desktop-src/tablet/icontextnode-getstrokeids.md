---
description: Извлекает массив идентификаторов для штрихов в объекте Иконтекстноде.
ms.assetid: 2420afec-6859-449b-92d8-0f4327281852
title: 'Метод Иконтекстноде:: Жетстрокеидс (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 25592cd245eba135fa7e459ff3c5c5207fc6ff0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145526"
---
# <a name="icontextnodegetstrokeids-method"></a><span data-ttu-id="e8061-103">Метод Иконтекстноде:: Жетстрокеидс</span><span class="sxs-lookup"><span data-stu-id="e8061-103">IContextNode::GetStrokeIds method</span></span>

<span data-ttu-id="e8061-104">Извлекает массив идентификаторов для штрихов в объекте [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="e8061-104">Retrieves an array of identifiers for the strokes within the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8061-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8061-105">Syntax</span></span>


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokes
);
```



## <a name="parameters"></a><span data-ttu-id="e8061-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8061-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8061-107">*пулстрокеидскаунт* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e8061-107">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8061-108">Число штрихов.</span><span class="sxs-lookup"><span data-stu-id="e8061-108">The number of strokes.</span></span> <span data-ttu-id="e8061-109">Передаваемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="e8061-109">The value that is passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e8061-110">*пплстрокес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e8061-110">*pplStrokes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8061-111">Указатель на массив идентификаторов Stroke для данного объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="e8061-111">A pointer to the array of stroke identifiers for this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8061-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8061-112">Return value</span></span>

<span data-ttu-id="e8061-113">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e8061-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e8061-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8061-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="e8061-115">Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *пплстрокес* , если эта информация больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="e8061-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokes* when you no longer need the information.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8061-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e8061-116">Requirements</span></span>



| <span data-ttu-id="e8061-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e8061-117">Requirement</span></span> | <span data-ttu-id="e8061-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e8061-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8061-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8061-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e8061-120">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e8061-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e8061-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8061-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e8061-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e8061-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e8061-123">Header</span><span class="sxs-lookup"><span data-stu-id="e8061-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8061-124"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e8061-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e8061-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e8061-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8061-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8061-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e8061-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8061-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8061-128">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="e8061-128">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="e8061-129">**Иконтекстноде:: Жетстрокеид**</span><span class="sxs-lookup"><span data-stu-id="e8061-129">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="e8061-130">**Иконтекстноде:: Жетстрокекаунт**</span><span class="sxs-lookup"><span data-stu-id="e8061-130">**IContextNode::GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)
</dt> <dt>

[<span data-ttu-id="e8061-131">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="e8061-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

