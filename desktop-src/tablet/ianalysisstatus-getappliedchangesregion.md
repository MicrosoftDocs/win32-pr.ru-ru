---
description: Извлекает регион документа, соответствующий изменениям, внесенным в дереве узлов контекста объекта Иинканализер в результате анализа рукописного ввода.
ms.assetid: 25d511fb-ba2d-4c46-8a8c-8bb4187c9a5c
title: 'Метод Ианалисисстатус:: Жетапплиедчанжесрегион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.GetAppliedChangesRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 08f6690091207b648c39cded161de64585e44b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542087"
---
# <a name="ianalysisstatusgetappliedchangesregion-method"></a><span data-ttu-id="b4124-103">Метод Ианалисисстатус:: Жетапплиедчанжесрегион</span><span class="sxs-lookup"><span data-stu-id="b4124-103">IAnalysisStatus::GetAppliedChangesRegion method</span></span>

<span data-ttu-id="b4124-104">Извлекает регион документа, соответствующий изменениям, внесенным в дереве узлов контекста объекта [**иинканализер**](iinkanalyzer.md) в результате анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="b4124-104">Retrieves the region of the document that corresponds to changes that were made in the [**IInkAnalyzer**](iinkanalyzer.md) object's context node tree as a result of ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4124-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4124-105">Syntax</span></span>


```C++
HRESULT GetAppliedChangesRegion(
  [out] IAnalysisRegion **pAppliedChangesRegion
);
```



## <a name="parameters"></a><span data-ttu-id="b4124-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4124-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4124-107">*папплиедчанжесрегион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b4124-107">*pAppliedChangesRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4124-108">Указатель на [**ианалисисрегион**](ianalysisregion.md) документа, в котором были внесены изменения.</span><span class="sxs-lookup"><span data-stu-id="b4124-108">A pointer to the [**IAnalysisRegion**](ianalysisregion.md) of the document where changes were made.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4124-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4124-109">Return value</span></span>

<span data-ttu-id="b4124-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b4124-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b4124-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4124-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b4124-112">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *папплиедчанжесрегион* , когда больше не нужно использовать область анализа.</span><span class="sxs-lookup"><span data-stu-id="b4124-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pAppliedChangesRegion* when you no longer need to use the analysis region.</span></span>

 

<span data-ttu-id="b4124-113">Этот метод чаще всего используется, когда приложение получает сведения для отладки и должно стать недействительным область, в которой могут возникнуть изменения, чтобы отрисовывать отладочную информацию.</span><span class="sxs-lookup"><span data-stu-id="b4124-113">This method is most frequently used when the application receives information for debugging purposes and needs to invalidate the area where changes might occur so that the debugging information is painted.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4124-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b4124-114">Requirements</span></span>



| <span data-ttu-id="b4124-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b4124-115">Requirement</span></span> | <span data-ttu-id="b4124-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b4124-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4124-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4124-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b4124-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b4124-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b4124-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4124-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b4124-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b4124-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b4124-121">Header</span><span class="sxs-lookup"><span data-stu-id="b4124-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4124-122"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b4124-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b4124-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b4124-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4124-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4124-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b4124-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4124-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4124-126">**ианалисисстатус**</span><span class="sxs-lookup"><span data-stu-id="b4124-126">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="b4124-127">**ианалисисрегион**</span><span class="sxs-lookup"><span data-stu-id="b4124-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="b4124-128">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="b4124-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

