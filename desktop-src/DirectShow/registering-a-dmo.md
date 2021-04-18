---
description: Регистрация DMO
ms.assetid: 9f74fc1c-b903-4725-b667-3c56a2726dbc
title: Регистрация DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c5364304fd5f6a9557c84a4b27c86d29fa4e84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682228"
---
# <a name="registering-a-dmo"></a><span data-ttu-id="f58da-103">Регистрация DMO</span><span class="sxs-lookup"><span data-stu-id="f58da-103">Registering a DMO</span></span>

<span data-ttu-id="f58da-104">Чтобы клиенты могли использовать DMO, идентификатор CLSID должен быть зарегистрирован в системе пользователя.</span><span class="sxs-lookup"><span data-stu-id="f58da-104">In order for clients to use your DMO, the CLSID must be registered on the user's system.</span></span> <span data-ttu-id="f58da-105">Это делается с помощью функции **DllRegisterServer** библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="f58da-105">This is done through the DLL's **DllRegisterServer** function.</span></span> <span data-ttu-id="f58da-106">Если используется библиотека активных шаблонов (ATL), мастер ATL автоматически создает эту функцию.</span><span class="sxs-lookup"><span data-stu-id="f58da-106">If you are using the Active Template Library (ATL), the ATL wizard automatically generates this function.</span></span>

<span data-ttu-id="f58da-107">Можно также зарегистрировать DMO в одной или нескольких стандартных категориях DMO.</span><span class="sxs-lookup"><span data-stu-id="f58da-107">You can also register your DMO under one or more standard DMO categories.</span></span> <span data-ttu-id="f58da-108">Это позволяет клиентам обнаруживать объекты DMO с помощью функции [**дмоенум**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) .</span><span class="sxs-lookup"><span data-stu-id="f58da-108">This enables clients to discover your DMO using the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function.</span></span> <span data-ttu-id="f58da-109">Категории определяются по идентификатору GUID и перечислены в разделе [GUID DMO](dmo-guids.md).</span><span class="sxs-lookup"><span data-stu-id="f58da-109">The categories are defined by GUID, and are listed in the section [DMO GUIDs](dmo-guids.md).</span></span>

<span data-ttu-id="f58da-110">Регистрация DMO в категории является необязательной.</span><span class="sxs-lookup"><span data-stu-id="f58da-110">Registering a DMO under a category is optional.</span></span> <span data-ttu-id="f58da-111">Для этого вызовите функцию [**дморегистер**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) и укажите понятное имя DMO, CLSID и категорию.</span><span class="sxs-lookup"><span data-stu-id="f58da-111">To do so, call the [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) function and specify the friendly name of the DMO, the CLSID, and the category.</span></span> <span data-ttu-id="f58da-112">При необходимости можно также зарегистрировать набор типов мультимедиа, поддерживаемых дмос.</span><span class="sxs-lookup"><span data-stu-id="f58da-112">Optionally, you can also register a set of media types that your DMOs supports.</span></span> <span data-ttu-id="f58da-113">Дополнительные сведения см. в разделе [типы мультимедиа DMO](dmo-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="f58da-113">For more information, see [DMO Media Types](dmo-media-types.md).</span></span>

<span data-ttu-id="f58da-114">В следующем примере показано, как зарегистрировать DMO для звуковых эффектов, поддерживающих входные и выходные данные PCM.</span><span class="sxs-lookup"><span data-stu-id="f58da-114">The following example shows how to register an audio effect DMO that supports PCM audio input and output.</span></span> <span data-ttu-id="f58da-115">В этом случае типы входных и выходных данных одинаковы.</span><span class="sxs-lookup"><span data-stu-id="f58da-115">In this case the input types and output types are the same.</span></span>


```C++
STDAPI DllRegisterServer(void)
{
    // Register the DMO as a PCM audio effect DMO
    DMO_PARTIAL_MEDIATYPE mt;
    mt.type    = MEDIATYPE_Audio;
    mt.subtype = MEDIASUBTYPE_PCM;
    HRESULT hr = DMORegister(
        L"MyDMO",                  // Friendly name
        CLSID_MyDMO,               // CLSID
        DMOCATEGORY_AUDIO_EFFECT,  // Category
        0,                         // Flags 
        1,                         // Number of input types
        &mt,                       // Array of input types
        1,                         // Number of output types
        &mt);                      // Array of output types

    if (FAILED(hr)) return hr;

    // Registers the object, with no typelib.
    return _Module.RegisterServer(FALSE);
}
```



<span data-ttu-id="f58da-116">В этом примере предполагается, что для создания проекта использовалась библиотека ATL. Последняя строка функции вызывает стандартный метод ATL для регистрации сервера COM.</span><span class="sxs-lookup"><span data-stu-id="f58da-116">This example assumes that ATL was used to create the project; the last line of the function calls the standard ATL method to register the COM server.</span></span> <span data-ttu-id="f58da-117">Если вы не используете ATL, функция будет выглядеть иначе.</span><span class="sxs-lookup"><span data-stu-id="f58da-117">If you are not using ATL, your function will look different.</span></span>

<span data-ttu-id="f58da-118">**Отмена регистрации DMO**</span><span class="sxs-lookup"><span data-stu-id="f58da-118">**Unregistering a DMO**</span></span>

<span data-ttu-id="f58da-119">Функция **DllUnregisterServer** должна удалить все записи реестра, создаваемые функцией **DllRegisterServer** .</span><span class="sxs-lookup"><span data-stu-id="f58da-119">Your **DllUnregisterServer** function must remove any registry entries that the **DllRegisterServer** function creates.</span></span> <span data-ttu-id="f58da-120">При вызове **дморегистер** при регистрации DMO необходимо [**дмаунрегистер**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) с той же категорией при отмене регистрации DMO.</span><span class="sxs-lookup"><span data-stu-id="f58da-120">If you call **DMORegister** when you register the DMO, you must [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) with the same category when you unregister the DMO.</span></span>

<span data-ttu-id="f58da-121">В следующем примере удаляются записи реестра, созданные в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="f58da-121">The following example removes the registry entries created in the previous example:</span></span>


```C++
STDAPI DllUnregisterServer(void)
{
    DMOUnregister(CLSID_MyDMO, DMOCATEGORY_AUDIO_EFFECT);
    return _Module.UnregisterServer(TRUE);
}
```



<span data-ttu-id="f58da-122">**Значения для DirectShow**</span><span class="sxs-lookup"><span data-stu-id="f58da-122">**DirectShow Merit Values**</span></span>

<span data-ttu-id="f58da-123">В целях создания графов фильтров DirectShow присваивает дмос значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f58da-123">For purposes of building filter graphs, DirectShow assigns a default merit value to DMOs.</span></span> <span data-ttu-id="f58da-124">Это значение можно переопределить, добавив запись реестра в раздел реестра DMO в \_ \_ корневом CLSID классов hKey \\ .</span><span class="sxs-lookup"><span data-stu-id="f58da-124">You can override this value by adding a registry entry to the DMO's registry key in HKEY\_CLASSES\_ROOT\\CLSID.</span></span> <span data-ttu-id="f58da-125">Включите значение **DWORD** с именем `Merit` , значение которого указывает на неуспешный выбор.</span><span class="sxs-lookup"><span data-stu-id="f58da-125">Include a **DWORD** value named `Merit` whose value specifies the merit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f58da-126">См. также</span><span class="sxs-lookup"><span data-stu-id="f58da-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f58da-127">Написание DMO</span><span class="sxs-lookup"><span data-stu-id="f58da-127">Writing a DMO</span></span>](writing-a-dmo.md)
</dt> </dl>

 

 



