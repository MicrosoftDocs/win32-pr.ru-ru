---
description: Массив шаблонов фабрики
ms.assetid: 310afccd-42a6-426e-b455-7bf98062bf36
title: Массив шаблонов фабрики
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645f2c8d05f37ab64142747755d6a0e7727f4b11
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140718"
---
# <a name="factory-template-array"></a><span data-ttu-id="dcc15-103">Массив шаблонов фабрики</span><span class="sxs-lookup"><span data-stu-id="dcc15-103">Factory Template Array</span></span>

<span data-ttu-id="dcc15-104">Шаблон фабрики содержит следующие открытые переменные члена:</span><span class="sxs-lookup"><span data-stu-id="dcc15-104">The factory template contains the following public member variables:</span></span>

``` syntax
const WCHAR *              m_Name;                // Name
const CLSID *              m_ClsID;               // CLSID
LPFNNewCOMObject           m_lpfnNew;             // Function to create an instance
                                                  //   of the component
LPFNInitRoutine            m_lpfnInit;            // Initialization function (optional)
const AMOVIESETUP_FILTER * m_pAMovieSetup_Filter; // Set-up information (for filters)
```

<span data-ttu-id="dcc15-105">Два указателя функций, [**m \_ лпфннев**](cfactorytemplate-m-lpfnnew.md) и [**m \_ лпфнинит**](cfactorytemplate-m-lpfninit.md), используют следующие определения типов:</span><span class="sxs-lookup"><span data-stu-id="dcc15-105">The two function pointers, [**m\_lpfnNew**](cfactorytemplate-m-lpfnnew.md) and [**m\_lpfnInit**](cfactorytemplate-m-lpfninit.md), use the following type definitions:</span></span>

``` syntax
typedef CUnknown *(CALLBACK *LPFNNewCOMObject)(LPUNKNOWN pUnkOuter, HRESULT *phr);
typedef void (CALLBACK *LPFNInitRoutine)(BOOL bLoading, const CLSID *rclsid);
```

<span data-ttu-id="dcc15-106">Первый — это функция создания экземпляра для компонента.</span><span class="sxs-lookup"><span data-stu-id="dcc15-106">The first is the instantiation function for the component.</span></span> <span data-ttu-id="dcc15-107">Второй — Необязательная функция инициализации.</span><span class="sxs-lookup"><span data-stu-id="dcc15-107">The second is an optional initialization function.</span></span> <span data-ttu-id="dcc15-108">Если вы предоставляете функцию инициализации, она вызывается из функции точки входа DLL.</span><span class="sxs-lookup"><span data-stu-id="dcc15-108">If you provide an initialization function, it is called from inside the DLL entry-point function.</span></span> <span data-ttu-id="dcc15-109">(Функция точки входа DLL обсуждается далее в этой статье.)</span><span class="sxs-lookup"><span data-stu-id="dcc15-109">(The DLL entry-point function is discussed later in this article.)</span></span>

