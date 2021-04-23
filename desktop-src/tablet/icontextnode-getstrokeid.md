---
description: Извлекает идентификатор штриха для штриха, на который ссылается значение индекса в объекте Иконтекстноде.
ms.assetid: faac142e-cac1-45f9-9b40-76c50ac7006b
title: 'Метод Иконтекстноде:: Жетстрокеид (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b193b3719ac6b67284e3ff8c4297455888f6c9cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810031"
---
# <a name="icontextnodegetstrokeid-method"></a><span data-ttu-id="ff72a-103">Метод Иконтекстноде:: Жетстрокеид</span><span class="sxs-lookup"><span data-stu-id="ff72a-103">IContextNode::GetStrokeId method</span></span>

<span data-ttu-id="ff72a-104">Извлекает идентификатор штриха для штриха, на который ссылается значение индекса в объекте [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ff72a-104">Retrieves the stroke identifier for the stroke referenced by an index value within the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff72a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff72a-105">Syntax</span></span>


```C++
HRESULT GetStrokeId(
  [in]  ULONG ulIndex,
  [out] LONG  *plStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="ff72a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff72a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff72a-107">*улиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff72a-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff72a-108">Индекс возвращаемого элемента Stroke.</span><span class="sxs-lookup"><span data-stu-id="ff72a-108">The index of the stroke to be returned.</span></span>

</dd> <dt>

<span data-ttu-id="ff72a-109">*плстрокеид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ff72a-109">*plStrokeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff72a-110">Идентификатор штриха для штриха, на который ссылается параметр *улиндекс* в текущем объекте [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ff72a-110">The stroke identifier for the stroke referenced by the *ulIndex* parameter within the current [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff72a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff72a-111">Return value</span></span>

<span data-ttu-id="ff72a-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ff72a-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff72a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ff72a-113">Requirements</span></span>



| <span data-ttu-id="ff72a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ff72a-114">Requirement</span></span> | <span data-ttu-id="ff72a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ff72a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff72a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff72a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ff72a-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ff72a-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ff72a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff72a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ff72a-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ff72a-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ff72a-120">Header</span><span class="sxs-lookup"><span data-stu-id="ff72a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff72a-121"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ff72a-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ff72a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ff72a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff72a-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff72a-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ff72a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff72a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff72a-125">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="ff72a-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ff72a-126">**Иконтекстноде:: Жетстрокеидс**</span><span class="sxs-lookup"><span data-stu-id="ff72a-126">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="ff72a-127">**Иконтекстноде:: Жетстрокекаунт**</span><span class="sxs-lookup"><span data-stu-id="ff72a-127">**IContextNode::GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)
</dt> <dt>

[<span data-ttu-id="ff72a-128">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="ff72a-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




