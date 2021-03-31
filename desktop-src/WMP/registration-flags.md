---
title: Флаги регистрации
description: Флаги регистрации
ms.assetid: ba1709c2-0fe5-4168-9aed-613d01eff21f
keywords:
- Подключаемые модули проигрывателя Windows Media, флаги регистрации
- подключаемые модули, флаги регистрации
- подключаемые модули пользовательского интерфейса, флаги регистрации
- Подключаемые модули пользовательского интерфейса, флаги регистрации
- Флаги, подключаемые модули пользовательского интерфейса
- реестр, подключаемые модули пользовательского интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac609b45866cd5f18edf61dffc2d3b7ac3c397ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069579"
---
# <a name="registration-flags"></a><span data-ttu-id="a3e46-109">Флаги регистрации</span><span class="sxs-lookup"><span data-stu-id="a3e46-109">Registration Flags</span></span>

<span data-ttu-id="a3e46-110">Когда мастер подключаемых модулей проигрывателя Windows Media создает новый проект подключаемого модуля пользовательского интерфейса, он создает в реестре раздел, содержащий сведения о подключаемом модуле.</span><span class="sxs-lookup"><span data-stu-id="a3e46-110">When the Windows Media Player Plug-in Wizard creates a new UI plug-in project, it creates a key in the registry that contains information about the plug-in.</span></span> <span data-ttu-id="a3e46-111">Этот раздел создается в следующем расположении:</span><span class="sxs-lookup"><span data-stu-id="a3e46-111">This key is created in the following location:</span></span>


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\UIPlugins\{ClassId}
```



<span data-ttu-id="a3e46-112">*ClassID* — это идентификатор класса подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="a3e46-112">*ClassId* is the class id of the plug-in.</span></span>

<span data-ttu-id="a3e46-113">Этот раздел включает следующие значения.</span><span class="sxs-lookup"><span data-stu-id="a3e46-113">This key includes the following values.</span></span>



| <span data-ttu-id="a3e46-114">Имя</span><span class="sxs-lookup"><span data-stu-id="a3e46-114">Name</span></span>                     | <span data-ttu-id="a3e46-115">Тип</span><span class="sxs-lookup"><span data-stu-id="a3e46-115">Type</span></span>       | <span data-ttu-id="a3e46-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a3e46-116">Description</span></span>                                                                                                                                                                               |
|--------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e46-117">Возможности</span><span class="sxs-lookup"><span data-stu-id="a3e46-117">Capabilities</span></span>             | <span data-ttu-id="a3e46-118">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="a3e46-118">REG\_DWORD</span></span> | <span data-ttu-id="a3e46-119">Значение типа DWORD, состоящее из по крайней мере одного флага типа подключаемого модуля, который может сочетаться с одним или несколькими флагами возможностей подключаемых модулей с помощью двоичных или бинарных операций.</span><span class="sxs-lookup"><span data-stu-id="a3e46-119">A DWORD value that consists of at least one plug-in type flag that may be combined with one or more plug-in capabilities flags by using binary OR operations.</span></span>                             |
| <span data-ttu-id="a3e46-120">Описание</span><span class="sxs-lookup"><span data-stu-id="a3e46-120">Description</span></span>              | <span data-ttu-id="a3e46-121">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a3e46-121">REG\_SZ</span></span>    | <span data-ttu-id="a3e46-122">Строка, содержащая описание подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="a3e46-122">A string that contains the description of the plug-in.</span></span> <span data-ttu-id="a3e46-123">Мастер подключаемых модулей создает строковый ресурс и предоставляет URL-адрес ресурса (с помощью протокола RES) для этого значения.</span><span class="sxs-lookup"><span data-stu-id="a3e46-123">The plug-in wizard creates a string resource and provides the URL of the resource (using the res protocol) for this value.</span></span>         |
| <span data-ttu-id="a3e46-124">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a3e46-124">FriendlyName</span></span>             | <span data-ttu-id="a3e46-125">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a3e46-125">REG\_SZ</span></span>    | <span data-ttu-id="a3e46-126">Строка, содержащая понятное для пользователя имя подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="a3e46-126">A string that contains the user-readable name for the plug-in.</span></span> <span data-ttu-id="a3e46-127">Мастер подключаемых модулей создает строковый ресурс и предоставляет URL-адрес ресурса (с помощью протокола RES) для этого значения.</span><span class="sxs-lookup"><span data-stu-id="a3e46-127">The plug-in wizard creates a string resource and provides the URL of the resource (using the res protocol) for this value.</span></span> |
| <span data-ttu-id="a3e46-128">Унинсталлпас (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a3e46-128">UninstallPath (optional)</span></span> | <span data-ttu-id="a3e46-129">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a3e46-129">REG\_SZ</span></span>    | <span data-ttu-id="a3e46-130">Строка, содержащая путь к исполняемому файлу, который удаляет подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="a3e46-130">A string that contains the path to an executable file that uninstalls the plug-in.</span></span>                                                                                                        |



 

<span data-ttu-id="a3e46-131">Дополнительные сведения о протоколе RES см. в пакете SDK для разработки в Интернете.</span><span class="sxs-lookup"><span data-stu-id="a3e46-131">For more information about the res protocol, see the Internet Development SDK.</span></span>

<span data-ttu-id="a3e46-132">В следующей таблице приведены флаги типа подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="a3e46-132">The following table details the plug-in type flags.</span></span>



| <span data-ttu-id="a3e46-133">Флаг типа подключаемого модуля</span><span class="sxs-lookup"><span data-stu-id="a3e46-133">Plug-in Type Flag</span></span>                | <span data-ttu-id="a3e46-134">Значение</span><span class="sxs-lookup"><span data-stu-id="a3e46-134">Value</span></span> | <span data-ttu-id="a3e46-135">Описание</span><span class="sxs-lookup"><span data-stu-id="a3e46-135">Description</span></span>                                       |
|----------------------------------|-------|---------------------------------------------------|
| <span data-ttu-id="a3e46-136">**\_фон типа подключаемого модуля \_**</span><span class="sxs-lookup"><span data-stu-id="a3e46-136">**PLUGIN\_TYPE\_BACKGROUND**</span></span>     | <span data-ttu-id="a3e46-137">0x1</span><span class="sxs-lookup"><span data-stu-id="a3e46-137">0x1</span></span>   | <span data-ttu-id="a3e46-138">Подключаемый модуль пользовательского интерфейса не отображает пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="a3e46-138">The UI plug-in does not display a user interface.</span></span> |
| <span data-ttu-id="a3e46-139">**Тип подключаемого модуля \_ \_ сепаратевиндов**</span><span class="sxs-lookup"><span data-stu-id="a3e46-139">**PLUGIN\_TYPE\_SEPARATEWINDOW**</span></span> | <span data-ttu-id="a3e46-140">0x2</span><span class="sxs-lookup"><span data-stu-id="a3e46-140">0x2</span></span>   | <span data-ttu-id="a3e46-141">Подключаемый модуль пользовательского интерфейса — это отдельный подключаемый модуль окна.</span><span class="sxs-lookup"><span data-stu-id="a3e46-141">The UI plug-in is a separate window plug-in.</span></span>      |
| <span data-ttu-id="a3e46-142">**Тип подключаемого модуля \_ \_ дисплайареа**</span><span class="sxs-lookup"><span data-stu-id="a3e46-142">**PLUGIN\_TYPE\_DISPLAYAREA**</span></span>    | <span data-ttu-id="a3e46-143">0x3</span><span class="sxs-lookup"><span data-stu-id="a3e46-143">0x3</span></span>   | <span data-ttu-id="a3e46-144">Подключаемый модуль пользовательского интерфейса является подключаемым модулем области просмотра.</span><span class="sxs-lookup"><span data-stu-id="a3e46-144">The UI plug-in is a display area plug-in.</span></span>         |
| <span data-ttu-id="a3e46-145">**Тип подключаемого модуля \_ \_ сеттингсареа**</span><span class="sxs-lookup"><span data-stu-id="a3e46-145">**PLUGIN\_TYPE\_SETTINGSAREA**</span></span>   | <span data-ttu-id="a3e46-146">0x4</span><span class="sxs-lookup"><span data-stu-id="a3e46-146">0x4</span></span>   | <span data-ttu-id="a3e46-147">Подключаемый модуль пользовательского интерфейса — это подключаемый модуль области параметров.</span><span class="sxs-lookup"><span data-stu-id="a3e46-147">The UI plug-in is a settings area plug-in.</span></span>        |
| <span data-ttu-id="a3e46-148">**Тип подключаемого модуля \_ \_ метадатаареа**</span><span class="sxs-lookup"><span data-stu-id="a3e46-148">**PLUGIN\_TYPE\_METADATAAREA**</span></span>   | <span data-ttu-id="a3e46-149">0x5</span><span class="sxs-lookup"><span data-stu-id="a3e46-149">0x5</span></span>   | <span data-ttu-id="a3e46-150">Подключаемый модуль пользовательского интерфейса является подключаемым модулем области метаданных.</span><span class="sxs-lookup"><span data-stu-id="a3e46-150">The UI plug-in is a metadata area plug-in.</span></span>        |



 

<span data-ttu-id="a3e46-151">В следующей таблице приведены флаги возможностей подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="a3e46-151">The following table details the plug-in capabilities flags.</span></span>



| <span data-ttu-id="a3e46-152">Флаг возможностей подключаемого модуля</span><span class="sxs-lookup"><span data-stu-id="a3e46-152">Plug-in Capabilities Flag</span></span>             | <span data-ttu-id="a3e46-153">Значение</span><span class="sxs-lookup"><span data-stu-id="a3e46-153">Value</span></span>      | <span data-ttu-id="a3e46-154">Описание</span><span class="sxs-lookup"><span data-stu-id="a3e46-154">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e46-155">**Флаги подключаемого модуля \_ \_ акцептсмедиа**</span><span class="sxs-lookup"><span data-stu-id="a3e46-155">**PLUGIN\_FLAGS\_ACCEPTSMEDIA**</span></span>       | <span data-ttu-id="a3e46-156">0x10000000</span><span class="sxs-lookup"><span data-stu-id="a3e46-156">0x10000000</span></span> | <span data-ttu-id="a3e46-157">Подключаемый модуль пользовательского интерфейса может принимать массивы указателей объектов **мультимедиа** , когда проигрыватель Windows Media вызывает [**Ивмпплугинуи:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="a3e46-157">The UI plug-in can accept **Media** object pointer arrays when Windows Media Player calls [**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a3e46-158">**Флаги подключаемого модуля \_ \_ акцептсплайлистс**</span><span class="sxs-lookup"><span data-stu-id="a3e46-158">**PLUGIN\_FLAGS\_ACCEPTSPLAYLISTS**</span></span>   | <span data-ttu-id="a3e46-159">0x8000000</span><span class="sxs-lookup"><span data-stu-id="a3e46-159">0x8000000</span></span>  | <span data-ttu-id="a3e46-160">Подключаемый модуль пользовательского интерфейса может принимать массивы указателей объектов **списков воспроизведения** , когда проигрыватель Windows Media вызывает [**Ивмпплугинуи:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="a3e46-160">The UI plug-in can accept **Playlist** object pointer arrays when Windows Media Player calls [**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a3e46-161">**Флаги подключаемого модуля \_ \_ хаспресетс**</span><span class="sxs-lookup"><span data-stu-id="a3e46-161">**PLUGIN\_FLAGS\_HASPRESETS**</span></span>         | <span data-ttu-id="a3e46-162">0x4000000</span><span class="sxs-lookup"><span data-stu-id="a3e46-162">0x4000000</span></span>  | <span data-ttu-id="a3e46-163">Подключаемый модуль пользовательского интерфейса использует предустановки.</span><span class="sxs-lookup"><span data-stu-id="a3e46-163">The UI plug-in uses presets.</span></span> <span data-ttu-id="a3e46-164">Если подключаемый модуль задает этот флаг, проигрыватель Windows Media выполнит запрос к подключаемому модулю для предустановленной информации путем вызова [**ивмпплугинуи::-Property**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .</span><span class="sxs-lookup"><span data-stu-id="a3e46-164">If the plug-in specifies this flag, Windows Media Player will query the plug-in for preset information by calling [**IWMPPluginUI::GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="a3e46-165">**Флаги подключаемого модуля \_ \_ хаспропертипаже**</span><span class="sxs-lookup"><span data-stu-id="a3e46-165">**PLUGIN\_FLAGS\_HASPROPERTYPAGE**</span></span>    | <span data-ttu-id="a3e46-166">0x80000000</span><span class="sxs-lookup"><span data-stu-id="a3e46-166">0x80000000</span></span> | <span data-ttu-id="a3e46-167">Подключаемый модуль пользовательского интерфейса предоставляет диалоговое окно страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="a3e46-167">The UI plug-in provides a property page dialog.</span></span> <span data-ttu-id="a3e46-168">Проигрыватель Windows Media вызовет [**ивмпплугинуи::D исплайпропертипаже**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) , если этот флаг установлен при вызове страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="a3e46-168">Windows Media Player will call [**IWMPPluginUI::DisplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) if this flag is set when the property page is invoked.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="a3e46-169">**Флаги подключаемого модуля \_ \_ скрыты**</span><span class="sxs-lookup"><span data-stu-id="a3e46-169">**PLUGIN\_FLAGS\_HIDDEN**</span></span>             | <span data-ttu-id="a3e46-170">0x02000000</span><span class="sxs-lookup"><span data-stu-id="a3e46-170">0x02000000</span></span> | <span data-ttu-id="a3e46-171">Подключаемый модуль фонового пользовательского интерфейса не отображается в меню " **подключаемые модули** ", доступ к которому осуществляется из меню " **вид** " или " **Сервис** ", или кнопка " **выбрать параметры воспроизведения** " в окне воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a3e46-171">The background UI plug-in does not appear on the **Plug-ins** menu that is accessed from the **View** or **Tools** menus or the **Select Now Playing options** button in Now Playing.</span></span> <span data-ttu-id="a3e46-172">Он отображается на вкладке **подключаемые** модули диалогового окна Параметры.</span><span class="sxs-lookup"><span data-stu-id="a3e46-172">It does appear on the **Plug-ins** tab of the Options dialog.</span></span> <span data-ttu-id="a3e46-173">В этом случае значок запуска фонового подключаемого модуля отображается в строке состояния. Этот флаг не влияет на подключаемые модули, отличные от фоновых подключаемых модулей пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a3e46-173">It does cause the Background Plug-in Running icon to appear in the status bar.This flag has no effect on plug-ins other than background UI plug-ins.</span></span><br/> |
| <span data-ttu-id="a3e46-174">**Флаги подключаемого модуля \_ \_ инсталлауторун**</span><span class="sxs-lookup"><span data-stu-id="a3e46-174">**PLUGIN\_FLAGS\_INSTALLAUTORUN**</span></span>     | <span data-ttu-id="a3e46-175">0x40000000</span><span class="sxs-lookup"><span data-stu-id="a3e46-175">0x40000000</span></span> | <span data-ttu-id="a3e46-176">Проигрыватель Windows Media автоматически запускает подключаемый модуль пользовательского интерфейса при установке подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="a3e46-176">Windows Media Player runs the UI plug-in automatically when the plug-in is installed.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="a3e46-177">**Флаги подключаемого модуля \_ \_ лаунчпропертипаже**</span><span class="sxs-lookup"><span data-stu-id="a3e46-177">**PLUGIN\_FLAGS\_LAUNCHPROPERTYPAGE**</span></span> | <span data-ttu-id="a3e46-178">0x20000000</span><span class="sxs-lookup"><span data-stu-id="a3e46-178">0x20000000</span></span> | <span data-ttu-id="a3e46-179">Проигрыватель Windows Media вызывает [**ивмпплугинуи::D исплайпропертипаже**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) при первом запуске подключаемого модуля пользовательского интерфейса. Если этот флаг указан, также следует указать **Флаги подключаемого модуля \_ \_ хаспропертипаже** .</span><span class="sxs-lookup"><span data-stu-id="a3e46-179">Windows Media Player calls [**IWMPPluginUI::DisplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) when the UI plug-in runs for the first time.If this flag is specified, **PLUGIN\_FLAGS\_HASPROPERTYPAGE** should be specified also.</span></span><br/>                                                                                                                                                             |



 

<span data-ttu-id="a3e46-180">В вмпплуг. h определены следующие константы.</span><span class="sxs-lookup"><span data-stu-id="a3e46-180">The following constants are defined in wmpplug.h.</span></span> <span data-ttu-id="a3e46-181">Не изменяйте значения, связанные с этими константами.</span><span class="sxs-lookup"><span data-stu-id="a3e46-181">Do not change the values associated with these constants.</span></span>



| <span data-ttu-id="a3e46-182">Имя</span><span class="sxs-lookup"><span data-stu-id="a3e46-182">Name</span></span>                                    | <span data-ttu-id="a3e46-183">Описание</span><span class="sxs-lookup"><span data-stu-id="a3e46-183">Description</span></span>                               |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="a3e46-184">**инсталлрегкэй подключаемого модуля \_**</span><span class="sxs-lookup"><span data-stu-id="a3e46-184">**PLUGIN\_INSTALLREGKEY**</span></span>               | <span data-ttu-id="a3e46-185">Расположение раздела реестра подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="a3e46-185">The location of the plug-in registry key.</span></span> |
| <span data-ttu-id="a3e46-186">**подключаемый модуль \_ инсталлрегкэй \_ FRIENDLYNAME**</span><span class="sxs-lookup"><span data-stu-id="a3e46-186">**PLUGIN\_INSTALLREGKEY\_FRIENDLYNAME**</span></span> | <span data-ttu-id="a3e46-187">Имя значения понятного имени.</span><span class="sxs-lookup"><span data-stu-id="a3e46-187">The name of the friendly name value.</span></span>      |
| <span data-ttu-id="a3e46-188">**Описание подключаемого модуля \_ инсталлрегкэй \_**</span><span class="sxs-lookup"><span data-stu-id="a3e46-188">**PLUGIN\_INSTALLREGKEY\_DESCRIPTION**</span></span>  | <span data-ttu-id="a3e46-189">Имя значения описания.</span><span class="sxs-lookup"><span data-stu-id="a3e46-189">The name of the description value.</span></span>        |
| <span data-ttu-id="a3e46-190">**\_возможности инсталлрегкэй подключаемого модуля \_**</span><span class="sxs-lookup"><span data-stu-id="a3e46-190">**PLUGIN\_INSTALLREGKEY\_CAPABILITIES**</span></span> | <span data-ttu-id="a3e46-191">Имя значения возможностей.</span><span class="sxs-lookup"><span data-stu-id="a3e46-191">The name of the capabilities value.</span></span>       |
| <span data-ttu-id="a3e46-192">**Удаление подключаемого модуля \_ инсталлрегкэй \_**</span><span class="sxs-lookup"><span data-stu-id="a3e46-192">**PLUGIN\_INSTALLREGKEY\_UNINSTALL**</span></span>    | <span data-ttu-id="a3e46-193">Имя значения пути удаления.</span><span class="sxs-lookup"><span data-stu-id="a3e46-193">The name of the uninstall path value.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="a3e46-194">См. также</span><span class="sxs-lookup"><span data-stu-id="a3e46-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3e46-195">**Ивмпплугинуи::D Исплайпропертипаже**</span><span class="sxs-lookup"><span data-stu-id="a3e46-195">**IWMPPluginUI::DisplayPropertyPage**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage)
</dt> <dt>

[<span data-ttu-id="a3e46-196">**Ивмпплугинуи:: Property**</span><span class="sxs-lookup"><span data-stu-id="a3e46-196">**IWMPPluginUI::GetProperty**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty)
</dt> <dt>

[<span data-ttu-id="a3e46-197">**Ивмпплугинуи:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="a3e46-197">**IWMPPluginUI::SetProperty**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)
</dt> <dt>

[<span data-ttu-id="a3e46-198">**Справочник по программированию подключаемых модулей пользовательского интерфейса**</span><span class="sxs-lookup"><span data-stu-id="a3e46-198">**User Interface Plug-ins Programming Reference**</span></span>](user-interface-plug-ins-programming-reference.md)
</dt> </dl>

 

 





