---
description: Получает значение, указывающее, является ли объект Иконтекстноде частично заполнен или полностью заполнен.
ms.assetid: 13ac3fb2-7baa-48d7-bf8e-f36b4031fbc4
title: 'Метод Иконтекстноде:: Жетпартиаллипопулатед (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b05cb8aae681a7302ae7da40a7412cf828fc159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145529"
---
# <a name="icontextnodegetpartiallypopulated-method"></a><span data-ttu-id="142d4-103">Метод Иконтекстноде:: Жетпартиаллипопулатед</span><span class="sxs-lookup"><span data-stu-id="142d4-103">IContextNode::GetPartiallyPopulated method</span></span>

<span data-ttu-id="142d4-104">Получает значение, указывающее, является ли объект [**иконтекстноде**](icontextnode.md) частично заполнен или полностью заполнен.</span><span class="sxs-lookup"><span data-stu-id="142d4-104">Retrieves the value that indicates whether an [**IContextNode**](icontextnode.md) object is partially populated or fully populated.</span></span>

## <a name="syntax"></a><span data-ttu-id="142d4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="142d4-105">Syntax</span></span>


```C++
HRESULT GetPartiallyPopulated(
  [out] VARIANT_BOOL *pfPartiallyPopulated
);
```



## <a name="parameters"></a><span data-ttu-id="142d4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="142d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="142d4-107">*пфпартиаллипопулатед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="142d4-107">*pfPartiallyPopulated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="142d4-108">**Вариант \_ Значение TRUE** , если данный объект [**иконтекстноде**](icontextnode.md) не содержит полных данных. в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="142d4-108">**VARIANT\_TRUE** if this [**IContextNode**](icontextnode.md) object does not contain complete data; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="142d4-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="142d4-109">Return value</span></span>

<span data-ttu-id="142d4-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="142d4-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="142d4-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="142d4-111">Remarks</span></span>

<span data-ttu-id="142d4-112">Используйте этот метод, если приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="142d4-112">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="142d4-113">Дополнительные сведения см. [в разделе Учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="142d4-113">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="142d4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="142d4-114">Requirements</span></span>



| <span data-ttu-id="142d4-115">Требование</span><span class="sxs-lookup"><span data-stu-id="142d4-115">Requirement</span></span> | <span data-ttu-id="142d4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="142d4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="142d4-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="142d4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="142d4-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="142d4-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="142d4-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="142d4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="142d4-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="142d4-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="142d4-121">Header</span><span class="sxs-lookup"><span data-stu-id="142d4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="142d4-122"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="142d4-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="142d4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="142d4-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="142d4-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="142d4-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="142d4-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="142d4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="142d4-126">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="142d4-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="142d4-127">**Иконтекстноде:: Сетпартиаллипопулатед**</span><span class="sxs-lookup"><span data-stu-id="142d4-127">**IContextNode::SetPartiallyPopulated**</span></span>](icontextnode-setpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="142d4-128">**Иконтекстноде:: Креатепартиаллипопулатедсубноде**</span><span class="sxs-lookup"><span data-stu-id="142d4-128">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="142d4-129">**\_Ианалисиспроксевентс::P Опулатеконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="142d4-129">**\_IAnalysisProxyEvents::PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[<span data-ttu-id="142d4-130">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="142d4-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




