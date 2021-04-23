---
description: API кодировщика
ms.assetid: 3d19152f-17a3-4576-a2a2-5b827d9ca8d1
title: API кодировщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 386b964f44dc4dc69896ead34bbe0d0177b198a1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423041"
---
# <a name="encoder-api"></a><span data-ttu-id="6d26a-103">API кодировщика</span><span class="sxs-lookup"><span data-stu-id="6d26a-103">Encoder API</span></span>

<span data-ttu-id="6d26a-104">API кодировщика предоставляет единообразный интерфейс для настройки кодировщиков программного обеспечения и оборудования.</span><span class="sxs-lookup"><span data-stu-id="6d26a-104">The Encoder API provides a uniform interface for configuring software and hardware encoders.</span></span> <span data-ttu-id="6d26a-105">Приложения могут использовать API кодировщика для настройки кодировщика и хранения параметров конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6d26a-105">Applications can use the Encoder API to configure an encoder and to store the configuration settings.</span></span> <span data-ttu-id="6d26a-106">Поставщики кодировщиков могут использовать API кодировщика для предоставления возможностей кодировщика.</span><span class="sxs-lookup"><span data-stu-id="6d26a-106">Encoder vendors can use the Encoder API to expose the capabilities of an encoder.</span></span> <span data-ttu-id="6d26a-107">Несмотря на то, что API кодировщика предназначен в основном для кодировщиков, это достаточно, так как декодеры могут его поддерживать.</span><span class="sxs-lookup"><span data-stu-id="6d26a-107">Although the Encoder API is designed primarily for encoders, it is general enough that decoders can support it as well.</span></span>

