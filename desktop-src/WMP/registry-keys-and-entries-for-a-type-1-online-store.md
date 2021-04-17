---
title: Разделы реестра и записи для Интернет-магазина типа 1
description: Разделы реестра и записи для Интернет-магазина типа 1
ms.assetid: cf25a004-e0c3-407c-8704-54be3601528b
keywords:
- Интернет-магазины проигрывателя Windows Media в Интернете, реестр
- Интернет-магазины, реестр
- Тип 1 Интернет-магазины, реестр
- реестр, тип 1 Интернет-магазины
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1329ad69e91ebce41b258d1e148403f62caceb96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105681586"
---
# <a name="registry-keys-and-entries-for-a-type-1-online-store"></a><span data-ttu-id="79d7a-107">Разделы реестра и записи для Интернет-магазина типа 1</span><span class="sxs-lookup"><span data-stu-id="79d7a-107">Registry Keys and Entries for a Type 1 Online Store</span></span>

<span data-ttu-id="79d7a-108">Чтобы сделать Интернет-магазин типа 1 доступным в проигрывателе Windows Media, поставщик Интернет-магазина должен создать следующие подразделы и записи реестра на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="79d7a-108">To make a type 1 online store available in Windows Media Player, the online store provider must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\AppID\appid]
@=pluginName
"DllSurrogate"=""

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className
"AppID"="appid"

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="threading"
```



> [!Note]  
> <span data-ttu-id="79d7a-109">Установка значения Дллсуррогате в пустую строку указывает, что среда выполнения COM загрузит подключаемый модуль интернет-магазина в суррогатную библиотеку DLL по умолчанию dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="79d7a-109">Setting the value of DllSurrogate to the empty string indicates that the COM runtime will load the online store's plug-in into the default DLL surrogate, dllhost.exe.</span></span>

 

<span data-ttu-id="79d7a-110">В предыдущем синтаксисе реестра символы курсивом являются заполнителями для имен и глобально уникальных идентификаторов (GUID), характерных для Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="79d7a-110">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the online store.</span></span> <span data-ttu-id="79d7a-111">В следующей таблице описаны эти заполнители.</span><span class="sxs-lookup"><span data-stu-id="79d7a-111">The following table describes those placeholders.</span></span>



| <span data-ttu-id="79d7a-112">Заполнитель</span><span class="sxs-lookup"><span data-stu-id="79d7a-112">Placeholder</span></span>    | <span data-ttu-id="79d7a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="79d7a-113">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79d7a-114">*keyName*</span><span class="sxs-lookup"><span data-stu-id="79d7a-114">*keyName*</span></span>      | <span data-ttu-id="79d7a-115">Строка, согласованная между корпорацией Майкрософт и Интернет-магазином.</span><span class="sxs-lookup"><span data-stu-id="79d7a-115">A string agreed upon between Microsoft and the online store.</span></span> <span data-ttu-id="79d7a-116">Эта строка уникально идентифицирует Интернет-магазин. Пример: "Proseware"</span><span class="sxs-lookup"><span data-stu-id="79d7a-116">This string uniquely identifies the online store.Example: "Proseware"</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="79d7a-117">*flags*</span><span class="sxs-lookup"><span data-stu-id="79d7a-117">*flags*</span></span>        | <span data-ttu-id="79d7a-118">Побитовое **или** для одного или нескольких флагов возможностей подключаемых модулей. Эти флаги определяют, должен ли проигрыватель Windows Media вызывать определенные методы [ивмпконтентпартнер](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner).</span><span class="sxs-lookup"><span data-stu-id="79d7a-118">A bitwise **OR** of one or more plug-in capability flags These flags specify whether Windows Media Player should call particular methods of [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner).</span></span> <span data-ttu-id="79d7a-119">Дополнительные сведения о поддерживаемых флагах см. в таблице флагов возможностей подключаемых модулей, которые следуют за этой таблицей. Пример: 00000058</span><span class="sxs-lookup"><span data-stu-id="79d7a-119">For information about supported flags, see the table of plug-in capability flags that follows this table.Example: 00000058</span></span><br/> |
| <span data-ttu-id="79d7a-120">*этому*</span><span class="sxs-lookup"><span data-stu-id="79d7a-120">*clsid*</span></span>        | <span data-ttu-id="79d7a-121">Идентификатор GUID, который является идентификатором класса (CLSID) для класса, реализующего **ивмпконтентпартнер** в подключаемом модуле Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="79d7a-121">A GUID that is the class identifier (CLSID) for the class that implements **IWMPContentPartner** in the online store's plug-in.</span></span> <span data-ttu-id="79d7a-122">Этот GUID должен быть в формате реестра, заполненном фигурными скобками. Формат: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="79d7a-122">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                  |
| <span data-ttu-id="79d7a-123">*FriendlyName*</span><span class="sxs-lookup"><span data-stu-id="79d7a-123">*friendlyname*</span></span> | <span data-ttu-id="79d7a-124">Понятное имя Интернет-магазина. Пример: "Proseware Music Service"</span><span class="sxs-lookup"><span data-stu-id="79d7a-124">A friendly name for the online store.Example: "Proseware Music Service"</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="79d7a-125">*appid*</span><span class="sxs-lookup"><span data-stu-id="79d7a-125">*appid*</span></span>        | <span data-ttu-id="79d7a-126">Идентификатор GUID, который является идентификатором приложения (AppID) для подключаемого модуля интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="79d7a-126">A GUID that is the application identifier (AppID) for the online store's plug-in.</span></span> <span data-ttu-id="79d7a-127">Этот GUID должен быть в формате реестра, заполненном фигурными скобками. Формат: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="79d7a-127">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                                                                |
| <span data-ttu-id="79d7a-128">*pluginName*</span><span class="sxs-lookup"><span data-stu-id="79d7a-128">*pluginName*</span></span>   | <span data-ttu-id="79d7a-129">Имя подключаемого модуля интернет-магазина. Пример: "подключаемый модуль партнера по содержимому Proseware"</span><span class="sxs-lookup"><span data-stu-id="79d7a-129">A name for the online store's plug-in.Example: "Proseware Content Partner Plug-in"</span></span><br/>                                                                                                                                                                                                                                   |
| <span data-ttu-id="79d7a-130">*className*</span><span class="sxs-lookup"><span data-stu-id="79d7a-130">*className*</span></span>    | <span data-ttu-id="79d7a-131">Имя класса, реализующего **ивмпконтентпартнер** в подключаемом модуле Интернет-магазина. Пример: "Кпросеварепартнер"</span><span class="sxs-lookup"><span data-stu-id="79d7a-131">The name of the class that implements **IWMPContentpartner** in the online store's plug-in.Example: "CProsewarePartner"</span></span><br/>                                                                                                                                                                                              |
| <span data-ttu-id="79d7a-132">*moduleName*</span><span class="sxs-lookup"><span data-stu-id="79d7a-132">*moduleName*</span></span>   | <span data-ttu-id="79d7a-133">Полный путь к библиотеке DLL, которая реализует подключаемый модуль интернет-магазина. Пример: "C: \\ Program Files \\ Proseware \\ProsewarePartner.dll"</span><span class="sxs-lookup"><span data-stu-id="79d7a-133">The fully qualified path to the DLL that implements the online store's plug-in.Example: "C:\\Program Files\\Proseware\\ProsewarePartner.dll"</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="79d7a-134">*Threading*</span><span class="sxs-lookup"><span data-stu-id="79d7a-134">*threading*</span></span>    | <span data-ttu-id="79d7a-135">Тип подразделения, в котором выполняется подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="79d7a-135">The type of apartment the plug-in runs in.</span></span> <span data-ttu-id="79d7a-136">"ThreadingModel" = "апартамент" указывает, что подключаемый модуль запускается в однопотоковом подразделении (STA).</span><span class="sxs-lookup"><span data-stu-id="79d7a-136">"ThreadingModel"="Apartment" indicates that the plug-in runs in a single-threaded apartment (STA).</span></span> <span data-ttu-id="79d7a-137">"ThreadingModel" = "Free" указывает, что подключаемый модуль запускается в многопоточном апартаменте (MTA).</span><span class="sxs-lookup"><span data-stu-id="79d7a-137">"ThreadingModel"="Free" indicates that the plug-in runs in the multithreaded apartment (MTA).</span></span>                                                                                     |



 

<span data-ttu-id="79d7a-138">В следующей таблице описаны флаги возможностей подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="79d7a-138">The following table describes the plug-in capability flags.</span></span>



| <span data-ttu-id="79d7a-139">Флаг</span><span class="sxs-lookup"><span data-stu-id="79d7a-139">Flag</span></span>                                    | <span data-ttu-id="79d7a-140">Значение</span><span class="sxs-lookup"><span data-stu-id="79d7a-140">Value</span></span> | <span data-ttu-id="79d7a-141">Описание</span><span class="sxs-lookup"><span data-stu-id="79d7a-141">Description</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79d7a-142">\_баккграундпроцессинг ограничения \_ подписки</span><span class="sxs-lookup"><span data-stu-id="79d7a-142">SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING</span></span> | <span data-ttu-id="79d7a-143">0x8</span><span class="sxs-lookup"><span data-stu-id="79d7a-143">0x8</span></span>   | <span data-ttu-id="79d7a-144">Проигрыватель Windows Media должен вызвать [ивмпконтентпартнер:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) , чтобы сообщить подключаемому модулю о необходимости запуска и прекращения фоновой обработки.</span><span class="sxs-lookup"><span data-stu-id="79d7a-144">Windows Media Player should call [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) to inform the plug-in when it should start and stop background processing.</span></span>                                                                                                     |
| <span data-ttu-id="79d7a-145">\_девицеаваилабле ограничения \_ подписки</span><span class="sxs-lookup"><span data-stu-id="79d7a-145">SUBSCRIPTION\_CAP\_DEVICEAVAILABLE</span></span>      | <span data-ttu-id="79d7a-146">0x10</span><span class="sxs-lookup"><span data-stu-id="79d7a-146">0x10</span></span>  | <span data-ttu-id="79d7a-147">Проигрыватель Windows Media должен вызывать [ивмпконтентпартнер:: упдатедевице](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).</span><span class="sxs-lookup"><span data-stu-id="79d7a-147">Windows Media Player should call [IWMPContentPartner::UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).</span></span>                                                                                                                                                                   |
| <span data-ttu-id="79d7a-148">\_ограничение подписки \_ — \_ контентпартнер</span><span class="sxs-lookup"><span data-stu-id="79d7a-148">SUBSCRIPTION\_CAP\_IS\_CONTENTPARTNER</span></span>   | <span data-ttu-id="79d7a-149">0x40</span><span class="sxs-lookup"><span data-stu-id="79d7a-149">0x40</span></span>  | <span data-ttu-id="79d7a-150">Информирует проигрыватель Windows Media, что подключаемый модуль реализует интерфейс **ивмпконтентпартнер** .</span><span class="sxs-lookup"><span data-stu-id="79d7a-150">Informs Windows Media Player that the plug-in implements the **IWMPContentPartner** interface.</span></span> <span data-ttu-id="79d7a-151">Все подключаемые модули Интернет-магазина типа 1 должны устанавливать этот флаг.</span><span class="sxs-lookup"><span data-stu-id="79d7a-151">All type 1 online store plug-ins must set this flag.</span></span>                                                                                                                         |
| <span data-ttu-id="79d7a-152">\_алтлогин ограничения \_ подписки</span><span class="sxs-lookup"><span data-stu-id="79d7a-152">SUBSCRIPTION\_CAP\_ALTLOGIN</span></span>             | <span data-ttu-id="79d7a-153">0x80</span><span class="sxs-lookup"><span data-stu-id="79d7a-153">0x80</span></span>  | <span data-ttu-id="79d7a-154">Информирует проигрыватель Windows Media, что подключаемый модуль поддерживает альтернативное имя входа.</span><span class="sxs-lookup"><span data-stu-id="79d7a-154">Informs Windows Media Player that the plug-in supports an alternate login.</span></span> <span data-ttu-id="79d7a-155">Если подключаемый модуль поддерживает альтернативное имя входа, проигрыватель Windows Media Получает альтернативный URL-адрес и заголовок для входа путем вызова [ивмпконтентпартнер:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo).</span><span class="sxs-lookup"><span data-stu-id="79d7a-155">If the plug-in supports an alternate login, Windows Media Player retrieves the alternate login URL and caption by calling [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo).</span></span> |



 

<span data-ttu-id="79d7a-156">**Записи реестра для разработки и тестирования**</span><span class="sxs-lookup"><span data-stu-id="79d7a-156">**Registry Entries for Development and Testing**</span></span>

<span data-ttu-id="79d7a-157">После начала разработки Интернет-магазина Корпорация Майкрософт предоставляет два ключа: тестовый ключ и рабочий ключ.</span><span class="sxs-lookup"><span data-stu-id="79d7a-157">When you begin developing your online store, Microsoft provides you with two keys: a test key and a production key.</span></span> <span data-ttu-id="79d7a-158">На этапе разработки и тестирования Интернет-магазин будет отображаться в проигрывателе Windows Media только в том случае, если ваш тестовый ключ или рабочий ключ находится в реестре на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="79d7a-158">During the development and testing phase, your online store will appear in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="79d7a-159">Дополнительные сведения о тестовых и производственных ключах см. в статье [ключи тестирования и производства для Интернет-магазина типа 1](test-and-production-keys-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="79d7a-159">For more information about the test and production keys, see [Test and Production Keys for a Type 1 Online Store](test-and-production-keys-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="79d7a-160">Поместите свой тестовый или рабочий ключ в следующее место в реестре.</span><span class="sxs-lookup"><span data-stu-id="79d7a-160">Place your test or production key in the following location in the registry.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



<span data-ttu-id="79d7a-161">Обратите внимание, что значение записи реестра Тестпараметер может указывать несколько тестовых или рабочих ключей.</span><span class="sxs-lookup"><span data-stu-id="79d7a-161">Note that the value of the TestParameter registry entry can specify multiple test or production keys.</span></span> <span data-ttu-id="79d7a-162">Например, предположим, что у Proseware есть тестовый ключ "1234", а Contoso — тестовый ключ "2345".</span><span class="sxs-lookup"><span data-stu-id="79d7a-162">For example, suppose that Proseware has a test key of "1234" and Contoso has a test key of "2345".</span></span> <span data-ttu-id="79d7a-163">Следующая запись реестра указывает, что хранилища тестов для Proseware и Contoso будут отображаться в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="79d7a-163">The following registry entry specifies that the test stores for Proseware and Contoso will appear in Windows Media Player.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



<span data-ttu-id="79d7a-164">**Запись реестра Активесервице**</span><span class="sxs-lookup"><span data-stu-id="79d7a-164">**ActiveService Registry Entry**</span></span>

<span data-ttu-id="79d7a-165">Когда пользователь активирует Интернет-магазин, проигрыватель Windows Media записывает в реестр сведения, определяющие активное Интернет-магазин.</span><span class="sxs-lookup"><span data-stu-id="79d7a-165">When the user activates an online store, Windows Media Player writes information in the registry that identifies the active online store.</span></span> <span data-ttu-id="79d7a-166">Проигрыватель Windows Media помещает сведения в следующем расположении в реестре на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="79d7a-166">Windows Media Player places the information in the following location in the registry on the user's computer.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



<span data-ttu-id="79d7a-167">В приведенном выше синтаксисе реестра *serviceInfo* — это заполнитель для строки, содержащей описательные сведения об активном Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="79d7a-167">In the preceding registry syntax, *serviceInfo* is a placeholder for a string that contains descriptive information about the active online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79d7a-168">См. также</span><span class="sxs-lookup"><span data-stu-id="79d7a-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79d7a-169">**Справочные материалы по интернет-магазинам типа 1**</span><span class="sxs-lookup"><span data-stu-id="79d7a-169">**Reference for Type 1 Online Stores**</span></span>](reference-for-type-1-online-stores.md)
</dt> </dl>

 

 





