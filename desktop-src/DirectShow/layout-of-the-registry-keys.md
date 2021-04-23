---
description: Структура разделов реестра
ms.assetid: c041d094-8165-446f-bf77-0d53b728fe7a
title: Структура разделов реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5783a9f083f639912188f418238f46a5d45ed922
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672941"
---
# <a name="layout-of-the-registry-keys"></a><span data-ttu-id="37505-103">Структура разделов реестра</span><span class="sxs-lookup"><span data-stu-id="37505-103">Layout of the Registry Keys</span></span>

<span data-ttu-id="37505-104">Фильтры DirectShow регистрируются в двух местах:</span><span class="sxs-lookup"><span data-stu-id="37505-104">DirectShow filters are registered in two places:</span></span>

-   <span data-ttu-id="37505-105">Библиотека DLL, содержащая фильтр, регистрируется в качестве сервера COM фильтра.</span><span class="sxs-lookup"><span data-stu-id="37505-105">The DLL that contains the filter is registered as the filter's COM server.</span></span> <span data-ttu-id="37505-106">Когда приложение вызывает **CoCreateInstance** для создания фильтра, Библиотека Microsoft Windows com использует эту запись реестра для нахождение библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="37505-106">When an application calls **CoCreateInstance** to create the filter, the Microsoft Windows COM library uses this registry entry to locate the DLL.</span></span>
-   <span data-ttu-id="37505-107">Дополнительные сведения о фильтре можно зарегистрировать в категории фильтров.</span><span class="sxs-lookup"><span data-stu-id="37505-107">Additional information about the filter can be registered within a filter category.</span></span> <span data-ttu-id="37505-108">Эта информация включает [перечислитель системных устройств](system-device-enumerator.md) и средство [сопоставления фильтров](filter-mapper.md) для нахождение фильтра.</span><span class="sxs-lookup"><span data-stu-id="37505-108">This information enables the [System Device Enumerator](system-device-enumerator.md) and the [Filter Mapper](filter-mapper.md) to locate the filter.</span></span>

<span data-ttu-id="37505-109">Для регистрации дополнительных сведений о фильтрах фильтры не требуются.</span><span class="sxs-lookup"><span data-stu-id="37505-109">Filters are not required to register the additional filter information.</span></span> <span data-ttu-id="37505-110">Пока библиотека DLL зарегистрирована как сервер COM, приложение может создать фильтр и добавить его в граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="37505-110">As long as the DLL is registered as the COM server, an application can create the filter and add it to a filter graph.</span></span> <span data-ttu-id="37505-111">Однако если вы хотите, чтобы фильтр был обнаруживаемым перечислителем системных устройств или средством сопоставления фильтров, необходимо зарегистрировать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="37505-111">However, if you want your filter to be discoverable by the System Device Enumerator or the Filter Mapper, you must register the additional information.</span></span>

<span data-ttu-id="37505-112">Запись реестра для библиотеки DLL имеет следующие ключи:</span><span class="sxs-lookup"><span data-stu-id="37505-112">The registry entry for the DLL has the following keys:</span></span>


```
HKEY_CLASSES_ROOT
    CLSID
        Filter CLSID 
            REG_SZ: (Default) = Friendly name

            InprocServer32
                REG_SZ: (Default) = File name of the DLL
                REG_SZ: ThreadingModel = Both
```



<span data-ttu-id="37505-113">Запись реестра для сведений о фильтрах имеет следующие ключи:</span><span class="sxs-lookup"><span data-stu-id="37505-113">The registry entry for the filter information has the following keys:</span></span>


```
HKEY_CLASSES_ROOT
    CLSID
        Category
            Instance
                Filter CLSID
                    REG_SZ: CLSID = Filter CLSID
                    REG_BINARY: FilterData = Filter information
                    REG_SZ: FriendlyName = Friendly name
```




```
Category
```



<span data-ttu-id="37505-114">Идентификатор GUID категории фильтра.</span><span class="sxs-lookup"><span data-stu-id="37505-114">is the GUID of a filter category.</span></span> <span data-ttu-id="37505-115">(См. раздел [Фильтрация категорий](filter-categories.md).) Сведения о фильтре упаковываются в двоичный формат.</span><span class="sxs-lookup"><span data-stu-id="37505-115">(See [Filter Categories](filter-categories.md).) The filter information is packed into a binary format.</span></span> <span data-ttu-id="37505-116">Интерфейс [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) распаковать эти данные при поиске фильтра в реестре.</span><span class="sxs-lookup"><span data-stu-id="37505-116">The [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface unpacks this data when it searches the registry for a filter.</span></span>

<span data-ttu-id="37505-117">Все идентификаторы GUID категорий фильтров перечислены в реестре в следующем разделе:</span><span class="sxs-lookup"><span data-stu-id="37505-117">All of the filter category GUIDs are listed in the registry under the following key:</span></span>


```C++
HKEY_CLASSES_ROOT\CLSID\{DA4E3DA0-D07D-11d0-BD50-00A0C911CE86}\Instance
```



 

 



