---
description: Описывает, как инициализировать объектную модель XPS, которая позволяет программе создавать документы XPS.
ms.assetid: 920d940f-5ae2-4376-8c7b-0cef04f21df7
title: Инициализация объектной модели XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac44a69d171c1d38633512b0e275dcdeaea8738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344832"
---
# <a name="initialize-an-xps-om"></a><span data-ttu-id="9d16b-103">Инициализация объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="9d16b-103">Initialize an XPS OM</span></span>

<span data-ttu-id="9d16b-104">Описывает, как инициализировать объектную модель XPS, которая позволяет программе создавать документы XPS.</span><span class="sxs-lookup"><span data-stu-id="9d16b-104">Describes how to initialize an XPS OM, which allows a program to create an XPS document.</span></span>

<span data-ttu-id="9d16b-105">Интерфейсы API документа XPS создаются интерфейсом [**икспсомобжектфактори**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) .</span><span class="sxs-lookup"><span data-stu-id="9d16b-105">The interfaces of the XPS Document API are created by an [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) interface.</span></span> <span data-ttu-id="9d16b-106">Чтобы получить указатель на **икспсомобжектфактори** , который можно использовать в программе, вызовите [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="9d16b-106">To obtain a pointer to an **IXpsOMObjectFactory** that can be used in your program, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="9d16b-107">Прежде чем использовать приведенные ниже примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования документов XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="9d16b-107">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="9d16b-108">Пример кода</span><span class="sxs-lookup"><span data-stu-id="9d16b-108">Code Example</span></span>

<span data-ttu-id="9d16b-109">В следующем примере создается фабрика объектов, которая будет использоваться для создания интерфейсов OM-модели XPS в других примерах.</span><span class="sxs-lookup"><span data-stu-id="9d16b-109">The following example creates the object factory that will be used to create XPS OM interfaces in other examples.</span></span>


```C++
    IXpsOMObjectFactory *xpsFactory;

    HRESULT hr = S_OK;

    // Init COM for this thread if it hasn't 
    //  been initialized, yet.
    hr = CoInitializeEx(0, COINIT_MULTITHREADED);

    hr = CoCreateInstance(
        __uuidof(XpsOMObjectFactory),
        NULL, 
        CLSCTX_INPROC_SERVER,
        __uuidof(IXpsOMObjectFactory),
        reinterpret_cast<LPVOID*>(&xpsFactory));

    if (SUCCEEDED(hr))
    {
        // Make sure that you got a pointer 
        //  to the interface.

        // Use object factory...

        // ... and release when done
        xpsFactory->Release();
    }

    // Uninitialize COM when finished
    CoUninitialize();
```



## <a name="best-practices"></a><span data-ttu-id="9d16b-110">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="9d16b-110">Best Practices</span></span>

<span data-ttu-id="9d16b-111">Чтобы сделать программу более эффективной, можно получить указатель на интерфейс [**икспсомобжектфактори**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) в первый раз, когда необходимо вызвать **икспсомобжектфактори** для создания интерфейса, а затем сохранить указатель для использования в других областях программы.</span><span class="sxs-lookup"><span data-stu-id="9d16b-111">You can make your program more efficient by obtaining a pointer to an [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) interface the first time that you need to call **IXpsOMObjectFactory** to create an interface, and then saving the pointer for use in other areas of the program.</span></span> <span data-ttu-id="9d16b-112">Если программе больше не требуется фабрика объектов или она не понадобится в течение определенного времени, указатель может быть освобожден.</span><span class="sxs-lookup"><span data-stu-id="9d16b-112">When the program no longer needs the object factory, or will not need it for a while, the pointer can be released.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d16b-113">См. также</span><span class="sxs-lookup"><span data-stu-id="9d16b-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9d16b-114">**Следующие шаги**</span><span class="sxs-lookup"><span data-stu-id="9d16b-114">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="9d16b-115">Создание пустой объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="9d16b-115">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)
</dt> <dt>

<span data-ttu-id="9d16b-116">**Используется в этом разделе**</span><span class="sxs-lookup"><span data-stu-id="9d16b-116">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="9d16b-117">**икспсомобжектфактори**</span><span class="sxs-lookup"><span data-stu-id="9d16b-117">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="9d16b-118">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="9d16b-118">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

<span data-ttu-id="9d16b-119">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="9d16b-119">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="9d16b-120">Упаковка</span><span class="sxs-lookup"><span data-stu-id="9d16b-120">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="9d16b-121">Справочник по API документов XPS</span><span class="sxs-lookup"><span data-stu-id="9d16b-121">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="9d16b-122">XPS</span><span class="sxs-lookup"><span data-stu-id="9d16b-122">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
