---
description: API документа XPS реализует объектную модель XPS и позволяет разработчикам создавать объекты-функции XPS, управлять содержимым документов XPS в собственных \\ \\ программах Windows и сохранять OM XPS в файл или поток в виде документа XPS.
ms.assetid: dbb48dae-1ee6-4a8b-9184-8b796755087e
title: Об API документов XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e24a93061b7f09697a987aa83be121dac42703c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693422"
---
# <a name="about-xps-document-api"></a><span data-ttu-id="4e702-103">Об API документов XPS</span><span class="sxs-lookup"><span data-stu-id="4e702-103">About XPS Document API</span></span>

<span data-ttu-id="4e702-104">[API документа XPS](documents-xps.md) реализует объектную модель XPS и позволяет разработчикам создавать объекты-функции XPS, управлять содержимым документов XPS в собственных \\ \\ программах Windows и сохранять OM XPS в файл или поток в виде документа XPS.</span><span class="sxs-lookup"><span data-stu-id="4e702-104">The [XPS Document API](documents-xps.md) implements the XPS object model and enables developers to create an XPS OM, manipulate XPS document content in native Windows \\\\ programs, and save the XPS OM to a file or stream as an XPS document.</span></span> <span data-ttu-id="4e702-105">Разработчики модулей конвейера фильтра XPSDrv также могут использовать API документов XPS для управления содержимым документов XPS в фильтре драйвера принтера XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="4e702-105">Developers of XPSDrv filter pipeline modules can also use the XPS Document API to manipulate XPS document content in an XPSDrv printer driver filter.</span></span>

## <a name="xps-document-api-overview"></a><span data-ttu-id="4e702-106">Общие сведения об API документов XPS</span><span class="sxs-lookup"><span data-stu-id="4e702-106">XPS Document API Overview</span></span>

<span data-ttu-id="4e702-107">Объектная модель XPS — это информационная модель документа XPS.</span><span class="sxs-lookup"><span data-stu-id="4e702-107">The XPS object model is the information model of an XPS document.</span></span> <span data-ttu-id="4e702-108">Информационная модель документа XPS отличается от модели разметки, используемой внутри частей документа.</span><span class="sxs-lookup"><span data-stu-id="4e702-108">The information model of the XPS document is separate from the markup model that is used inside the document parts.</span></span> <span data-ttu-id="4e702-109">Объектная модель XPS описывает организацию внутренних компонентов, образующих документ XPS, а модель разметки описывает содержимое этих компонентов.</span><span class="sxs-lookup"><span data-stu-id="4e702-109">The XPS object model describes the organization of the internal components that make up an XPS document, and the markup model describes the contents of those components.</span></span>

<span data-ttu-id="4e702-110">В программе экземпляр модели объектов XPS создается как объектная модель XPS.</span><span class="sxs-lookup"><span data-stu-id="4e702-110">In a program, the XPS object model is instantiated as an XPS OM.</span></span> <span data-ttu-id="4e702-111">МОДЕЛЬ XPS, по сути, представляет собой версию содержимого XPS-документа в памяти.</span><span class="sxs-lookup"><span data-stu-id="4e702-111">The XPS OM is essentially an in-memory version of an XPS document's contents.</span></span> <span data-ttu-id="4e702-112">Несмотря на то, что в логической организации используется документ XPS, объектная модель XPS не считается документом XPS, пока он не будет сериализован в файл или поток.</span><span class="sxs-lookup"><span data-stu-id="4e702-112">While similar in logical organization to an XPS document, an XPS OM is not considered an XPS document until it has been serialized to a file or a stream.</span></span>

<span data-ttu-id="4e702-113">Точная структура разметки недоступна для модели XPS, когда документ XPS десериализуется из разметки в OM-объект XPS.</span><span class="sxs-lookup"><span data-stu-id="4e702-113">The exact structure of the markup is not available to the XPS OM when an XPS document is deserialized from markup to an XPS OM.</span></span> <span data-ttu-id="4e702-114">Например, если свойство было представлено как элемент или атрибут в разметке, значение свойства объекта документа будет представлено OM DOM точно таким же образом.</span><span class="sxs-lookup"><span data-stu-id="4e702-114">For example, whether the property was represented as an element or an attribute in the markup, the property value of a document object is presented by the XPS OM in exactly the same way.</span></span>

<span data-ttu-id="4e702-115">[API документов XPS](documents-xps.md) можно разделить на следующие категории:</span><span class="sxs-lookup"><span data-stu-id="4e702-115">The [XPS Document API](documents-xps.md) can be divided into the following categories:</span></span>

