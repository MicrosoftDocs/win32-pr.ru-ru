---
description: Использование перечислителя системных устройств
ms.assetid: 70db139c-2c5b-4574-bec3-dfe758b16715
title: Использование перечислителя системных устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f8f66cb64e9f7bb51d6b0716b9fa23cf531435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104557454"
---
# <a name="using-the-system-device-enumerator"></a><span data-ttu-id="1c431-103">Использование перечислителя системных устройств</span><span class="sxs-lookup"><span data-stu-id="1c431-103">Using the System Device Enumerator</span></span>

<span data-ttu-id="1c431-104">Перечислитель системных устройств обеспечивает единообразный способ перечисления по категориям фильтров, зарегистрированных в системе пользователя.</span><span class="sxs-lookup"><span data-stu-id="1c431-104">The System Device Enumerator provides a uniform way to enumerate, by category, the filters registered on a user's system.</span></span> <span data-ttu-id="1c431-105">Кроме того, он различает отдельные аппаратные устройства, даже если один и тот же фильтр поддерживает их.</span><span class="sxs-lookup"><span data-stu-id="1c431-105">Moreover, it differentiates between individual hardware devices, even if the same filter supports them.</span></span> <span data-ttu-id="1c431-106">Это особенно полезно для устройств, использующих WDM (WDM) и фильтр Кспрокси.</span><span class="sxs-lookup"><span data-stu-id="1c431-106">This is particularly useful for devices that use the Windows Driver Model (WDM) and the KSProxy filter.</span></span> <span data-ttu-id="1c431-107">Например, у пользователя может быть несколько устройств записи видео WDM, которые поддерживаются одним и тем же фильтром.</span><span class="sxs-lookup"><span data-stu-id="1c431-107">For example, the user might have several WDM video capture devices, all supported by the same filter.</span></span> <span data-ttu-id="1c431-108">Перечислитель системных устройств обрабатывает их как отдельные экземпляры устройств.</span><span class="sxs-lookup"><span data-stu-id="1c431-108">The System Device Enumerator treats them as separate device instances.</span></span>

<span data-ttu-id="1c431-109">Перечислитель системных устройств работает путем создания перечислителя для определенной категории, например для записи звука или сжатия видео.</span><span class="sxs-lookup"><span data-stu-id="1c431-109">The System Device Enumerator works by creating an enumerator for a specific category, such as audio capture or video compression.</span></span> <span data-ttu-id="1c431-110">Перечислитель категорий Возвращает уникальный моникер для каждого устройства в категории.</span><span class="sxs-lookup"><span data-stu-id="1c431-110">The category enumerator returns a unique moniker for each device in the category.</span></span> <span data-ttu-id="1c431-111">Перечислитель категорий автоматически включает в категорию все соответствующие самонастраивающийся устройства.</span><span class="sxs-lookup"><span data-stu-id="1c431-111">The category enumerator automatically includes any relevant Plug and Play devices in the category.</span></span> <span data-ttu-id="1c431-112">Список категорий см. в разделе [Фильтрация категорий](filter-categories.md).</span><span class="sxs-lookup"><span data-stu-id="1c431-112">For a list of categories, see [Filter Categories](filter-categories.md).</span></span>

<span data-ttu-id="1c431-113">Чтобы использовать перечислитель системных устройств, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1c431-113">To use the System Device Enumerator, do the following:</span></span>

