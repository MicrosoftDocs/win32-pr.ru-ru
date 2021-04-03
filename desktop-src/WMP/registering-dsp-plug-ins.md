---
title: Регистрация подключаемых модулей DSP
description: Регистрация подключаемых модулей DSP
ms.assetid: af264ff7-702b-4a49-a14d-ab8563a40c4e
keywords:
- Подключаемые модули проигрывателя Windows Media, записи реестра
- подключаемые модули, записи реестра
- подключаемые модули обработки цифровых сигналов, записи реестра
- Подключаемые модули DSP, записи реестра
- реестр, подключаемые модули DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64e7afd43cf242d57c0a9375c4cbda56e457ef1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987201"
---
# <a name="registering-dsp-plug-ins"></a><span data-ttu-id="73695-108">Регистрация подключаемых модулей DSP</span><span class="sxs-lookup"><span data-stu-id="73695-108">Registering DSP Plug-ins</span></span>

<span data-ttu-id="73695-109">Чтобы сделать подключаемый модуль DSP доступным в проигрывателе Windows Media, необходимо создать следующие подразделы и записи реестра на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="73695-109">To make your DSP plug-in available in Windows Media Player you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\PluginClsid]
@=PluginClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PluginClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Threading"
```



<span data-ttu-id="73695-110">В предыдущем синтаксисе реестра символы курсивом являются заполнителями для имен и глобально уникальных идентификаторов (GUID), характерных для подключаемого модуля DSP.</span><span class="sxs-lookup"><span data-stu-id="73695-110">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="73695-111">В следующей таблице описаны эти заполнители.</span><span class="sxs-lookup"><span data-stu-id="73695-111">The following table describes those placeholders.</span></span>



| <span data-ttu-id="73695-112">Заполнитель</span><span class="sxs-lookup"><span data-stu-id="73695-112">Placeholder</span></span>               | <span data-ttu-id="73695-113">Описание</span><span class="sxs-lookup"><span data-stu-id="73695-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73695-114">*плугинклсид*</span><span class="sxs-lookup"><span data-stu-id="73695-114">*PluginClsid*</span></span>             | <span data-ttu-id="73695-115">Идентификатор GUID, который является идентификатором класса для основного класса подключаемого модуля DSP.</span><span class="sxs-lookup"><span data-stu-id="73695-115">A GUID that is the class identifier for the DSP plug-in's primary class.</span></span> <span data-ttu-id="73695-116">Это класс, реализующий **имедиаобжект**, **иплугиненабле** и, возможно, **испеЦифипропертипажес**.</span><span class="sxs-lookup"><span data-stu-id="73695-116">This is the class that implements **IMediaObject**, **IPluginEnable**, and possibly **ISpecifyPropertyPages**.</span></span> <span data-ttu-id="73695-117">В подключаемом модуле с двойным режимом этот класс также реализует **имфтрансформ** и **имфжетсервице**. Этот GUID должен быть в формате реестра, заполненном фигурными скобками.</span><span class="sxs-lookup"><span data-stu-id="73695-117">In a dual-mode plug-in, this class also implements **IMFTransform** and **IMFGetService**.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="73695-118">Формат: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="73695-118">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="73695-119">*плугинклассфриендлинаме*</span><span class="sxs-lookup"><span data-stu-id="73695-119">*PluginClassFriendlyName*</span></span> | <span data-ttu-id="73695-120">Понятное имя для первичного класса подключаемого модуля DSP. Пример: "класс Просеваредсп"</span><span class="sxs-lookup"><span data-stu-id="73695-120">A friendly name for the DSP plug-in's primary class.Example: "ProsewareDSP Class"</span></span><br/>                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="73695-121">*плугинмодуленаме*</span><span class="sxs-lookup"><span data-stu-id="73695-121">*PluginModuleName*</span></span>        | <span data-ttu-id="73695-122">Полный путь к библиотеке DLL, реализующей подключаемый модуль DSP. Пример: "C: \\ Program Files \\ Proseware \\ProsewareDsp.dll"</span><span class="sxs-lookup"><span data-stu-id="73695-122">The fully qualified path to the DLL that implements the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDsp.dll"</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="73695-123">*Работа с потоками*</span><span class="sxs-lookup"><span data-stu-id="73695-123">*Threading*</span></span>               | <span data-ttu-id="73695-124">Строка, указывающая потоковую модель для подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="73695-124">A string that specifies the threading model for the plug-in.</span></span> <span data-ttu-id="73695-125">Если подключаемый модуль будет работать с проигрывателем Windows Media 11 в Windows Vista, эта запись реестра должна быть равна «Both».</span><span class="sxs-lookup"><span data-stu-id="73695-125">If the plug-in is going to run with Windows Media Player 11 on Windows Vista, this registry entry must be equal to "Both".</span></span> <span data-ttu-id="73695-126">Если подключаемый модуль будет работать в Windows XP или более ранних операционных системах, эта запись реестра может быть равна либо "апартамент", либо "обоих".</span><span class="sxs-lookup"><span data-stu-id="73695-126">If the plug-in is going to run on Windows XP or older operating systems, this registry entry can be equal to either "Apartment" or "Both".</span></span>                                                                                           |



 

<span data-ttu-id="73695-127">Если подключаемый модуль DSP реализует пользовательский интерфейс, а подключаемый модуль будет запускаться в проигрывателе Windows Media 11 в Windows Vista, необходимо создать следующие подразделы и записи реестра на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="73695-127">If your DSP plug-in implements a custom interface and if your plug-in is going to run in Windows Media Player 11 on Windows Vista, you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid]
@=PSFactoryBuffer

[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid\InprocServer32]
@=ProxyStubModuleName
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId]
@=CustomInterfaceName

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\NumMethods]
@=NumberOfMethods

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\ProxyStubClsid32]
@=ProxyStubClsid
```



