---
description: Чтобы получить более подробный контроль над поведением автозаполнения или добавить пользовательский источник строк автозаполнения, необходимо самостоятельно управлять объектом автозаполнения.
ms.assetid: E1A7B1B0-2879-452E-9EBB-73F02B932200
title: Включение автозаполнения вручную
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee4b327c6ccdd62fd921c56cfb046edb8527bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985445"
---
# <a name="how-to-enable-autocomplete-manually"></a><span data-ttu-id="fc5a8-103">Включение автозаполнения вручную</span><span class="sxs-lookup"><span data-stu-id="fc5a8-103">How to Enable Autocomplete Manually</span></span>

<span data-ttu-id="fc5a8-104">Чтобы получить более подробный контроль над поведением автозаполнения или добавить пользовательский источник строк автозаполнения, необходимо самостоятельно управлять объектом автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-104">To gain more detailed control over the autocomplete behavior, or to add a custom source of autocomplete strings, you must manage the autocomplete object yourself.</span></span> <span data-ttu-id="fc5a8-105">Автозаполнение можно включить вручную следующими способами.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-105">You can enable autocomplete manually in the following ways.</span></span>

## <a name="instructions"></a><span data-ttu-id="fc5a8-106">Инструкции</span><span class="sxs-lookup"><span data-stu-id="fc5a8-106">Instructions</span></span>

### <a name="creating-a-simple-autocomplete-object"></a><span data-ttu-id="fc5a8-107">Создание простого автозаполнения объекта</span><span class="sxs-lookup"><span data-stu-id="fc5a8-107">Creating a Simple Autocomplete Object</span></span>

<span data-ttu-id="fc5a8-108">В следующих шагах показано, как создать и инициализировать простой объект автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-108">The following steps show how to create and initialize a simple autocomplete object.</span></span> <span data-ttu-id="fc5a8-109">Простой объект автозаполнения завершает строки из одного источника.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-109">A simple autocomplete object completes strings from a single source.</span></span> <span data-ttu-id="fc5a8-110">В этом примере была намеренно опущена проверка ошибок.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-110">Error checking has been intentionally omitted in this example.</span></span>

1.  <span data-ttu-id="fc5a8-111">Создайте объект автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-111">Create the autocomplete object.</span></span>

    ```C++
    IAutoComplete *pac;

    HRESULT hr = CoCreateInstance(CLSID_AutoComplete, 
                                    NULL, 
                                  CLSCTX_INPROC_SERVER,
                                  IID_PPV_ARGS(&pac));
    ```

    

2.  <span data-ttu-id="fc5a8-112">Создайте источник автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-112">Create the autocomplete source.</span></span> <span data-ttu-id="fc5a8-113">Можно использовать [предопределенный источник автозаполнения](ac-ovw.md) или написать собственный пользовательский источник.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-113">You can use a [predefined autocomplete source](ac-ovw.md) or you can write your own custom source.</span></span>

    <span data-ttu-id="fc5a8-114">В следующем коде используется один из стандартных источников автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-114">The following code uses one of the predefined autocomplete sources.</span></span>

    ```C++
    IUnknown *punkSource;

    hr = CoCreateInstance(CLSID_ACListISF, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&punkSource));
    ```

    

    <span data-ttu-id="fc5a8-115">В следующем коде используется источник настраиваемого автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-115">The following code uses a custom autocomplete source.</span></span> <span data-ttu-id="fc5a8-116">Вы можете написать собственный источник автозаполнения, реализовав объект, который предоставляет интерфейс [**иенумстринг**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) .</span><span class="sxs-lookup"><span data-stu-id="fc5a8-116">You can write your own autocomplete source by implementing an object that exposes the [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) interface.</span></span> <span data-ttu-id="fc5a8-117">Объект также может дополнительно реализовать интерфейсы [**иаклист**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) и [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) .</span><span class="sxs-lookup"><span data-stu-id="fc5a8-117">The object can also optionally implement the [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) and [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) interfaces.</span></span>

    ```C++
    CCustomAutoCompleteSource *pcacs = new CCustomAutoCompleteSource();

    hr = pcacs->QueryInterface(IID_PPV_ARGS(&punkSource));
    if(SUCCEEDED(hr))
    {
        // ...
    }

    pcacs->Release();
    ```

    

