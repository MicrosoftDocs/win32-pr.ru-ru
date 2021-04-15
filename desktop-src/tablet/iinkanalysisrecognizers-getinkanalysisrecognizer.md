---
description: Извлекает Иинканалисисрекогнизер по указанному индексу.
ms.assetid: e4db56c6-7c15-4336-bc0a-f50222c3520e
title: 'Метод Иинканалисисрекогнизерс:: Жетинканалисисрекогнизер (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1008ae0b26d30233c3b00167391523d321cd381e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497571"
---
# <a name="iinkanalysisrecognizersgetinkanalysisrecognizer-method"></a><span data-ttu-id="81322-103">Метод Иинканалисисрекогнизерс:: Жетинканалисисрекогнизер</span><span class="sxs-lookup"><span data-stu-id="81322-103">IInkAnalysisRecognizers::GetInkAnalysisRecognizer method</span></span>

<span data-ttu-id="81322-104">Извлекает [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="81322-104">Retrieves the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="81322-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81322-105">Syntax</span></span>


```C++
HRESULT GetInkAnalysisRecognizer(
  [in]  ULONG                  ulIndex,
  [out] IInkAnalysisRecognizer **ppInkAnalysisRecognizer
);
```



## <a name="parameters"></a><span data-ttu-id="81322-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="81322-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81322-107">*улиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81322-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81322-108">Отсчитываемый от нуля индекс объекта [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) , который необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="81322-108">The zero-based index of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="81322-109">*ппинканалисисрекогнизер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="81322-109">*ppInkAnalysisRecognizer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81322-110">Указатель на [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="81322-110">A pointer to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81322-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81322-111">Return value</span></span>

<span data-ttu-id="81322-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="81322-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="81322-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81322-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="81322-114">Чтобы избежать утечки памяти, вызовите [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппинканалисисрекогнизер* , когда больше не нужно использовать распознаватель рукописного анализа.</span><span class="sxs-lookup"><span data-stu-id="81322-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppInkAnalysisRecognizer* when you no longer need to use the ink analysis recognizer.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="81322-115">Требования</span><span class="sxs-lookup"><span data-stu-id="81322-115">Requirements</span></span>



| <span data-ttu-id="81322-116">Требование</span><span class="sxs-lookup"><span data-stu-id="81322-116">Requirement</span></span> | <span data-ttu-id="81322-117">Значение</span><span class="sxs-lookup"><span data-stu-id="81322-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81322-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81322-118">Minimum supported client</span></span><br/> | <span data-ttu-id="81322-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="81322-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="81322-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81322-120">Minimum supported server</span></span><br/> | <span data-ttu-id="81322-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="81322-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="81322-122">Header</span><span class="sxs-lookup"><span data-stu-id="81322-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="81322-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="81322-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="81322-124">DLL</span><span class="sxs-lookup"><span data-stu-id="81322-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81322-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81322-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="81322-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81322-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81322-127">**инканалисисрекогнизерс**</span><span class="sxs-lookup"><span data-stu-id="81322-127">**InkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="81322-128">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="81322-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

