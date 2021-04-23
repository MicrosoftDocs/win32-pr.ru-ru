---
description: В этом разделе описывается реализация библиотеки DLL для фильтра DirectShow с использованием базовых классов DirectShow.
ms.assetid: d47980d1-6d0c-4b0d-a875-7b072562944a
title: Фабрики классов и шаблоны фабрики
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02699a8ff0740ddcf1d86b8514fd45dac9e32ed
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104557479"
---
# <a name="class-factories-and-factory-templates"></a><span data-ttu-id="8c70e-103">Фабрики классов и шаблоны фабрики</span><span class="sxs-lookup"><span data-stu-id="8c70e-103">Class Factories and Factory Templates</span></span>

<span data-ttu-id="8c70e-104">В этом разделе описывается реализация библиотеки DLL для фильтра DirectShow с использованием [базовых классов DirectShow](directshow-base-classes.md).</span><span class="sxs-lookup"><span data-stu-id="8c70e-104">This topic describes how to implement a DLL for a DirectShow filter, using the [DirectShow Base Classes](directshow-base-classes.md).</span></span>

<span data-ttu-id="8c70e-105">Прежде чем клиент создаст экземпляр COM-объекта, он создает экземпляр фабрики класса объекта, используя вызов функции [**кожетклассобжект**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) .</span><span class="sxs-lookup"><span data-stu-id="8c70e-105">Before a client creates an instance of a COM object, it creates an instance of the object's class factory, using a call to the [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) function.</span></span> <span data-ttu-id="8c70e-106">Затем клиент вызывает метод **IClassFactory:: CreateInstance** фабрики классов.</span><span class="sxs-lookup"><span data-stu-id="8c70e-106">The client then calls the class factory's **IClassFactory::CreateInstance** method.</span></span> <span data-ttu-id="8c70e-107">Это фабрика класса, которая фактически создает компонент и возвращает указатель на запрашиваемый интерфейс.</span><span class="sxs-lookup"><span data-stu-id="8c70e-107">It is the class factory that actually creates the component and returns a pointer to the requested interface.</span></span> <span data-ttu-id="8c70e-108">(Функция [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) объединяет эти шаги в вызове функции.)</span><span class="sxs-lookup"><span data-stu-id="8c70e-108">(The [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function combines these steps, inside the function call.)</span></span>

<span data-ttu-id="8c70e-109">На следующем рисунке показана последовательность вызовов методов.</span><span class="sxs-lookup"><span data-stu-id="8c70e-109">The following illustration shows the sequence of method calls.</span></span>

![вызовы методов для создания фабрики класса](images/classfactory.png)

<span data-ttu-id="8c70e-111">[**Кожетклассобжект**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) вызывает функцию [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) , которая определена в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="8c70e-111">[**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) calls the [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) function, which is defined in the DLL.</span></span> <span data-ttu-id="8c70e-112">Эта функция создает фабрику класса и возвращает указатель на интерфейс в фабрике класса.</span><span class="sxs-lookup"><span data-stu-id="8c70e-112">This function creates the class factory and returns a pointer to an interface on the class factory.</span></span> <span data-ttu-id="8c70e-113">DirectShow реализует **DllGetClassObject** , но функция зависит от кода особым образом.</span><span class="sxs-lookup"><span data-stu-id="8c70e-113">DirectShow implements **DllGetClassObject** for you, but the function relies on your code in a specific way.</span></span> <span data-ttu-id="8c70e-114">Чтобы понять, как это работает, необходимо понимать, как DirectShow реализует фабрики классов.</span><span class="sxs-lookup"><span data-stu-id="8c70e-114">To understand how it works, you must understand how DirectShow implements class factories.</span></span>

<span data-ttu-id="8c70e-115">Фабрика классов — это COM-объект, предназначенный для создания другого COM-объекта.</span><span class="sxs-lookup"><span data-stu-id="8c70e-115">A class factory is a COM object dedicated to creating another COM object.</span></span> <span data-ttu-id="8c70e-116">Каждая фабрика классов имеет один тип объекта, который он создает.</span><span class="sxs-lookup"><span data-stu-id="8c70e-116">Each class factory has one type of object that it creates.</span></span> <span data-ttu-id="8c70e-117">В DirectShow каждая фабрика классов является экземпляром одного и того же класса C++ **кклассфактори**.</span><span class="sxs-lookup"><span data-stu-id="8c70e-117">In DirectShow, every class factory is an instance of the same C++ class, **CClassFactory**.</span></span> <span data-ttu-id="8c70e-118">Фабрики классов являются специализированными с помощью другого класса, [**кфакторитемплате**](cfactorytemplate.md), также называемого *шаблоном фабрики*.</span><span class="sxs-lookup"><span data-stu-id="8c70e-118">Class factories are specialized by means of another class, [**CFactoryTemplate**](cfactorytemplate.md), also called the *factory template*.</span></span> <span data-ttu-id="8c70e-119">Каждая фабрика классов содержит указатель на шаблон фабрики.</span><span class="sxs-lookup"><span data-stu-id="8c70e-119">Each class factory holds a pointer to a factory template.</span></span> <span data-ttu-id="8c70e-120">Шаблон фабрики содержит сведения о конкретном компоненте, например идентификатор класса компонента (CLSID) и указатель на функцию, которая создает компонент.</span><span class="sxs-lookup"><span data-stu-id="8c70e-120">The factory template contains information about a specific component, such as the component's class identifier (CLSID), and a pointer to a function that creates the component.</span></span>

<span data-ttu-id="8c70e-121">Библиотека DLL объявляет глобальный массив шаблонов фабрики, по одному для каждого компонента в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="8c70e-121">The DLL declares a global array of factory templates, one for each component in the DLL.</span></span> <span data-ttu-id="8c70e-122">Когда [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) создает новую фабрику классов, она ищет в массиве шаблон с соответствующим идентификатором CLSID.</span><span class="sxs-lookup"><span data-stu-id="8c70e-122">When [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) makes a new class factory, it searches the array for a template with a matching CLSID.</span></span> <span data-ttu-id="8c70e-123">При условии, что он находит один, он создает фабрику класса, содержащую указатель на соответствующий шаблон.</span><span class="sxs-lookup"><span data-stu-id="8c70e-123">Assuming it finds one, it creates a class factory that holds a pointer to the matching template.</span></span> <span data-ttu-id="8c70e-124">Когда клиент вызывает метод **IClassFactory:: CreateInstance**, фабрика класса вызывает функцию создания экземпляра, определенную в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="8c70e-124">When the client calls **IClassFactory::CreateInstance**, the class factory calls the instantiation function defined in the template.</span></span>

<span data-ttu-id="8c70e-125">На следующем рисунке показана последовательность вызовов методов.</span><span class="sxs-lookup"><span data-stu-id="8c70e-125">The following illustration shows the sequence of method calls.</span></span>

![шаблоны фабрик классов в библиотеке DLL](images/classfactory2.png)

<span data-ttu-id="8c70e-127">Преимуществом этой архитектуры является то, что вы можете определить лишь несколько вещей, относящихся к конкретному компоненту, например функцию создания экземпляра, без реализации всей фабрики классов.</span><span class="sxs-lookup"><span data-stu-id="8c70e-127">The benefit of this architecture is that you can define just a few things that are specific to your component, such as the instantiation function, without implementing the entire class factory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c70e-128">См. также</span><span class="sxs-lookup"><span data-stu-id="8c70e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c70e-129">Создание библиотеки DLL фильтра DirectShow</span><span class="sxs-lookup"><span data-stu-id="8c70e-129">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 