1.  <span data-ttu-id="1c431-114">Создайте перечислитель системных устройств, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="1c431-114">Create the system device enumerator by calling **CoCreateInstance**.</span></span> <span data-ttu-id="1c431-115">Идентификатор класса (CLSID) — это CLSID \_ системдевицеенум.</span><span class="sxs-lookup"><span data-stu-id="1c431-115">The class identifier (CLSID) is CLSID\_SystemDeviceEnum.</span></span>
2.  <span data-ttu-id="1c431-116">Получите перечислитель категорий, вызвав [**икреатедевенум:: креатеклассенумератор**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) с идентификатором CLSID нужной категории.</span><span class="sxs-lookup"><span data-stu-id="1c431-116">Obtain a category enumerator by calling [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the CLSID of the desired category.</span></span> <span data-ttu-id="1c431-117">Этот метод возвращает указатель интерфейса **иенуммоникер** .</span><span class="sxs-lookup"><span data-stu-id="1c431-117">This method returns an **IEnumMoniker** interface pointer.</span></span> <span data-ttu-id="1c431-118">Если категория пуста (или не существует), метод возвращает значение S false, \_ а не код ошибки.</span><span class="sxs-lookup"><span data-stu-id="1c431-118">If the category is empty (or does not exist), the method returns S\_FALSE rather than an error code.</span></span> <span data-ttu-id="1c431-119">Если это так, возвращаемый указатель **иенуммоникер** будет **иметь значение NULL** и разыменование этого указателя вызовет исключение.</span><span class="sxs-lookup"><span data-stu-id="1c431-119">If so, the returned **IEnumMoniker** pointer is **NULL** and dereferencing it will cause an exception.</span></span> <span data-ttu-id="1c431-120">Таким образом, \_ при вызове **креатеклассенумератор** явным образом проверяйте, что вместо вызова обычного макроса с **успехом** .</span><span class="sxs-lookup"><span data-stu-id="1c431-120">Therefore, explicitly test for S\_OK when you call **CreateClassEnumerator**, instead of calling the usual **SUCCEEDED** macro.</span></span>
3.  <span data-ttu-id="1c431-121">Используйте метод **иенуммоникер:: Next** для перечисления каждого моникера.</span><span class="sxs-lookup"><span data-stu-id="1c431-121">Use the **IEnumMoniker::Next** method to enumerate each moniker.</span></span> <span data-ttu-id="1c431-122">Этот метод возвращает указатель интерфейса **IMoniker** .</span><span class="sxs-lookup"><span data-stu-id="1c431-122">This method returns an **IMoniker** interface pointer.</span></span> <span data-ttu-id="1c431-123">Когда **следующий** метод достигает конца перечисления, он также возвращает \_ значение false, поэтому еще раз проверьте наличие \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1c431-123">When the **Next** method reaches the end of the enumeration, it also returns S\_FALSE, so again check for S\_OK.</span></span>
4.  <span data-ttu-id="1c431-124">Чтобы получить понятное имя устройства (например, для вывода в пользовательском интерфейсе), вызовите метод **IMoniker:: биндтостораже** .</span><span class="sxs-lookup"><span data-stu-id="1c431-124">To retrieve the friendly name of the device (for example, to display in the user interface), call the **IMoniker::BindToStorage** method.</span></span>
5.  <span data-ttu-id="1c431-125">Чтобы создать и инициализировать фильтр DirectShow, управляющий устройством, вызовите **IMoniker:: биндтубжект** в моникере.</span><span class="sxs-lookup"><span data-stu-id="1c431-125">To create and initialize the DirectShow filter that manages the device, call **IMoniker::BindToObject** on the moniker.</span></span> <span data-ttu-id="1c431-126">Вызовите [**ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) , чтобы добавить фильтр в граф.</span><span class="sxs-lookup"><span data-stu-id="1c431-126">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the graph.</span></span>

<span data-ttu-id="1c431-127">Этот процесс представлен на схеме ниже.</span><span class="sxs-lookup"><span data-stu-id="1c431-127">The following diagram illustrates this process.</span></span>

![Перечисление устройств](images/sysdevenum.png)

<span data-ttu-id="1c431-129">В следующем примере показано, как перечислить Видеокомпрессоры, установленные в системе пользователя.</span><span class="sxs-lookup"><span data-stu-id="1c431-129">The following example shows how to enumerate the video compressors installed on the user's system.</span></span> <span data-ttu-id="1c431-130">Для краткости в примере выполняется минимальная проверка ошибок.</span><span class="sxs-lookup"><span data-stu-id="1c431-130">For brevity, the example performs minimal error checking.</span></span>


```C++
// Create the System Device Enumerator.
HRESULT hr;
ICreateDevEnum *pSysDevEnum = NULL;
hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC_SERVER,
    IID_ICreateDevEnum, (void **)&pSysDevEnum);
if (FAILED(hr))
{
    return hr;
}

// Obtain a class enumerator for the video compressor category.
IEnumMoniker *pEnumCat = NULL;
hr = pSysDevEnum->CreateClassEnumerator(CLSID_VideoCompressorCategory, &pEnumCat, 0);

if (hr == S_OK) 
{
    // Enumerate the monikers.
    IMoniker *pMoniker = NULL;
    ULONG cFetched;
    while(pEnumCat->Next(1, &pMoniker, &cFetched) == S_OK)
    {
        IPropertyBag *pPropBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pPropBag);
        if (SUCCEEDED(hr))
        {
            // To retrieve the filter's friendly name, do the following:
            VARIANT varName;
            VariantInit(&varName);
            hr = pPropBag->Read(L"FriendlyName", &varName, 0);
            if (SUCCEEDED(hr))
            {
                // Display the name in your UI somehow.
            }
            VariantClear(&varName);

            // To create an instance of the filter, do the following:
            IBaseFilter *pFilter;
            hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter,
                (void**)&pFilter);
            // Now add the filter to the graph. 
            //Remember to release pFilter later.
            pPropBag->Release();
        }
        pMoniker->Release();
    }
    pEnumCat->Release();
}
pSysDevEnum->Release();
```



<span data-ttu-id="1c431-131">**Моникеры устройств**</span><span class="sxs-lookup"><span data-stu-id="1c431-131">**Device Monikers**</span></span>

<span data-ttu-id="1c431-132">Для моникеров устройств можно передать моникер методу [**IFilterGraph2:: аддсаурцефилтерформоникер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) , чтобы создать фильтр записи для устройства.</span><span class="sxs-lookup"><span data-stu-id="1c431-132">For device monikers, you can pass the moniker to the [**IFilterGraph2::AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) method to create a capture filter for the device.</span></span> <span data-ttu-id="1c431-133">Пример кода см. в документации по этому методу.</span><span class="sxs-lookup"><span data-stu-id="1c431-133">For example code, see the documentation for that method.</span></span>

<span data-ttu-id="1c431-134">Метод **IMoniker:: DisplayName** Возвращает отображаемое имя моникера.</span><span class="sxs-lookup"><span data-stu-id="1c431-134">The **IMoniker::GetDisplayName** method returns the display name of the moniker.</span></span> <span data-ttu-id="1c431-135">Хотя отображаемое имя доступно для чтения, оно обычно не отображается для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="1c431-135">Although the display name is readable, you would not typically display it to an end-user.</span></span> <span data-ttu-id="1c431-136">Вместо этого получите понятное имя из контейнера свойств, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="1c431-136">Get the friendly name from the property bag instead, as described previously.</span></span>

<span data-ttu-id="1c431-137">Метод **IMoniker::P арседисплайнаме** или функция **мкпарседисплайнаме** можно использовать для создания моникера устройства по умолчанию для данной категории фильтра.</span><span class="sxs-lookup"><span data-stu-id="1c431-137">The **IMoniker::ParseDisplayName** method or the **MkParseDisplayName** function can be used to create a default device moniker for a given filter category.</span></span> <span data-ttu-id="1c431-138">Используйте отображаемое имя в форме `@device:*:{category-clsid}` , где `category-clsid` — строковое представление GUID категории.</span><span class="sxs-lookup"><span data-stu-id="1c431-138">Use a display name with the form `@device:*:{category-clsid}`, where `category-clsid` is the string representation of the category GUID.</span></span> <span data-ttu-id="1c431-139">Моникер по умолчанию является первым моникером, возвращенным перечислителем устройства для этой категории.</span><span class="sxs-lookup"><span data-stu-id="1c431-139">The default moniker is the first moniker returned by the device enumerator for that category.</span></span>

 

 



