---
title: Простота регистрации специальных технологий
description: В этой статье объясняется, как зарегистрировать приложение со специальными возможностями в центре специальных возможностей. В нем также объясняется, как адаптировать приложение специальных возможностей, чтобы оно хорошо работало с защищенным рабочим столом.
ms.assetid: 6F1F2AAE-B2E4-4F26-8BDF-A3DE8F5C5460
ms.topic: article
ms.date: 04/02/2019
ms.openlocfilehash: 66901cd899fc578b032f86e3752fcdcac0788ba1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700904"
---
# <a name="ease-of-access---assistive-technology-registration"></a><span data-ttu-id="0a492-104">Простота регистрации специальных технологий</span><span class="sxs-lookup"><span data-stu-id="0a492-104">Ease of Access   Assistive Technology Registration</span></span>

<span data-ttu-id="0a492-105">В этой статье объясняется, как зарегистрировать приложение со специальными возможностями в центре специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="0a492-105">This article explains how to register an accessibility application with the Ease of Access Center.</span></span> <span data-ttu-id="0a492-106">В нем также объясняется, как адаптировать приложение специальных возможностей, чтобы оно хорошо работало с защищенным рабочим столом.</span><span class="sxs-lookup"><span data-stu-id="0a492-106">It also explains how to tailor your accessibility application so it works well with the secure desktop.</span></span>

<span data-ttu-id="0a492-107">Центр специальных возможностей — это приложение панели управления для Microsoft Windows, объединяющее функциональные возможности для специальных возможностей и простоты использования.</span><span class="sxs-lookup"><span data-stu-id="0a492-107">The Ease of Access Center is a Control Panel application for Microsoft Windows brings together functionality for accessibility and ease of use.</span></span> <span data-ttu-id="0a492-108">С помощью центра специальных возможностей пользователи могут настроить свои компьютеры в соответствии с их физическими и восприятными потребностями.</span><span class="sxs-lookup"><span data-stu-id="0a492-108">By using the Ease of Access Center, users can configure their computers to suit their physical and cognitive needs.</span></span>

<span data-ttu-id="0a492-109">Одной из функций центра специальных возможностей является помощь пользователям в запуске приложений специальных возможностей, включая экранный диктор, экранную клавиатуру и экранную лупу.</span><span class="sxs-lookup"><span data-stu-id="0a492-109">One function of the Ease of Access Center is to help users launch accessibility applications, including Narrator, On-Screen Keyboard, and Magnifier.</span></span> <span data-ttu-id="0a492-110">Зарегистрированные сторонние приложения также отображаются в центре замедления доступа и могут быть запущены непосредственно из.</span><span class="sxs-lookup"><span data-stu-id="0a492-110">Registered third-party applications also appear in the Ease of Access Center and can be launched directly from there.</span></span>

<span data-ttu-id="0a492-111">Приложения со специальными возможностями должны беспрепятственно работать с защищенным рабочим столом.</span><span class="sxs-lookup"><span data-stu-id="0a492-111">Accessibility applications need to work smoothly with the secure desktop.</span></span> <span data-ttu-id="0a492-112">Безопасный рабочий стол — это пользовательский интерфейс, который появляется, когда компьютер заблокирован (при входе в систему или когда пользователь заблокировал Рабочий стол) и когда пользователю предлагается разрешить потенциально небезопасное действие.</span><span class="sxs-lookup"><span data-stu-id="0a492-112">The secure desktop is the user interface that appears when the computer is locked (at log-on or when the user has locked the desktop), and when the user is prompted to allow a potentially unsafe action.</span></span> <span data-ttu-id="0a492-113">По соображениям безопасности Windows размещает ограничения на программное обеспечение сторонних разработчиков, работающее на защищенном рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="0a492-113">For security reasons, Windows places limits on third-party software running on the secure desktop.</span></span> <span data-ttu-id="0a492-114">Если вы хотите, чтобы приложение специальных возможностей выполнялось на защищенном рабочем столе, необходимо зарегистрировать приложение в центре специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="0a492-114">If you want your accessibility application to run on the secure desktop, you need to register the application with the Ease of Access Center.</span></span>

## <a name="registering-with-the-ease-of-access-center"></a><span data-ttu-id="0a492-115">Регистрация в центре специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="0a492-115">Registering with the Ease of Access Center</span></span>

<span data-ttu-id="0a492-116">Приложения специальных возможностей регистрируются в центре специальных возможностей, создавая один или несколько разделов реестра при установке приложения.</span><span class="sxs-lookup"><span data-stu-id="0a492-116">Accessibility applications register with the Ease of Access Center by creating one or more registry keys when the application is installed.</span></span> <span data-ttu-id="0a492-117">В следующей таблице перечислены сведения, содержащиеся в разделах реестра.</span><span class="sxs-lookup"><span data-stu-id="0a492-117">The following table lists the information contained in the registry keys.</span></span>



