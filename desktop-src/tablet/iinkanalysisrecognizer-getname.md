---
description: Возвращает имя распознавателя.
ms.assetid: bd97fead-1e80-49dc-ada0-38eb5dc015ae
title: Метод Иинканалисисрекогнизер::-Name (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fe263878d1fd5e914cf033111997d297a20c54f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662405"
---
# <a name="iinkanalysisrecognizergetname-method"></a><span data-ttu-id="97b08-103">Метод Иинканалисисрекогнизер:: Name</span><span class="sxs-lookup"><span data-stu-id="97b08-103">IInkAnalysisRecognizer::GetName method</span></span>

<span data-ttu-id="97b08-104">Возвращает имя распознавателя.</span><span class="sxs-lookup"><span data-stu-id="97b08-104">Retrieves the name of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="97b08-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97b08-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a><span data-ttu-id="97b08-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="97b08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97b08-107">*пбстрнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="97b08-107">*pbstrName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97b08-108">Имя распознавателя.</span><span class="sxs-lookup"><span data-stu-id="97b08-108">The name of the recognizer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97b08-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97b08-109">Return value</span></span>

<span data-ttu-id="97b08-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="97b08-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="97b08-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97b08-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="97b08-112">Чтобы избежать утечки памяти, вызовите [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для \* *пбстрнаме* , когда больше не нужно использовать строку.</span><span class="sxs-lookup"><span data-stu-id="97b08-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrName* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="97b08-113">Имя локализовано для языка, не зависящего от региона, который поддерживает распознаватель.</span><span class="sxs-lookup"><span data-stu-id="97b08-113">The name is localized for the region-neutral language that the recognizer supports.</span></span>

## <a name="requirements"></a><span data-ttu-id="97b08-114">Требования</span><span class="sxs-lookup"><span data-stu-id="97b08-114">Requirements</span></span>



| <span data-ttu-id="97b08-115">Требование</span><span class="sxs-lookup"><span data-stu-id="97b08-115">Requirement</span></span> | <span data-ttu-id="97b08-116">Значение</span><span class="sxs-lookup"><span data-stu-id="97b08-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97b08-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97b08-117">Minimum supported client</span></span><br/> | <span data-ttu-id="97b08-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="97b08-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="97b08-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97b08-119">Minimum supported server</span></span><br/> | <span data-ttu-id="97b08-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="97b08-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="97b08-121">Header</span><span class="sxs-lookup"><span data-stu-id="97b08-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="97b08-122"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="97b08-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="97b08-123">DLL</span><span class="sxs-lookup"><span data-stu-id="97b08-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97b08-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97b08-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="97b08-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97b08-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97b08-126">**иинканалисисрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="97b08-126">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="97b08-127">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="97b08-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