<span data-ttu-id="6d26a-108">API кодировщика предоставляется приложениям через интерфейс [**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) , который предоставляется фильтром кодировщика.</span><span class="sxs-lookup"><span data-stu-id="6d26a-108">The Encoder API is exposed to applications through the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface, which is exposed by the encoder filter.</span></span> <span data-ttu-id="6d26a-109">Фильтр кодировщика может быть собственным фильтром DirectShow, аппаратным кодировщиком или объектом мультимедиа DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="6d26a-109">The encoder filter may be a native DirectShow filter, a hardware encoder, or a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="6d26a-110">Фильтры программного обеспечения. кодировщик, реализованный как собственный фильтр DirectShow, должен напрямую предоставлять [**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="6d26a-110">Software filters: An encoder that is implemented as a native DirectShow filter should expose the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) directly.</span></span>
-   <span data-ttu-id="6d26a-111">Аппаратные кодировщики. устройство кодирования предоставляется через один или несколько Австреам минидриверс, которые представлены в пользовательском режиме Кспрокси.</span><span class="sxs-lookup"><span data-stu-id="6d26a-111">Hardware encoders: The encoding device is exposed through one or more AVStream minidrivers, which are represented in user mode by KSProxy.</span></span> <span data-ttu-id="6d26a-112">Кспрокси преобразует вызовы метода [**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) в наборы свойств KS.</span><span class="sxs-lookup"><span data-stu-id="6d26a-112">KSProxy translates [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) method calls into KS property sets.</span></span> <span data-ttu-id="6d26a-113">Дополнительные сведения см. в документации по DDK.</span><span class="sxs-lookup"><span data-stu-id="6d26a-113">For more information, see the DDK documentation.</span></span>
-   <span data-ttu-id="6d26a-114">Дмос: DMO должен предоставлять интерфейс [**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="6d26a-114">DMOs: The DMO should expose the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="6d26a-115">Приложения DirectShow могут запрашивать фильтр оболочки DMO, который предоставляет интерфейс, выполнив статистическую обработку DMO.</span><span class="sxs-lookup"><span data-stu-id="6d26a-115">DirectShow applications can query the DMO Wrapper filter, which exposes the interface by aggregating the DMO.</span></span> <span data-ttu-id="6d26a-116">Приложения, не основанные на DirectShow, могут напрямую запрашивать DMO.</span><span class="sxs-lookup"><span data-stu-id="6d26a-116">Applications not based on DirectShow can query the DMO directly.</span></span>

### <a name="encoder-capabilties"></a><span data-ttu-id="6d26a-117">Кодировщик предложения</span><span class="sxs-lookup"><span data-stu-id="6d26a-117">Encoder Capabilties</span></span>

<span data-ttu-id="6d26a-118">Кодировщик может зарегистрировать список возможностей высокого уровня, сохранив их в системном реестре.</span><span class="sxs-lookup"><span data-stu-id="6d26a-118">An encoder can register a list of high-level capabilities by storing them in the system registry.</span></span> <span data-ttu-id="6d26a-119">Каждая возможность идентифицируется по идентификатору GUID.</span><span class="sxs-lookup"><span data-stu-id="6d26a-119">Each capability is identified by a GUID.</span></span> <span data-ttu-id="6d26a-120">Чтобы перечислить возможности конкретного кодировщика, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6d26a-120">To enumerate the capabilities of a particular encoder, do the following:</span></span>

1.  <span data-ttu-id="6d26a-121">Создайте моникер, представляющий фильтр кодировщика.</span><span class="sxs-lookup"><span data-stu-id="6d26a-121">Create the moniker that represents the encoder filter.</span></span> <span data-ttu-id="6d26a-122">(См. раздел [Использование перечислителя системных устройств](using-the-system-device-enumerator.md).)</span><span class="sxs-lookup"><span data-stu-id="6d26a-122">(See [Using the System Device Enumerator](using-the-system-device-enumerator.md).)</span></span>
2.  <span data-ttu-id="6d26a-123">Запросите моникер фильтра для интерфейса [**ижеткапабилитиескэй**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) .</span><span class="sxs-lookup"><span data-stu-id="6d26a-123">Query the filter moniker for the [**IGetCapabilitiesKey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) interface.</span></span>
3.  <span data-ttu-id="6d26a-124">Вызовите [**ижеткапабилитиескэй:: жеткапабилитиескэй**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey).</span><span class="sxs-lookup"><span data-stu-id="6d26a-124">Call [**IGetCapabilitiesKey::GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey).</span></span> <span data-ttu-id="6d26a-125">Метод возвращает маркер раздела реестра, содержащего список возможностей фильтра.</span><span class="sxs-lookup"><span data-stu-id="6d26a-125">The method returns a handle to the registry key that contains the filter's capabilities list.</span></span>
4.  <span data-ttu-id="6d26a-126">Вызовите функцию **реженумвалуе** , чтобы перечислить значения для возвращаемого ключа.</span><span class="sxs-lookup"><span data-stu-id="6d26a-126">Call the **RegEnumValue** function to enumerate the values for the returned key.</span></span>

<span data-ttu-id="6d26a-127">Если вы разработке кодировщик, создайте записи реестра для возможностей при регистрации фильтра.</span><span class="sxs-lookup"><span data-stu-id="6d26a-127">If you are devloping an encoder, create the registry entries for the capabilities when the filter is registered.</span></span> <span data-ttu-id="6d26a-128">Для фильтров программного обеспечения создайте ключ с именем **capabilities** , который находится рядом с ключами **FilterData** и **FriendlyName** .</span><span class="sxs-lookup"><span data-stu-id="6d26a-128">For software filters, create a key named **Capabilities** that is adjacent to the **FilterData** and **FriendlyName** keys.</span></span> <span data-ttu-id="6d26a-129">Как правило, эти сведения добавляются после вызова [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) для регистрации стандартных данных фильтра.</span><span class="sxs-lookup"><span data-stu-id="6d26a-129">Typically, you would add this information after calling [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) to register the standard filter data.</span></span> <span data-ttu-id="6d26a-130">Дополнительные сведения см. [в разделе Регистрация фильтров DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="6d26a-130">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="6d26a-131">Кроме того, можно создать ключ **капабилитиеслокатион** , содержащий строку с расположением ключа **возможностей** в реестре.</span><span class="sxs-lookup"><span data-stu-id="6d26a-131">Alternatively, you can create a **CapabilitiesLocation** key that contains a string giving the location of the **Capabilities** key in the registry.</span></span> <span data-ttu-id="6d26a-132">Строка должна начинаться с "HKLM \\ ", "HKCR \\ " или "HKCU \\ ", чтобы указать поддерево реестра.</span><span class="sxs-lookup"><span data-stu-id="6d26a-132">The string should start with "HKLM\\", "HKCR\\", or "HKCU\\" to indicate the registry subtree.</span></span> <span data-ttu-id="6d26a-133">Для самонастраивающийся устройств файлы установки драйвера должны создать ключ **возможностей** , смежный с ключом **FriendlyName** фильтра, или использовать ключ **капабилитиеслокатион** , как описано в разделе Фильтры программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="6d26a-133">For Plug and Play devices, the driver's setup files should create a **Capabilities** key adjacent to the filter's **FriendlyName** key, or it can use a **CapabilitiesLocation** key as described for software filters.</span></span>

<span data-ttu-id="6d26a-134">После создания ключа **возможностей** Создайте значение для каждого GUID возможности.</span><span class="sxs-lookup"><span data-stu-id="6d26a-134">Once you have created the **Capabilities** key, create a value for each capability GUID.</span></span> <span data-ttu-id="6d26a-135">Имя значения должно быть строковым форматом идентификатора GUID в форме `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` .</span><span class="sxs-lookup"><span data-stu-id="6d26a-135">The name of the value should be the string form of the GUID, in the form `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}`.</span></span> <span data-ttu-id="6d26a-136">Каждый тип значения должен быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="6d26a-136">Each value type should be one of the following:</span></span>

-   <span data-ttu-id="6d26a-137">Одно числовое значение.</span><span class="sxs-lookup"><span data-stu-id="6d26a-137">Single numerical value.</span></span> <span data-ttu-id="6d26a-138">Используйте значение **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="6d26a-138">Use a **DWORD** value.</span></span>
-   <span data-ttu-id="6d26a-139">GUID.</span><span class="sxs-lookup"><span data-stu-id="6d26a-139">GUID.</span></span> <span data-ttu-id="6d26a-140">Используйте форму строки GUID.</span><span class="sxs-lookup"><span data-stu-id="6d26a-140">Use the string form of the GUID.</span></span>
-   <span data-ttu-id="6d26a-141">Числовые пары.</span><span class="sxs-lookup"><span data-stu-id="6d26a-141">Numeric pairs.</span></span> <span data-ttu-id="6d26a-142">Используйте строку с формой "a, b" для представления пар значений, таких как ширина и высота, числитель и знаменатель для дробей.</span><span class="sxs-lookup"><span data-stu-id="6d26a-142">Use a string with the form "a,b" to represent pairs of values, such as width and height, or numerator and denominator for fractions.</span></span>
-   <span data-ttu-id="6d26a-143">Массивы значений.</span><span class="sxs-lookup"><span data-stu-id="6d26a-143">Arrays of values.</span></span> <span data-ttu-id="6d26a-144">Используйте несколько строк (**reg \_ SZ \_ Multi**), чтобы представить более одного значения.</span><span class="sxs-lookup"><span data-stu-id="6d26a-144">Use multi-strings (**REG\_SZ\_MULTI**) to represent more than one value.</span></span>

<span data-ttu-id="6d26a-145">В следующем примере показана структура реестра для фильтра программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="6d26a-145">The following example shows the registry layout for a software filter:</span></span>


```C++
\HKCR\CLSID\Filter Category\Instance\Filter CLSID\Capabilities\
    
Values: 
    
    guid1: 1234 (REG_DWORD)   
    
    guid2: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" (REG_SZ)
    
    guid3: "2","4","6" (REG_SZ_MULTI)
    
    guid4: "720,480" (REG_SZ) 
```



### <a name="encoder-profiles"></a><span data-ttu-id="6d26a-146">Профили кодировщика</span><span class="sxs-lookup"><span data-stu-id="6d26a-146">Encoder Profiles</span></span>

<span data-ttu-id="6d26a-147">*Профиль кодировщика* — это фиксированный список параметров конфигурации, которые можно применить к кодировщику во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="6d26a-147">An *encoder profile* is a fixed list of configuration settings that can be applied to an encoder at run time.</span></span> <span data-ttu-id="6d26a-148">Профили не зависят от кодировщика; приложение может выбрать кодировщик, затем выбрать профиль и применить параметры профиля к кодировщику.</span><span class="sxs-lookup"><span data-stu-id="6d26a-148">Profiles are independent of the encoder; an application can select an encoder, then select a profile and apply the profile settings to the encoder.</span></span> <span data-ttu-id="6d26a-149">Профили определяются по идентификатору GUID и должны храниться в следующем расположении в реестре:</span><span class="sxs-lookup"><span data-stu-id="6d26a-149">Profiles are identified by GUID and should be stored in the following location in the registry:</span></span>


```C++
\HKLM\Software\Microsoft\EncoderProfiles\Profile GUID\
```



<span data-ttu-id="6d26a-150">где *GUID профиля*</span><span class="sxs-lookup"><span data-stu-id="6d26a-150">where *Profile GUID*</span></span>

<span data-ttu-id="6d26a-151">строковый формат идентификатора GUID, определяющего профиль.</span><span class="sxs-lookup"><span data-stu-id="6d26a-151">is the string form of the GUID that identifies the profile.</span></span> <span data-ttu-id="6d26a-152">Создайте значения для каждого параметра.</span><span class="sxs-lookup"><span data-stu-id="6d26a-152">Create values for each setting.</span></span> <span data-ttu-id="6d26a-153">Также создайте строковое значение с именем FriendlyName, данные которого определяют профиль (например, "Ловбандвидсвидео").</span><span class="sxs-lookup"><span data-stu-id="6d26a-153">Also create a string value named "FriendlyName" whose data identifies the profile (such as "LowBandwidthVideo").</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d26a-154">См. также</span><span class="sxs-lookup"><span data-stu-id="6d26a-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d26a-155">Разработка кодировщика и декодера</span><span class="sxs-lookup"><span data-stu-id="6d26a-155">Encoder and Decoder Development</span></span>](encoder-and-decoder-development.md)
</dt> </dl>

 

 



