---
description: Указывает, что в данный момент выполняет диспетчер очереди при обработке задания печати XPS.
ms.assetid: 4fa5b749-e4f9-4f08-97b5-e58f82d0b485
title: Перечисление Епринткспсжобпрогресс (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobProgress
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2a09b55ed72a6276a1a9d224cc08e03546f887d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546082"
---
# <a name="eprintxpsjobprogress-enumeration"></a><span data-ttu-id="c27bf-103">Перечисление Епринткспсжобпрогресс</span><span class="sxs-lookup"><span data-stu-id="c27bf-103">EPrintXPSJobProgress enumeration</span></span>

<span data-ttu-id="c27bf-104">Указывает, что в данный момент выполняет диспетчер очереди при обработке задания печати XPS.</span><span class="sxs-lookup"><span data-stu-id="c27bf-104">Specifies what the spooler is currently doing as it processes an XPS print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="c27bf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c27bf-105">Syntax</span></span>


```C++
typedef enum tagEPrintXPSJobProgress { 
  kAddingDocumentSequence,
  kDocumentSequenceAdded,
  kAddingFixedDocument,
  kFixedDocumentAdded,
  kAddingFixedPage,
  kFixedPageAdded,
  kResourceAdded,
  kFontAdded,
  kImageAdded,
  kXpsDocumentCommitted
} EPrintXPSJobProgress;
```



## <a name="constants"></a><span data-ttu-id="c27bf-106">Константы</span><span class="sxs-lookup"><span data-stu-id="c27bf-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c27bf-107"><span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**каддингдокументсекуенце**</span><span class="sxs-lookup"><span data-stu-id="c27bf-107"><span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**kAddingDocumentSequence**</span></span>
</dt> <dd>

<span data-ttu-id="c27bf-108">Последовательность документов собирается добавиться в задание XPS.</span><span class="sxs-lookup"><span data-stu-id="c27bf-108">A document sequence is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="c27bf-109"><span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**кдокументсекуенцеаддед**</span><span class="sxs-lookup"><span data-stu-id="c27bf-109"><span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**kDocumentSequenceAdded**</span></span>
</dt> <dd>

<span data-ttu-id="c27bf-110">В задание XPS добавлена последовательность документов.</span><span class="sxs-lookup"><span data-stu-id="c27bf-110">A document sequence has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="c27bf-111"><span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**каддингфикседдокумент**</span><span class="sxs-lookup"><span data-stu-id="c27bf-111"><span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**kAddingFixedDocument**</span></span>
</dt> <dd>

<span data-ttu-id="c27bf-112">Фиксированный документ будет добавлен в задание XPS.</span><span class="sxs-lookup"><span data-stu-id="c27bf-112">A fixed document is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="c27bf-113"><span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**кфикседдокументаддед**</span><span class="sxs-lookup"><span data-stu-id="c27bf-113"><span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**kFixedDocumentAdded**</span></span>
</dt> <dd>

<span data-ttu-id="c27bf-114">К заданию XPS добавлен фиксированный документ.</span><span class="sxs-lookup"><span data-stu-id="c27bf-114">A fixed document has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="c27bf-115"><span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**каддингфикседпаже**</span><span class="sxs-lookup"><span data-stu-id="c27bf-115"><span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**kAddingFixedPage**</span></span>
</dt> <dd>

<span data-ttu-id="c27bf-116">Страница собирается добавиться в задание XPS.</span><span class="sxs-lookup"><span data-stu-id="c27bf-116">A page is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="c27bf-117"><span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**кфикседпажеаддед**</span><span class="sxs-lookup"><span data-stu-id="c27bf-117"><span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**kFixedPageAdded**</span></span>
</dt> <dd>

<span data-ttu-id="c27bf-118">В задание XPS добавлена страница.</span><span class="sxs-lookup"><span data-stu-id="c27bf-118">A page has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="c27bf-119"><span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**кресаурцеаддед**</span><span class="sxs-lookup"><span data-stu-id="c27bf-119"><span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**kResourceAdded**</span></span>
</dt> <dd>

<span data-ttu-id="c27bf-120">Ресурс был добавлен в задание XPS.</span><span class="sxs-lookup"><span data-stu-id="c27bf-120">A resource had been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="c27bf-121"><span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**кфонтаддед**</span><span class="sxs-lookup"><span data-stu-id="c27bf-121"><span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**kFontAdded**</span></span>
</dt> <dd>

<span data-ttu-id="c27bf-122">В задание XPS добавлен шрифт.</span><span class="sxs-lookup"><span data-stu-id="c27bf-122">A font has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="c27bf-123"><span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**кимажеаддед**</span><span class="sxs-lookup"><span data-stu-id="c27bf-123"><span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**kImageAdded**</span></span>
</dt> <dd>

<span data-ttu-id="c27bf-124">В задание XPS Добавлено изображение.</span><span class="sxs-lookup"><span data-stu-id="c27bf-124">An image has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="c27bf-125"><span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**ккспсдокументкоммиттед**</span><span class="sxs-lookup"><span data-stu-id="c27bf-125"><span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**kXpsDocumentCommitted**</span></span>
</dt> <dd>

<span data-ttu-id="c27bf-126">Данные для задания XPS были зафиксированы.</span><span class="sxs-lookup"><span data-stu-id="c27bf-126">The data for the XPS job has been committed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c27bf-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c27bf-127">Remarks</span></span>

<span data-ttu-id="c27bf-128">Это перечисление в основном используется в качестве параметра функции [**репортжобпроцессингпрогресс**](reportjobprocessingprogress.md) .</span><span class="sxs-lookup"><span data-stu-id="c27bf-128">This enumeration is primarily used as a parameter for the [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) function.</span></span>

<span data-ttu-id="c27bf-129">Эти значения могут быть связаны либо с очередью печати, либо с фазой отрисовки задания печати.</span><span class="sxs-lookup"><span data-stu-id="c27bf-129">These values can refer to either the spooling or the rendering phase of a print job.</span></span>

## <a name="requirements"></a><span data-ttu-id="c27bf-130">Требования</span><span class="sxs-lookup"><span data-stu-id="c27bf-130">Requirements</span></span>



| <span data-ttu-id="c27bf-131">Требование</span><span class="sxs-lookup"><span data-stu-id="c27bf-131">Requirement</span></span> | <span data-ttu-id="c27bf-132">Значение</span><span class="sxs-lookup"><span data-stu-id="c27bf-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c27bf-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c27bf-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c27bf-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c27bf-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c27bf-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c27bf-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c27bf-136">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c27bf-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c27bf-137">Header</span><span class="sxs-lookup"><span data-stu-id="c27bf-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c27bf-138"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c27bf-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