-   [<span data-ttu-id="4e702-116">Интерфейсы магистральной модели XPS</span><span class="sxs-lookup"><span data-stu-id="4e702-116">XPS OM Trunk Interfaces</span></span>](xps-om-trunk-interfaces.md)

    <span data-ttu-id="4e702-117">Магистральные интерфейсы обеспечивают доступ к компонентам верхнего уровня структуры документа XPS.</span><span class="sxs-lookup"><span data-stu-id="4e702-117">The trunk interfaces provide access to the top-level components of the XPS document structure.</span></span> <span data-ttu-id="4e702-118">Эти интерфейсы также предоставляют средства для сериализации OM-объекта XPS и десериализации документа XPS.</span><span class="sxs-lookup"><span data-stu-id="4e702-118">These interfaces also provide the means to serialize an XPS OM and deserialize an XPS document.</span></span>

-   [<span data-ttu-id="4e702-119">Интерфейсы страницы OM XPS</span><span class="sxs-lookup"><span data-stu-id="4e702-119">XPS OM Page Interfaces</span></span>](xps-object-model-page-interfaces.md)

    <span data-ttu-id="4e702-120">Интерфейсы страницы обеспечивают доступ к содержимому страницы в документе XPS.</span><span class="sxs-lookup"><span data-stu-id="4e702-120">The page interfaces provide access to the contents of a page in an XPS document.</span></span> <span data-ttu-id="4e702-121">Интерфейсы, описывающие содержимое страницы, также включаются в интерфейсы страницы.</span><span class="sxs-lookup"><span data-stu-id="4e702-121">The interfaces that describe the content of the page are also included with the page interfaces.</span></span>

-   [<span data-ttu-id="4e702-122">Цифровые подписи модели XPS</span><span class="sxs-lookup"><span data-stu-id="4e702-122">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)

    <span data-ttu-id="4e702-123">МОДЕЛЬ XPS поддерживает цифровые подписи.</span><span class="sxs-lookup"><span data-stu-id="4e702-123">The XPS OM supports digital signatures.</span></span> <span data-ttu-id="4e702-124">Однако вы можете получить доступ к цифровым подписям в документе XPS напрямую, не создавая модель XPS.</span><span class="sxs-lookup"><span data-stu-id="4e702-124">However, you can access digital signatures in an XPS document directly without creating an XPS OM.</span></span> <span data-ttu-id="4e702-125">Дополнительные сведения о доступе к цифровым подписям XPS без модели XPS см. в статье [API цифровой подписи XPS](xps-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="4e702-125">For more information about how to access XPS digital signatures without an XPS OM, see [XPS Digital Signature API](xps-digital-signatures.md).</span></span>

-   [<span data-ttu-id="4e702-126">Интерфейсы билета на печать Operations Manager XPS</span><span class="sxs-lookup"><span data-stu-id="4e702-126">XPS OM Print Ticket Interfaces</span></span>](xps-object-model-print-ticket-interfaces.md)

    <span data-ttu-id="4e702-127">Документы XPS поддерживают печать билетов на уровне пакета (задания), документа и страницы.</span><span class="sxs-lookup"><span data-stu-id="4e702-127">XPS documents support print tickets at the package (job), document, and page level.</span></span> <span data-ttu-id="4e702-128">В билетах печати содержатся сведения о форматировании содержимого документов для печати или просмотра.</span><span class="sxs-lookup"><span data-stu-id="4e702-128">Print tickets contain information about how to format document content for printing or viewing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e702-129">См. также</span><span class="sxs-lookup"><span data-stu-id="4e702-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4e702-130">**В этом разделе**</span><span class="sxs-lookup"><span data-stu-id="4e702-130">**In This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="4e702-131">Интерфейсы магистральной модели XPS</span><span class="sxs-lookup"><span data-stu-id="4e702-131">XPS OM Trunk Interfaces</span></span>](xps-om-trunk-interfaces.md)
</dt> <dt>

[<span data-ttu-id="4e702-132">Интерфейсы страницы OM XPS</span><span class="sxs-lookup"><span data-stu-id="4e702-132">XPS OM Page Interfaces</span></span>](xps-object-model-page-interfaces.md)
</dt> <dt>

[<span data-ttu-id="4e702-133">Цифровые подписи модели XPS</span><span class="sxs-lookup"><span data-stu-id="4e702-133">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)
</dt> <dt>

[<span data-ttu-id="4e702-134">Интерфейсы билета на печать Operations Manager XPS</span><span class="sxs-lookup"><span data-stu-id="4e702-134">XPS OM Print Ticket Interfaces</span></span>](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

<span data-ttu-id="4e702-135">**Другие связанные разделы**</span><span class="sxs-lookup"><span data-stu-id="4e702-135">**Other Related Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="4e702-136">Инициализация объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="4e702-136">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="4e702-137">Цифровые подписи модели XPS</span><span class="sxs-lookup"><span data-stu-id="4e702-137">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)
</dt> <dt>

[<span data-ttu-id="4e702-138">Справочник по API документов XPS</span><span class="sxs-lookup"><span data-stu-id="4e702-138">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="4e702-139">XPS</span><span class="sxs-lookup"><span data-stu-id="4e702-139">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



