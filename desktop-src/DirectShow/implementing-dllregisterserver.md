---
description: Реализация DllRegisterServer
ms.assetid: aaa4069e-0b6a-4a76-b950-1a85a9ed969d
title: Реализация DllRegisterServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b994e80a181b69efffbe6123382957e7a38f8278
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140343"
---
# <a name="implementing-dllregisterserver"></a><span data-ttu-id="3b322-103">Реализация DllRegisterServer</span><span class="sxs-lookup"><span data-stu-id="3b322-103">Implementing DllRegisterServer</span></span>

<span data-ttu-id="3b322-104">Последним шагом является реализация функции **DllRegisterServer** .</span><span class="sxs-lookup"><span data-stu-id="3b322-104">The final step is to implement the **DllRegisterServer** function.</span></span> <span data-ttu-id="3b322-105">Библиотека DLL, содержащая компонент, должна экспортировать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="3b322-105">The DLL that contains the component must export this function.</span></span> <span data-ttu-id="3b322-106">Функция будет вызываться приложением настройки или при запуске пользователем средства Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="3b322-106">The function will be called by a set-up application, or when the user runs the Regsvr32.exe tool.</span></span>

<span data-ttu-id="3b322-107">В следующем примере показана минимальная реализация **DlLRegisterServer**:</span><span class="sxs-lookup"><span data-stu-id="3b322-107">The following example shows a minimal implementation of **DlLRegisterServer**:</span></span>


```C++
STDAPI DllRegisterServer(void)
{
    return AMovieDllRegisterServer2(TRUE);
}
```



<span data-ttu-id="3b322-108">Функция [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) создает записи реестра для каждого компонента в</span><span class="sxs-lookup"><span data-stu-id="3b322-108">The [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function creates registry entries for every component in the</span></span>


```
g_Templates
```



<span data-ttu-id="3b322-109">Массив.</span><span class="sxs-lookup"><span data-stu-id="3b322-109">array.</span></span> <span data-ttu-id="3b322-110">Однако эта функция имеет некоторые ограничения.</span><span class="sxs-lookup"><span data-stu-id="3b322-110">However, this function has some limitations.</span></span> <span data-ttu-id="3b322-111">Во-первых, он назначает каждый фильтр категории "фильтры DirectShow" (CLSID \_ легациамфилтеркатегори), но не каждый фильтр принадлежит к этой категории.</span><span class="sxs-lookup"><span data-stu-id="3b322-111">First, it assigns every filter to the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory), but not every filter belongs in this category.</span></span> <span data-ttu-id="3b322-112">Например, фильтры записи и фильтры сжатия имеют собственные категории.</span><span class="sxs-lookup"><span data-stu-id="3b322-112">Capture filters and compression filters, for example, have their own categories.</span></span> <span data-ttu-id="3b322-113">Во-вторых, если фильтр поддерживает аппаратное устройство, может потребоваться зарегистрировать два дополнительных фрагмента информации, которые **AMovieDLLRegisterServer2** не обрабатывает: *средний уровень* и *Категория ПИН-кода*.</span><span class="sxs-lookup"><span data-stu-id="3b322-113">Second, if your filter supports a hardware device, you might need to register two additional pieces of information that **AMovieDLLRegisterServer2** does not handle: the *medium* and the *pin category*.</span></span> <span data-ttu-id="3b322-114">Средний уровень определяет способ связи на аппаратном устройстве, таком как шина.</span><span class="sxs-lookup"><span data-stu-id="3b322-114">A medium defines a method of communication in a hardware device, such as a bus.</span></span> <span data-ttu-id="3b322-115">Категория закрепления определяет функцию ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="3b322-115">The pin category defines the function of a pin.</span></span> <span data-ttu-id="3b322-116">Сведения о средних средах см. в разделе «КСПИН \_ Medium» в пакете средств разработки драйверов Microsoft Windows (DDK).</span><span class="sxs-lookup"><span data-stu-id="3b322-116">For information on mediums, see "KSPIN\_MEDIUM" in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="3b322-117">Список категорий ПИН-кодов см. в разделе [закрепить набор свойств](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="3b322-117">For a list of pin categories, see [Pin Property Set](pin-property-set.md).</span></span>

<span data-ttu-id="3b322-118">Если необходимо указать категорию фильтра, среднюю или закрепление, вызовите метод [**IFilterMapper2:: регистерфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) из функции **DllRegisterServer**.</span><span class="sxs-lookup"><span data-stu-id="3b322-118">If you want to specify a filter category, a medium, or a pin category, call the [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method from within **DllRegisterServer**.</span></span> <span data-ttu-id="3b322-119">Этот метод принимает указатель на структуру [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) , которая задает сведения о фильтре.</span><span class="sxs-lookup"><span data-stu-id="3b322-119">This method takes a pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure, which specifies information about the filter.</span></span>

<span data-ttu-id="3b322-120">Чтобы усложнить важность, структура **REGFILTER2** поддерживает два разных формата для регистрации ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="3b322-120">To complicate matters somewhat, the **REGFILTER2** structure supports two different formats for registering pins.</span></span> <span data-ttu-id="3b322-121">Элемент **двверсион** задает формат:</span><span class="sxs-lookup"><span data-stu-id="3b322-121">The **dwVersion** member specifies the format:</span></span>

-   <span data-ttu-id="3b322-122">Если **двверсион** имеет значение 1, то формат ПИН-кода — **амовиесетуп \_ PIN** (описанный выше).</span><span class="sxs-lookup"><span data-stu-id="3b322-122">If **dwVersion** is 1, the pin format is **AMOVIESETUP\_PIN** (described previously).</span></span>
-   <span data-ttu-id="3b322-123">Если **двверсион** имеет значение 2, то формат ПИН-кода — [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).</span><span class="sxs-lookup"><span data-stu-id="3b322-123">If **dwVersion** is 2, the pin format is [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).</span></span>

<span data-ttu-id="3b322-124">Структура **REGFILTERPINS2** включает записи для средних и контактных категорий.</span><span class="sxs-lookup"><span data-stu-id="3b322-124">The **REGFILTERPINS2** structure includes entries for pin mediums and pin categories.</span></span> <span data-ttu-id="3b322-125">Кроме того, в нем используются битовые флаги для некоторых элементов, которые **амовиесетуп \_ закрепить** как логические значения.</span><span class="sxs-lookup"><span data-stu-id="3b322-125">Also, it uses bit flags for some items that **AMOVIESETUP\_PIN** declares as Boolean values.</span></span>

<span data-ttu-id="3b322-126">В следующем примере показано, как вызвать **IFilterMapper2:: регистерфилтер** из функции **DllRegisterServer**:</span><span class="sxs-lookup"><span data-stu-id="3b322-126">The following example shows how to call **IFilterMapper2::RegisterFilter** from inside **DllRegisterServer**:</span></span>


```C++
REGFILTER2 rf2FilterReg = {
    1,              // Version 1 (no pin mediums or pin category).
    MERIT_NORMAL,   // Merit.
    1,              // Number of pins.
    &sudPins        // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
        return hr;

    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->RegisterFilter(
        CLSID_SomeFilter,                // Filter CLSID. 
        g_wszName,                       // Filter name.
        NULL,                            // Device moniker. 
        &CLSID_VideoCompressorCategory,  // Video compressor category.
        g_wszName,                       // Instance data.
        &rf2FilterReg                    // Pointer to filter information.
    );
    pFM2->Release();
    return hr;
}
```



 

 



