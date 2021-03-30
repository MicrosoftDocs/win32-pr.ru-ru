---
description: Определяет, содержит ли указанный Ианалисисрегион значение, совпадающее с текущим объектом Ианалисисрегион.
ms.assetid: 44c09cfe-65fc-4175-ad05-01c605218c58
title: 'Метод Ианалисисрегион:: Екуалсрегион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.EqualsRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6a647c13f1279cd39e4947b9fdbcc9ed4e1ef4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145562"
---
# <a name="ianalysisregionequalsregion-method"></a><span data-ttu-id="e1d1c-103">Метод Ианалисисрегион:: Екуалсрегион</span><span class="sxs-lookup"><span data-stu-id="e1d1c-103">IAnalysisRegion::EqualsRegion method</span></span>

<span data-ttu-id="e1d1c-104">Определяет, содержит ли указанный [**ианалисисрегион**](ianalysisregion.md) значение, совпадающее с текущим объектом **ианалисисрегион** .</span><span class="sxs-lookup"><span data-stu-id="e1d1c-104">Determines whether the specified [**IAnalysisRegion**](ianalysisregion.md) contains the same value as the current **IAnalysisRegion** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d1c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1d1c-105">Syntax</span></span>


```C++
HRESULT EqualsRegion(
  [in]  IAnalysisRegion *pOtherRegion,
  [out] VARIANT_BOOL    *pfRegionsEqual
);
```



## <a name="parameters"></a><span data-ttu-id="e1d1c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1d1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1d1c-107">*посеррегион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1d1c-107">*pOtherRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1d1c-108">Объект [**ианалисисрегион**](ianalysisregion.md) для сравнения с текущим **ианалисисрегион**.</span><span class="sxs-lookup"><span data-stu-id="e1d1c-108">The [**IAnalysisRegion**](ianalysisregion.md) object to compare with the current **IAnalysisRegion**.</span></span>

</dd> <dt>

<span data-ttu-id="e1d1c-109">*пфрегионсекуал* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e1d1c-109">*pfRegionsEqual* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1d1c-110">**Вариант \_ Значение TRUE** , если указанный [**ианалисисрегион**](ianalysisregion.md) содержит то же значение, что и текущий ианалисисрегион; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="e1d1c-110">**VARIANT\_TRUE** if the specified [**IAnalysisRegion**](ianalysisregion.md) contains the same value as the current IAnalysisRegion; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1d1c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1d1c-111">Return value</span></span>

<span data-ttu-id="e1d1c-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e1d1c-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1d1c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e1d1c-113">Requirements</span></span>



| <span data-ttu-id="e1d1c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e1d1c-114">Requirement</span></span> | <span data-ttu-id="e1d1c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e1d1c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d1c-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e1d1c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e1d1c-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e1d1c-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e1d1c-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e1d1c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e1d1c-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e1d1c-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e1d1c-120">Header</span><span class="sxs-lookup"><span data-stu-id="e1d1c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1d1c-121"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e1d1c-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e1d1c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e1d1c-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1d1c-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1d1c-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e1d1c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1d1c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d1c-125">**ианалисисрегион**</span><span class="sxs-lookup"><span data-stu-id="e1d1c-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> </dl>

 

 




