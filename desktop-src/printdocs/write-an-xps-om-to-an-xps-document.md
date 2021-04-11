---
description: Описание процедуры записи содержимого объектной модели XPS в программу в файл документа XPS.
ms.assetid: 8bee8059-b901-4a99-a7e4-60dad831c239
title: Запись объектной модели XPS в документ XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811f773394ee9dbbcf77dc75d1429322bb733631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265347"
---
# <a name="write-an-xps-om-to-an-xps-document"></a><span data-ttu-id="e7e77-103">Запись объектной модели XPS в документ XPS</span><span class="sxs-lookup"><span data-stu-id="e7e77-103">Write an XPS OM to an XPS Document</span></span>

<span data-ttu-id="e7e77-104">Описание процедуры записи содержимого объектной модели XPS в программу в файл документа XPS.</span><span class="sxs-lookup"><span data-stu-id="e7e77-104">Describes how to write the contents of an XPS OM in a program to an XPS document file.</span></span>

<span data-ttu-id="e7e77-105">Если программа содержит ОБЪЕКТную систему XPS, содержащую полный документ, программа может записать OM XPS в файл как документ XPS, вызвав метод [**вритетофиле**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) интерфейса [**икспсомпаккаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) .</span><span class="sxs-lookup"><span data-stu-id="e7e77-105">If a program has an XPS OM that contains a complete document, the program can write the XPS OM to a file as an XPS document, by calling the [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface.</span></span>

<span data-ttu-id="e7e77-106">Прежде чем использовать эти примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования документов XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="e7e77-106">Before using these code examples in a program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="writing-a-complete-xps-om-to-an-xps-document"></a><span data-ttu-id="e7e77-107">Запись полнофункциональной модели XPS в документ XPS</span><span class="sxs-lookup"><span data-stu-id="e7e77-107">Writing a complete XPS OM to an XPS document</span></span>

<span data-ttu-id="e7e77-108">После настройки содержимого объектной модели XPS можно сохранить объект XPS в файл как документ XPS, вызвав метод [**вритетофиле**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) интерфейса [**икспсомпаккаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) .</span><span class="sxs-lookup"><span data-stu-id="e7e77-108">After you set the contents of an XPS OM, you can save the XPS OM to a file as an XPS document, by calling the [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface.</span></span>


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        fileName,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE                    // Optimize Markup Size
        );

```



> [!Note]  
> <span data-ttu-id="e7e77-109">При записи объектной модели XPS в файл или поток не создается автоматически эскиз для документа XPS.</span><span class="sxs-lookup"><span data-stu-id="e7e77-109">Writing an XPS OM to a file or stream does not automatically create a thumbnail for the XPS document.</span></span> <span data-ttu-id="e7e77-110">Чтобы создать эскиз документа XPS, используйте интерфейс [**икспсомсумбнаилженератор**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) .</span><span class="sxs-lookup"><span data-stu-id="e7e77-110">To create a thumbnail of the XPS document, use the [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) interface.</span></span>

 

## <a name="incrementally-writing-an-xps-document"></a><span data-ttu-id="e7e77-111">Добавочная запись документа XPS</span><span class="sxs-lookup"><span data-stu-id="e7e77-111">Incrementally writing an XPS document</span></span>

<span data-ttu-id="e7e77-112">Интерфейс [**икспсомпаккажевритер**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) можно использовать для добавочной записи частей XPS-документа; Например, если элементы документа создаются или обрабатываются последовательно.</span><span class="sxs-lookup"><span data-stu-id="e7e77-112">The [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface can be used to write the parts of an XPS document incrementally; for example, when the document parts are created or processed in sequence.</span></span>

> [!Note]  
> <span data-ttu-id="e7e77-113">При записи объектной модели XPS в файл или поток не создается автоматически эскиз для документа XPS.</span><span class="sxs-lookup"><span data-stu-id="e7e77-113">Writing an XPS OM to a file or stream does not automatically create a thumbnail for the XPS document.</span></span> <span data-ttu-id="e7e77-114">Чтобы создать эскиз документа XPS, используйте интерфейс [**икспсомсумбнаилженератор**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) .</span><span class="sxs-lookup"><span data-stu-id="e7e77-114">To create a thumbnail of the XPS document, use the [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) interface.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e7e77-115">См. также</span><span class="sxs-lookup"><span data-stu-id="e7e77-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e7e77-116">**Следующие шаги**</span><span class="sxs-lookup"><span data-stu-id="e7e77-116">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="e7e77-117">Печать OM-объекта XPS</span><span class="sxs-lookup"><span data-stu-id="e7e77-117">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="e7e77-118">**Используется в этом разделе**</span><span class="sxs-lookup"><span data-stu-id="e7e77-118">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="e7e77-119">**иопкпартури**</span><span class="sxs-lookup"><span data-stu-id="e7e77-119">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="e7e77-120">**икспсомпаккаже**</span><span class="sxs-lookup"><span data-stu-id="e7e77-120">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="e7e77-121">**икспсомсумбнаилженератор**</span><span class="sxs-lookup"><span data-stu-id="e7e77-121">**IXpsOMThumbnailGenerator**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

<span data-ttu-id="e7e77-122">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="e7e77-122">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="e7e77-123">Инициализация объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="e7e77-123">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="e7e77-124">Справочник по API документов XPS</span><span class="sxs-lookup"><span data-stu-id="e7e77-124">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="e7e77-125">XPS</span><span class="sxs-lookup"><span data-stu-id="e7e77-125">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
