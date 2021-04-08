---
description: Для пользователей по всему миру текстовые входные данные являются частью современных вычислительных систем, ведения блогов, комментирования, твитов, обмена мгновенными сообщениями и других типов текста. В Windows 8 Проверка орфографии встроена в элементы управления для редактирования.
ms.assetid: ED569D4F-568B-4381-91C3-8EAEDA4DD47C
title: Об API проверки орфографии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0d356823e665781052e2a2d5ea98b358155038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910992"
---
# <a name="about-the-spell-checking-api"></a><span data-ttu-id="ac550-104">Об API проверки орфографии</span><span class="sxs-lookup"><span data-stu-id="ac550-104">About the Spell Checking API</span></span>

<span data-ttu-id="ac550-105">Для пользователей по всему миру текстовые входные данные являются частью современных вычислительных систем, ведения блогов, комментирования, твитов, обмена мгновенными сообщениями и других типов текста.</span><span class="sxs-lookup"><span data-stu-id="ac550-105">For users worldwide, textual input is part of a modern computing experience, for blogging, commenting, tweeting, instant messaging, or any other kind of text typing.</span></span> <span data-ttu-id="ac550-106">В Windows 8 Проверка орфографии встроена в элементы управления для редактирования.</span><span class="sxs-lookup"><span data-stu-id="ac550-106">In Windows 8, spell checking is built-in to edit controls.</span></span>

<span data-ttu-id="ac550-107">Разработчики могут использовать API проверки орфографии в своих приложениях для использования доступных служб проверки орфографии.</span><span class="sxs-lookup"><span data-stu-id="ac550-107">Developers can use the spell checking API in their apps to consume available spell checking services.</span></span> <span data-ttu-id="ac550-108">Разработчики также могут создавать средства проверки орфографии, которые становятся поставщиками и интегрированы в платформу проверки орфографии Windows.</span><span class="sxs-lookup"><span data-stu-id="ac550-108">Developers can also create spell checkers that become providers and are integrated into the Windows spell checking framework.</span></span>

<span data-ttu-id="ac550-109">API проверки орфографии предназначен для использования профессиональными разработчиками C/C++ приложений COM.</span><span class="sxs-lookup"><span data-stu-id="ac550-109">The Spell Checking API is designed for use by professional C/C++ developers of Windows Component Object Model (COM) apps.</span></span> <span data-ttu-id="ac550-110">API проверки орфографии не поддерживается для использования в службе Windows или ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="ac550-110">The Spell Checking API is not supported for use in a Windows or ASP.NET service.</span></span>

## <a name="versioning"></a><span data-ttu-id="ac550-111">Управление версиями</span><span class="sxs-lookup"><span data-stu-id="ac550-111">Versioning</span></span>

<span data-ttu-id="ac550-112">API проверки орфографии доступен, начиная с Windows 8 или Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ac550-112">The Spell Checking API is available beginning with the Windows 8 or Windows Server 2012.</span></span> <span data-ttu-id="ac550-113">Будущие дополнения к API будут обрабатываться путем создания новых интерфейсов, которые можно определить с помощью [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на существующих.</span><span class="sxs-lookup"><span data-stu-id="ac550-113">Future additions to the API will be handled by creating new interfaces that can be determined using [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the existing ones.</span></span>

## <a name="interfaces"></a><span data-ttu-id="ac550-114">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="ac550-114">Interfaces</span></span>

