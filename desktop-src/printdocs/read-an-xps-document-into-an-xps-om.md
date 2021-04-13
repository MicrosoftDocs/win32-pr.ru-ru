---
description: Описание процедуры чтения существующего документа XPS из файла в объектную модель XPS.
ms.assetid: 92a8d19f-1c9e-4e02-a3d4-f2869ec871df
title: Чтение XPS-документа в объектную модель XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c3b703de24be58db875618b575cebf9c1c0b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348222"
---
# <a name="read-an-xps-document-into-an-xps-om"></a><span data-ttu-id="8363e-103">Чтение XPS-документа в объектную модель XPS</span><span class="sxs-lookup"><span data-stu-id="8363e-103">Read an XPS Document into an XPS OM</span></span>

<span data-ttu-id="8363e-104">Описание процедуры чтения существующего документа XPS из файла в объектную модель XPS.</span><span class="sxs-lookup"><span data-stu-id="8363e-104">Describes how to read an existing XPS document from a file into an XPS OM.</span></span>

<span data-ttu-id="8363e-105">Чтобы создать объект XPS из документа XPS, вызовите метод [**икспсомобжектфактори:: креатепаккажефромфиле**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) .</span><span class="sxs-lookup"><span data-stu-id="8363e-105">To create an XPS OM from an XPS document, call the [**IXpsOMObjectFactory::CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) method.</span></span>

<span data-ttu-id="8363e-106">Прежде чем использовать эти примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования документов XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="8363e-106">Before using these code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="8363e-107">Пример кода</span><span class="sxs-lookup"><span data-stu-id="8363e-107">Code Example</span></span>

<span data-ttu-id="8363e-108">В следующем примере кода предполагается, что инициализация, описанная в разделе [Инициализация OM-модели XPS](xps-object-model-initialization.md) , выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8363e-108">The following code example assumes that the initialization described in [Initialize an XPS OM](xps-object-model-initialization.md) has succeeded.</span></span>


```C++
    IXpsOMPackage *package = NULL;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &package);

    // package now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.

    // When finished with the package, release the object.
    if (NULL != package) package->Release();
```



<span data-ttu-id="8363e-109">Чтобы создать объект XPS из документа XPS, хранящегося в виде потока, вызовите [**икспсомобжектфактори:: креатепаккажефромстреам**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream).</span><span class="sxs-lookup"><span data-stu-id="8363e-109">To create an XPS OM from an XPS document that is stored as a stream, call [**IXpsOMObjectFactory::CreatePackageFromStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream).</span></span>

## <a name="remarks"></a><span data-ttu-id="8363e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8363e-110">Remarks</span></span>

<span data-ttu-id="8363e-111">Если вы написали модуль XPS сразу же после считывания пакета XPS в него, часть исходного содержимого может быть утеряна или изменена.</span><span class="sxs-lookup"><span data-stu-id="8363e-111">If you write an XPS OM immediately after you have read an XPS package into it, some of the original content might be lost or changed.</span></span>

<span data-ttu-id="8363e-112">Некоторые изменения, которые могут возникнуть в этом случае, перечислены в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="8363e-112">Some of the changes that can occur in such case are listed in the table that follows:</span></span>

| <span data-ttu-id="8363e-113">Функция документа</span><span class="sxs-lookup"><span data-stu-id="8363e-113">Document feature</span></span>                      | <span data-ttu-id="8363e-114">Действие</span><span class="sxs-lookup"><span data-stu-id="8363e-114">Action</span></span>                                                             |
|---------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="8363e-115">Цифровые подписи</span><span class="sxs-lookup"><span data-stu-id="8363e-115">Digital signatures</span></span><br/>         | <span data-ttu-id="8363e-116">Удалено из документа</span><span class="sxs-lookup"><span data-stu-id="8363e-116">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="8363e-117">Часть Дискардконтрол</span><span class="sxs-lookup"><span data-stu-id="8363e-117">DiscardControl part</span></span><br/>        | <span data-ttu-id="8363e-118">Удалено из документа</span><span class="sxs-lookup"><span data-stu-id="8363e-118">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="8363e-119">Части внешнего документа</span><span class="sxs-lookup"><span data-stu-id="8363e-119">Foreign document parts</span></span><br/>     | <span data-ttu-id="8363e-120">Удалено из документа</span><span class="sxs-lookup"><span data-stu-id="8363e-120">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="8363e-121">Разметка FixedPage</span><span class="sxs-lookup"><span data-stu-id="8363e-121">FixedPage markup</span></span><br/>           | <span data-ttu-id="8363e-122">Изменено с исходного</span><span class="sxs-lookup"><span data-stu-id="8363e-122">Modified from the original</span></span><br/>                              |
| <span data-ttu-id="8363e-123">Разметка словаря ресурсов</span><span class="sxs-lookup"><span data-stu-id="8363e-123">Resource dictionary markup</span></span><br/> | <span data-ttu-id="8363e-124">Изменено с исходного, если установлен флаг оптимизации</span><span class="sxs-lookup"><span data-stu-id="8363e-124">Modified from the original, if Optimization flag is set</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="8363e-125">См. также</span><span class="sxs-lookup"><span data-stu-id="8363e-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8363e-126">**Следующие шаги**</span><span class="sxs-lookup"><span data-stu-id="8363e-126">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="8363e-127">Навигация по OM XPS</span><span class="sxs-lookup"><span data-stu-id="8363e-127">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="8363e-128">Запись текста в объектную модель XPS</span><span class="sxs-lookup"><span data-stu-id="8363e-128">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="8363e-129">Рисование графики в OM-объекте XPS</span><span class="sxs-lookup"><span data-stu-id="8363e-129">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="8363e-130">Размещение изображений в объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="8363e-130">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="8363e-131">**Используется в этом разделе**</span><span class="sxs-lookup"><span data-stu-id="8363e-131">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="8363e-132">**икспсомобжектфактори**</span><span class="sxs-lookup"><span data-stu-id="8363e-132">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="8363e-133">**икспсомпаккаже**</span><span class="sxs-lookup"><span data-stu-id="8363e-133">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

<span data-ttu-id="8363e-134">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="8363e-134">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="8363e-135">Инициализация объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="8363e-135">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="8363e-136">API для упаковки</span><span class="sxs-lookup"><span data-stu-id="8363e-136">Packaging API</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="8363e-137">Справочник по API документов XPS</span><span class="sxs-lookup"><span data-stu-id="8363e-137">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="8363e-138">XPS</span><span class="sxs-lookup"><span data-stu-id="8363e-138">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

