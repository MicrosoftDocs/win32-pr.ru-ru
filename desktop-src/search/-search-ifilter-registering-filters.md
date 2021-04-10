---
description: Необходимо зарегистрировать обработчик фильтра. Можно также выбрать существующий обработчик фильтра для данного расширения имени файла либо с помощью реестра, либо с помощью интерфейса Илоадфилтер.
ms.assetid: 3478b948-73c7-4533-974a-d9b5186a651b
title: Регистрация обработчиков фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18f39688bbea3bb0dd73ef28a0ba6e8b0dcf7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144125"
---
# <a name="registering-filter-handlers"></a><span data-ttu-id="a5068-104">Регистрация обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="a5068-104">Registering Filter Handlers</span></span>

<span data-ttu-id="a5068-105">Необходимо зарегистрировать обработчик фильтра.</span><span class="sxs-lookup"><span data-stu-id="a5068-105">Your filter handler must be registered.</span></span> <span data-ttu-id="a5068-106">Можно также выбрать существующий обработчик фильтра для данного расширения имени файла либо с помощью реестра, либо с помощью интерфейса [**илоадфилтер**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) .</span><span class="sxs-lookup"><span data-stu-id="a5068-106">You can also locate an existing filter handler for a given file name extension either through the registry or by using the [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) interface.</span></span>