<span data-ttu-id="73695-128">В предыдущем синтаксисе реестра символы в курсиве являются заполнителями для имен, числовых значений и глобально уникальных идентификаторов (GUID), характерных для подключаемого модуля DSP.</span><span class="sxs-lookup"><span data-stu-id="73695-128">In the preceding registry syntax, the symbols in italic are placeholders for names, numeric values, and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="73695-129">В следующей таблице описаны эти заполнители.</span><span class="sxs-lookup"><span data-stu-id="73695-129">The following table describes those placeholders.</span></span>



| <span data-ttu-id="73695-130">Заполнитель</span><span class="sxs-lookup"><span data-stu-id="73695-130">Placeholder</span></span>           | <span data-ttu-id="73695-131">Описание</span><span class="sxs-lookup"><span data-stu-id="73695-131">Description</span></span>                                                                                                                                                                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73695-132">*проксистубклсид*</span><span class="sxs-lookup"><span data-stu-id="73695-132">*ProxyStubClsid*</span></span>      | <span data-ttu-id="73695-133">Идентификатор GUID, который является идентификатором класса для класса, реализующего прокси-серверы и заглушки для настраиваемых интерфейсов подключаемого модуля DSP. Этот GUID должен быть в формате реестра, заполненном фигурными скобками.</span><span class="sxs-lookup"><span data-stu-id="73695-133">A GUID that is the class identifier for the class that implements the proxies and stubs for the DSP plug-in's custom interfaces.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="73695-134">Формат: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="73695-134">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="73695-135">*проксистубмодуленаме*</span><span class="sxs-lookup"><span data-stu-id="73695-135">*ProxyStubModuleName*</span></span> | <span data-ttu-id="73695-136">Полный путь к библиотеке DLL, которая реализует интерфейсы прокси-сервера и заглушки для подключаемого модуля DSP. Пример: "C: \\ Program Files \\ Proseware \\ProsewareDspPS.dll"</span><span class="sxs-lookup"><span data-stu-id="73695-136">The fully qualified path to the DLL that implements the proxy and stub interfaces for the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDspPS.dll"</span></span><br/>                                                                                               |
| <span data-ttu-id="73695-137">*кустоминтерфацеид*</span><span class="sxs-lookup"><span data-stu-id="73695-137">*CustomInterfaceId*</span></span>   | <span data-ttu-id="73695-138">GUID, который является идентификатором интерфейса для пользовательского интерфейса, реализованного подключаемым модулем DSP. Этот GUID должен быть в формате реестра, заполненном фигурными скобками.</span><span class="sxs-lookup"><span data-stu-id="73695-138">A GUID that is the interface identifier for a custom interface that is implemented by the DSP plug-in.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="73695-139">Формат: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="73695-139">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                           |
| <span data-ttu-id="73695-140">*кустоминтерфаценаме*</span><span class="sxs-lookup"><span data-stu-id="73695-140">*CustomInterfaceName*</span></span> | <span data-ttu-id="73695-141">Имя пользовательского интерфейса, реализуемого подключаемым модулем DSP. Пример: "Ипросеваредсп"</span><span class="sxs-lookup"><span data-stu-id="73695-141">The name of a custom interface that is implemented by the DSP plug-in.Example: "IProsewareDsp"</span></span><br/>                                                                                                                                                                  |
| <span data-ttu-id="73695-142">*нумберофмесодс*</span><span class="sxs-lookup"><span data-stu-id="73695-142">*NumberOfMethods*</span></span>     | <span data-ttu-id="73695-143">Количество методов, включая наследуемые методы, определенные настраиваемым интерфейсом. Пример: "5"</span><span class="sxs-lookup"><span data-stu-id="73695-143">The number of methods, including inherited methods, defined by a custom interface.Example: "5"</span></span><br/>                                                                                                                                                                  |



 

