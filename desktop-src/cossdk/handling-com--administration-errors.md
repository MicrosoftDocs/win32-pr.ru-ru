---
description: Обработка ошибок администрирования COM+
ms.assetid: 03f00c19-ff81-478b-b545-048f3dbe5eda
title: Обработка ошибок администрирования COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e7e5838d7fee7616a23f5e361df1aef65421492
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710747"
---
# <a name="handling-com-administration-errors"></a><span data-ttu-id="9d2cb-103">Обработка ошибок администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="9d2cb-103">Handling COM+ Administration Errors</span></span>

<span data-ttu-id="9d2cb-104">Ошибки, формируемые при использовании объектов Комадмин, регистрируются двумя способами:</span><span class="sxs-lookup"><span data-stu-id="9d2cb-104">Errors that are generated when using the COMAdmin objects are reported in two ways, as follows:</span></span>

-   <span data-ttu-id="9d2cb-105">Использование кодов ошибок, характерных для библиотеки Комадмин.</span><span class="sxs-lookup"><span data-stu-id="9d2cb-105">Using error codes specific to the COMAdmin library.</span></span>
-   <span data-ttu-id="9d2cb-106">Использование расширенных сведений об ошибках, доступных в специальной коллекции [**errorInfo**](errorinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="9d2cb-106">Using extended error information available in a special [**ErrorInfo**](errorinfo.md) collection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9d2cb-107">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="9d2cb-107">Error Codes</span></span>

<span data-ttu-id="9d2cb-108">Код ошибок администрирования обрабатывается так же, как и любое сообщение об ошибке COM.</span><span class="sxs-lookup"><span data-stu-id="9d2cb-108">You handle administration error codes as you would any COM error message.</span></span> <span data-ttu-id="9d2cb-109">В Microsoft Visual C++ эти коды возвращаются в виде значений **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9d2cb-109">In Microsoft Visual C++, these codes are returned as **HRESULT** values.</span></span> <span data-ttu-id="9d2cb-110">В Microsoft Visual Basic они создаются как исключения, которые можно перехватить.</span><span class="sxs-lookup"><span data-stu-id="9d2cb-110">In Microsoft Visual Basic, they are thrown as exceptions that you can catch.</span></span> <span data-ttu-id="9d2cb-111">Для программистов C++ коды ошибок администрирования COM+ определяются в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="9d2cb-111">For C++ programmers, the COM+ administration error codes are defined in Winerror.h.</span></span> <span data-ttu-id="9d2cb-112">Для Visual Basic программистов они доступны в интегрированной среде разработки Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9d2cb-112">For Visual Basic programmers, they are available through the Visual Basic IDE.</span></span>

## <a name="errorinfo-collection"></a><span data-ttu-id="9d2cb-113">Коллекция ErrorInfo</span><span class="sxs-lookup"><span data-stu-id="9d2cb-113">ErrorInfo Collection</span></span>

<span data-ttu-id="9d2cb-114">При возникновении ошибки, о которой сообщается какой либо код ошибки, может быть доступна более подробная информация в зависимости от характера ошибки.</span><span class="sxs-lookup"><span data-stu-id="9d2cb-114">When an error occurs, signaled by some kind of failure code, more detailed information may be available, depending on the nature of the error.</span></span> <span data-ttu-id="9d2cb-115">Объекты Комадмин предоставляют расширенные сведения в случаях, когда точная причина сбоя трудно определить без подробного отчета, например с несколькими операциями чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="9d2cb-115">The COMAdmin objects provide extended information in circumstances where the precise cause of the failure is difficult to determine without a detailed report, such as with multiple read and write operations.</span></span>

<span data-ttu-id="9d2cb-116">Например, при использовании таких методов, как [**Заполнение**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) и [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) для объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) , можно считывать или записывать данные для каждого элемента в коллекции.</span><span class="sxs-lookup"><span data-stu-id="9d2cb-116">For example, when you use methods such as [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on a [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, you can be reading or writing data for every item in the collection.</span></span> <span data-ttu-id="9d2cb-117">Могут возникать сложные ошибки, которые могут быть трудно диагностировать на основе одного числового кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="9d2cb-117">Complicated errors can occur, and they can be difficult to diagnose based on a single numeric error code.</span></span> <span data-ttu-id="9d2cb-118">Таким образом, Библиотека Комадмин предоставляет расширенные сведения об ошибке через специальную коллекцию.</span><span class="sxs-lookup"><span data-stu-id="9d2cb-118">Therefore, the COMAdmin Library makes extended error information through a special collection.</span></span>

<span data-ttu-id="9d2cb-119">Когда доступна расширенная информация об ошибке, она помещается в коллекцию [**errorInfo**](errorinfo.md) , связанную с исходной коллекцией, в которой возникла ошибка.</span><span class="sxs-lookup"><span data-stu-id="9d2cb-119">When extended error information is available, it is placed in the [**ErrorInfo**](errorinfo.md) collection that is related to the original collection that had the error.</span></span> <span data-ttu-id="9d2cb-120">Чтобы получить отчет об ошибках, получите коллекцию **errorInfo** , связанную с исходной коллекцией, и изучите содержащиеся в ней элементы.</span><span class="sxs-lookup"><span data-stu-id="9d2cb-120">To retrieve the error report, get the **ErrorInfo** collection that is related to the original collection and examine the items it contains.</span></span> <span data-ttu-id="9d2cb-121">Коллекцию **errorInfo** можно получить с помощью функции [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) в [**комадминкаталогколлектион**](comadmincatalogcollection.md), и оставить второй параметр пустым, где обычно указывается свойство ключа родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="9d2cb-121">You can retrieve the **ErrorInfo** collection by using [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) on [**COMAdminCatalogCollection**](comadmincatalogcollection.md), leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

<span data-ttu-id="9d2cb-122">При возникновении ошибки необходимо немедленно получить и заполнить коллекцию [**errorInfo**](errorinfo.md) для коллекции, которая завершилась сбоем, без выполнения каких бы то ни было других операций с этой коллекцией.</span><span class="sxs-lookup"><span data-stu-id="9d2cb-122">When you get an error, you must immediately get and populate the [**ErrorInfo**](errorinfo.md) collection for the collection that failed, without performing any other operations on that collection.</span></span> <span data-ttu-id="9d2cb-123">В противном случае коллекция **errorInfo** сбрасывается и не содержит подробностей об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9d2cb-123">Otherwise, the **ErrorInfo** collection is reset and does not detail that failure.</span></span>

<span data-ttu-id="9d2cb-124">Элементы в коллекции [**errorInfo**](errorinfo.md) предоставляют специальные свойства отчетов об ошибках Мажорреф и минорреф, которые подробноируют конкретную причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="9d2cb-124">The items in the [**ErrorInfo**](errorinfo.md) collection expose the special error-reporting properties MajorRef and MinorRef, which detail the particular cause of the error.</span></span> <span data-ttu-id="9d2cb-125">Дополнительные сведения см. в разделе **errorInfo**.</span><span class="sxs-lookup"><span data-stu-id="9d2cb-125">For more information, see **ErrorInfo**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d2cb-126">См. также</span><span class="sxs-lookup"><span data-stu-id="9d2cb-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d2cb-127">Операции администрирования COM+ в транзакциях</span><span class="sxs-lookup"><span data-stu-id="9d2cb-127">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="9d2cb-128">Вводный пример с использованием каталога администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="9d2cb-128">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="9d2cb-129">Общие сведения об объектах Комадмин</span><span class="sxs-lookup"><span data-stu-id="9d2cb-129">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="9d2cb-130">Получение коллекций в каталоге COM+</span><span class="sxs-lookup"><span data-stu-id="9d2cb-130">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="9d2cb-131">Установка свойств и сохранение изменений в каталоге COM+</span><span class="sxs-lookup"><span data-stu-id="9d2cb-131">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