| <span data-ttu-id="0a492-118">Имя</span><span class="sxs-lookup"><span data-stu-id="0a492-118">Name</span></span>                        | <span data-ttu-id="0a492-119">Описание</span><span class="sxs-lookup"><span data-stu-id="0a492-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="0a492-120">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="0a492-120">Mandatory/Optional</span></span> | <span data-ttu-id="0a492-121">Язык</span><span class="sxs-lookup"><span data-stu-id="0a492-121">Language</span></span>      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------|
| <span data-ttu-id="0a492-122">Имя приложения</span><span class="sxs-lookup"><span data-stu-id="0a492-122">Application Name</span></span>            | <span data-ttu-id="0a492-123">Имя приложения, которое находится в файле ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a492-123">The name of the application, which is in a resource file.</span></span> <span data-ttu-id="0a492-124">Это значение реестра содержит строку в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="0a492-124">This registry value contains a string in a specified format.</span></span> <span data-ttu-id="0a492-125">Это может быть локализованная версия имени приложения, если приложение локализовано на языках, отличных от английского.</span><span class="sxs-lookup"><span data-stu-id="0a492-125">This could be a localized version of the application name, if the application is localized in languages other than English.</span></span> <span data-ttu-id="0a492-126">Имя отображается в центре замедления доступа.</span><span class="sxs-lookup"><span data-stu-id="0a492-126">The name appears in the Ease of Access Center.</span></span><br/>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="0a492-127">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0a492-127">Mandatory</span></span>          | <span data-ttu-id="0a492-128">Локального</span><span class="sxs-lookup"><span data-stu-id="0a492-128">Localized</span></span>     |
| <span data-ttu-id="0a492-129">атексе</span><span class="sxs-lookup"><span data-stu-id="0a492-129">ATExe</span></span>                       | <span data-ttu-id="0a492-130">Имя исполняемого файла или образа приложения.</span><span class="sxs-lookup"><span data-stu-id="0a492-130">The name of the application executable file or image.</span></span> <span data-ttu-id="0a492-131">Windows использует это значение, чтобы определить, выполняется ли приложение со специальными возможностями.</span><span class="sxs-lookup"><span data-stu-id="0a492-131">Windows uses this value to determine whether the accessibility application is running.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="0a492-132">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0a492-132">Mandatory</span></span>          | <span data-ttu-id="0a492-133">Не локализовано</span><span class="sxs-lookup"><span data-stu-id="0a492-133">Not localized</span></span> |
| <span data-ttu-id="0a492-134">кописеттингстолоккеддесктоп</span><span class="sxs-lookup"><span data-stu-id="0a492-134">CopySettingsToLockedDesktop</span></span> | <span data-ttu-id="0a492-135">Значение **типа DWORD** , указывающее, следует ли копировать параметры приложения специальных возможностей на заблокированный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="0a492-135">A **DWORD** value that indicates whether to copy the accessibility application's settings to the locked desktop.</span></span><br/> <span data-ttu-id="0a492-136">Если это значение равно 1, приложение может записывать параметры в расположение в реестре пользователя, и Windows копирует параметры в то же расположение в реестре пользователя для заблокированного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="0a492-136">If this value is 1, the application can write settings to a location in the user registry, and Windows copies the settings to the same location in the user registry for the locked desktop.</span></span> <span data-ttu-id="0a492-137">Это позволяет приложению сохранять свое состояние с "нормального" рабочего стола на заблокированном рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="0a492-137">This enables the application to persist its state from the "normal" desktop to the locked desktop.</span></span><br/>                                                                                                                                                             | <span data-ttu-id="0a492-138">Необязательно</span><span class="sxs-lookup"><span data-stu-id="0a492-138">Optional</span></span>           | <span data-ttu-id="0a492-139">Не локализовано</span><span class="sxs-lookup"><span data-stu-id="0a492-139">Not localized</span></span> |
| <span data-ttu-id="0a492-140">Описание</span><span class="sxs-lookup"><span data-stu-id="0a492-140">Description</span></span>                 | <span data-ttu-id="0a492-141">Краткое описание приложения из файла ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a492-141">A brief description of the application, from a resource file.</span></span> <span data-ttu-id="0a492-142">Это значение реестра содержит строку в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="0a492-142">This registry value contains a string in a specified format.</span></span> <span data-ttu-id="0a492-143">Это может быть локализованная версия описания, если приложение локализовано на языках, отличных от английского.</span><span class="sxs-lookup"><span data-stu-id="0a492-143">This could be a localized version of the description, if the application is localized in languages other than English.</span></span> <span data-ttu-id="0a492-144">Длина этой строки должна быть меньше 512 символов.</span><span class="sxs-lookup"><span data-stu-id="0a492-144">The length of this string must be less than 512 characters.</span></span><br/> <span data-ttu-id="0a492-145">Описание отображается в центре специальных возможностей, чтобы предоставить пользователю дополнительные сведения о приложении для доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="0a492-145">The description appears in the Ease of Access Center to provide additional information about the accessibility application to the user.</span></span><br/> <span data-ttu-id="0a492-146">Это значение также может использоваться для уведомления пользователя о том, что приложение не используется в защищенном рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="0a492-146">This value can also be used to notify the user that the application is not used on the secure desktop.</span></span><br/>      | <span data-ttu-id="0a492-147">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0a492-147">Mandatory</span></span>          | <span data-ttu-id="0a492-148">Локального</span><span class="sxs-lookup"><span data-stu-id="0a492-148">Localized</span></span>     |
| <span data-ttu-id="0a492-149">Профиль</span><span class="sxs-lookup"><span data-stu-id="0a492-149">Profile</span></span>                     | <span data-ttu-id="0a492-150">Небольшая часть XML, указывающая, что предоставляет приложение.</span><span class="sxs-lookup"><span data-stu-id="0a492-150">A short piece of XML that specifies the accommodations that the application provides.</span></span> <span data-ttu-id="0a492-151">Это гарантирует, что приложение появится в правильной категории в центре специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="0a492-151">It ensures that the application appears under the correct category in the Ease of Access Center.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="0a492-152">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0a492-152">Mandatory</span></span>          | <span data-ttu-id="0a492-153">Не локализовано</span><span class="sxs-lookup"><span data-stu-id="0a492-153">Not localized</span></span> |
| <span data-ttu-id="0a492-154">пассивеаутостартбехавиор</span><span class="sxs-lookup"><span data-stu-id="0a492-154">PassiveAutoStartBehavior</span></span>    | <p><span data-ttu-id="0a492-155">Значение **типа DWORD** , указывающее, включено ли устаревшее поведение автоматического запуска.</span><span class="sxs-lookup"><span data-stu-id="0a492-155">A **DWORD** value that indicates whether legacy auto-start behavior is enabled.</span></span></p><p><span data-ttu-id="0a492-156">Значение по умолчанию — 0, что означает, что для в требуется устаревшее поведение автоматического запуска.</span><span class="sxs-lookup"><span data-stu-id="0a492-156">The default value is 0, which indicates that an AT requires legacy auto-start behavior.</span></span> <span data-ttu-id="0a492-157">Это приводит к тому, что параметр "запустить после входа" для этого параметра будет установлен в диалоговом окне "экран" (OOBE) и панели управления (см. раздел **Панель управления — > простота доступа > простота центра доступа — > изменить параметры входа**) и автоматически запустится после UAC и экрана блокировки.</span><span class="sxs-lookup"><span data-stu-id="0a492-157">This  causes the “Start after sign-in” setting for that AT to be checked in the Out Of Box Experience (OOBE) and Control Panel (see **Control Panel -> Ease of Access -> Ease of Access Center -> Change sign-in settings**), and automatically starts the AT after UAC and lock-screen.</span></span></p><p><span data-ttu-id="0a492-158">Значение 1 указывает, что в необходимо использовать новое поведение автоматического запуска, при котором параметр "запустить после входа" для этого параметра не установлен в окне "завершение работы" (OOBE) и на панели управления, а компонент "автоматически" запускается один раз в сеансе пользователя (при входе), только если установлен флажок "запустить после входа".</span><span class="sxs-lookup"><span data-stu-id="0a492-158">A value of 1 indicates that the AT should use the new auto-start behavior where the “Start after sign-in” setting for that AT is not checked in the Out Of Box Experience (OOBE) and Control Panel, and the AT is automatically started once per user session (at login) only if the “start after sign-in” setting is checked.</span></span></p>                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="0a492-159">Необязательно</span><span class="sxs-lookup"><span data-stu-id="0a492-159">Optional</span></span>          | <span data-ttu-id="0a492-160">Не локализовано</span><span class="sxs-lookup"><span data-stu-id="0a492-160">Not localized</span></span> |
| <span data-ttu-id="0a492-161">секуредесктопаккоммодатион</span><span class="sxs-lookup"><span data-stu-id="0a492-161">SecureDesktopAccommodation</span></span>  | <span data-ttu-id="0a492-162">Имя альтернативного приложения специальных возможностей для запуска на защищенном рабочем столе в месте этого приложения.</span><span class="sxs-lookup"><span data-stu-id="0a492-162">The name of an alternate accessibility application to run on the secure desktop in the place of this application.</span></span> <span data-ttu-id="0a492-163">Альтернативой может быть другое приложение, другая версия того же приложения, одно из приложений специальных возможностей, включенных в Windows, или «нет», если вы не хотите запускать какое-либо приложение специальных возможностей на защищенном рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="0a492-163">The alternate can be a different application, a different version of the same application, one of the accessibility applications that is included in Windows, or "none" if you do not want to run any accessibility application on the secure desktop.</span></span> <br/>                                                                                                                                                                                                               | <span data-ttu-id="0a492-164">Необязательно</span><span class="sxs-lookup"><span data-stu-id="0a492-164">Optional</span></span>           | <span data-ttu-id="0a492-165">Не локализовано</span><span class="sxs-lookup"><span data-stu-id="0a492-165">Not localized</span></span> |
| <span data-ttu-id="0a492-166">Простой профиль</span><span class="sxs-lookup"><span data-stu-id="0a492-166">Simple Profile</span></span>              | <span data-ttu-id="0a492-167">Значение, которое описывает, как классифицировать приложение в виде слова или двух: средство чтения с экрана, экранная лупа или экранная клавиатура, например.</span><span class="sxs-lookup"><span data-stu-id="0a492-167">A value that describes how to classify the application in a word or two: Screen reader, Magnifier, or On-screen keyboard, for example.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="0a492-168">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0a492-168">Mandatory</span></span>          | <span data-ttu-id="0a492-169">Не локализовано</span><span class="sxs-lookup"><span data-stu-id="0a492-169">Not localized</span></span> |
| <span data-ttu-id="0a492-170">StartExe</span><span class="sxs-lookup"><span data-stu-id="0a492-170">StartExe</span></span>                    | <span data-ttu-id="0a492-171">Полный путь к исполняемому файлу.</span><span class="sxs-lookup"><span data-stu-id="0a492-171">The full path of the executable.</span></span> <span data-ttu-id="0a492-172">Это значение используется для запуска приложения со специальными возможностями.</span><span class="sxs-lookup"><span data-stu-id="0a492-172">This value is used to launch the accessibility application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="0a492-173">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0a492-173">Mandatory</span></span>          | <span data-ttu-id="0a492-174">Не локализовано</span><span class="sxs-lookup"><span data-stu-id="0a492-174">Not localized</span></span> |
| <span data-ttu-id="0a492-175">стартпарамс</span><span class="sxs-lookup"><span data-stu-id="0a492-175">StartParams</span></span>                 | <span data-ttu-id="0a492-176">аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="0a492-176">Command-line arguments.</span></span> <span data-ttu-id="0a492-177">Эти значения используются вместе с StartExe для запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="0a492-177">These values are used along with StartExe to start the application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="0a492-178">Необязательно</span><span class="sxs-lookup"><span data-stu-id="0a492-178">Optional</span></span>           | <span data-ttu-id="0a492-179">Не локализовано</span><span class="sxs-lookup"><span data-stu-id="0a492-179">Not localized</span></span> |
| <span data-ttu-id="0a492-180">терминатеондесктопсвитч</span><span class="sxs-lookup"><span data-stu-id="0a492-180">TerminateOnDesktopSwitch</span></span>    | <span data-ttu-id="0a492-181">Значение **типа DWORD** , указывающее, как приложение со специальными возможностями реагирует на переходы от защищенного рабочего стола или от него.</span><span class="sxs-lookup"><span data-stu-id="0a492-181">A **DWORD** value that specifies how the accessibility application responds to transitions to or from the secure desktop.</span></span><br/> <span data-ttu-id="0a492-182">Если это значение не существует или равно 1, Windows завершает работу и перезапускает приложение при каждом переходе на защищенный рабочий стол или с него.</span><span class="sxs-lookup"><span data-stu-id="0a492-182">If this value does not exist or is 1, Windows terminates and restarts the application on each transition to or from the secure desktop.</span></span> <span data-ttu-id="0a492-183">Это поведение установлено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0a492-183">This is the default behavior.</span></span><br/> <span data-ttu-id="0a492-184">Если это значение равно 0, Windows не будет завершать работу приложения со специальными возможностями при переходе на Рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="0a492-184">If this value is 0, Windows does not terminate the accessibility application on a desktop transition.</span></span> <span data-ttu-id="0a492-185">Приложение продолжит работу на предыдущем рабочем столе, и Windows запустит новый экземпляр на новом рабочем столе, если на нем еще не запущен экземпляр.</span><span class="sxs-lookup"><span data-stu-id="0a492-185">The application continues to run on the previous desktop, and Windows starts a new instance on the new desktop if an instance is not already running there.</span></span><br/> | <span data-ttu-id="0a492-186">Необязательно</span><span class="sxs-lookup"><span data-stu-id="0a492-186">Optional</span></span>           | <span data-ttu-id="0a492-187">Не локализовано</span><span class="sxs-lookup"><span data-stu-id="0a492-187">Not localized</span></span> |


 

