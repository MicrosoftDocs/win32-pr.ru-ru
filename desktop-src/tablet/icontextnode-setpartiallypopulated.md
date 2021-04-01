---
description: Изменяет значение, указывающее, является ли Иконтекстноде частично или полностью заполненным.
ms.assetid: 4d8e1ec0-757d-4346-a77e-263bd612972b
title: 'Метод Иконтекстноде:: Сетпартиаллипопулатед (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 31707468945fd3c5eb413bcdb984748a55867982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072780"
---
# <a name="icontextnodesetpartiallypopulated-method"></a><span data-ttu-id="f5785-103">Метод Иконтекстноде:: Сетпартиаллипопулатед</span><span class="sxs-lookup"><span data-stu-id="f5785-103">IContextNode::SetPartiallyPopulated method</span></span>

<span data-ttu-id="f5785-104">Изменяет значение, указывающее, является ли [**иконтекстноде**](icontextnode.md) частично или полностью заполненным.</span><span class="sxs-lookup"><span data-stu-id="f5785-104">Modifies the value that indicates whether this [**IContextNode**](icontextnode.md) is partially or fully populated.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5785-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5785-105">Syntax</span></span>


```C++
HRESULT SetPartiallyPopulated(
  [in] VARIANT_BOOL fPartiallyPopulated
);
```



## <a name="parameters"></a><span data-ttu-id="f5785-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5785-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5785-107">*фпартиаллипопулатед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5785-107">*fPartiallyPopulated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5785-108">**Вариант \_ Значение TRUE** , если [**иконтекстноде**](icontextnode.md) заполняется частично; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="f5785-108">**VARIANT\_TRUE** if this [**IContextNode**](icontextnode.md) is partially populated; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5785-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5785-109">Return value</span></span>

<span data-ttu-id="f5785-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f5785-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f5785-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5785-111">Remarks</span></span>

<span data-ttu-id="f5785-112">Используйте этот метод, если приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="f5785-112">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="f5785-113">Дополнительные сведения см. [в разделе Учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f5785-113">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="f5785-114">При виртуализации дерева документов обязательно задайте значение Пропертигуидсфорконтекстнодес. Ротатедбаундингбокс (с помощью Контекстноде. Аддпропертивалуе) для всех объектов Контекстноде.</span><span class="sxs-lookup"><span data-stu-id="f5785-114">When virtualizing your document tree, be sure to set the PropertyGuidsForContextNodes.RotatedBoundingBox value (using ContextNode.AddPropertyValue) on all ContextNode objects.</span></span> <span data-ttu-id="f5785-115">Свойство Ротатедбаундингбокс вычисляется с помощью InkAnalyzer, а по умолчанию — для всех операций записи Контекстнодес.</span><span class="sxs-lookup"><span data-stu-id="f5785-115">The RotatedBoundingBox property is calculated by the InkAnalyzer and by default should be on all writing ContextNodes.</span></span> <span data-ttu-id="f5785-116">Однако если приложение виртуализировать результаты анализа, задав свойство Партиаллипопулатед, то при обработке события Популатеконтекстноде необходимо заполнить свойство Ротатедбаундингбокс.</span><span class="sxs-lookup"><span data-stu-id="f5785-116">However, if your application virtualizes the analysis results by setting the PartiallyPopulated property, when handling the PopulateContextNode event be sure to populate the RotatedBoundingBox property.</span></span> <span data-ttu-id="f5785-117">Сбой установки свойства Ротатедбаундингбокс приведет к тому, что в текущей операции анализа будет использоваться потенциально больше данных документа</span><span class="sxs-lookup"><span data-stu-id="f5785-117">Failure to set the RotatedBoundingBox property will result in potentially more document data being used in the current analysis operation</span></span>

## <a name="requirements"></a><span data-ttu-id="f5785-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f5785-118">Requirements</span></span>



| <span data-ttu-id="f5785-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f5785-119">Requirement</span></span> | <span data-ttu-id="f5785-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f5785-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5785-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5785-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f5785-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f5785-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f5785-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5785-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f5785-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f5785-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f5785-125">Header</span><span class="sxs-lookup"><span data-stu-id="f5785-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5785-126"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f5785-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f5785-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f5785-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5785-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5785-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f5785-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5785-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5785-130">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="f5785-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="f5785-131">**\_Ианалисиспроксевентс::P Опулатеконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="f5785-131">**\_IAnalysisProxyEvents::PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[<span data-ttu-id="f5785-132">**Иконтекстноде:: Креатепартиаллипопулатедсубноде**</span><span class="sxs-lookup"><span data-stu-id="f5785-132">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="f5785-133">**Иконтекстноде:: Жетпартиаллипопулатед**</span><span class="sxs-lookup"><span data-stu-id="f5785-133">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="f5785-134">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="f5785-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




