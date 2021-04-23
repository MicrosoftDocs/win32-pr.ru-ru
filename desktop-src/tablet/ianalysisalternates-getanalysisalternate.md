---
description: Извлекает объект Ианалисисалтернате по указанному индексу в коллекции.
ms.assetid: d927e2f1-ca21-415d-90ad-d1ded575fcb7
title: 'Метод Ианалисисалтернатес:: Жетаналисисалтернате (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 122bccc4985ed7ba5617e9d373ecdf3d0c84dac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692457"
---
# <a name="ianalysisalternatesgetanalysisalternate-method"></a><span data-ttu-id="a5b42-103">Метод Ианалисисалтернатес:: Жетаналисисалтернате</span><span class="sxs-lookup"><span data-stu-id="a5b42-103">IAnalysisAlternates::GetAnalysisAlternate method</span></span>

<span data-ttu-id="a5b42-104">Извлекает объект [**ианалисисалтернате**](ianalysisalternate.md) по указанному индексу в коллекции.</span><span class="sxs-lookup"><span data-stu-id="a5b42-104">Retrieves the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5b42-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5b42-105">Syntax</span></span>


```C++
HRESULT GetAnalysisAlternate(
  [in]  ULONG              ulIndex,
  [out] IAnalysisAlternate **ppAlternate
);
```



## <a name="parameters"></a><span data-ttu-id="a5b42-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5b42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5b42-107">*улиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5b42-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5b42-108">Отсчитываемый от нуля индекс объекта [**ианалисисалтернате**](ianalysisalternate.md) , который необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="a5b42-108">The zero-based index of the [**IAnalysisAlternate**](ianalysisalternate.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="a5b42-109">*ппалтернате* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a5b42-109">*ppAlternate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5b42-110">Указатель на объект [**ианалисисалтернате**](ianalysisalternate.md) по указанному индексу в коллекции.</span><span class="sxs-lookup"><span data-stu-id="a5b42-110">A pointer to the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5b42-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5b42-111">Return value</span></span>

<span data-ttu-id="a5b42-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a5b42-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a5b42-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5b42-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="a5b42-114">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппалтернате* , когда больше не нужно использовать альтернативный анализ.</span><span class="sxs-lookup"><span data-stu-id="a5b42-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternate* when you no longer need to use the analysis alternate.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a5b42-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a5b42-115">Requirements</span></span>



| <span data-ttu-id="a5b42-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a5b42-116">Requirement</span></span> | <span data-ttu-id="a5b42-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a5b42-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b42-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5b42-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a5b42-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a5b42-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a5b42-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5b42-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a5b42-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a5b42-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a5b42-122">Header</span><span class="sxs-lookup"><span data-stu-id="a5b42-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5b42-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a5b42-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a5b42-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a5b42-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5b42-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5b42-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a5b42-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5b42-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5b42-127">**ианалисисалтернатес**</span><span class="sxs-lookup"><span data-stu-id="a5b42-127">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="a5b42-128">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="a5b42-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

