---
description: Извлекает тип указанного штриха.
ms.assetid: bbd0bc23-89f9-4033-bc32-f9bd737c960c
title: 'Метод Иинканализер:: Жетстрокетипе (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9358b2583f31fd26310ea880470f36404021fec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263138"
---
# <a name="iinkanalyzergetstroketype-method"></a><span data-ttu-id="690e0-103">Метод Иинканализер:: Жетстрокетипе</span><span class="sxs-lookup"><span data-stu-id="690e0-103">IInkAnalyzer::GetStrokeType method</span></span>

<span data-ttu-id="690e0-104">Извлекает тип указанного штриха.</span><span class="sxs-lookup"><span data-stu-id="690e0-104">Retrieves the type of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="690e0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="690e0-105">Syntax</span></span>


```C++
HRESULT GetStrokeType(
  [in]  LONG       lStrokeId,
  [out] StrokeType *pStrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="690e0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="690e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="690e0-107">*лстрокеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="690e0-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="690e0-108">Идентификатор штриха.</span><span class="sxs-lookup"><span data-stu-id="690e0-108">The stroke identifier.</span></span>

</dd> <dt>

<span data-ttu-id="690e0-109">*пстрокетипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="690e0-109">*pStrokeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="690e0-110">Классификация указанного штриха.</span><span class="sxs-lookup"><span data-stu-id="690e0-110">The classification of the specified stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="690e0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="690e0-111">Return value</span></span>

<span data-ttu-id="690e0-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="690e0-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="690e0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="690e0-113">Remarks</span></span>

<span data-ttu-id="690e0-114">Если тип штриха — [**строкетипе**](stroketype.md) значение строкетипе \_ неклассифицировано, [**иинканализер**](iinkanalyzer.md) классифицирует штрих во время анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="690e0-114">If the stroke's type is the [**StrokeType**](stroketype.md) value StrokeType\_Unclassified, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="690e0-115">В противном случае **иинканализер** использует тип, заданный для штриха.</span><span class="sxs-lookup"><span data-stu-id="690e0-115">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="690e0-116">[**Иинканализер**](iinkanalyzer.md) не задает значение типа Stroke как часть анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="690e0-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="690e0-117">Чтобы указать или изменить тип обводки, используйте метод [**иинканализер:: сетстрокетипе**](iinkanalyzer-setstroketype.md) или [**метод Иинканализер:: сетстрокестипе**](iinkanalyzer-setstrokestype.md).</span><span class="sxs-lookup"><span data-stu-id="690e0-117">To specify or change the stroke type, use [**IInkAnalyzer::SetStrokeType Method**](iinkanalyzer-setstroketype.md) or [**IInkAnalyzer::SetStrokesType Method**](iinkanalyzer-setstrokestype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="690e0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="690e0-118">Requirements</span></span>



| <span data-ttu-id="690e0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="690e0-119">Requirement</span></span> | <span data-ttu-id="690e0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="690e0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="690e0-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="690e0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="690e0-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="690e0-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="690e0-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="690e0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="690e0-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="690e0-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="690e0-125">Header</span><span class="sxs-lookup"><span data-stu-id="690e0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="690e0-126"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="690e0-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="690e0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="690e0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="690e0-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="690e0-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="690e0-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="690e0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="690e0-130">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="690e0-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="690e0-131">**Метод Иинканализер:: Сетстрокетипе**</span><span class="sxs-lookup"><span data-stu-id="690e0-131">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> <dt>

[<span data-ttu-id="690e0-132">**Метод Иинканализер:: Сетстрокестипе**</span><span class="sxs-lookup"><span data-stu-id="690e0-132">**IInkAnalyzer::SetStrokesType Method**</span></span>](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[<span data-ttu-id="690e0-133">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="690e0-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