### <a name="localization"></a><span data-ttu-id="0a492-188">Локализация</span><span class="sxs-lookup"><span data-stu-id="0a492-188">Localization</span></span>

<span data-ttu-id="0a492-189">Значения реестра для имени и описания приложения должны быть локализованы для поддержки многоязыкового интерфейса пользователя (MUI).</span><span class="sxs-lookup"><span data-stu-id="0a492-189">The registry values of Application Name and Description need to be localizable to support Multilingual User Interface (MUI).</span></span>

<span data-ttu-id="0a492-190">Эти строки имеют следующий формат, где угловые скобки обозначают обязательные элементы, а квадратные скобки обозначают необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="0a492-190">These strings are in the following format, where angle brackets signify required elements and square brackets signify an optional element.</span></span>

<span data-ttu-id="0a492-191">*@ <Ресдллпас \\ ресдллфиленаме>,- <resID> \[ ;<comment>\]*</span><span class="sxs-lookup"><span data-stu-id="0a492-191">*@<ResDllPath\\ResDLLFilename>,-<resID>\[;<comment>\]*</span></span>

<span data-ttu-id="0a492-192">*<ресдллпас \\ Ресдллфиленаме>* — это путь к библиотеке DLL ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a492-192">*<ResDllPath\\ResDLLFilename>* is the path to the resource DLL.</span></span> <span data-ttu-id="0a492-193">Путь может содержать переменные среды.</span><span class="sxs-lookup"><span data-stu-id="0a492-193">The path can contain environmental variables.</span></span>

<span data-ttu-id="0a492-194">*<resID>* Идентификатор ресурса для строки.</span><span class="sxs-lookup"><span data-stu-id="0a492-194">*<resID>* is the resource ID for the string.</span></span>

<span data-ttu-id="0a492-195">*\[ комментарий \]* содержит любые необязательные комментарии.</span><span class="sxs-lookup"><span data-stu-id="0a492-195">*\[comment\]* contains any optional comments.</span></span>

<span data-ttu-id="0a492-196">Пример:</span><span class="sxs-lookup"><span data-stu-id="0a492-196">Here is an example:</span></span>


```
@%SystemRoot%\system32\anyAT.dll,-5020
```