<span data-ttu-id="73695-144">Если подключаемый модуль DSP предоставляет страницу свойств, необходимо создать следующие подразделы и записи реестра на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="73695-144">If your DSP plug-in provides a property page, you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\PropPageClsid]
@=PropPageClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PropPageClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Apartment"
```



<span data-ttu-id="73695-145">В предыдущем синтаксисе реестра символы курсивом являются заполнителями для имен и глобально уникальных идентификаторов (GUID), характерных для подключаемого модуля DSP.</span><span class="sxs-lookup"><span data-stu-id="73695-145">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="73695-146">В следующей таблице описаны эти заполнители.</span><span class="sxs-lookup"><span data-stu-id="73695-146">The following table describes those placeholders.</span></span>



| <span data-ttu-id="73695-147">Заполнитель</span><span class="sxs-lookup"><span data-stu-id="73695-147">Placeholder</span></span>                 | <span data-ttu-id="73695-148">Описание</span><span class="sxs-lookup"><span data-stu-id="73695-148">Description</span></span>                                                                                                                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73695-149">*проппажеклсид*</span><span class="sxs-lookup"><span data-stu-id="73695-149">*PropPageClsid*</span></span>             | <span data-ttu-id="73695-150">Идентификатор GUID, который является идентификатором класса для класса страницы свойств, предоставляемого подключаемым модулем DSP. Этот GUID должен быть в формате реестра, заполненном фигурными скобками.</span><span class="sxs-lookup"><span data-stu-id="73695-150">A GUID that is the class identifier for the property page class provided by the DSP plug-in.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="73695-151">Формат: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="73695-151">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="73695-152">*проппажеклассфриендлинаме*</span><span class="sxs-lookup"><span data-stu-id="73695-152">*PropPageClassFriendlyName*</span></span> | <span data-ttu-id="73695-153">Понятное имя для класса страницы свойств. Пример: "класс страницы свойств Просеваредсп"</span><span class="sxs-lookup"><span data-stu-id="73695-153">A friendly name for the property page class.Example: "ProsewareDSP Property Page Class"</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="73695-154">*плугинмодуленаме*</span><span class="sxs-lookup"><span data-stu-id="73695-154">*PluginModuleName*</span></span>          | <span data-ttu-id="73695-155">Полный путь к библиотеке DLL, реализующей подключаемый модуль DSP. Пример: "C: \\ Program Files \\ Proseware \\ProsewareDsp.dll"</span><span class="sxs-lookup"><span data-stu-id="73695-155">The fully qualified path to the DLL that implements the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDsp.dll"</span></span><br/>                                                                                               |



 

<span data-ttu-id="73695-156">**Вызов Ивмпплугинрегистрар**</span><span class="sxs-lookup"><span data-stu-id="73695-156">**Calling IWMPPluginRegistrar**</span></span>

<span data-ttu-id="73695-157">В дополнение к подразделам и записям реестра, описанным в предыдущих списках и таблицах, необходимо создать некоторые разделы и записи реестра, вызвав [ивмпмедиаплугинрегистрар:: вмпрегистерплайерплугин](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin).</span><span class="sxs-lookup"><span data-stu-id="73695-157">In addition to the registry subkeys and entries described in the preceding lists and tables, you must create some registry keys and entries by calling [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin).</span></span> <span data-ttu-id="73695-158">Этот метод выполняет необходимую регистрацию, чтобы позволить проигрывателю Windows Media распознать подключаемый модуль и предоставить его пользователю в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="73695-158">This method performs the necessary registration to enable Windows Media Player to recognize your plug-in and present it as an option to the user.</span></span>

<span data-ttu-id="73695-159">Вызовите метод **ивмпмедиаплугинрегистрар:: вмпрегистерплайерплугин** в функции **DllRegisterServer** подключаемого модуля и вызовите [ивмпмедиаплугинрегистрар:: вмпунрегистерплайерплугин](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) в функции **DllUnregisterServer** подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="73695-159">Call **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** in your plug-in's **DllRegisterServer** function, and call [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) in your plug-in's **DllUnregisterServer** function.</span></span> <span data-ttu-id="73695-160">Чтобы получить указатель на интерфейс **ивмпмедиаплугинрегистрар** , вызовите **COCREATEINSTANCE**, передав CLSID \_ вмпмедиаплугинрегистрар в качестве идентификатора класса.</span><span class="sxs-lookup"><span data-stu-id="73695-160">To get a pointer to an **IWMPMediaPluginRegistrar** interface, call **CoCreateInstance**, passing CLSID\_WMPMediaPluginRegistrar as the Class ID.</span></span> <span data-ttu-id="73695-161">Константа CLSID \_ вмпмедиаплугинрегистрар определена в вмпсервицес. h.</span><span class="sxs-lookup"><span data-stu-id="73695-161">The constant CLSID\_WMPMediaPluginRegistrar is defined in wmpservices.h.</span></span>

<span data-ttu-id="73695-162">**Регистрация в мастере подключаемых модулей DSP**</span><span class="sxs-lookup"><span data-stu-id="73695-162">**Registration in the DSP Plug-in Wizard**</span></span>

<span data-ttu-id="73695-163">Мастер подключаемых модулей DSP, включенный в Windows SDK, создает образец кода, основанный на библиотеке активных шаблонов (ATL).</span><span class="sxs-lookup"><span data-stu-id="73695-163">The DSP plug-in wizard, which is included in the Windows SDK, generates sample code that is based on Active Template Library (ATL).</span></span> <span data-ttu-id="73695-164">В примере функции **DllRegisterServer** подключаемого модуля вызывается функция **регистерсервер** библиотеки ATL, которая создает подразделы и записи реестра в соответствии с двумя файлами скриптов реестра в проекте Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="73695-164">The sample plug-in's **DllRegisterServer** function calls ATL's **RegisterServer** function, which creates registry subkeys and entries according to two registry script files in the Visual Studio project.</span></span> <span data-ttu-id="73695-165">Файл *имяПроекта*. RGS содержит скрипт для регистрации основного класса подключаемого модуля, а свойство *имя_проекта файла ИмяПроекта* содержит скрипт для регистрации класса страницы свойств подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="73695-165">The file *ProjectName*.rgs contains the script for registering the plug-in's main class, and the file *ProjectName* PropPage.rgs contains the script for registering the plug-in's property page class.</span></span> <span data-ttu-id="73695-166">Пример функции **DllRegisterServer** подключаемого модуля также вызывает **Ивмпплугинрегистрар:: вмпрегистерплайерплугин**.</span><span class="sxs-lookup"><span data-stu-id="73695-166">The sample plug-in's **DllRegisterServer** function also calls **IWMPPluginRegistrar::WMPRegisterPlayerPlugin**.</span></span>

<span data-ttu-id="73695-167">Мастер подключаемых модулей DSP также создает код для компонента-заглушки прокси-сервера, который является самостоятельно регистрируемым файлом DLL.</span><span class="sxs-lookup"><span data-stu-id="73695-167">The DSP plug-in wizard also generates code for a proxy-stub component that is a self-registering .dll file.</span></span> <span data-ttu-id="73695-168">Код регистрации для этого файла находится в DLLDATA. cpp.</span><span class="sxs-lookup"><span data-stu-id="73695-168">The registration code for that file is in dlldata.cpp.</span></span> <span data-ttu-id="73695-169">Подпрограммы макроса **dlldata \_** расширяются для включения реализации **DllRegisterServer**.</span><span class="sxs-lookup"><span data-stu-id="73695-169">The macro **DLLDATA\_ROUTINES** expands to include an implementation of **DllRegisterServer**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73695-170">См. также</span><span class="sxs-lookup"><span data-stu-id="73695-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73695-171">**Обзор подключаемого модуля DSP**</span><span class="sxs-lookup"><span data-stu-id="73695-171">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="73695-172">**ивмпмедиаплугинрегистрар**</span><span class="sxs-lookup"><span data-stu-id="73695-172">**IWMPMediaPluginRegistrar**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar)
</dt> </dl>

 

 





