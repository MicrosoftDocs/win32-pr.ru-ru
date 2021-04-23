---
description: Перечисление эффектов и переходов
ms.assetid: 364b7bfb-5d6e-4ca6-b0c8-7a0180c3f61a
title: Перечисление эффектов и переходов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e533f36501ac8da6015cc31eea6c2c111bf6a208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673013"
---
# <a name="enumerating-effects-and-transitions"></a><span data-ttu-id="8c683-103">Перечисление эффектов и переходов</span><span class="sxs-lookup"><span data-stu-id="8c683-103">Enumerating Effects and Transitions</span></span>

<span data-ttu-id="8c683-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="8c683-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="8c683-105">DirectShow предоставляет объект [перечислителя системных устройств](system-device-enumerator.md) для перечисления устройств.</span><span class="sxs-lookup"><span data-stu-id="8c683-105">DirectShow provides a [System Device Enumerator](system-device-enumerator.md) object for enumerating devices.</span></span> <span data-ttu-id="8c683-106">Его можно использовать для получения моникеров для эффектов или переходов, установленных в системе пользователя.</span><span class="sxs-lookup"><span data-stu-id="8c683-106">You can use it to retrieve monikers for effects or transitions installed on the user's system.</span></span>

<span data-ttu-id="8c683-107">Перечислитель системных устройств предоставляет интерфейс [**икреатедевенум**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) .</span><span class="sxs-lookup"><span data-stu-id="8c683-107">The system device enumerator exposes the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span> <span data-ttu-id="8c683-108">Он возвращает перечислители категорий для указанных категорий устройств.</span><span class="sxs-lookup"><span data-stu-id="8c683-108">It returns category enumerators for specified device categories.</span></span> <span data-ttu-id="8c683-109">Перечислитель категорий, в свою очередь, предоставляет интерфейс [**иенуммоникер**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) и возвращает моникеры для каждого устройства в категории.</span><span class="sxs-lookup"><span data-stu-id="8c683-109">A category enumerator, in turn, exposes the [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) interface and returns monikers for each device in the category.</span></span> <span data-ttu-id="8c683-110">Подробное описание использования **икреатедевенум** см. в разделе [Перечисление устройств и фильтров](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="8c683-110">For a detailed discussion of using **ICreateDevEnum**, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span> <span data-ttu-id="8c683-111">Ниже приведена краткая сводка, относящаяся к службам редактирования DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8c683-111">The following is a brief summary, specific to DirectShow Editing Services.</span></span>

<span data-ttu-id="8c683-112">Чтобы перечислить эффекты или переходы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8c683-112">To enumerate effects or transitions, perform the following steps.</span></span>

1.  <span data-ttu-id="8c683-113">Создайте экземпляр перечислителя системных устройств.</span><span class="sxs-lookup"><span data-stu-id="8c683-113">Create an instance of the system device enumerator.</span></span>
2.  <span data-ttu-id="8c683-114">Вызовите метод [**икреатедевенум:: креатеклассенумератор**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) , чтобы получить перечислитель категорий.</span><span class="sxs-lookup"><span data-stu-id="8c683-114">Call the [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method to retrieve a category enumerator.</span></span> <span data-ttu-id="8c683-115">Категории определяются идентификаторами классов (CLSID).</span><span class="sxs-lookup"><span data-stu-id="8c683-115">Categories are defined by class identifiers (CLSIDs).</span></span> <span data-ttu-id="8c683-116">Используйте CLSID \_ VideoEffects1Category для эффектов или CLSID \_ VideoEffects2Category для переходов.</span><span class="sxs-lookup"><span data-stu-id="8c683-116">Use CLSID\_VideoEffects1Category for effects or CLSID\_VideoEffects2Category for transitions.</span></span>
3.  <span data-ttu-id="8c683-117">Вызовите метод **иенуммоникер:: Next** , чтобы получить все моникеры в перечислении.</span><span class="sxs-lookup"><span data-stu-id="8c683-117">Call **IEnumMoniker::Next** to retrieve each moniker in the enumeration.</span></span>
4.  <span data-ttu-id="8c683-118">Для каждого моникера вызовите **IMoniker:: биндтостораже** , чтобы получить связанный с ним контейнер свойств.</span><span class="sxs-lookup"><span data-stu-id="8c683-118">For each moniker, call **IMoniker::BindToStorage** to retrieve its associated property bag.</span></span>

<span data-ttu-id="8c683-119">Контейнер свойств содержит понятное имя и глобальный уникальный идентификатор (GUID) для действия или перехода.</span><span class="sxs-lookup"><span data-stu-id="8c683-119">The property bag contains the friendly name and the globally unique identifier (GUID) for the effect or transition.</span></span> <span data-ttu-id="8c683-120">Приложение может отобразить список понятных имен, а затем получить соответствующий идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="8c683-120">An application can display a list of friendly names and then obtain the corresponding GUID.</span></span>

<span data-ttu-id="8c683-121">Эти шаги показаны в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="8c683-121">The following code example illustrates these steps.</span></span>


```C++
ICreateDevEnum *pCreateDevEnum = NULL;
IEnumMoniker *pEnumMoniker = NULL;

// Create the System Device Enumerator.
HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
    CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, (void**)&pCreateDevEnum);
if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

// Create an enumerator for the video effects category.
hr = pCreateDevEnum->CreateClassEnumerator(
    CLSID_VideoEffects1Category,  // Video effects category. 
    &pEnumMoniker, 0);               

// Note: Use CLSID_VideoEffects2Category for video transitions.

if (hr == S_OK)  // S_FALSE means the category is empty.
{
    // Enumerate each video effect.
    IMoniker *pMoniker;
    while (S_OK == pEnumMoniker->Next(1, &pMoniker, NULL))
    {
        IPropertyBag *pBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pBag);
        if(FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(OLESTR("FriendlyName"), &var, NULL);
        if (SUCCEEDED(hr))
        {
            if ( ... )  // Check if var.bstrVal is the name you want.
            {
                VARIANT var2;
                GUID guid;
                var2.vt = VT_BSTR;
                pBag->Read(OLESTR("guid"), &var2, NULL);
                CLSIDFromString(var2.bstrVal, &guid);
                VariantClear(&var2);
                // GUID is now the CLSID for the effect.
            }
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnumMoniker->Release();
}
pCreateDevEnum->Release();
```



## <a name="related-topics"></a><span data-ttu-id="8c683-122">См. также</span><span class="sxs-lookup"><span data-stu-id="8c683-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c683-123">Работа с эффектами и переходами</span><span class="sxs-lookup"><span data-stu-id="8c683-123">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