3.  <span data-ttu-id="fc5a8-118">Задайте параметры источника автозаполнения (необязательно).</span><span class="sxs-lookup"><span data-stu-id="fc5a8-118">Set the options on the autocomplete source (optional).</span></span>

    <span data-ttu-id="fc5a8-119">Поведение источника автозаполнения можно настроить, задав его параметры, если источник предоставляет интерфейс [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) .</span><span class="sxs-lookup"><span data-stu-id="fc5a8-119">You can customize the behavior of the autocomplete source by setting its options if the source exposes the [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) interface.</span></span> <span data-ttu-id="fc5a8-120">При использовании предопределенных источников автозаполнения только CLSID \_ аклистисф экспортирует **IACList2**.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-120">When using the predefined autocomplete sources, only CLSID\_ACListISF exports **IACList2**.</span></span> <span data-ttu-id="fc5a8-121">Полный список параметров и их значений см. в разделе [**IACList2:: сетоптионс**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span><span class="sxs-lookup"><span data-stu-id="fc5a8-121">For a complete list of options and their values, see [**IACList2::SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span></span>

    ```C++
    IACList2 *pal2;

    hr = punkSource->QueryInterface(IID_PPV_ARGS(&pal2));
    if (SUCCEEDED(hr))
    {
        hr = pal2->SetOptions(ACLO_FILESYSONLY);
        pal2->Release();
    }
    ```

    

4.  <span data-ttu-id="fc5a8-122">Инициализируйте объект автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-122">Initialize the autocomplete object.</span></span>

    <span data-ttu-id="fc5a8-123">В этом примере **хвндедит** является маркером окна редактирования элемента управления, для которого необходимо включить Автозаполнение.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-123">In this example, **hwndEdit** is the handle of the edit control window for which autocomplete is to be enabled.</span></span> <span data-ttu-id="fc5a8-124">Описание последних двух неиспользуемых параметров см. в разделе [**иаутокомплете:: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) .</span><span class="sxs-lookup"><span data-stu-id="fc5a8-124">See [**IAutoComplete::Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) for a description of the final two unused parameters.</span></span>

    ```C++
    hr = pac->Init(hwndEdit, punkSource, NULL, NULL);
    ```

    

5.  <span data-ttu-id="fc5a8-125">Задайте параметры объекта автозаполнения (необязательно).</span><span class="sxs-lookup"><span data-stu-id="fc5a8-125">Set the options of the autocomplete object (optional).</span></span>

    <span data-ttu-id="fc5a8-126">Поведение объекта автозаполнения можно настроить, задав его параметры.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-126">You can customize the behavior of the autocomplete object by setting its options.</span></span> <span data-ttu-id="fc5a8-127">Полный список параметров и их значений см. в документации по [**IACList2:: сетоптионс**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span><span class="sxs-lookup"><span data-stu-id="fc5a8-127">For a complete list of options and their values, see the documentation for [**IACList2::SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span></span>

    ```C++
    IAutoComplete2 *pac2;

    hr = pac->QueryInterface(IID_PPV_ARGS(&pac2));

    if (SUCCEEDED(hr))
    {
        hr = pac2->SetOptions(ACO_AUTOSUGGEST);
        pac2->Release();
    }
    ```

    

6.  <span data-ttu-id="fc5a8-128">Освободите объекты.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-128">Release the objects.</span></span>

    > [!Note]  
    > <span data-ttu-id="fc5a8-129">Объект автозаполнения остается прикрепленным к элементу управления "поле ввода" даже после его освобождения.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-129">The autocomplete object remains attached to the edit control even after you release it.</span></span> <span data-ttu-id="fc5a8-130">Если вам нужно получить доступ к этим объектам позднее — если вы хотите изменить параметры автозаполнения позже, например, не требуется освобождать их на этом этапе.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-130">If you foresee a need to access these objects later—if you want to change the autocomplete options at a later time, for example—it is not required that you release them at this point.</span></span>

     

    ```C++
    punkSource->Release();
    pac->Release();
    ```

    

