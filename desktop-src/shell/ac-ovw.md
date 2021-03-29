---
description: Автозаполнение расширяет строки, которые были частично введены в элемент управления "Правка", в строки целиком.
title: Использование автозаполнения
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b990395b-fc10-48f9-a718-7cc006e37eb7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fbbf0c53fc1b26002d1b46a9a6a6f67cd15e3ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984372"
---
# <a name="using-autocomplete"></a><span data-ttu-id="80a11-103">Использование автозаполнения</span><span class="sxs-lookup"><span data-stu-id="80a11-103">Using Autocomplete</span></span>

<span data-ttu-id="80a11-104">Автозаполнение расширяет строки, которые были частично введены в [элемент управления "Правка](/windows/desktop/Controls/edit-controls) ", в строки целиком.</span><span class="sxs-lookup"><span data-stu-id="80a11-104">Autocompletion expands strings that have been partially entered in an [edit control](/windows/desktop/Controls/edit-controls) into complete strings.</span></span> <span data-ttu-id="80a11-105">Например, когда пользователь начинает вводить URL-адрес в элемент управления «поле ввода адреса», внедренный в панель инструментов Windows Internet Explorer, автозаполнение расширяет строку на один или несколько полных параметров URL-адресов, которые соответствуют существующей частичной строке.</span><span class="sxs-lookup"><span data-stu-id="80a11-105">For example, when a user starts to enter a URL in the Address edit control that is embedded in the Windows Internet Explorer toolbar, autocompletion expands the string into one or more complete URL options that are consistent with the existing partial string.</span></span> <span data-ttu-id="80a11-106">Частичная строка URL-адреса, например "Mic", может быть расширена до " https://www.microsoft.com " или " https://www.microsoft.com/windows ".</span><span class="sxs-lookup"><span data-stu-id="80a11-106">A partial URL string such as "mic" might be expanded to "https://www.microsoft.com" or "https://www.microsoft.com/windows".</span></span> <span data-ttu-id="80a11-107">Автозаполнение обычно используется с элементами управления "поле ввода" или с элементами управления с внедренным элементом управления "поле ввода", например с элементом управления [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) .</span><span class="sxs-lookup"><span data-stu-id="80a11-107">Autocompletion is typically used with edit controls or with controls that have an embedded edit control, such as the [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) control.</span></span>

## <a name="adding-autocomplete-functionality-to-your-application"></a><span data-ttu-id="80a11-108">Добавление функции автозаполнения в приложение</span><span class="sxs-lookup"><span data-stu-id="80a11-108">Adding Autocomplete Functionality to Your Application</span></span>

<span data-ttu-id="80a11-109">Приложение может добавлять функции автозаполнения в элемент управления "Правка" двумя способами:</span><span class="sxs-lookup"><span data-stu-id="80a11-109">An application can add autocomplete functionality to an edit control in two ways:</span></span>

-   <span data-ttu-id="80a11-110">[**Шаутокомплете**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) — это простая функция, которая может Автозаполнение пути к файлу или URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="80a11-110">[**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) is a simple function that can autocomplete a file path or URL.</span></span>
-   <span data-ttu-id="80a11-111">Интерфейс [**иаутокомплете**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) предоставляется объектом автозаполнения ( \_ Автозаполнение CLSID).</span><span class="sxs-lookup"><span data-stu-id="80a11-111">[**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) interface is exposed by the autocomplete object (CLSID\_AutoComplete).</span></span> <span data-ttu-id="80a11-112">Это позволяет приложениям инициализировать, включать и отключать объект.</span><span class="sxs-lookup"><span data-stu-id="80a11-112">It allows applications to initialize, enable, and disable the object.</span></span> <span data-ttu-id="80a11-113">**Иаутокомплете** обеспечивает больший контроль над источниками автозаполнения, включая возможность добавления пользовательского источника.</span><span class="sxs-lookup"><span data-stu-id="80a11-113">**IAutoComplete** allows more control over autocomplete sources, including the ability to add a custom source.</span></span> <span data-ttu-id="80a11-114">Оставшаяся часть этого раздела посвящена использованию **иаутокомплете**.</span><span class="sxs-lookup"><span data-stu-id="80a11-114">The remainder of this topic discusses the use of **IAutoComplete**.</span></span> <span data-ttu-id="80a11-115">См. статью [как включить Автозаполнение вручную](how-to-enable-autocomplete-manually.md) для конкретных примеров использования.</span><span class="sxs-lookup"><span data-stu-id="80a11-115">See [How To Enable Autocomplete Manually](how-to-enable-autocomplete-manually.md) for specific usage examples.</span></span>

## <a name="autocomplete-modes"></a><span data-ttu-id="80a11-116">Режимы автозаполнения</span><span class="sxs-lookup"><span data-stu-id="80a11-116">Autocomplete Modes</span></span>

<span data-ttu-id="80a11-117">При использовании [**иаутокомплете**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete)автозавершение может отображать завершенную строку в двух режимах: автоматическое добавление и Автозаполнение.</span><span class="sxs-lookup"><span data-stu-id="80a11-117">When using [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete), autocompletion can display the completed string in two modes: autoappend and autosuggest.</span></span> <span data-ttu-id="80a11-118">Режимы независимы; можно включить один или оба варианта.</span><span class="sxs-lookup"><span data-stu-id="80a11-118">The modes are independent; you can enable either or both.</span></span> <span data-ttu-id="80a11-119">Чтобы указать режим, вызовите метод [**IAutoComplete2:: сетоптионс**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions).</span><span class="sxs-lookup"><span data-stu-id="80a11-119">To specify the mode, call [**IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions).</span></span>

<dl> <dt>

<span data-ttu-id="80a11-120"><span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Автодобавление</span><span class="sxs-lookup"><span data-stu-id="80a11-120"><span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Autoappend</span></span>
</dt> <dd>

<span data-ttu-id="80a11-121">В режиме автодобавления, автозаполнение добавляет оставшуюся часть наиболее вероятной строки кандидатов к существующим символам, выделяя добавленные символы.</span><span class="sxs-lookup"><span data-stu-id="80a11-121">In autoappend mode, autocompletion appends the remainder of the most likely candidate string to the existing characters, highlighting the appended characters.</span></span> <span data-ttu-id="80a11-122">Если пользователь продолжит вводить символы, они будут добавлены в существующую частичную строку.</span><span class="sxs-lookup"><span data-stu-id="80a11-122">If the user continues to enter characters, they are added to the existing partial string.</span></span> <span data-ttu-id="80a11-123">Если пользователь добавляет символ, идентичный следующему выделенному символу, выделение для этого символа будет отключено.</span><span class="sxs-lookup"><span data-stu-id="80a11-123">If the user adds a character that is identical to the next highlighted character, the highlighting for that character is turned off.</span></span> <span data-ttu-id="80a11-124">Остальные символы по-прежнему будут выделены.</span><span class="sxs-lookup"><span data-stu-id="80a11-124">The remaining characters will still be highlighted.</span></span> <span data-ttu-id="80a11-125">Если пользователь добавляет символ, который не соответствует следующему выделенному символу, автозавершение пытается создать новую строку-кандидат на основе большей частичной строки и добавляет оставшуюся часть новой строки-кандидата в текущую частичную строку.</span><span class="sxs-lookup"><span data-stu-id="80a11-125">If the user adds a character that does not match the next highlighted character, autocompletion attempts to generate a new candidate string based on the larger partial string and appends the remainder of the new candidate string to the current partial string.</span></span> <span data-ttu-id="80a11-126">Если не удается найти потенциальную строку, отображаются только введенные символы, а поле редактирования ведет себя без автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="80a11-126">If no candidate string can be found, only the typed characters appear and the edit box behaves as it would without autocompletion.</span></span> <span data-ttu-id="80a11-127">Этот процесс продолжится, пока пользователь не примет строку.</span><span class="sxs-lookup"><span data-stu-id="80a11-127">This process continues until the user accepts a string.</span></span>

</dd> <dt>

<span data-ttu-id="80a11-128"><span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>Автозаполнения</span><span class="sxs-lookup"><span data-stu-id="80a11-128"><span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>Autosuggest</span></span>
</dt> <dd>

<span data-ttu-id="80a11-129">В режиме автозаполнения в автозаполнении отображается раскрывающийся список с одной или несколькими предложенными полными строками под элементом управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="80a11-129">In autosuggest mode, autocompletion displays a drop-down list, with one or more suggested complete strings, beneath the edit control.</span></span> <span data-ttu-id="80a11-130">Пользователь может выбрать одну из предлагаемых строк или продолжить ввод.</span><span class="sxs-lookup"><span data-stu-id="80a11-130">The user can select one of the suggested strings or continue typing.</span></span> <span data-ttu-id="80a11-131">По мере ввода текста раскрывающийся список может быть изменен на основе текущей частичной строки.</span><span class="sxs-lookup"><span data-stu-id="80a11-131">As typing progresses, the drop-down list might be modified based on the current partial string.</span></span> <span data-ttu-id="80a11-132">Если установить \_ флаг поиска ACO в [**IAutoComplete2:: сетоптионс**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions), функция автозаполнения предоставляет параметр в нижней части раскрывающегося списка для поиска текущей частичной строки.</span><span class="sxs-lookup"><span data-stu-id="80a11-132">If you set the ACO\_SEARCH flag in [**IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions), autocomplete provides an option, at the bottom of the drop-down list, to search for the current partial string.</span></span> <span data-ttu-id="80a11-133">Этот параметр отображается, даже если нет предлагаемых строк.</span><span class="sxs-lookup"><span data-stu-id="80a11-133">This option is displayed even if there are no suggested strings.</span></span> <span data-ttu-id="80a11-134">Если пользователь выбирает вариант поиска, приложение должно запустить поисковую систему, чтобы помочь пользователю.</span><span class="sxs-lookup"><span data-stu-id="80a11-134">If the user selects the search option, your application should launch a search engine to assist the user.</span></span>

</dd> </dl>

## <a name="using-predefined-autocomplete-sources"></a><span data-ttu-id="80a11-135">Использование предопределенных источников автозаполнения</span><span class="sxs-lookup"><span data-stu-id="80a11-135">Using Predefined Autocomplete Sources</span></span>

<span data-ttu-id="80a11-136">Автозаполнение зависит от наличия источника, который предоставляет строки для сопоставления с частичной строкой пользователя.</span><span class="sxs-lookup"><span data-stu-id="80a11-136">Autocompletion depends on having a source that provides it with strings to match against the user's partial string.</span></span> <span data-ttu-id="80a11-137">Существует возможность предоставления пользовательского источника автозаполнения, но некоторые из наиболее распространенных источников предоставляются системой.</span><span class="sxs-lookup"><span data-stu-id="80a11-137">You have the option of providing a custom autocomplete source, but several of the most common sources are provided by the system.</span></span>

<dl> <dt>

<span data-ttu-id="80a11-138"><span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>\_АКЛХИСТОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="80a11-138"><span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>CLSID\_ACLHistory</span></span>
</dt> <dd>

<span data-ttu-id="80a11-139">Источник автозаполнения, соответствующий списку URL-адресов в списке журнала пользователя.</span><span class="sxs-lookup"><span data-stu-id="80a11-139">An autocomplete source that matches against the URL list in the user's History list.</span></span>

</dd> <dt>

<span data-ttu-id="80a11-140"><span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>\_АКЛМРУ CLSID</span><span class="sxs-lookup"><span data-stu-id="80a11-140"><span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>CLSID\_ACLMRU</span></span>
</dt> <dd>

<span data-ttu-id="80a11-141">Источник автозаполнения, соответствующий списку URL-адресов в списке недавно использовавшихся пользователей.</span><span class="sxs-lookup"><span data-stu-id="80a11-141">An autocomplete source that matches against the URL list in the user's Recently Used list.</span></span>

</dd> <dt>

<span data-ttu-id="80a11-142"><span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>\_АКЛИСТИСФ CLSID</span><span class="sxs-lookup"><span data-stu-id="80a11-142"><span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>CLSID\_ACListISF</span></span>
</dt> <dd>

<span data-ttu-id="80a11-143">Источник автозаполнения, который соответствует элементам в пространстве имен оболочки: файлы на компьютере пользователя, а также элементы в виртуальных папках, таких как панель управления.</span><span class="sxs-lookup"><span data-stu-id="80a11-143">An autocomplete source that matches against items in the Shell namespace: files on the user's computer as well as items in virtual folders such as Control Panel.</span></span>

</dd> </dl>

<span data-ttu-id="80a11-144">Бывают случаи, когда, вместо немедленного освобождения ресурсов, может потребоваться хранить указатели интерфейса для различных объектов, участвующих в автозаполнении.</span><span class="sxs-lookup"><span data-stu-id="80a11-144">There are occasions when, rather than immediately freeing the resources, you might want to retain the interface pointers to the various objects involved in autocomplete.</span></span> <span data-ttu-id="80a11-145">В частности, это делается, когда необходимо динамически настроить поведение автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="80a11-145">In particular, this is done when you want to adjust the autocomplete behavior dynamically.</span></span> <span data-ttu-id="80a11-146">Чаще всего это происходит при использовании \_ объекта CLSID аклистисф, который выполняет Автозаполнение из пространства имен оболочки и имеет параметр ([**Акло \_ куррентдир**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) перечисления из текущего каталога.</span><span class="sxs-lookup"><span data-stu-id="80a11-146">The most common instance of this occurs when using the CLSID\_ACListISF object, which autocompletes from the Shell namespace and has the option ([**ACLO\_CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) of enumerating from the current directory as well.</span></span> <span data-ttu-id="80a11-147">Например, при переходе к новой папке Internet Explorer изменяет текущий каталог адресной строки, поэтому параметры необходимо динамически изменить.</span><span class="sxs-lookup"><span data-stu-id="80a11-147">For example, when you navigate to a new folder, Internet Explorer changes the Address bar's current directory and therefore the settings need to be changed dynamically.</span></span> <span data-ttu-id="80a11-148">Существует два способа указать каталог, который \_ объект CLSID аклистисф должен рассматривать как текущий каталог:</span><span class="sxs-lookup"><span data-stu-id="80a11-148">There are two ways to specify the directory that the CLSID\_ACListISF object should treat as the current directory:</span></span>

-   <span data-ttu-id="80a11-149">[**Иперсистфолдер**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) указывает каталог через [**итемидлист**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist).</span><span class="sxs-lookup"><span data-stu-id="80a11-149">[**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) specifies the directory through an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist).</span></span>
-   <span data-ttu-id="80a11-150">[**Икуррентворкингдиректори**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) указывает каталог по строке пути.</span><span class="sxs-lookup"><span data-stu-id="80a11-150">[**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) specifies the directory through a path string.</span></span>

<span data-ttu-id="80a11-151">В следующем примере предполагается, что **PAL** является указателем на интерфейс [**ИАКЛИСТ**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) \_ объекта аклистисф CLSID:</span><span class="sxs-lookup"><span data-stu-id="80a11-151">In the following, assume that **pal** is a pointer to the [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) interface of a CLSID\_ACListISF object:</span></span>

-   <span data-ttu-id="80a11-152">Использование [**иперсистфолдер**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder):</span><span class="sxs-lookup"><span data-stu-id="80a11-152">Using [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder):</span></span>

    <span data-ttu-id="80a11-153">Чтобы сообщить объекту CLSID \_ аклистисф, что определенный [**итемидлист**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) должен рассматриваться как текущий каталог, можно использовать интерфейс [**иперсистфолдер**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) объекта.</span><span class="sxs-lookup"><span data-stu-id="80a11-153">To tell the CLSID\_ACListISF object that a particular [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) should be treated as the current directory, you can use the object's [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) interface.</span></span> <span data-ttu-id="80a11-154">Так как **итемидлист** может ссылаться на виртуальную папку, этот метод является более гибким, чем использование [**икуррентворкингдиректори**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).</span><span class="sxs-lookup"><span data-stu-id="80a11-154">Since an **ITEMIDLIST** can refer to a virtual folder, this method is more flexible than using [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).</span></span>

    <span data-ttu-id="80a11-155">Обратите внимание, что в следующих примерах используется преобразованный QueryInterface, позволяющий упростить список параметров.</span><span class="sxs-lookup"><span data-stu-id="80a11-155">Note that the following examples use the templatized QueryInterface, which allows for a simplified parameter list.</span></span>

    ```C++
    IPersistFolder *ppf;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&ppf));   
    if (SUCCEEDED(hr))
    {
        hr = ppf->Initialize(pidlCurrentDirectory);
        ppf->Release();
    }
    ```

    

-   <span data-ttu-id="80a11-156">Использование [**икуррентворкингдиректори**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):</span><span class="sxs-lookup"><span data-stu-id="80a11-156">Using [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):</span></span>

    <span data-ttu-id="80a11-157">Чтобы предоставить объекту CLSID \_ аклистисф путь в качестве текущего каталога, можно использовать интерфейс [**икуррентворкингдиректори**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) объекта.</span><span class="sxs-lookup"><span data-stu-id="80a11-157">To give the CLSID\_ACListISF object a path as the current directory, you can use the object's [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) interface.</span></span>

    ```C++
    WCHAR pwszDirectory[MAX_PATH] = L"C:\\Program Files";
    ICurrentWorkingDirectory *pcwd;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&pcwd));    
    if (SUCCEEDED(hr))
    {
        hr = pcwd->SetDirectory(pwszDirectory);
        pcwd->Release();
    }
    ```

    

 

 