<span data-ttu-id="0a492-197">Дополнительные сведения о MUI см. в [статье центр знаний Windows MUI](../intl/about-multilingual-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="0a492-197">For more information about MUI, see [Windows MUI Knowledge Center](../intl/about-multilingual-user-interface.md).</span></span>

### <a name="hci-profile"></a><span data-ttu-id="0a492-198">Профиль ХЦИ</span><span class="sxs-lookup"><span data-stu-id="0a492-198">HCI Profile</span></span>

<span data-ttu-id="0a492-199">Профиль взаимодействия с человеком (ХЦИ) позволяет определить, какие именно сведения должны быть предоставлены в зависимости от потребностей пользователя.</span><span class="sxs-lookup"><span data-stu-id="0a492-199">The Human Computer Interaction (HCI) profile is a way to determine what accommodations to provide based on the needs of the user.</span></span> <span data-ttu-id="0a492-200">Приложения со специальными возможностями должны регистрировать сведения о типе инвалидности, которые может поддерживать приложение.</span><span class="sxs-lookup"><span data-stu-id="0a492-200">Accessibility applications should register information about the kind of disability the application helps to accommodate.</span></span>

<span data-ttu-id="0a492-201">Значение реестра Profile содержит XML-код, описывающий разновидность инвалидности, которая является целью приложения специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="0a492-201">The Profile registry value contains XML that describes the kind of disability targeted by the accessibility application.</span></span> <span data-ttu-id="0a492-202">Этот XML имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="0a492-202">This XML has the following format:</span></span>


```XML
<HCIModel>
<Accommodation type="disability"/>
</HCIModel>
```



<span data-ttu-id="0a492-203">Для атрибута **типа проживания** допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0a492-203">The valid values for the **Accommodation type** attribute are as follows:</span></span>

-   <span data-ttu-id="0a492-204">Концепция умеренного зрения</span><span class="sxs-lookup"><span data-stu-id="0a492-204">mild vision</span></span>
-   <span data-ttu-id="0a492-205">серьезное видение</span><span class="sxs-lookup"><span data-stu-id="0a492-205">severe vision</span></span>
-   <span data-ttu-id="0a492-206">Неумеренное восприятие</span><span class="sxs-lookup"><span data-stu-id="0a492-206">mild cognitive</span></span>
-   <span data-ttu-id="0a492-207">серьезное восприятие</span><span class="sxs-lookup"><span data-stu-id="0a492-207">severe cognitive</span></span>
-   <span data-ttu-id="0a492-208">подвижность (умеренно)</span><span class="sxs-lookup"><span data-stu-id="0a492-208">mild dexterity</span></span>
-   <span data-ttu-id="0a492-209">серьезная подвижность</span><span class="sxs-lookup"><span data-stu-id="0a492-209">severe dexterity</span></span>
-   <span data-ttu-id="0a492-210">слух (умеренно)</span><span class="sxs-lookup"><span data-stu-id="0a492-210">mild hearing</span></span>
-   <span data-ttu-id="0a492-211">серьезный слух</span><span class="sxs-lookup"><span data-stu-id="0a492-211">severe hearing</span></span>
-   <span data-ttu-id="0a492-212">распознавание речи (умеренно)</span><span class="sxs-lookup"><span data-stu-id="0a492-212">mild speech</span></span>
-   <span data-ttu-id="0a492-213">серьезное распознавание речи</span><span class="sxs-lookup"><span data-stu-id="0a492-213">severe speech</span></span>

> [!Note]  
> <span data-ttu-id="0a492-214">Эти значения указываются с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="0a492-214">These values are case sensitive.</span></span>

 

<span data-ttu-id="0a492-215">Если приложение со специальными возможностями поддерживает несколько размещений, значение реестра Profile должно включать атрибут **типа проживания** для каждого размещения.</span><span class="sxs-lookup"><span data-stu-id="0a492-215">If an accessibility application supports multiple accommodations, the Profile registry value should include an **Accommodation type** attribute for each accommodation.</span></span>

### <a name="ease-of-access-registry-details"></a><span data-ttu-id="0a492-216">Сведения о реестре специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="0a492-216">Ease of Access registry details</span></span>

<span data-ttu-id="0a492-217">Чтобы зарегистрировать приложение специальных возможностей, необходимо создать ключ для приложения в следующем расположении реестра и заполнить его парами "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="0a492-217">To register your accessibility application, you need to create a key for your application at the following registry location and populate it with name-value pairs.</span></span>

<span data-ttu-id="0a492-218">**HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATS\\**</span><span class="sxs-lookup"><span data-stu-id="0a492-218">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\**</span></span>

<span data-ttu-id="0a492-219">Присвойте разделу реестра приложения имя в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="0a492-219">Name your application's registry key using the following format:</span></span>

<span data-ttu-id="0a492-220">*"CompanyName \_ ProductName \_ v \# "*</span><span class="sxs-lookup"><span data-stu-id="0a492-220">*"CompanyName\_ProductName\_v\#"*</span></span>

<span data-ttu-id="0a492-221">Например, "Contoso \_ лупой \_ v 2.0".</span><span class="sxs-lookup"><span data-stu-id="0a492-221">For example, "Contoso\_Magnifier\_v2.0".</span></span>

<span data-ttu-id="0a492-222">Чтобы добавить значения реестра, программа установки должна быть запущена с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="0a492-222">To add registry values, your installation program must be running with elevated privileges.</span></span>

### <a name="secure-desktop-accommodation"></a><span data-ttu-id="0a492-223">Безопасное настольное проживание</span><span class="sxs-lookup"><span data-stu-id="0a492-223">Secure desktop accommodation</span></span>

<span data-ttu-id="0a492-224">Раздел реестра **секуредесктопаккоммодатион** позволяет указать, как приложение со специальными возможностями реагирует на защищенный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="0a492-224">The **SecureDesktopAccommodation** registry key lets you specify how your accessibility application responds to the secure desktop.</span></span> <span data-ttu-id="0a492-225">По умолчанию центр специальных возможностей запускает приложение на безопасном рабочем столе, если оно уже было запущено на нормальном рабочем столе, или если оно настроено для запуска на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="0a492-225">By default, the Ease of Access Center launches your application on the secure desktop if it was already running on the normal desktop, or if it is configured to run on the logon desktop.</span></span> <span data-ttu-id="0a492-226">С помощью ключа **секуредесктопаккоммодатион** можно:</span><span class="sxs-lookup"><span data-stu-id="0a492-226">By using the **SecureDesktopAccommodation** key, you can:</span></span>

-   <span data-ttu-id="0a492-227">Укажите альтернативную версию приложения для использования на защищенном рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="0a492-227">Specify an alternate version of your application for use on the secure desktop.</span></span> <span data-ttu-id="0a492-228">Например, у вас может быть альтернативная версия, которая отключает небезопасные функции или оптимизирована для использования меньшего объема памяти и ускоряет запуск.</span><span class="sxs-lookup"><span data-stu-id="0a492-228">For example, you might have an alternate version that disables unsecured features, or is optimized to use less memory and launch faster.</span></span>

    <span data-ttu-id="0a492-229">Чтобы указать альтернативную версию, задайте для ключа **секуредесктопаккоммодатион** имя альтернативной версии.</span><span class="sxs-lookup"><span data-stu-id="0a492-229">To specify the alternate version, set the **SecureDesktopAccommodation** key to the name of the alternate version.</span></span> <span data-ttu-id="0a492-230">Например, если приложение зарегистрировано на \_ ключе средства чтения с экрана Contoso \_ версии 1.0, можно зарегистрировать альтернативную версию на экране Contoso \_ Screen реадерсекуре \_ v 1.0.</span><span class="sxs-lookup"><span data-stu-id="0a492-230">For example, if you registered your application at the Contoso\_Screen Reader\_v1.0 key, you could register the alternate version at Contoso\_Screen ReaderSecure\_v1.0.</span></span> <span data-ttu-id="0a492-231">Затем установите для ключа **Секуредесктопаккоммодатион** \_ средства чтения с экрана Contoso \_ v 1.0 значение "Contoso \_ Screen реадерсекуре \_ v 1.0".</span><span class="sxs-lookup"><span data-stu-id="0a492-231">Then, set the **SecureDesktopAccommodation** key of Contoso\_Screen Reader\_v1.0 to "Contoso\_Screen ReaderSecure\_v1.0".</span></span>

-   <span data-ttu-id="0a492-232">Укажите приложение Microsoft Accessibility для использования в защищенном рабочем столе вместо приложения.</span><span class="sxs-lookup"><span data-stu-id="0a492-232">Specify a Microsoft accessibility application to use on the secure desktop in place of your application.</span></span> <span data-ttu-id="0a492-233">Для этого параметра задайте для **секуредесктопаккоммодатион** имя конкретного приложения Microsoft Accessibility: "ОСК", "магнифиерпане" или "Экранный диктор".</span><span class="sxs-lookup"><span data-stu-id="0a492-233">For this option, set **SecureDesktopAccommodation** to the name of the particular Microsoft accessibility application: "osk", "magnifierpane", or "Narrator".</span></span>
-   <span data-ttu-id="0a492-234">Укажите, что приложение не должно запускаться на защищенном рабочем столе, и ни на какое другое приложение не следует.</span><span class="sxs-lookup"><span data-stu-id="0a492-234">Specify that your application should not run on the secure desktop, and neither should any alternate application.</span></span> <span data-ttu-id="0a492-235">Для этого параметра задайте для **секуредесктопаккоммодатион** значение "нет" (рекомендуется) или имя несуществующего приложения.</span><span class="sxs-lookup"><span data-stu-id="0a492-235">For this option, set **SecureDesktopAccommodation** to "none" (recommend) or the name of a nonexistent application.</span></span>

<span data-ttu-id="0a492-236">Если раздел реестра **секуредесктопаккоммодатион** для приложения специальных возможностей Указывает приложение Microsoft Accessibility для запуска на защищенном рабочем столе вместо приложения, Windows уведомляет пользователя об этом при переходе на защищенный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="0a492-236">If the **SecureDesktopAccommodation** registry key for your accessibility application specifies a Microsoft accessibility application to run on the secure desktop in place of your application, Windows notifies the user of this when making the transition to the secure desktop.</span></span> <span data-ttu-id="0a492-237">Чтобы уведомить пользователя, Windows выводит строку, указанную в разделе реестра Description для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="0a492-237">To notify the user, Windows displays the string specified in the Description registry key for your application.</span></span> <span data-ttu-id="0a492-238">Например, если приложение Скринреадер Deluxe 1,0 использует экранный диктор Майкрософт на защищенном рабочем столе, он будет содержать строку описания, например "Экранный диктор Майкрософт будет использоваться в заблокированном, входном и других защищенных настольных компьютерах вместо Скринреадер Deluxe 1,0".</span><span class="sxs-lookup"><span data-stu-id="0a492-238">For example, if the ScreenReader Deluxe 1.0 application uses Microsoft Narrator on the secure desktop, it would include a Description string such as, "Microsoft Narrator will be used in the locked, logon, and other secure desktops in place of ScreenReader Deluxe 1.0."</span></span>

<span data-ttu-id="0a492-239">Если для ключа **секуредесктопаккоммодатион** вашего приложения задано значение "нет", используйте ключ **описания** , чтобы сообщить пользователю, что приложение недоступно на защищенном рабочем столе, а альтернативы не предоставлены.</span><span class="sxs-lookup"><span data-stu-id="0a492-239">If your application's **SecureDesktopAccommodation** key is set to "none", use the **Description** key to tell the user your application is not available on the secure desktop and no alternative is provided.</span></span>

<span data-ttu-id="0a492-240">Windows отображает текст описания в соответствующих местах центра специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="0a492-240">Windows displays the Description text in the relevant locations in the Ease of Access Center.</span></span>

### <a name="running-at-installation-and-on-the-logon-desktop"></a><span data-ttu-id="0a492-241">Запуск при установке и на рабочем столе входа в систему</span><span class="sxs-lookup"><span data-stu-id="0a492-241">Running at installation and on the logon desktop</span></span>

<span data-ttu-id="0a492-242">Если вы добавите имя зарегистрированного ключа приложения специальных возможностей в строку в следующем расположении реестра, Windows запустит приложение сразу после установки.</span><span class="sxs-lookup"><span data-stu-id="0a492-242">If you append your accessibility application's registered key name to the string at the following registry location, Windows will launch your application immediately after it is installed.</span></span> <span data-ttu-id="0a492-243">Кроме того, Windows автоматически запустит приложение, когда активен вход в систему.</span><span class="sxs-lookup"><span data-stu-id="0a492-243">Also, Windows will automatically run your application whenever the logon desktop is active.</span></span>

<span data-ttu-id="0a492-244">**\\ \\ \\ \\ \\ Настройка специальных возможностей в HKCU Software Microsoft Windows NT CurrentVersion \\**</span><span class="sxs-lookup"><span data-stu-id="0a492-244">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\Configuration**</span></span>

<span data-ttu-id="0a492-245">Ключ конфигурации представляет собой строку с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="0a492-245">The Configuration key is a comma-delimited string.</span></span> <span data-ttu-id="0a492-246">Чтобы добавить приложение, добавьте строку, совпадающую с ключом реестра приложения, в HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATS \\ .</span><span class="sxs-lookup"><span data-stu-id="0a492-246">To add your application, append a string that is the same as your application's registry key at HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\.</span></span>

### <a name="running-in-a-job"></a><span data-ttu-id="0a492-247">Выполнение в задании</span><span class="sxs-lookup"><span data-stu-id="0a492-247">Running in a job</span></span>

<span data-ttu-id="0a492-248">Если раздел реестра **терминатеондесктопсвитч** отсутствует или имеет ненулевое значение, Windows запускает приложение в контексте задания, завершая и перезапуская приложение при каждом переходе к рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="0a492-248">If the **TerminateOnDesktopSwitch** registry key is not present or is set to non-zero, Windows runs the application in the context of a job, terminating and restarting the application with each desktop transition.</span></span> <span data-ttu-id="0a492-249">Выполнение в задании гарантирует, что только один экземпляр приложения выполняется в определенный момент времени, и освобождает приложение от необходимости наблюдения за состоянием рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="0a492-249">Running in a job ensures that only a single instance of the application is running at a particular time, and frees the application from having to monitor the desktop state.</span></span> <span data-ttu-id="0a492-250">Ниже перечислены недостатки выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="0a492-250">The disadvantages of running in a job include:</span></span>

-   <span data-ttu-id="0a492-251">При каждом переходе к рабочему столу приложение привлечет затраты на запуск.</span><span class="sxs-lookup"><span data-stu-id="0a492-251">The application incurs a startup cost with each desktop transition.</span></span>
-   <span data-ttu-id="0a492-252">Приложение можно запустить только через центр специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="0a492-252">The application can be started only through the Ease of Access Center.</span></span>
-   <span data-ttu-id="0a492-253">Приложение должно постоянно сохранять свои параметры, так как оно может быть прервано в любой момент при переходе на Рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="0a492-253">The application must continually save its settings because it can be terminated at any time by a desktop transition.</span></span>

<span data-ttu-id="0a492-254">Если ключ **терминатеондесктопсвитч** существует и имеет значение 0, Windows не запускает приложение со специальными возможностями в задании.</span><span class="sxs-lookup"><span data-stu-id="0a492-254">If the **TerminateOnDesktopSwitch** key exists and is set to 0, Windows doesn't run the accessibility application in a job.</span></span> <span data-ttu-id="0a492-255">Подобное разделение обеспечивает следующие преимущества.</span><span class="sxs-lookup"><span data-stu-id="0a492-255">This has the following advantages:</span></span>

-   <span data-ttu-id="0a492-256">Затраты на запуск не связаны с переходами настольных систем.</span><span class="sxs-lookup"><span data-stu-id="0a492-256">No startup costs are associated with desktop transitions.</span></span>
-   <span data-ttu-id="0a492-257">Приложение может быть запущено за пределами центра доступа.</span><span class="sxs-lookup"><span data-stu-id="0a492-257">The application can be started outside of the Ease of Access Center.</span></span>

<span data-ttu-id="0a492-258">Ниже перечислены недостатки, которые не выполняются в задании.</span><span class="sxs-lookup"><span data-stu-id="0a492-258">The disadvantages of not running in a job include:</span></span>

-   <span data-ttu-id="0a492-259">Поскольку приложение перезапускается при переходах настольных систем, оно должно обнаруживать, когда текущий рабочий стол неактивен, и отвечать соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="0a492-259">Because the application isn t restarted on desktop transitions, it must detect when the current desktop is inactive and respond appropriately.</span></span> <span data-ttu-id="0a492-260">Например, приложение должно освобождать управление оборудованием, чтобы его можно было использовать в защищенной версии приложения, и приложение должно перейти в спящий режим, чтобы избежать использования ресурсов процессора.</span><span class="sxs-lookup"><span data-stu-id="0a492-260">For example, the application must relinquish control of hardware so the secure desktop version of the application can use it, and the application should enter sleep mode to avoid using processor resources.</span></span>
-   <span data-ttu-id="0a492-261">Если приложение может быть запущено в меню Пуск, в проводнике Windows или в командной строке, необходимо сообщить о простоте центра доступа.</span><span class="sxs-lookup"><span data-stu-id="0a492-261">If the application can be started through the Start menu, Windows Explorer, or the command line, the Ease of Access Center needs to be informed.</span></span> <span data-ttu-id="0a492-262">Дополнительные сведения см. в разделе **ключ эмблемы Windows + U**.</span><span class="sxs-lookup"><span data-stu-id="0a492-262">For more information, see **Windows Logo key + U**.</span></span>
-   <span data-ttu-id="0a492-263">Поскольку несколько копий приложения могут выполняться одновременно на разных настольных компьютерах, приложение должно быть написано для поддержки нескольких выполняющихся копий.</span><span class="sxs-lookup"><span data-stu-id="0a492-263">Because multiple copies of the application can run simultaneously on different desktops, the application must be written to support multiple running copies.</span></span>

### <a name="windows-logo-key--u"></a><span data-ttu-id="0a492-264">Клавиша Windows + U</span><span class="sxs-lookup"><span data-stu-id="0a492-264">Windows Logo key + U</span></span>

<span data-ttu-id="0a492-265">Если приложение специальных возможностей настроено для выполнения в задании, код запуска приложения должен содержать вызов функции [**испроцессинжоб**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) , чтобы определить, запускается ли приложение в задании.</span><span class="sxs-lookup"><span data-stu-id="0a492-265">If your accessibility application is configured to run in a job, your application's startup code should include a call to the [**IsProcessInJob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) function to determine whether the application is starting in a job.</span></span> <span data-ttu-id="0a492-266">Если это так, приложение должно запустить центр доступа и выйти из него.</span><span class="sxs-lookup"><span data-stu-id="0a492-266">If it is, the application should start the Ease of Access Center and then exit.</span></span> <span data-ttu-id="0a492-267">В следующем примере показано, как вызвать **испроцессинжоб**.</span><span class="sxs-lookup"><span data-stu-id="0a492-267">The following example shows how to call **IsProcessInJob**.</span></span>


```C++
BOOL fAlreadyInJob;
BOOL fSuccess = IsProcessInJob(GetCurrentProcess(), NULL, &fAlreadyInJob); 
```



<span data-ttu-id="0a492-268">Если приложение специальных возможностей настроено для выполнения вне задания, оно должно уведомить центр доступа, что приложение запускается, и продолжит работу в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="0a492-268">If the accessibility application is configured to run outside of a job, it should notify the Ease of Access Center that the application is starting and continue as normal.</span></span>

<span data-ttu-id="0a492-269">Независимо от того, как настроено приложение, если оно предоставляет способ выхода из приложения (например, кнопка "Закрыть"), приложение должно уведомить центр доступа, что он завершает работу.</span><span class="sxs-lookup"><span data-stu-id="0a492-269">Regardless of how the application is configured, if it provides a way to exit from within the application, such as a Close button, the application must notify the Ease of Access Center that it is exiting.</span></span>

<span data-ttu-id="0a492-270">Приложение уведомляет центр доступа, задавая временный раздел реестра, а затем добавляя сочетание клавиш Windows + U в входной поток.</span><span class="sxs-lookup"><span data-stu-id="0a492-270">An application notifies the Ease of Access Center by setting a temporary registry key and then injecting the Windows Logo key + U key combination into the input stream.</span></span>

<span data-ttu-id="0a492-271">Приложение должно создать временный ключ в следующем расположении.</span><span class="sxs-lookup"><span data-stu-id="0a492-271">The application should create the temporary key at the following location.</span></span>

<span data-ttu-id="0a492-272">**HKCU \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ акцессибилититемп**</span><span class="sxs-lookup"><span data-stu-id="0a492-272">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\AccessibilityTemp**</span></span>

<span data-ttu-id="0a492-273">Временный ключ должен иметь то же имя, что и зарегистрированное имя приложения, например " \_ считыватель экрана Contoso \_ v 1.0".</span><span class="sxs-lookup"><span data-stu-id="0a492-273">The temporary key should have the same name as the registered application name, such as "Contoso\_Screen Reader\_v1.0".</span></span> <span data-ttu-id="0a492-274">Значение ключа — **DWORD** , установленный в 0x0003 при запуске, или 0x0002 при выходе из приложения.</span><span class="sxs-lookup"><span data-stu-id="0a492-274">The value of the key is a **DWORD** set to 0x0003 when it is starting, or 0x0002 when the application is exiting.</span></span>


```C++
INPUT input[4] = {0};

input[0].type = INPUT_KEYBOARD;
input[0].ki.wVk = VK_LWIN;
input[0].ki.dwFlags = 0;

input[1].type = INPUT_KEYBOARD;
input[1].ki.wVk = 0x55; // U key
input[1].ki.dwFlags = 0;

input[2].type = INPUT_KEYBOARD;
input[2].ki.wVk = 0x55; // U key
input[2].ki.dwFlags = KEYEVENTF_KEYUP;

input[3].type = INPUT_KEYBOARD;
input[3].ki.wVk = VK_LWIN;
input[3].ki.dwFlags = KEYEVENTF_KEYUP;

SendInput(ARRAYSIZE(input), input, sizeof(input[0]));
```



### <a name="windows-logo-key--volume-up"></a><span data-ttu-id="0a492-275">Ключ эмблемы Windows + громкость</span><span class="sxs-lookup"><span data-stu-id="0a492-275">Windows Logo key + Volume Up</span></span>

<span data-ttu-id="0a492-276">Когда пользователь запускает приложение специальных возможностей, нажав сочетание клавиш Windows + Клавиша вверх (например, на планшетном устройстве), центр доступа передает приложению следующий аргумент командной строки:</span><span class="sxs-lookup"><span data-stu-id="0a492-276">When the user starts your accessibility application by pressing the Windows Logo key + Volume Up key combination (such as on a tablet device), the Ease of Access Center passes the following command-line argument to the application:</span></span>

<span data-ttu-id="0a492-277">**/хардваребуттонлаунч**</span><span class="sxs-lookup"><span data-stu-id="0a492-277">**/hardwarebuttonlaunch**</span></span>

<span data-ttu-id="0a492-278">Приложение может использовать этот аргумент, чтобы определить, следует ли запускать нормальную работу или соответствующим образом настроить поведение.</span><span class="sxs-lookup"><span data-stu-id="0a492-278">Your application can use this argument to determine whether to start normally, or to adjust behavior accordingly.</span></span>

### <a name="transferring-secure-desktop-settings"></a><span data-ttu-id="0a492-279">Передача параметров безопасного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="0a492-279">Transferring secure desktop settings</span></span>

<span data-ttu-id="0a492-280">Если приложение специальных возможностей поддерживает безопасный рабочий стол, можно использовать реестр для копирования параметров при переходе приложения на защищенный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="0a492-280">If your accessibility application supports the secure desktop, you can use the registry to copy settings when the application transitions to the secure desktop.</span></span> <span data-ttu-id="0a492-281">Копирование параметров помогает сделать переход на защищенный рабочий стол более плавным для пользователя.</span><span class="sxs-lookup"><span data-stu-id="0a492-281">Copying settings helps makes the transition to the secure desktop more seamless for the user.</span></span>

<span data-ttu-id="0a492-282">Чтобы скопировать параметры, задайте для раздела реестра Кописеттингстолоккеддесктоп приложения значение 1 и сохраните параметры в следующем расположении реестра.</span><span class="sxs-lookup"><span data-stu-id="0a492-282">To copy settings, set the application's CopySettingsToLockedDesktop registry key to 1, and store the settings in the following registry location.</span></span>

<span data-ttu-id="0a492-283">**HKCU \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ атконфиг\\<AT Key Name>**</span><span class="sxs-lookup"><span data-stu-id="0a492-283">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATConfig\\<AT Key Name>**</span></span>

<span data-ttu-id="0a492-284">Центр специальных возможностей наблюдает за этим расположением реестра во время работы приложения.</span><span class="sxs-lookup"><span data-stu-id="0a492-284">The Ease of Access Center monitors this registry location while the application is running.</span></span> <span data-ttu-id="0a492-285">При переходе на защищенный рабочий стол центр доступа копирует параметры в то же расположение, что и в кусте "безопасный Настольный компьютер s".</span><span class="sxs-lookup"><span data-stu-id="0a492-285">When a transition to the secure desktop occurs, the Ease of Access Center copies the settings to the same location in the secure desktop s HKCU hive.</span></span> <span data-ttu-id="0a492-286">Затем приложение может считывать параметры и возобновлять его состояние.</span><span class="sxs-lookup"><span data-stu-id="0a492-286">The application can then read the settings and resume its state.</span></span>

<span data-ttu-id="0a492-287">Приложение специальных возможностей должно записывать свои параметры через регулярные промежутки времени или каждый раз при изменении значений.</span><span class="sxs-lookup"><span data-stu-id="0a492-287">Your accessibility application should write its settings at regular intervals or whenever the values change.</span></span> <span data-ttu-id="0a492-288">Запись параметров при выходе из приложения не будет работать.</span><span class="sxs-lookup"><span data-stu-id="0a492-288">Writing settings on application exit will not work.</span></span> <span data-ttu-id="0a492-289">Если приложение выполняется в задании, оно завершается на переходе от защищенного рабочего стола, прежде чем код выхода сможет запуститься.</span><span class="sxs-lookup"><span data-stu-id="0a492-289">If the application is running in a job, it is terminated on the transition away from the secure desktop, before the exit code has a chance to run.</span></span> <span data-ttu-id="0a492-290">Если приложение не выполняется в задании, оно не завершается на переходе от защищенного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="0a492-290">If the application is not running in a job, the application is not terminated on the transition away from the secure desktop.</span></span>

### <a name="caution"></a><span data-ttu-id="0a492-291">Внимание!</span><span class="sxs-lookup"><span data-stu-id="0a492-291">Caution</span></span>

<span data-ttu-id="0a492-292">Так как описанные здесь разделы реестра написаны в пользовательском режиме, они не являются безопасными.</span><span class="sxs-lookup"><span data-stu-id="0a492-292">Because the registry keys described here are written in user mode, they are not secure.</span></span> <span data-ttu-id="0a492-293">Если приложение специальных возможностей считывает содержимое этих ключей, следует тщательно проверить данные и использовать их с осторожностью.</span><span class="sxs-lookup"><span data-stu-id="0a492-293">If your accessibility application reads the contents of these keys, it should carefully check the data and use it with caution.</span></span> <span data-ttu-id="0a492-294">В частности, приложение должно выполнить проверку значений **DWORD** , быть осторожным с длиной строк, не должно считывать имена подключаемых модулей DLL и не выполнять команды, найденные в строках.</span><span class="sxs-lookup"><span data-stu-id="0a492-294">Specifically, your application should do a bounds check on **DWORD** values, be careful with string lengths, should not read plug-in DLL names, and should not execute any commands found in strings.</span></span>

## <a name="registry-examples"></a><span data-ttu-id="0a492-295">Примеры реестра</span><span class="sxs-lookup"><span data-stu-id="0a492-295">Registry Examples</span></span>

<span data-ttu-id="0a492-296">В следующем примере показаны возможные значения реестра для вымышленного продукта с именем Contoso Скринреадер версии 2,0, локализованное имя которого хранится в виде ресурса.</span><span class="sxs-lookup"><span data-stu-id="0a492-296">The following example shows the possible registry values for a fictitious product called Contoso ScreenReader version 2.0, whose localized name is stored as a resource.</span></span>

<span data-ttu-id="0a492-297">Значения в таблице находятся в следующем разделе:</span><span class="sxs-lookup"><span data-stu-id="0a492-297">The values in the table are under the following key:</span></span>

<span data-ttu-id="0a492-298">**HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATS " \\ contoso \_ Screen Reader \_ v 2.0"**</span><span class="sxs-lookup"><span data-stu-id="0a492-298">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\Contoso\_Screen Reader\_v2.0**</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a492-299">Имя</span><span class="sxs-lookup"><span data-stu-id="0a492-299">Name</span></span></th>
<th><span data-ttu-id="0a492-300">Тип</span><span class="sxs-lookup"><span data-stu-id="0a492-300">Type</span></span></th>
<th><span data-ttu-id="0a492-301">Данные</span><span class="sxs-lookup"><span data-stu-id="0a492-301">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a492-302">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="0a492-302">ApplicationName</span></span></td>
<td><span data-ttu-id="0a492-303">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-303">REG_SZ</span></span></td>
<td><span data-ttu-id="0a492-304">@% SystemRoot% \system32\ContosoRes.dll,-5020</span><span class="sxs-lookup"><span data-stu-id="0a492-304">@%SystemRoot%\system32\ContosoRes.dll,-5020</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a492-305">Описание</span><span class="sxs-lookup"><span data-stu-id="0a492-305">Description</span></span></td>
<td><span data-ttu-id="0a492-306">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-306">REG_SZ</span></span></td>
<td><span data-ttu-id="0a492-307">@% SystemRoot% \system32\ContosoRes.dll,-5040</span><span class="sxs-lookup"><span data-stu-id="0a492-307">@%SystemRoot%\system32\ContosoRes.dll,-5040</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a492-308">Профиль</span><span class="sxs-lookup"><span data-stu-id="0a492-308">Profile</span></span></td>
<td><span data-ttu-id="0a492-309">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-309">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a492-310">XML</span><span class="sxs-lookup"><span data-stu-id="0a492-310">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a492-311">симплепрофиле</span><span class="sxs-lookup"><span data-stu-id="0a492-311">SimpleProfile</span></span></td>
<td><span data-ttu-id="0a492-312">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-312">REG_SZ</span></span></td>
<td><span data-ttu-id="0a492-313">скринреадер</span><span class="sxs-lookup"><span data-stu-id="0a492-313">ScreenReader</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a492-314">StartExe</span><span class="sxs-lookup"><span data-stu-id="0a492-314">StartExe</span></span></td>
<td><span data-ttu-id="0a492-315">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-315">REG_SZ</span></span></td>
<td><span data-ttu-id="0a492-316">C:\ContosoTools\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="0a492-316">C:\ContosoTools\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a492-317">стартпарамс</span><span class="sxs-lookup"><span data-stu-id="0a492-317">StartParams</span></span></td>
<td><span data-ttu-id="0a492-318">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-318">REG_SZ</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="0a492-319">секуредесктопаккоммодатион</span><span class="sxs-lookup"><span data-stu-id="0a492-319">SecureDesktopAccommodation</span></span></td>
<td><span data-ttu-id="0a492-320">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-320">REG_SZ</span></span></td>
<td><span data-ttu-id="0a492-321">Narrator</span><span class="sxs-lookup"><span data-stu-id="0a492-321">Narrator</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0a492-322">Если приложение предоставляет средство чтения с экрана и экранную лупу в одном исполняемом файле, значения для компонента чтения с экрана могут выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0a492-322">If the application provides both a screen reader and a screen magnifier in a single executable, the values for the screen reader component might look like this:</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a492-323">Имя</span><span class="sxs-lookup"><span data-stu-id="0a492-323">Name</span></span></th>
<th><span data-ttu-id="0a492-324">Тип</span><span class="sxs-lookup"><span data-stu-id="0a492-324">Type</span></span></th>
<th><span data-ttu-id="0a492-325">Данные</span><span class="sxs-lookup"><span data-stu-id="0a492-325">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a492-326">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="0a492-326">ApplicationName</span></span></td>
<td><span data-ttu-id="0a492-327">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-327">REG_SZ</span></span></td>
<td><span data-ttu-id="0a492-328">@C:\Program Files\Contoso\Contosores.dll,-30</span><span class="sxs-lookup"><span data-stu-id="0a492-328">@C:\Program Files\Contoso\Contosores.dll,-30</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a492-329">Описание</span><span class="sxs-lookup"><span data-stu-id="0a492-329">Description</span></span></td>
<td><span data-ttu-id="0a492-330">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-330">REG_SZ</span></span></td>
<td><span data-ttu-id="0a492-331">@C:\Program Files\Contoso\Contosores.dll,-32</span><span class="sxs-lookup"><span data-stu-id="0a492-331">@C:\Program Files\Contoso\Contosores.dll,-32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a492-332">Профиль</span><span class="sxs-lookup"><span data-stu-id="0a492-332">Profile</span></span></td>
<td><span data-ttu-id="0a492-333">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-333">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a492-334">XML</span><span class="sxs-lookup"><span data-stu-id="0a492-334">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a492-335">симплепрофиле</span><span class="sxs-lookup"><span data-stu-id="0a492-335">SimpleProfile</span></span></td>
<td><span data-ttu-id="0a492-336">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-336">REG_SZ</span></span></td>
<td><span data-ttu-id="0a492-337">скринреадер</span><span class="sxs-lookup"><span data-stu-id="0a492-337">ScreenReader</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a492-338">StartExe</span><span class="sxs-lookup"><span data-stu-id="0a492-338">StartExe</span></span></td>
<td><span data-ttu-id="0a492-339">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-339">REG_SZ</span></span></td>
<td><span data-ttu-id="0a492-340">C:\Program Files\Contoso\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="0a492-340">C:\Program Files\Contoso\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a492-341">стартпарамс</span><span class="sxs-lookup"><span data-stu-id="0a492-341">StartParams</span></span></td>
<td><span data-ttu-id="0a492-342">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-342">REG_SZ</span></span></td>
<td><span data-ttu-id="0a492-343">/r</span><span class="sxs-lookup"><span data-stu-id="0a492-343">/r</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0a492-344">Значения для компонента экранной лупы будут иметь следующий ключ:</span><span class="sxs-lookup"><span data-stu-id="0a492-344">The values for the magnifier component would be in the following key:</span></span>

<span data-ttu-id="0a492-345">**HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ контосоибилити \\ ATS \\ contoso \_ лупой \_ v 2.0**</span><span class="sxs-lookup"><span data-stu-id="0a492-345">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Contosoibility\\ATs\\Contoso\_Magnifier\_v2.0**</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a492-346">Имя</span><span class="sxs-lookup"><span data-stu-id="0a492-346">Name</span></span></th>
<th><span data-ttu-id="0a492-347">Тип</span><span class="sxs-lookup"><span data-stu-id="0a492-347">Type</span></span></th>
<th><span data-ttu-id="0a492-348">Данные</span><span class="sxs-lookup"><span data-stu-id="0a492-348">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a492-349">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="0a492-349">ApplicationName</span></span></td>
<td><span data-ttu-id="0a492-350">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-350">REG_SZ</span></span></td>
<td><span data-ttu-id="0a492-351">@c:\Program Files\Contoso\Contosores.dll,-31</span><span class="sxs-lookup"><span data-stu-id="0a492-351">@c:\Program Files\Contoso\Contosores.dll,-31</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a492-352">Описание</span><span class="sxs-lookup"><span data-stu-id="0a492-352">Description</span></span></td>
<td><span data-ttu-id="0a492-353">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-353">REG_SZ</span></span></td>
<td><span data-ttu-id="0a492-354">@c:\Program Files\Contoso\Contosores.dll,-42</span><span class="sxs-lookup"><span data-stu-id="0a492-354">@c:\Program Files\Contoso\Contosores.dll,-42</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a492-355">Профиль</span><span class="sxs-lookup"><span data-stu-id="0a492-355">Profile</span></span></td>
<td><span data-ttu-id="0a492-356">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-356">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a492-357">XML</span><span class="sxs-lookup"><span data-stu-id="0a492-357">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;mild vision&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a492-358">симплепрофиле</span><span class="sxs-lookup"><span data-stu-id="0a492-358">SimpleProfile</span></span></td>
<td><span data-ttu-id="0a492-359">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-359">REG_SZ</span></span></td>
<td><span data-ttu-id="0a492-360">Увеличения</span><span class="sxs-lookup"><span data-stu-id="0a492-360">Magnification</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a492-361">StartExe</span><span class="sxs-lookup"><span data-stu-id="0a492-361">StartExe</span></span></td>
<td><span data-ttu-id="0a492-362">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-362">REG_SZ</span></span></td>
<td><span data-ttu-id="0a492-363">c:\Program Files\Contoso\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="0a492-363">c:\Program Files\Contoso\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a492-364">стартпарамс</span><span class="sxs-lookup"><span data-stu-id="0a492-364">StartParams</span></span></td>
<td><span data-ttu-id="0a492-365">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0a492-365">REG_SZ</span></span></td>
<td><span data-ttu-id="0a492-366">/m</span><span class="sxs-lookup"><span data-stu-id="0a492-366">/m</span></span></td>
</tr>
</tbody>
</table>



 

 