<span data-ttu-id="dcc15-110">Предположим, вы создаете библиотеку DLL, содержащую компонент с именем Кмикомпонент, который наследует от [**кункновн**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="dcc15-110">Suppose you are creating a DLL that contains a component named CMyComponent, which inherits from [**CUnknown**](cunknown.md).</span></span> <span data-ttu-id="dcc15-111">В библиотеке DLL необходимо указать следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="dcc15-111">You must provide the following items in your DLL:</span></span>

-   <span data-ttu-id="dcc15-112">Функция инициализации — открытый метод, возвращающий новый экземпляр Кмикомпонент.</span><span class="sxs-lookup"><span data-stu-id="dcc15-112">The initialization function, a public method that returns a new instance of CMyComponent.</span></span>
-   <span data-ttu-id="dcc15-113">Глобальный массив шаблонов фабрики, именуемый *g \_ Templates.*</span><span class="sxs-lookup"><span data-stu-id="dcc15-113">A global array of factory templates, named *g\_Templates.*</span></span> <span data-ttu-id="dcc15-114">Этот массив содержит шаблон фабрики для Кмикомпонент.</span><span class="sxs-lookup"><span data-stu-id="dcc15-114">This array contains the factory template for CMyComponent.</span></span>
-   <span data-ttu-id="dcc15-115">Глобальная переменная с именем *g \_ ктемплатес* , указывающая размер массива.</span><span class="sxs-lookup"><span data-stu-id="dcc15-115">A global variable named *g\_cTemplates* that specifies the size of the array.</span></span>

<span data-ttu-id="dcc15-116">В следующем примере показано, как объявить эти элементы:</span><span class="sxs-lookup"><span data-stu-id="dcc15-116">The following example shows how to declare these items:</span></span>


```C++
// Public method that returns a new instance. 
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = new CMyComponent(NAME("My Component"), pUnk, pHr );
    if (pNewObject == NULL) {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 

CFactoryTemplate g_Templates[1] = 
{
    { 
      L"My Component",                // Name
      &CLSID_MyComponent,             // CLSID
      CMyComponent::CreateInstance,   // Method to create an instance of MyComponent
      NULL,                           // Initialization function
      NULL                            // Set-up information (for filters)
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);    
```



<span data-ttu-id="dcc15-117">`CreateInstance`Метод вызывает конструктор класса и возвращает указатель на новый экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="dcc15-117">The `CreateInstance` method calls the class constructor and returns a pointer to the new class instance.</span></span> <span data-ttu-id="dcc15-118">Параметр *Punk* является указателем на агрегатор [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="dcc15-118">The parameter *pUnk* is a pointer to the aggregating [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="dcc15-119">Этот параметр можно просто передать конструктору класса.</span><span class="sxs-lookup"><span data-stu-id="dcc15-119">You can simply pass this parameter to the class constructor.</span></span> <span data-ttu-id="dcc15-120">Параметр *фр* является указателем на значение HRESULT.</span><span class="sxs-lookup"><span data-stu-id="dcc15-120">The parameter *pHr* is a pointer to an HRESULT value.</span></span> <span data-ttu-id="dcc15-121">Конструктор класса присваивает этому свойству соответствующее значение, но если конструктор завершается неудачно, задайте для него значение E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="dcc15-121">The class constructor sets this to an appropriate value, but if the constructor fails, set the value to E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="dcc15-122">Макрос [**Name**](name.md) создает строку в отладочных сборках, но разрешается в **значение NULL** в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="dcc15-122">The [**NAME**](name.md) macro generates a string in debug builds but resolves to **NULL** in retail builds.</span></span> <span data-ttu-id="dcc15-123">Он используется в этом примере для присвоения компоненту имени, которое отображается в журналах отладки, но не занимается памятью в окончательной версии.</span><span class="sxs-lookup"><span data-stu-id="dcc15-123">It is used in this example to give the component a name that appears in debug logs but does not occupy memory in the final version.</span></span>

<span data-ttu-id="dcc15-124">`CreateInstance`Метод может иметь любое имя, так как фабрика классов ссылается на указатель на функцию в шаблоне фабрики.</span><span class="sxs-lookup"><span data-stu-id="dcc15-124">The `CreateInstance` method can have any name, because the class factory refers to the function pointer in the factory template.</span></span> <span data-ttu-id="dcc15-125">Однако *\_ шаблоны g* и *g \_ ктемплатес* являются глобальными переменными, которые фабрика класса планирует найти, поэтому они должны иметь в точности эти имена.</span><span class="sxs-lookup"><span data-stu-id="dcc15-125">However, *g\_Templates* and *g\_cTemplates* are global variables that the class factory expects to find, so they must have exactly those names.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dcc15-126">См. также</span><span class="sxs-lookup"><span data-stu-id="dcc15-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcc15-127">Создание библиотеки DLL фильтра DirectShow</span><span class="sxs-lookup"><span data-stu-id="dcc15-127">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 
