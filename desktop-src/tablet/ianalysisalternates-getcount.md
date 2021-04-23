---
description: Возвращает количество объектов Ианалисисалтернате, содержащихся в коллекции Ианалисисалтернатес.
ms.assetid: 17b71b5a-638a-4e6e-a43b-4ca3c8eba257
title: 'Метод Ианалисисалтернатес:: NOCOUNT (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6300ff994d7bd49461e9be39aa433586ecaabc75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692456"
---
# <a name="ianalysisalternatesgetcount-method"></a><span data-ttu-id="d4ac3-103">Метод Ианалисисалтернатес:: NOCOUNT</span><span class="sxs-lookup"><span data-stu-id="d4ac3-103">IAnalysisAlternates::GetCount method</span></span>

<span data-ttu-id="d4ac3-104">Возвращает количество объектов [**ианалисисалтернате**](ianalysisalternate.md) , содержащихся в коллекции [**ианалисисалтернатес**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="d4ac3-104">Retrieves the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ac3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4ac3-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="d4ac3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4ac3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4ac3-107">*пулкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d4ac3-107">*pulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ac3-108">32-разрядное целое число без знака, равное количеству объектов [**ианалисисалтернате**](ianalysisalternate.md) , содержащихся в коллекции [**ианалисисалтернатес**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="d4ac3-108">An unsigned 32-bit integer that is set to the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4ac3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4ac3-109">Return value</span></span>

<span data-ttu-id="d4ac3-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d4ac3-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ac3-111">Требования</span><span class="sxs-lookup"><span data-stu-id="d4ac3-111">Requirements</span></span>



| <span data-ttu-id="d4ac3-112">Требование</span><span class="sxs-lookup"><span data-stu-id="d4ac3-112">Requirement</span></span> | <span data-ttu-id="d4ac3-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d4ac3-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ac3-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4ac3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d4ac3-115">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d4ac3-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d4ac3-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4ac3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d4ac3-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d4ac3-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d4ac3-118">Header</span><span class="sxs-lookup"><span data-stu-id="d4ac3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4ac3-119"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d4ac3-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d4ac3-120">DLL</span><span class="sxs-lookup"><span data-stu-id="d4ac3-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4ac3-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4ac3-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d4ac3-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4ac3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ac3-123">**ианалисисалтернатес**</span><span class="sxs-lookup"><span data-stu-id="d4ac3-123">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="d4ac3-124">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="d4ac3-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




