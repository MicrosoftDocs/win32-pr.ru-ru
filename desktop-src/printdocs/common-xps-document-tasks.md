---
description: На этой странице перечислены некоторые задачи программирования, которые обычно выполняются с помощью API документа XPS.
ms.assetid: ced2098f-5462-40d7-a728-4e53f7f41003
title: Распространенные задачи программирования документов XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c40ee0c901b9d906d4d59c69bab4cfc22d8208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673691"
---
# <a name="common-xps-document-programming-tasks"></a><span data-ttu-id="1fc88-103">Распространенные задачи программирования документов XPS</span><span class="sxs-lookup"><span data-stu-id="1fc88-103">Common XPS Document Programming Tasks</span></span>

<span data-ttu-id="1fc88-104">На этой странице перечислены некоторые задачи программирования, которые обычно выполняются с помощью API документа XPS.</span><span class="sxs-lookup"><span data-stu-id="1fc88-104">This page lists some of the programming tasks that are commonly performed with the XPS Document API.</span></span>

## <a name="common-xps-document-tasks"></a><span data-ttu-id="1fc88-105">Распространенные задачи документа XPS</span><span class="sxs-lookup"><span data-stu-id="1fc88-105">Common XPS Document Tasks</span></span>

<span data-ttu-id="1fc88-106">В следующих примерах кода показаны некоторые задачи программирования, которые обычно выполняются при использовании API документов XPS для работы с OM XPS.</span><span class="sxs-lookup"><span data-stu-id="1fc88-106">The following code examples illustrate some of the programming tasks that are commonly performed when the XPS Document API is used for working with an XPS OM.</span></span>

<dl>

[<span data-ttu-id="1fc88-107">Инициализация объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="1fc88-107">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)  
[<span data-ttu-id="1fc88-108">Создание пустой объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="1fc88-108">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)  
[<span data-ttu-id="1fc88-109">Чтение XPS-документа в объектную модель XPS</span><span class="sxs-lookup"><span data-stu-id="1fc88-109">Read an XPS Document into an XPS OM</span></span>](read-an-xps-document-into-an-xps-om.md)  
[<span data-ttu-id="1fc88-110">Навигация по OM XPS</span><span class="sxs-lookup"><span data-stu-id="1fc88-110">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)  
[<span data-ttu-id="1fc88-111">Запись текста в объектную модель XPS</span><span class="sxs-lookup"><span data-stu-id="1fc88-111">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)  
[<span data-ttu-id="1fc88-112">Рисование графики в OM-объекте XPS</span><span class="sxs-lookup"><span data-stu-id="1fc88-112">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)  
[<span data-ttu-id="1fc88-113">Размещение изображений в объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="1fc88-113">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)  
[<span data-ttu-id="1fc88-114">Запись объектной модели XPS в документ XPS</span><span class="sxs-lookup"><span data-stu-id="1fc88-114">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)  
[<span data-ttu-id="1fc88-115">Печать OM-объекта XPS</span><span class="sxs-lookup"><span data-stu-id="1fc88-115">Print an XPS OM</span></span>](print-an-xps-om.md)  
[<span data-ttu-id="1fc88-116">Работа с интерфейсами коллекции OM в XPS</span><span class="sxs-lookup"><span data-stu-id="1fc88-116">Working with XPS OM Collection Interfaces</span></span>](working-with-xps-object-model-collection-interfaces.md)  
</dl>

## <a name="disclaimer"></a><span data-ttu-id="1fc88-117">Отказ от ответственности</span><span class="sxs-lookup"><span data-stu-id="1fc88-117">Disclaimer</span></span>

<span data-ttu-id="1fc88-118">Примеры кода не предназначены для завершения и работы программ.</span><span class="sxs-lookup"><span data-stu-id="1fc88-118">Code examples are not intended to be complete and working programs.</span></span> <span data-ttu-id="1fc88-119">Примеры кода, упоминаемые на этой странице, например, не выполняют проверку параметров, проверку ошибок или обработку ошибок.</span><span class="sxs-lookup"><span data-stu-id="1fc88-119">The code examples that are referenced on this page, for example, do not perform parameter checking, error checking, or error handling.</span></span> <span data-ttu-id="1fc88-120">Используйте эти примеры в качестве отправной точки, а затем добавьте код, необходимый для создания надежного приложения.</span><span class="sxs-lookup"><span data-stu-id="1fc88-120">Use these examples as a starting point, and then add the code necessary to create a robust application.</span></span> <span data-ttu-id="1fc88-121">Дополнительные сведения о возвращаемых значениях **HRESULT** и стратегиях обработки ошибок см. [в разделе Обработка ошибок в com](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="1fc88-121">For more information about **HRESULT** return values and error handling strategies, see [Error Handling in COM](../com/error-handling-in-com.md).</span></span>

<span data-ttu-id="1fc88-122">Прежде чем можно будет использовать интерфейсы Operations Manager XPS, необходимо инициализировать COM в потоке, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="1fc88-122">Before XPS OM interfaces can be used, COM must be initialized in the thread, as shown in the following example code.</span></span>


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



<span data-ttu-id="1fc88-123">Для ясности в этих примерах кода используется очень простая модель XPS, которая может быть недостаточно сложной для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="1fc88-123">For clarity, these code examples use a very simple XPS OM, one that might not be complex enough for your application.</span></span> <span data-ttu-id="1fc88-124">В качестве примера в примерах кода, которые добавляют содержимое на страницу, визуальные элементы страницы добавляются непосредственно в список визуальных объектов страницы. Однако на практике может потребоваться сгруппировать визуальные объекты в объекты Canvas, чтобы несколько объектов могли обрабатываться как группа.</span><span class="sxs-lookup"><span data-stu-id="1fc88-124">As a case in point, in the code examples that add content to a page, the visual elements of a page are added directly to the page's list of visual objects; in practice, however, you might want to group visual objects into canvas objects, so that multiple objects could be acted upon as a group.</span></span> <span data-ttu-id="1fc88-125">Таким образом, чтобы обеспечить поддержку одного и того же содержимого для нескольких размеров страницы, можно сгруппировать визуальное содержимое страницы в один объект Canvas, а затем применить преобразование к холсту, чтобы масштабировать его до текущего размера страницы.</span><span class="sxs-lookup"><span data-stu-id="1fc88-125">Thus, to enable support of the same content for more than one page size, you could group the visual content of a page into a single canvas object, and then apply a transform to the canvas to scale it to the current page size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fc88-126">См. также</span><span class="sxs-lookup"><span data-stu-id="1fc88-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fc88-127">Обработка ошибок в COM</span><span class="sxs-lookup"><span data-stu-id="1fc88-127">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> <dt>

[<span data-ttu-id="1fc88-128">XPS</span><span class="sxs-lookup"><span data-stu-id="1fc88-128">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