### <a name="creating-a-compound-autocomplete-object"></a><span data-ttu-id="fc5a8-131">Создание составного объекта автозаполнения</span><span class="sxs-lookup"><span data-stu-id="fc5a8-131">Creating a Compound Autocomplete Object</span></span>

<span data-ttu-id="fc5a8-132">Составной объект автозаполнения соответствует строкам из нескольких источников.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-132">A compound autocomplete object matches against strings from multiple sources.</span></span> <span data-ttu-id="fc5a8-133">Например, в адресной строке Windows Internet Explorer используется составной объект автозаполнения, так как пользователь может начать вводить имя файла или URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-133">For example, the Windows Internet Explorer Address bar uses a compound autocomplete object because the user might begin typing the name of a file or a URL.</span></span> <span data-ttu-id="fc5a8-134">Большинство действий, связанных с созданием составного объекта автозаполнения, аналогичны шагам в разделе "Создание простого автозаполнения объекта".</span><span class="sxs-lookup"><span data-stu-id="fc5a8-134">Most of the steps involved in creating a compound autocomplete object are identical to the steps in "Creating a Simple Autocomplete Object."</span></span> <span data-ttu-id="fc5a8-135">Эти действия обозначены как таковые.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-135">Those steps are indicated as such.</span></span>

1.  <span data-ttu-id="fc5a8-136">Создайте объект автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-136">Create the autocomplete object.</span></span> <span data-ttu-id="fc5a8-137">Это аналогично шагу 1 выше.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-137">This is the same as step 1 above.</span></span>

2.  <span data-ttu-id="fc5a8-138">Создайте диспетчер объектов составного источника автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-138">Create the autocomplete compound source object manager.</span></span>

    <span data-ttu-id="fc5a8-139">Объект составного источника автозаполнения позволяет объединять несколько источников автозаполнения в один источник автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-139">The autocomplete compound source object allows multiple autocomplete sources to be combined into a single autocomplete source.</span></span>

    ```C++
    IObjMgr *pom;

    hr = CoCreateInstance(CLSID_ACLMulti, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pom));
    ```

    

3.  <span data-ttu-id="fc5a8-140">Создание и Настройка параметров для каждого источника автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-140">Create and set options for each of the autocomplete sources.</span></span> <span data-ttu-id="fc5a8-141">Повторите шаги 2 и 3 для каждого источника.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-141">Repeat steps 2 and 3 above for each source.</span></span>

4.  <span data-ttu-id="fc5a8-142">Присоедините каждый источник автозаполнения к диспетчеру исходных объектов.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-142">Attach each autocomplete source to the source object manager.</span></span>

    ```C++
    hr = pom->Append(punkSource1);
    hr = pom->Append(punkSource2);
    ```

    

5.  <span data-ttu-id="fc5a8-143">Инициализируйте объект автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-143">Initialize the autocomplete object.</span></span>

    <span data-ttu-id="fc5a8-144">Это аналогично шагу 4 выше, за исключением того, что вместо передачи простого источника автозаполнения в [**иаутокомплете:: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init)передается диспетчер объектов составного источника.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-144">This is the same as step 4 above, except that instead of passing the simple autocomplete source to [**IAutoComplete::Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init), you pass the compound source object manager.</span></span>

    ```C++
    hr = pac->Init(hwndEdit, pom, NULL, NULL);
    ```

    

6.  <span data-ttu-id="fc5a8-145">Задайте параметры объекта автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-145">Set the options of the autocomplete object.</span></span> <span data-ttu-id="fc5a8-146">Это аналогично шагу 5 выше.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-146">This is the same as step 5 above.</span></span>

7.  <span data-ttu-id="fc5a8-147">Освободите объекты.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-147">Release the objects.</span></span>

    <span data-ttu-id="fc5a8-148">Как и в случае с простым вариантом, объекты можно освободить сразу после их использования, но можно также изменить параметры позже.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-148">As in the simple case, you can release the objects as soon as you are finished using them, but you can also retain them to change options later.</span></span>

    ```C++
    pac->Release();
    pom->Release();

    // Release each individual source.
    punkSource1->Release(); 
    punkSource2->Release();
    ```

    

 

 
