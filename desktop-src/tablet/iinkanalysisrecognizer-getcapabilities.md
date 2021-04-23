---
description: Получает возможности распознавателя.
ms.assetid: 9014bd9b-54fb-4735-9eb8-56a6188a5fc0
title: 'Метод Иинканалисисрекогнизер:: Capabilities (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetCapabilities
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07b66ffbed6f3e57edb8a6bfad36959fabbc047c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145493"
---
# <a name="iinkanalysisrecognizergetcapabilities-method"></a><span data-ttu-id="8db6a-103">Метод Иинканалисисрекогнизер:: Capabilities</span><span class="sxs-lookup"><span data-stu-id="8db6a-103">IInkAnalysisRecognizer::GetCapabilities method</span></span>

<span data-ttu-id="8db6a-104">Получает возможности распознавателя.</span><span class="sxs-lookup"><span data-stu-id="8db6a-104">Retrieves the capabilities of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="8db6a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8db6a-105">Syntax</span></span>


```C++
HRESULT GetCapabilities(
  [out] InkAnalysisRecognizerCapabilities *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="8db6a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8db6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8db6a-107">*пкапабилитиес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8db6a-107">*pCapabilities* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8db6a-108">Побитовое сочетание значений [**рекогнизеркапабилитиес**](recognizercapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="8db6a-108">A bitwise combination of [**RecognizerCapabilities**](recognizercapabilities.md) values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8db6a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8db6a-109">Return value</span></span>

<span data-ttu-id="8db6a-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8db6a-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8db6a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8db6a-111">Remarks</span></span>

<span data-ttu-id="8db6a-112">Это значение является константой для каждого [ **иинканалисисрекогнизер**](iinkanalysisrecognizer.md)</span><span class="sxs-lookup"><span data-stu-id="8db6a-112">This value is constant for each [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="8db6a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8db6a-113">Requirements</span></span>



| <span data-ttu-id="8db6a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8db6a-114">Requirement</span></span> | <span data-ttu-id="8db6a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8db6a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8db6a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8db6a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8db6a-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8db6a-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8db6a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8db6a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8db6a-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8db6a-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8db6a-120">Header</span><span class="sxs-lookup"><span data-stu-id="8db6a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8db6a-121"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8db6a-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8db6a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8db6a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8db6a-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8db6a-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8db6a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8db6a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8db6a-125">**иинканалисисрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="8db6a-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="8db6a-126">**рекогнизеркапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="8db6a-126">**RecognizerCapabilities**</span></span>](recognizercapabilities.md)
</dt> <dt>

[<span data-ttu-id="8db6a-127">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="8db6a-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




