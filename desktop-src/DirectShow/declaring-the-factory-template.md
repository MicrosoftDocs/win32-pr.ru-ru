---
description: Объявление шаблона фабрики
ms.assetid: 3060c167-ea23-4061-b32a-16e750f55e6f
title: Объявление шаблона фабрики
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3168f16b6281417846f13b7a17141282053c4705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139447"
---
# <a name="declaring-the-factory-template"></a><span data-ttu-id="70d23-103">Объявление шаблона фабрики</span><span class="sxs-lookup"><span data-stu-id="70d23-103">Declaring the Factory Template</span></span>

<span data-ttu-id="70d23-104">Следующим шагом является объявление шаблона фабрики для фильтра.</span><span class="sxs-lookup"><span data-stu-id="70d23-104">The next step is to declare the factory template for your filter.</span></span> <span data-ttu-id="70d23-105">Шаблон фабрики — это класс C++, который содержит сведения для фабрики класса.</span><span class="sxs-lookup"><span data-stu-id="70d23-105">A factory template is a C++ class that contains information for the class factory.</span></span> <span data-ttu-id="70d23-106">В библиотеке DLL объявите глобальный массив объектов [**кфакторитемплате**](cfactorytemplate.md) , по одному для каждого фильтра или COM-компонента в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="70d23-106">In your DLL, declare a global array of [**CFactoryTemplate**](cfactorytemplate.md) objects, one for each filter or COM component in your DLL.</span></span> <span data-ttu-id="70d23-107">Массив должен называться *g \_ Templates*.</span><span class="sxs-lookup"><span data-stu-id="70d23-107">The array must be named *g\_Templates*.</span></span> <span data-ttu-id="70d23-108">Дополнительные сведения о шаблонах фабрики см. [в разделе Создание библиотеки DLL фильтра DirectShow](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="70d23-108">For more information about factory templates, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

<span data-ttu-id="70d23-109">Элемент **\_ \_ фильтра m памовиесетуп** шаблона фабрики — это указатель на структуру [**\_ фильтра амовиесетуп**](amoviesetup-filter.md) , описанную ранее.</span><span class="sxs-lookup"><span data-stu-id="70d23-109">The **m\_pAMovieSetup\_Filter** member of the factory template is a pointer to the [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure described previously.</span></span> <span data-ttu-id="70d23-110">В следующем примере показан шаблон фабрики с использованием структуры, заданной в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="70d23-110">The following example shows a factory template, using the structure given in the previous example:</span></span>


```C++
CFactoryTemplate g_Templates[] = {
    {
        g_wszName,                      // Name.
        &CLSID_SomeFilter,              // CLSID.
        CSomeFilter::CreateInstance,    // Creation function.
        NULL,
        &sudFilterReg                   // Pointer to filter information.
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);
```



<span data-ttu-id="70d23-111">Если вы не объявили какие бы то ни было сведения о фильтре, **m \_ памовесетуп \_ Filter** может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="70d23-111">If you did not declare any filter information, **m\_pAMoveSetup\_Filter** can be **NULL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70d23-112">См. также</span><span class="sxs-lookup"><span data-stu-id="70d23-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70d23-113">Как зарегистрировать фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="70d23-113">How to Register DirectShow Filters</span></span>](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