<span data-ttu-id="a5068-107">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a5068-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="a5068-108">Регистрация обработчиков фильтров для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="a5068-108">Registering Filters Handlers for Windows Search</span></span>](#registering-filter-handlers)
  - [<span data-ttu-id="a5068-109">Устаревший подход к регистрации обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="a5068-109">Obsolete Approach for Registering Filters Handlers</span></span>](#obsolete-approach-for-registering-filters-handlers)
- [<span data-ttu-id="a5068-110">Замена существующих обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="a5068-110">Replacing Existing Filter Handlers</span></span>](#replacing-existing-filter-handlers)
- [<span data-ttu-id="a5068-111">Поиск обработчика фильтра для заданного расширения файла</span><span class="sxs-lookup"><span data-stu-id="a5068-111">Finding a Filter Handler for a Given File Extension</span></span>](#finding-a-filter-handler-for-a-given-file-extension)
- [<span data-ttu-id="a5068-112">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a5068-112">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="a5068-113">См. также</span><span class="sxs-lookup"><span data-stu-id="a5068-113">Related topics</span></span>](#related-topics)

> [!NOTE]  
> <span data-ttu-id="a5068-114">Обработчик фильтра является реализацией интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="a5068-114">A filter handler is an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>

## <a name="registering-filters-handlers-for-windows-search"></a><span data-ttu-id="a5068-115">Регистрация обработчиков фильтров для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="a5068-115">Registering Filters Handlers for Windows Search</span></span>

<span data-ttu-id="a5068-116">Идентификаторы GUID, необходимые для регистрации нового обработчика протокола или поиска существующего обработчика протокола, перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a5068-116">The GUIDs you need for registering a new protocol handler or to find an existing protocol handler are listed in the following table.</span></span>

| <span data-ttu-id="a5068-117">Код GUID</span><span class="sxs-lookup"><span data-stu-id="a5068-117">GUID</span></span>                                     | <span data-ttu-id="a5068-118">Определено пользователем или приложением</span><span class="sxs-lookup"><span data-stu-id="a5068-118">User or application defined</span></span> | <span data-ttu-id="a5068-119">Описание</span><span class="sxs-lookup"><span data-stu-id="a5068-119">Description</span></span>                                                                                               |
|------------------------------------------|-----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5068-120">**89BCB740-6119-101A-BCB7-00DD010655AF**</span><span class="sxs-lookup"><span data-stu-id="a5068-120">**89BCB740-6119-101A-BCB7-00DD010655AF**</span></span> | <span data-ttu-id="a5068-121">Приложение</span><span class="sxs-lookup"><span data-stu-id="a5068-121">Application</span></span>                 | <span data-ttu-id="a5068-122">GUID интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) — это константа раздела реестра для всех обработчиков фильтров.</span><span class="sxs-lookup"><span data-stu-id="a5068-122">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface GUID is a registry key constant for all filter handlers.</span></span> |
| <span data-ttu-id="a5068-123">**{Персистенсандлергуид}**</span><span class="sxs-lookup"><span data-stu-id="a5068-123">**{PersistentHandlerGUID}**</span></span>              | <span data-ttu-id="a5068-124">Пользователь</span><span class="sxs-lookup"><span data-stu-id="a5068-124">User</span></span>                        | <span data-ttu-id="a5068-125">Это идентификатор GUID для постоянного обработчика.</span><span class="sxs-lookup"><span data-stu-id="a5068-125">This is the GUID for the persistent handler.</span></span>                                                              |
| <span data-ttu-id="a5068-126">**{Филтерхандлерклсид}**</span><span class="sxs-lookup"><span data-stu-id="a5068-126">**{FilterHandlerCLSID}**</span></span>                 | <span data-ttu-id="a5068-127">Пользователь</span><span class="sxs-lookup"><span data-stu-id="a5068-127">User</span></span>                        | <span data-ttu-id="a5068-128">Это идентификатор класса (CLSID) для обработчика фильтра.</span><span class="sxs-lookup"><span data-stu-id="a5068-128">This is the class identifier (CLSID) for the filter handler.</span></span>                                              |
| <span data-ttu-id="a5068-129">**{Аппликатионгуид}**</span><span class="sxs-lookup"><span data-stu-id="a5068-129">**{ApplicationGUID}**</span></span>                    | <span data-ttu-id="a5068-130">Пользователь</span><span class="sxs-lookup"><span data-stu-id="a5068-130">User</span></span>                        | <span data-ttu-id="a5068-131">Это промежуточный (агрегированный) GUID.</span><span class="sxs-lookup"><span data-stu-id="a5068-131">This is an intermediate (aggregated) GUID.</span></span>                                                                |

<span data-ttu-id="a5068-132">Обработчики фильтров должны быть зарегистрированы на \_ локальном компьютере hKey, \_ так как SearchFilterHost.exe выполняется под системной учетной записью и поэтому не может получить доступ к разделам реестра для \_ текущего пользователя hKey \_ , вошедшего в систему.</span><span class="sxs-lookup"><span data-stu-id="a5068-132">Filter handlers must be registered in HKEY\_LOCAL\_MACHINE because SearchFilterHost.exe is running under the SYSTEM account and therefore cannot access registry keys for HKEY\_CURRENT\_USER for the logged-on user.</span></span> <span data-ttu-id="a5068-133">Кроме того, Группа "Пользователи" должна иметь доступ для чтения и выполнения к самому обработчику фильтра. dll, так как SearchFilterHost.exe удаляет все права администратора и разрешает только права без прав администратора.</span><span class="sxs-lookup"><span data-stu-id="a5068-133">In addition, the Users group must have read-and-execute access to the filter handler .dll itself because SearchFilterHost.exe removes all administrator rights and permits only non-administrator rights.</span></span> <span data-ttu-id="a5068-134">Так как расположение проекта Visual Studio по умолчанию находится в каталоге текущего пользователя и не предоставляет разрешения на чтение группе Пользователи, необходимо либо переместить DLL-файл, либо изменить списки ACL, чтобы разрешить SearchFilterHost.exe доступ.</span><span class="sxs-lookup"><span data-stu-id="a5068-134">Because the default Visual Studio project location is in the current user's directory, and so does not give read permissions to the Users group, you must either move the .dll or change the ACLs to allow SearchFilterHost.exe access.</span></span>

<span data-ttu-id="a5068-135">При регистрации нового обработчика фильтров рекомендуется использовать описательное имя, например HTML IFilter.</span><span class="sxs-lookup"><span data-stu-id="a5068-135">When you register a new filter handler, we recommend that you use a descriptive name, for example, HTML IFilter.</span></span>

<span data-ttu-id="a5068-136">**Чтобы зарегистрировать новый обработчик фильтра, выполните следующие действия.**</span><span class="sxs-lookup"><span data-stu-id="a5068-136">**To register your new filter handler:**</span></span>

1. <span data-ttu-id="a5068-137">Укажите расширение и устойчивый идентификатор GUID обработчика, который будет использовать обработчик фильтра:</span><span class="sxs-lookup"><span data-stu-id="a5068-137">Specify the extension and persistent handler GUID that will use the filter handler:</span></span>

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                PersistentHandler
                   (Default) = {PersistentHandlerGUID}
```

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {PersistentHandlerGUID}
                      PersistentAddinsRegistered
                         {89BCB740-6119-101A-BCB7-00DD010655AF}l
                            (Default) = {FilterHandlerCLSID}
```

2. <span data-ttu-id="a5068-138">Зарегистрируйте обработчик фильтра со следующими ключами и значениями:</span><span class="sxs-lookup"><span data-stu-id="a5068-138">Register your filter handler with the following keys and values:</span></span>

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {FilterHandlerCLSID}
                      (Default) = {DescriptiveFilterHandlerName}
                      InprocServer32
                         (Default) = DLL Install Path
                         ThreadingModel = Both
```

### <a name="obsolete-approach-for-registering-filters-handlers"></a><span data-ttu-id="a5068-139">Устаревший подход к регистрации обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="a5068-139">Obsolete Approach for Registering Filters Handlers</span></span>

<span data-ttu-id="a5068-140">Этот подход не рекомендуется использовать.</span><span class="sxs-lookup"><span data-stu-id="a5068-140">This approach is not recommended for use.</span></span> <span data-ttu-id="a5068-141">Фильтры могут быть зарегистрированы для идентификатора CLSID, представляющего класс модели COM, и (или) для расширения имени файла.</span><span class="sxs-lookup"><span data-stu-id="a5068-141">Filters can be registered for a CLSID that represents a Component Object Model (COM) class, and/or for a file name extension.</span></span> <span data-ttu-id="a5068-142">Вы можете зарегистрировать оба фильтра, если необходимо зарегистрировать обработчик фильтра для класса, и другой обработчик фильтра для расширения имени файла в классе.</span><span class="sxs-lookup"><span data-stu-id="a5068-142">You could register both filters if you need to register a filter handler for a class, and a different filter handler for a file name extension within the class.</span></span> <span data-ttu-id="a5068-143">Обратите внимание, что обработчик фильтра, зарегистрированный для расширения имени файла, имеет приоритет над обработчиком фильтра для идентификатора CLSID.</span><span class="sxs-lookup"><span data-stu-id="a5068-143">Note that a filter handler registered for a file name extension takes precedence over a filter handler for a CLSID.</span></span>

<span data-ttu-id="a5068-144">Эти записи являются стандартными записями реестра OLE, включая запись для класса **CLSID \\ {аппликатионгуид}**.</span><span class="sxs-lookup"><span data-stu-id="a5068-144">These entries are standard OLE registry entries up to and including the entry for the class **CLSID\\{ApplicationGUID}**.</span></span> <span data-ttu-id="a5068-145">Библиотека DLL sample.dll реализует поведение выполняемого объекта для класса. txt.</span><span class="sxs-lookup"><span data-stu-id="a5068-145">The DLL sample.dll implements running object behavior for the .txt class.</span></span> <span data-ttu-id="a5068-146">Обратите внимание на лишнюю запись Персистенсандлер.</span><span class="sxs-lookup"><span data-stu-id="a5068-146">Note the extra entry, PersistentHandler.</span></span> <span data-ttu-id="a5068-147">Эта запись указывает класс, отвечающий за брокер запросов к постоянным объектам класса Sample.</span><span class="sxs-lookup"><span data-stu-id="a5068-147">This entry specifies the class that is responsible for brokering requests to the persistent objects of the sample class.</span></span> <span data-ttu-id="a5068-148">Запись в разделе **персистентаддинсрегистеред** определяет реализацию, ответственную за интерфейс с именем **89BCB740-6119-101A-BCB7-00DD010655AF**(IID \_ IFilter).</span><span class="sxs-lookup"><span data-stu-id="a5068-148">The entry under **PersistentAddinsRegistered** identifies the implementation responsible for the interface named **89BCB740-6119-101A-BCB7-00DD010655AF**(IID\_IFilter).</span></span> <span data-ttu-id="a5068-149">Класс, реализующий интерфейс **IID \_ IFilter** , имеет стандартные записи реестра OLE.</span><span class="sxs-lookup"><span data-stu-id="a5068-149">The class implementing **IID\_IFilter** has standard OLE registry entries.</span></span> <span data-ttu-id="a5068-150">Библиотека DLL InprocServer32 загружается с помощью стандартного механизма OLE.</span><span class="sxs-lookup"><span data-stu-id="a5068-150">The InprocServer32 DLL is loaded through the standard OLE mechanism.</span></span>

<span data-ttu-id="a5068-151">Windows Search просматривает потоковую модель, указанную для обработчика фильтра.</span><span class="sxs-lookup"><span data-stu-id="a5068-151">Windows Search observes the threading model specified for the filter handler.</span></span> <span data-ttu-id="a5068-152">Если для потоковой модели задано значение **both**, обработчик фильтра должен быть потокобезопасным; в противном случае, если он не является потокобезопасным, укажите **апартамент**.</span><span class="sxs-lookup"><span data-stu-id="a5068-152">When the threading model is set to **Both**, the filter handler must be thread safe; otherwise, if it is not thread safe, specify **Apartment**.</span></span> <span data-ttu-id="a5068-153">Обратите внимание, что обработчики фильтров всегда должны быть потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="a5068-153">Note that filter handlers should always be thread safe.</span></span>

<span data-ttu-id="a5068-154">В следующем примере записи реестра предназначены для обработчика фильтра, зарегистрированного для класса и расширения имени файла.</span><span class="sxs-lookup"><span data-stu-id="a5068-154">The following example registry entries are for a filter handler registered for a class and file name extension.</span></span> <span data-ttu-id="a5068-155">**{Персистенсандлергуид}** и **{филтерхандлерклсид}** используются в качестве переменных, указывающих значения, которые должны быть заданы создателем обработчика фильтра.</span><span class="sxs-lookup"><span data-stu-id="a5068-155">**{PersistentHandlerGUID}** and **{FilterHandlerCLSID}** are used as variables indicating values that need to be specified by the creator of the filter handler.</span></span> <span data-ttu-id="a5068-156">Значения имеют тип REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="a5068-156">The values are of type REG\_SZ.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Classes
         .txt
            (Default) = SampleFile
         SampleFile
            (Default) = Class for Sample Files
            CLSID
               (Default) = {ApplicationGUID}
         CLSID
            {ApplicationGUID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sample.dll
               PersistentHandler
                  (Default) = {PersistentHandlerGUID}
            {PersistentHandlerGUID}
               (Default) = Sample file persistent handler
               PersistentAddinsRegistered
                  {89BCB740-6119-101A-BCB7-00DD010655AF}l
                     (Default) = {FilterHandlerCLSID}
            {FilterHandlerCLSID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sampfilt.dll
                  ThreadingModel = Both
```

## <a name="replacing-existing-filter-handlers"></a><span data-ttu-id="a5068-157">Замена существующих обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="a5068-157">Replacing Existing Filter Handlers</span></span>

<span data-ttu-id="a5068-158">Не рекомендуется заменять встроенные обработчики фильтров для распространенных типов файлов, таких как txt, doc, HTML, URL и т. д., так как это может привести к нежелательным последствиям для других компонентов системы.</span><span class="sxs-lookup"><span data-stu-id="a5068-158">We recommend that you do not replace the built-in filter handlers for common file types such as .txt, .doc, .html, .url, and so forth, because doing so can have undesired effects on other system components.</span></span> <span data-ttu-id="a5068-159">Индексирование текста сообщений электронной почты зависит от обработчиков фильтров. txt, HTML и. RTF, например.</span><span class="sxs-lookup"><span data-stu-id="a5068-159">Indexing email message bodies depends on the .txt, .html, and .rtf filter handlers, for example.</span></span>

<span data-ttu-id="a5068-160">Если новый обработчик фильтра для типа файла устанавливается в качестве замены для существующей регистрации фильтра, установщик должен сохранить текущую регистрацию и восстановить ее при удалении нового обработчика фильтра.</span><span class="sxs-lookup"><span data-stu-id="a5068-160">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="a5068-161">Механизм фильтрации цепочек отсутствует.</span><span class="sxs-lookup"><span data-stu-id="a5068-161">There is no mechanism to chain filters.</span></span> <span data-ttu-id="a5068-162">Таким образом, новый обработчик фильтра отвечает за репликацию всех необходимых функций старого фильтра.</span><span class="sxs-lookup"><span data-stu-id="a5068-162">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>

## <a name="finding-a-filter-handler-for-a-given-file-extension"></a><span data-ttu-id="a5068-163">Поиск обработчика фильтра для заданного расширения файла</span><span class="sxs-lookup"><span data-stu-id="a5068-163">Finding a Filter Handler for a Given File Extension</span></span>

<span data-ttu-id="a5068-164">Интерфейс [**илоадфилтер**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) можно использовать для поиска обработчика фильтра для данного расширения имени файла.</span><span class="sxs-lookup"><span data-stu-id="a5068-164">You can use the [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) interface to find a filter handler for a given file name extension.</span></span> <span data-ttu-id="a5068-165">В следующем примере записи реестра иллюстрируют, как это сделать для HTML-файлов.</span><span class="sxs-lookup"><span data-stu-id="a5068-165">The following example registry entries illustrate how to do so for HTML files.</span></span> <span data-ttu-id="a5068-166">В этом примере обработчик фильтра для HTML-документов nlhtml.dll.</span><span class="sxs-lookup"><span data-stu-id="a5068-166">In this example, the filter handler for HTML documents is nlhtml.dll.</span></span> <span data-ttu-id="a5068-167">Значения имеют тип REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="a5068-167">The values are of type REG\_SZ.</span></span>

<span data-ttu-id="a5068-168">**Чтобы найти обработчик фильтра для данного расширения имени файла, выполните следующие действия.**</span><span class="sxs-lookup"><span data-stu-id="a5068-168">**To find the filter handler for a given file name extension:**</span></span>

1. <span data-ttu-id="a5068-169">Проверьте, имеет ли расширение для типа фильтруемых файлов постоянный обработчик, зарегистрированный в записи реестра \\ hKey \_ \_ \\ Software Machine \\ Classes. extension.</span><span class="sxs-lookup"><span data-stu-id="a5068-169">Check whether the extension for the type of files that are filtered has a persistent handler registered under the registry entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes.extension.</span></span> <span data-ttu-id="a5068-170">Если да, предоставьте этому разделу значение {Персистенсандлергуид}.</span><span class="sxs-lookup"><span data-stu-id="a5068-170">If so, let this key be {PersistentHandlerGUID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {PersistentHandlerGUID}
```

2. <span data-ttu-id="a5068-171">Если для расширения не зарегистрирован устойчивый обработчик, найдите идентификатор CLSID, связанный с типом документа, в записи реестра \\ hKey \_ Local \_ Machine \\ Software программные \\ классы.</span><span class="sxs-lookup"><span data-stu-id="a5068-171">If there is not a persistent handler registered for the extension, find the CLSID associated with the document type under the registry entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes.</span></span> <span data-ttu-id="a5068-172">Предоставьте этому ключу {Аппликатионгуид}.</span><span class="sxs-lookup"><span data-stu-id="a5068-172">Let this key be {ApplicationGUID}.</span></span> <span data-ttu-id="a5068-173">Затем определите, зарегистрирован ли постоянный обработчик для CLSID: с помощью {Аппликатионгуид} найдите постоянный обработчик для \\ \_ \_ \\ \\ \\ \\ записи CLSID {аппликатионгуид} для классов программного обеспечения на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="a5068-173">Then determine whether a persistent handler is registered for the CLSID: using {ApplicationGUID} locate the persistent handler for the \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{ApplicationGUID} entry.</span></span> <span data-ttu-id="a5068-174">Предоставьте этому ключу {Персистенсандлергуид}.</span><span class="sxs-lookup"><span data-stu-id="a5068-174">Let this key be {PersistentHandlerGUID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                (Default) = Class for WWW HTML files
                CLSID
                   (Default) = {25336920-03F9-11CF-8FD0-00AA00686F13}
             CLSID
                {25336920-03F9-11CF-8FD0-00AA00686F13}
                   PersistentHandler
                      (Default) = {PersistentHandlerGUID}
```

3. <span data-ttu-id="a5068-175">Определите идентификатор GUID постоянного обработчика: с помощью {Персистенсандлергуид} найдите GUID постоянного обработчика для типа документа.</span><span class="sxs-lookup"><span data-stu-id="a5068-175">Determine the GUID of the persistent handler: using {PersistentHandlerGUID} find the persistent handler GUID for the document type.</span></span> <span data-ttu-id="a5068-176">Значение в записи реестра HKEY \_ Local \_ Machine \\ Software \\ Classes \\ CLSID \\ {персистенсандлергуид} \\ персистентаддинсрегистеред \\ 89BCB740-6119-101A-BCB7-00DD010655AF дает постоянный идентификатор GUID обработчика для этого типа документа.</span><span class="sxs-lookup"><span data-stu-id="a5068-176">The value under the registry entry HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{PersistentHandlerGUID}\\PersistentAddinsRegistered\\ 89BCB740-6119-101A-BCB7-00DD010655AF yields the persistent handler GUID for this document type.</span></span> <span data-ttu-id="a5068-177">Предоставьте этому ключу {Филтерхандлерклсид}.</span><span class="sxs-lookup"><span data-stu-id="a5068-177">Let this key be {FilterHandlerCLSID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {PersistentHandlerGUID}
                (Default) = HTML File Persistent Handler<dl>
                    REG_SZ     {89BCB740-6119-101A-BCB7-00DD010655AF}
                    REG_SZ     (Default) = {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. <span data-ttu-id="a5068-178">Определение обработчика фильтра. с помощью {Филтерхандлерклсид}, который был определен на предыдущем шаге, найдите обработчик фильтра в разделе запись \\ hKey \_ локальный \_ компьютер \\ программное обеспечение \\ классы \\ CLSID \\ {филтерхандлерклсид} \\ InprocServer32.</span><span class="sxs-lookup"><span data-stu-id="a5068-178">Determine the filter handler: using {FilterHandlerCLSID} that was determined in the previous step locate the filter handler under the entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{FilterHandlerCLSID}\\InprocServer32.</span></span> <span data-ttu-id="a5068-179">В этом примере используется описательное имя обработчика фильтра HTML IFilter.</span><span class="sxs-lookup"><span data-stu-id="a5068-179">In this example the descriptive filter handler name used is HTML IFilter.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             CLSID
                {EEC97550-47A9-11CF-B952-00AA0051FE20}
                   (Default) = HTML IFilter
                    Data type  REG_SZ
                    InprocServer32
                    nlhtml.dll
```

## <a name="additional-resources"></a><span data-ttu-id="a5068-180">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a5068-180">Additional Resources</span></span>

- <span data-ttu-id="a5068-181">Пример кода [ифилтерсампле](-search-sample-ifiltersample.md) , доступный на [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), демонстрирует создание базового класса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) для реализации интерфейса **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="a5068-181">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) base class for implementing the **IFilter** interface.</span></span>
- <span data-ttu-id="a5068-182">Общие сведения о процессе индексирования см. [в разделе процесс индексирования](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a5068-182">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="a5068-183">Общие сведения о типах файлов см. в разделе [типы файлов](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="a5068-183">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="a5068-184">Сведения о запросе атрибутов сопоставления файлов для типа файлов см. в разделе [перцеиведтипес, системфилеассоЦиатионс и регистрация приложения](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5068-184">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5068-185">См. также</span><span class="sxs-lookup"><span data-stu-id="a5068-185">Related topics</span></span>

[<span data-ttu-id="a5068-186">Разработка обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="a5068-186">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="a5068-187">О обработчиках фильтров в поиске Windows</span><span class="sxs-lookup"><span data-stu-id="a5068-187">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="a5068-188">Рекомендации по созданию обработчиков фильтров в поиске Windows</span><span class="sxs-lookup"><span data-stu-id="a5068-188">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="a5068-189">Возвращение свойств из обработчика фильтра</span><span class="sxs-lookup"><span data-stu-id="a5068-189">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="a5068-190">Обработчики фильтров, поставляемые с Windows</span><span class="sxs-lookup"><span data-stu-id="a5068-190">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)

[<span data-ttu-id="a5068-191">Реализация обработчиков фильтров в поиске Windows</span><span class="sxs-lookup"><span data-stu-id="a5068-191">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="a5068-192">Тестирование обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="a5068-192">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
