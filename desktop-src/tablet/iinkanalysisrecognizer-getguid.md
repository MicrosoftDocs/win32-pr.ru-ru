---
description: Получает глобальный уникальный идентификатор (GUID) распознавателя.
ms.assetid: 9b98993b-eaf3-4207-9d56-33efeceb75cf
title: Метод Иинканалисисрекогнизер::-GUID (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetGuid
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9a027a405829e6d1237a8ec90dd59fcc8905006d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897478"
---
# <a name="iinkanalysisrecognizergetguid-method"></a><span data-ttu-id="a0e2b-103">Метод Иинканалисисрекогнизер::</span><span class="sxs-lookup"><span data-stu-id="a0e2b-103">IInkAnalysisRecognizer::GetGuid method</span></span>

<span data-ttu-id="a0e2b-104">Получает глобальный уникальный идентификатор (GUID) распознавателя.</span><span class="sxs-lookup"><span data-stu-id="a0e2b-104">Retrieves the globally unique identifier (GUID) of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0e2b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0e2b-105">Syntax</span></span>


```C++
HRESULT GetGuid(
  [out] GUID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="a0e2b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0e2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0e2b-107">*идентификатор процесса* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a0e2b-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0e2b-108">Идентификатор GUID, определяющий этот [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="a0e2b-108">The GUID that identifies this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0e2b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0e2b-109">Return value</span></span>

<span data-ttu-id="a0e2b-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a0e2b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0e2b-111">Требования</span><span class="sxs-lookup"><span data-stu-id="a0e2b-111">Requirements</span></span>



| <span data-ttu-id="a0e2b-112">Требование</span><span class="sxs-lookup"><span data-stu-id="a0e2b-112">Requirement</span></span> | <span data-ttu-id="a0e2b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a0e2b-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0e2b-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0e2b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a0e2b-115">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a0e2b-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a0e2b-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0e2b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a0e2b-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a0e2b-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a0e2b-118">Header</span><span class="sxs-lookup"><span data-stu-id="a0e2b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0e2b-119"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a0e2b-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a0e2b-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a0e2b-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0e2b-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0e2b-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a0e2b-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0e2b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0e2b-123">**иинканалисисрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="a0e2b-123">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="a0e2b-124">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="a0e2b-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