<span data-ttu-id="ac550-115">Все интерфейсы должны быть освобождены, если они больше не используются.</span><span class="sxs-lookup"><span data-stu-id="ac550-115">All interfaces must be released when they are no longer used.</span></span> <span data-ttu-id="ac550-116">Все возвращаемые (выходные параметры) **LPWSTR** строки (и элементы **лполестр** из [**иенумстринг**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) должны быть освобождены с помощью [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) , если они больше не используются.</span><span class="sxs-lookup"><span data-stu-id="ac550-116">All returned (out parameter) **LPWSTR** strings (and **LPOLESTR** items from [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) must be released with [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) when no longer used.</span></span>

## <a name="error-handling"></a><span data-ttu-id="ac550-117">Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="ac550-117">Error handling</span></span>

<span data-ttu-id="ac550-118">Ошибки возвращаются как **HRESULT** s.</span><span class="sxs-lookup"><span data-stu-id="ac550-118">Errors are returned as **HRESULT** s.</span></span> <span data-ttu-id="ac550-119">ИНТЕРФЕЙСЫ [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) и [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) не поддерживаются в этом API.</span><span class="sxs-lookup"><span data-stu-id="ac550-119">[**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) and [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) are not supported in this API.</span></span> <span data-ttu-id="ac550-120">Ошибки не являются особенно выполняемыми, за исключением неверных аргументов.</span><span class="sxs-lookup"><span data-stu-id="ac550-120">Errors are not particularly actionable except for incorrect arguments.</span></span>

<span data-ttu-id="ac550-121">Коды стандартных ошибок RPC могут возвращаться любыми вызовами API, так как они находятся вне процедуры.</span><span class="sxs-lookup"><span data-stu-id="ac550-121">Standard RPC error codes may be returned by any of the API calls because they are out-of-proc.</span></span> <span data-ttu-id="ac550-122">Применяются стандартные времена ожидания RPC.</span><span class="sxs-lookup"><span data-stu-id="ac550-122">Standard RPC timeouts apply.</span></span>

## <a name="security"></a><span data-ttu-id="ac550-123">Безопасность</span><span class="sxs-lookup"><span data-stu-id="ac550-123">Security</span></span>

<span data-ttu-id="ac550-124">API проверки орфографии может загрузить внешний код (поставщики проверки орфографии).</span><span class="sxs-lookup"><span data-stu-id="ac550-124">The Spell Checking API may load external code (spell check providers).</span></span> <span data-ttu-id="ac550-125">Он будет выполнять этот код вне процесса и в ограниченном контексте безопасности.</span><span class="sxs-lookup"><span data-stu-id="ac550-125">It will run this code out-of-proc and under a restricted security context.</span></span>

## <a name="dictionary-files"></a><span data-ttu-id="ac550-126">Файлы словарей</span><span class="sxs-lookup"><span data-stu-id="ac550-126">Dictionary files</span></span>

<span data-ttu-id="ac550-127">Пользовательские словари для языка, содержащие содержимое для списков добавленных, исключаемых и автослов, находятся в папке% AppData% \\ \\ правописания Майкрософт \\ *<language tag>* .</span><span class="sxs-lookup"><span data-stu-id="ac550-127">The user-specific dictionaries for a language, which hold the content for the Added, Excluded, and AutoCorrect word lists, are located under %AppData%\\Microsoft\\Spelling\\*<language tag>*.</span></span> <span data-ttu-id="ac550-128">Имена файлов: Default. dic (добавлен), Default. исключенного (исключено) и Default. ACL (Автозамена).</span><span class="sxs-lookup"><span data-stu-id="ac550-128">The filenames are default.dic (Added), default.exc (Excluded) and default.acl (AutoCorrect).</span></span> <span data-ttu-id="ac550-129">Файлы имеют формат открытого текста UTF-16 LE, который должен начинаться с соответствующей метки порядка байтов (BOM).</span><span class="sxs-lookup"><span data-stu-id="ac550-129">The files are UTF-16 LE plaintext that must start with the appropriate Byte Order Mark (BOM).</span></span> <span data-ttu-id="ac550-130">Каждая строка содержит слово (в списках добавленных и исключенных слов) или пару автозамены с словами, разделенными вертикальной чертой (" \| ") (в списке автозамены).</span><span class="sxs-lookup"><span data-stu-id="ac550-130">Each line contains a word (in the Added and Excluded word lists), or an autocorrect pair with the words separated by a vertical bar ("\|") (in the AutoCorrect word list).</span></span> <span data-ttu-id="ac550-131">Другие файлы. dic,. исключенного и. ACL, находящиеся в каталоге, будут обнаружены службой проверки орфографии и добавлены в списки пользовательских слов.</span><span class="sxs-lookup"><span data-stu-id="ac550-131">Other .dic, .exc, and .acl files present in the directory will be detected by the spell checking service and added to the user word lists.</span></span> <span data-ttu-id="ac550-132">Эти файлы считаются доступны только для чтения и не изменяются с помощью API проверки орфографии.</span><span class="sxs-lookup"><span data-stu-id="ac550-132">These files are considered to be read-only and are not modified by the spell checking API.</span></span>

## <a name="installing-a-spell-checking-provider"></a><span data-ttu-id="ac550-133">Установка поставщика проверки орфографии</span><span class="sxs-lookup"><span data-stu-id="ac550-133">Installing a spell checking provider</span></span>

<span data-ttu-id="ac550-134">При установке поставщика проверки орфографии все файлы, которые он использует, должны размещаться в расположении, допускающем доступ на чтение из идентификатора SID ([идентификатора безопасности](../secauthz/security-identifiers.md)) "все пакеты приложений".</span><span class="sxs-lookup"><span data-stu-id="ac550-134">The installation of a spell checking provider must place all the files it uses in a location that allows read access from the SID ([security identifier](../secauthz/security-identifiers.md)) "ALL APPLICATION PACKAGES".</span></span> <span data-ttu-id="ac550-135">Установка этой папки в папке "Program Files" работает правильно.</span><span class="sxs-lookup"><span data-stu-id="ac550-135">Installing it in a folder under "Program Files" works well.</span></span> <span data-ttu-id="ac550-136">Кроме того, поставщик должен задать некоторые ключи в реестре, чтобы он отображался в API проверки орфографии.</span><span class="sxs-lookup"><span data-stu-id="ac550-136">Also, the provider must set some keys in the registry for it to appear to the spell checking API.</span></span> <span data-ttu-id="ac550-137">В \_ \_ \_ \_ зависимости от того, должен ли он быть установлен только для текущего пользователя или для всех пользователей, он может находиться в кусте hKey «текущий пользователь куст» или на локальном компьютере hKey.</span><span class="sxs-lookup"><span data-stu-id="ac550-137">It can be in either the HKEY\_CURRENT\_USER hive or the HKEY\_LOCAL\_MACHINE hive depending on whether it should install only for the current user or all users.</span></span>


```
Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>
     Default (REG_SZ) = <Name of the provider>

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\InprocServer32
     ThreadingModel (REG_SZ) = "Both"

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\Version
     Version (REG_SZ) = <Version>

Key: <Registry hive>\SOFTWARE\Microsoft\Spelling\Spellers\<Provider id string>
     CLSID (REG_SZ) = <CLSID of the COM Server that implements the provider>
```



<span data-ttu-id="ac550-138">[Образец поставщика проверки орфографии](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) содержит пример регистрации, необходимый для установки поставщика.</span><span class="sxs-lookup"><span data-stu-id="ac550-138">The [spell checking provider sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) provides an example of the registration needed to install a provider.</span></span>

<span data-ttu-id="ac550-139">Если вы создаете новые параметры проверки орфографии для поставщика проверки орфографии, см. инструкции по именованию в разделе [**иоптиондескриптион:: ID**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) .</span><span class="sxs-lookup"><span data-stu-id="ac550-139">If you are creating new spell checking options for a spell checking provider, see [**IOptionDescription::Id**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) for guidance on naming.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac550-140">См. также</span><span class="sxs-lookup"><span data-stu-id="ac550-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac550-141">Справочник по API проверки орфографии</span><span class="sxs-lookup"><span data-stu-id="ac550-141">Spell Checking API Reference</span></span>](spell-checker-api-reference.md)
</dt> <dt>

[<span data-ttu-id="ac550-142">Пример проверки орфографии клиента</span><span class="sxs-lookup"><span data-stu-id="ac550-142">Spell checking client sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerClient)
</dt> <dt>

[<span data-ttu-id="ac550-143">Пример поставщика проверки орфографии</span><span class="sxs-lookup"><span data-stu-id="ac550-143">Spell checking provider sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)
</dt> <dt>

[<span data-ttu-id="ac550-144">**Иоптиондескриптион:: ID**</span><span class="sxs-lookup"><span data-stu-id="ac550-144">**IOptionDescription::Id**</span></span>](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id)
</dt> <dt>

[<span data-ttu-id="ac550-145">**иенумстринг**</span><span class="sxs-lookup"><span data-stu-id="ac550-145">**IEnumString**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)
</dt> <dt>

<span data-ttu-id="ac550-146">[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="ac550-146">[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
</dt> </dl>

 

 
