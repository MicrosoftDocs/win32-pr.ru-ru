---
description: Описывает методы открытия элемента панели управления для систем Windows Vista и более поздних версий, а также охватывает устаревшие команды панели управления.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Исполнение элементов панели управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaaac4b782273e0b4444fb2b5b6d3cab0b3599ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997834"
---
# <a name="executing-control-panel-items"></a><span data-ttu-id="58e40-103">Исполнение элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="58e40-103">Executing Control Panel Items</span></span>

> [!Note]  
> <span data-ttu-id="58e40-104">Если вы ищете список канонических имен и имена модулей для элементов панели управления, см. раздел [канонические имена элементов панели управления](controlpanel-canonical-names.md).</span><span class="sxs-lookup"><span data-stu-id="58e40-104">If you are looking for the list of canonical and module names for Control Panel items, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

 

<span data-ttu-id="58e40-105">Существует два способа открыть элемент панели управления:</span><span class="sxs-lookup"><span data-stu-id="58e40-105">There are two ways to open a Control Panel item:</span></span>

-   <span data-ttu-id="58e40-106">Пользователь может открыть панель управления, а затем открыть элемент, щелкнув или дважды щелкнув значок элемента.</span><span class="sxs-lookup"><span data-stu-id="58e40-106">The user can open Control Panel and then open an item by clicking or double-clicking the item's icon.</span></span>
-   <span data-ttu-id="58e40-107">Пользователь или приложение может запустить элемент панели управления, выполнив его непосредственно из командной строки.</span><span class="sxs-lookup"><span data-stu-id="58e40-107">The user or an application can start a Control Panel item by executing it directly from the command line prompt.</span></span>

<span data-ttu-id="58e40-108">Приложение может открыть панель управления программным способом с помощью функции [**винексек**](/windows/win32/api/winbase/nf-winbase-winexec) .</span><span class="sxs-lookup"><span data-stu-id="58e40-108">An application can open the Control Panel programmatically by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



<span data-ttu-id="58e40-109">В следующем примере показано, как приложение может запустить элемент панели управления с именем **MyCpl.cpl** с помощью функции [**винексек**](/windows/win32/api/winbase/nf-winbase-winexec) .</span><span class="sxs-lookup"><span data-stu-id="58e40-109">The following example shows how an application can start the Control Panel item named **MyCpl.cpl** by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



<span data-ttu-id="58e40-110">При открытии элемента панели управления с помощью командной строки можно указать, что он открывается на определенной вкладке в элементе.</span><span class="sxs-lookup"><span data-stu-id="58e40-110">When a Control Panel item is opened through a command line, you can instruct it to open to a particular tab in the item.</span></span> <span data-ttu-id="58e40-111">Из-за добавления и удаления определенных вкладок в некоторых элементах панели управления Windows Vista нумерация вкладок могла быть изменена в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="58e40-111">Due to the addition and removal of certain tabs in some Windows Vista Control Panel items, the numbering of the tabs might have changed from that in Windows XP.</span></span> <span data-ttu-id="58e40-112">Например, в следующем примере запускается четвертая вкладка в системном элементе в Windows XP и на третьей вкладке Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="58e40-112">For instance, the following example launches the fourth tab in the System item on Windows XP and the third tab on Windows Vista.</span></span>


```
control.exe sysdm.cpl,,3
```



<span data-ttu-id="58e40-113">В этом разделе обсуждается следующее.</span><span class="sxs-lookup"><span data-stu-id="58e40-113">This topic discusses the following:</span></span>

-   [<span data-ttu-id="58e40-114">Канонические имена Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58e40-114">Windows Vista Canonical Names</span></span>](#windows-vista-canonical-names)
-   [<span data-ttu-id="58e40-115">Новые команды для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58e40-115">New Commands for Windows Vista</span></span>](#new-commands-for-windows-vista)
-   [<span data-ttu-id="58e40-116">Устаревшие команды панели управления</span><span class="sxs-lookup"><span data-stu-id="58e40-116">Legacy Control Panel Commands</span></span>](#legacy-control-panel-commands)
-   [<span data-ttu-id="58e40-117">См. также</span><span class="sxs-lookup"><span data-stu-id="58e40-117">Related topics</span></span>](#related-topics)

## <a name="windows-vista-canonical-names"></a><span data-ttu-id="58e40-118">Канонические имена Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58e40-118">Windows Vista Canonical Names</span></span>

<span data-ttu-id="58e40-119">В Windows Vista и более поздних версиях предпочтительным способом запуска элемента панели управления из командной строки является использование канонического имени элемента панели управления.</span><span class="sxs-lookup"><span data-stu-id="58e40-119">In Windows Vista and later, the preferred method of launching a Control Panel item from a command line is to use the Control Panel item's canonical name.</span></span> <span data-ttu-id="58e40-120">Каноническое имя — это нелокализованная строка, которая объявляется элементом панели управления в реестре.</span><span class="sxs-lookup"><span data-stu-id="58e40-120">A canonical name is a non-localized string that the Control Panel item declares in the registry.</span></span> <span data-ttu-id="58e40-121">Значение по каноническому имени состоит в том, что оно абстрагирует имя модуля элемента панели управления.</span><span class="sxs-lookup"><span data-stu-id="58e40-121">The value of using a canonical name is that it abstracts the module name of the Control Panel item.</span></span> <span data-ttu-id="58e40-122">Элемент можно реализовать в DLL-библиотеке, а затем повторно реализовать его как exe-файл или изменить имя модуля.</span><span class="sxs-lookup"><span data-stu-id="58e40-122">An item can be implemented in a .dll and later be reimplemented as a .exe or change its module name.</span></span> <span data-ttu-id="58e40-123">При условии, что каноническое имя остается неизменным, любая программа, открывающая ее с помощью этого канонического имени, не нуждается в обновлении.</span><span class="sxs-lookup"><span data-stu-id="58e40-123">As long as the canonical name remains the same, then any program that opens it by using that canonical name does not need to be updated.</span></span>

<span data-ttu-id="58e40-124">По соглашению каноническое имя формируется как "Корпоратионнаме. Контролпанелитемнаме".</span><span class="sxs-lookup"><span data-stu-id="58e40-124">By convention, the canonical name is formed as "CorporationName.ControlPanelItemName".</span></span>

<span data-ttu-id="58e40-125">В следующем примере показано, как приложение может запустить элемент панели управления **Центр обновления Windows** с [**винексек**](/windows/win32/api/winbase/nf-winbase-winexec).</span><span class="sxs-lookup"><span data-stu-id="58e40-125">The following example shows how an application can start the Control Panel item **Windows Update** with [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).</span></span>


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



<span data-ttu-id="58e40-126">Чтобы запустить элемент панели управления с каноническим именем, используйте: "% SystemRoot% \\ system32 \\control.exe/Name *каноникалнаме*"</span><span class="sxs-lookup"><span data-stu-id="58e40-126">To start a Control Panel item with its canonical name, use: "%systemroot%\\system32\\control.exe /name *canonicalName*"</span></span>

<span data-ttu-id="58e40-127">Чтобы открыть определенную подстраницу в элементе или открыть ее с дополнительными параметрами, используйте: "% SystemRoot% \\ system32 \\control.exe/Name **каноникалнаме** очищенную **PageName**"</span><span class="sxs-lookup"><span data-stu-id="58e40-127">To open a specific sub-page in an item, or to open it with additional parameters, use: "%systemroot%\\system32\\control.exe /name **canonicalName** /page **pageName**"</span></span>

<span data-ttu-id="58e40-128">Приложение может также реализовать метод [**иопенконтролпанел:: Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) для запуска элементов панели управления, включая возможность открытия конкретной подстраницы.</span><span class="sxs-lookup"><span data-stu-id="58e40-128">An application can also implement the [**IOpenControlPanel::Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) method to launch Control Panel items, including the ability to open a specific sub-page.</span></span>

<span data-ttu-id="58e40-129">Полный список канонических имен элементов панели управления см. в разделе [канонические имена элементов панели управления](controlpanel-canonical-names.md).</span><span class="sxs-lookup"><span data-stu-id="58e40-129">For a complete list of Control Panel item canonical names, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

## <a name="new-commands-for-windows-vista"></a><span data-ttu-id="58e40-130">Новые команды для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58e40-130">New Commands for Windows Vista</span></span>

<span data-ttu-id="58e40-131">В Windows Vista некоторые параметры, которые были доступны в модуле. cpl в Windows XP, теперь реализуются как exe-файлы.</span><span class="sxs-lookup"><span data-stu-id="58e40-131">On Windows Vista, some options that were accessed by a .cpl module on Windows XP are now implemented as .exe files.</span></span> <span data-ttu-id="58e40-132">Это обеспечивает дополнительную безопасность, разрешая стандартным пользователям получать запрос на ввод учетных данных администратора при попытке запуска файлов.</span><span class="sxs-lookup"><span data-stu-id="58e40-132">This provides added security by allowing standard users to be prompted to provide administrator credentials when trying to launch the files.</span></span> <span data-ttu-id="58e40-133">К параметрам, которые не нуждаются в дополнительной безопасности, обращаются те же командные строки, которые использовались в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="58e40-133">Options that do not require extra security are accessed by the same command lines that were used in Windows XP.</span></span> <span data-ttu-id="58e40-134">Ниже приведен список команд, используемых в Windows Vista для доступа к конкретным вкладкам элементов панели управления.</span><span class="sxs-lookup"><span data-stu-id="58e40-134">The following is a list of commands used in Windows Vista to access specific tabs of Control Panel items:</span></span>

### <a name="personalization"></a><span data-ttu-id="58e40-135">Personalization</span><span class="sxs-lookup"><span data-stu-id="58e40-135">Personalization</span></span>

-   <span data-ttu-id="58e40-136">Размер шрифта и число точек на дюйм:% WINDIR% \\ system32 \\DpiScaling.exe</span><span class="sxs-lookup"><span data-stu-id="58e40-136">Font size and DPI: %windir%\\system32\\DpiScaling.exe</span></span>
-   <span data-ttu-id="58e40-137">Разрешение экрана:% WINDIR% \\ system32 \\control.exe desk.cpl, параметры,@Settings</span><span class="sxs-lookup"><span data-stu-id="58e40-137">Screen resolution: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="58e40-138">Параметры экрана:% WINDIR% \\ system32 \\control.exe desk.cpl, параметры,@Settings</span><span class="sxs-lookup"><span data-stu-id="58e40-138">Display settings: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="58e40-139">Темы:% WINDIR% \\ system32 \\control.exe desk.cpl, темы@Themes</span><span class="sxs-lookup"><span data-stu-id="58e40-139">Themes: %windir%\\system32\\control.exe desk.cpl,Themes,@Themes</span></span>
-   <span data-ttu-id="58e40-140">Экранная заставка:% WINDIR% \\ system32 \\control.exe desk.cpl, экранная заставка@screensaver</span><span class="sxs-lookup"><span data-stu-id="58e40-140">Screensaver: %windir%\\system32\\control.exe desk.cpl,screensaver,@screensaver</span></span>
-   <span data-ttu-id="58e40-141">Несколько мониторов:% WINDIR% \\ system32 \\control.exe desk.cpl, монитор,@Monitor</span><span class="sxs-lookup"><span data-stu-id="58e40-141">Multi-monitor: %windir%\\system32\\control.exe desk.cpl,Monitor,@Monitor</span></span>
-   <span data-ttu-id="58e40-142">Цветовая схема:% WINDIR% \\ system32 \\control.exe/Name Microsoft. Personal очищенную пажеколоризатион</span><span class="sxs-lookup"><span data-stu-id="58e40-142">Color Scheme: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageColorization</span></span>
-   <span data-ttu-id="58e40-143">Фон рабочего стола:% WINDIR% \\ system32 \\control.exe/Name Microsoft. Personal очищенную пажеваллпапер</span><span class="sxs-lookup"><span data-stu-id="58e40-143">Desktop background: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageWallpaper</span></span>

> [!Note]  
> <span data-ttu-id="58e40-144">Выпуски Starter и Basic не поддерживают команду control.exe/Name Microsoft. Personal.</span><span class="sxs-lookup"><span data-stu-id="58e40-144">Starter and Basic Editions do not support control.exe /name Microsoft.Personalization command.</span></span>

 

### <a name="system"></a><span data-ttu-id="58e40-145">Система</span><span class="sxs-lookup"><span data-stu-id="58e40-145">System</span></span>

-   <span data-ttu-id="58e40-146">Производительность:% WINDIR% \\ system32 \\SystemPropertiesPerformance.exe</span><span class="sxs-lookup"><span data-stu-id="58e40-146">Performance: %windir%\\system32\\SystemPropertiesPerformance.exe</span></span>
-   <span data-ttu-id="58e40-147">Удаленный доступ:% WINDIR% \\ system32 \\SystemPropertiesRemote.exe</span><span class="sxs-lookup"><span data-stu-id="58e40-147">Remote access: %windir%\\system32\\SystemPropertiesRemote.exe</span></span>
-   <span data-ttu-id="58e40-148">Имя компьютера:% WINDIR% \\ system32 \\SystemPropertiesComputerName.exe</span><span class="sxs-lookup"><span data-stu-id="58e40-148">Computer name: %windir%\\system32\\SystemPropertiesComputerName.exe</span></span>
-   <span data-ttu-id="58e40-149">Защита системы:% WINDIR% \\ system32 \\SystemPropertiesProtection.exe</span><span class="sxs-lookup"><span data-stu-id="58e40-149">System protection: %windir%\\system32\\SystemPropertiesProtection.exe</span></span>
-   <span data-ttu-id="58e40-150">Дополнительные свойства системы:% WINDIR% \\ system32 \\SystemPropertiesAdvanced.exe</span><span class="sxs-lookup"><span data-stu-id="58e40-150">Advanced system properties: %windir%\\system32\\SystemPropertiesAdvanced.exe</span></span>

### <a name="programs-and-features"></a><span data-ttu-id="58e40-151">"Программы и компоненты",</span><span class="sxs-lookup"><span data-stu-id="58e40-151">Programs and Features</span></span>

-   <span data-ttu-id="58e40-152">Установка и удаление программ:% WINDIR% \\ system32 \\control.exe/Name Microsoft. програмсандфеатурес</span><span class="sxs-lookup"><span data-stu-id="58e40-152">Add or remove programs: %windir%\\system32\\control.exe /name Microsoft.ProgramsAndFeatures</span></span>
-   <span data-ttu-id="58e40-153">Компоненты Windows:% WINDIR% \\ system32 \\OptionalFeatures.exe</span><span class="sxs-lookup"><span data-stu-id="58e40-153">Windows features: %windir%\\system32\\OptionalFeatures.exe</span></span>

### <a name="regional-and-language-options"></a><span data-ttu-id="58e40-154">Региональные и языковые параметры</span><span class="sxs-lookup"><span data-stu-id="58e40-154">Regional and Language Options</span></span>

-   <span data-ttu-id="58e40-155">Клавиатура:% systemroot% \\ system32 \\control.exe/Name Microsoft. регионаландлангуажеоптионс очищенную/p: "клавиатура"</span><span class="sxs-lookup"><span data-stu-id="58e40-155">Keyboard: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"keyboard"</span></span>
-   <span data-ttu-id="58e40-156">Расположение:% systemroot% \\ system32 \\control.exe/Name Microsoft. регионаландлангуажеоптионс очищенную/p: "Location"</span><span class="sxs-lookup"><span data-stu-id="58e40-156">Location: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"location"</span></span>
-   <span data-ttu-id="58e40-157">Администрирование:% systemroot% \\ system32 \\control.exe/Name Microsoft. регионаландлангуажеоптионс очищенную/p: "Administrative"</span><span class="sxs-lookup"><span data-stu-id="58e40-157">Administrative: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"administrative"</span></span>

### <a name="folder-options"></a><span data-ttu-id="58e40-158">Свойства папки</span><span class="sxs-lookup"><span data-stu-id="58e40-158">Folder Options</span></span>

-   <span data-ttu-id="58e40-159">Поиск папки:% WINDIR% \\ system32 \\rundll32.exe shell32.dll, параметры программы \_ Rundll 2</span><span class="sxs-lookup"><span data-stu-id="58e40-159">Folder searching: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 2</span></span>
-   <span data-ttu-id="58e40-160">Сопоставления файлов:% WINDIR% \\ system32 \\control.exe/Name Microsoft. Дефаултпрограмс очищенную пажефилеассок</span><span class="sxs-lookup"><span data-stu-id="58e40-160">File associations: %windir%\\system32\\control.exe /name Microsoft.DefaultPrograms /page pageFileAssoc</span></span>
-   <span data-ttu-id="58e40-161">Представление:% WINDIR% \\ system32 \\rundll32.exe shell32.dll, параметры программы \_ Rundll 7</span><span class="sxs-lookup"><span data-stu-id="58e40-161">View: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 7</span></span>
-   <span data-ttu-id="58e40-162">Общие:% WINDIR% \\ system32 \\rundll32.exe shell32.dll, параметры программы \_ Rundll 0</span><span class="sxs-lookup"><span data-stu-id="58e40-162">General: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 0</span></span>

### <a name="power-options"></a><span data-ttu-id="58e40-163">Параметры электропитания</span><span class="sxs-lookup"><span data-stu-id="58e40-163">Power Options</span></span>

-   <span data-ttu-id="58e40-164">Изменение текущих параметров плана:% WINDIR% \\ system32 \\control.exe/Name Microsoft. Повероптионс очищенную пажеплансеттингс</span><span class="sxs-lookup"><span data-stu-id="58e40-164">Edit current plan settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pagePlanSettings</span></span>
-   <span data-ttu-id="58e40-165">Параметры системы:% WINDIR% \\ system32 \\control.exe/Name Microsoft. Повероптионс очищенную пажеглобалсеттингс</span><span class="sxs-lookup"><span data-stu-id="58e40-165">System settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageGlobalSettings</span></span>
-   <span data-ttu-id="58e40-166">Создайте схему управления питанием:% WINDIR% \\ system32 \\control.exe/Name Microsoft. Повероптионс очищенную пажекреатеневплан</span><span class="sxs-lookup"><span data-stu-id="58e40-166">Create a power plan: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageCreateNewPlan</span></span>
-   <span data-ttu-id="58e40-167">Для страницы Дополнительные параметры нет канонической команды. доступ к ней осуществляется по старому способу:% WINDIR% \\ system32 \\control.exe powercfg.cpl,, 3</span><span class="sxs-lookup"><span data-stu-id="58e40-167">There is no canonical command for the Advanced Settings page, it is accessed in the older manner: %windir%\\system32\\control.exe powercfg.cpl,,3</span></span>

## <a name="legacy-control-panel-commands"></a><span data-ttu-id="58e40-168">Устаревшие команды панели управления</span><span class="sxs-lookup"><span data-stu-id="58e40-168">Legacy Control Panel Commands</span></span>

<span data-ttu-id="58e40-169">При использовании функции [**винексек**](/windows/win32/api/winbase/nf-winbase-winexec) система может распознать специальные команды панели управления.</span><span class="sxs-lookup"><span data-stu-id="58e40-169">When you use the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function, the system can recognize special Control Panel commands.</span></span> <span data-ttu-id="58e40-170">Эти команды предактуальны для Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="58e40-170">These commands predate Windows Vista.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="58e40-171">control.exe Desktop</span><span class="sxs-lookup"><span data-stu-id="58e40-171">control.exe desktop</span></span></td>
<td><span data-ttu-id="58e40-172">Открывает окно <strong>Свойства экрана</strong> .</span><span class="sxs-lookup"><span data-stu-id="58e40-172">Launches the <strong>Display Properties</strong> window.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="58e40-173">Выпуски Starter и Basic не поддерживают эту команду.</span><span class="sxs-lookup"><span data-stu-id="58e40-173">Starter and Basic Editions do not support this command.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58e40-174">Цвет control.exe</span><span class="sxs-lookup"><span data-stu-id="58e40-174">control.exe color</span></span></td>
<td><span data-ttu-id="58e40-175">Открывает окно <strong>свойства отображения</strong> с выделенной вкладкой <strong>Оформление</strong> .</span><span class="sxs-lookup"><span data-stu-id="58e40-175">Launches the <strong>Display Properties</strong> window with the <strong>Appearance</strong> tab preselected.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58e40-176">Дата и время control.exe</span><span class="sxs-lookup"><span data-stu-id="58e40-176">control.exe date/time</span></span></td>
<td><span data-ttu-id="58e40-177">Открывает окно <strong>Свойства даты и времени</strong> .</span><span class="sxs-lookup"><span data-stu-id="58e40-177">Launches the <strong>Date and Time Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58e40-178">control.exe Международная</span><span class="sxs-lookup"><span data-stu-id="58e40-178">control.exe international</span></span></td>
<td><span data-ttu-id="58e40-179">Открывает окно язык <strong>и региональные параметры</strong> .</span><span class="sxs-lookup"><span data-stu-id="58e40-179">Launches the <strong>Regional and Language Options</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58e40-180">control.exe мыши</span><span class="sxs-lookup"><span data-stu-id="58e40-180">control.exe mouse</span></span></td>
<td><span data-ttu-id="58e40-181">Запускает окно <strong>свойств мыши</strong> .</span><span class="sxs-lookup"><span data-stu-id="58e40-181">Launches the <strong>Mouse Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58e40-182">control.exe клавиатура</span><span class="sxs-lookup"><span data-stu-id="58e40-182">control.exe keyboard</span></span></td>
<td><span data-ttu-id="58e40-183">Запускает окно <strong>Свойства клавиатуры</strong> .</span><span class="sxs-lookup"><span data-stu-id="58e40-183">Launches the <strong>Keyboard Properties</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58e40-184">control.exe принтеры</span><span class="sxs-lookup"><span data-stu-id="58e40-184">control.exe printers</span></span></td>
<td><span data-ttu-id="58e40-185">Отображает папку <strong>Принтеры и факсы</strong> .</span><span class="sxs-lookup"><span data-stu-id="58e40-185">Displays the <strong>Printers and Faxes</strong> folder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58e40-186">control.exe шрифты</span><span class="sxs-lookup"><span data-stu-id="58e40-186">control.exe fonts</span></span></td>
<td><span data-ttu-id="58e40-187">Отображает папку <strong>Fonts</strong> .</span><span class="sxs-lookup"><span data-stu-id="58e40-187">Displays the <strong>Fonts</strong> folder.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="58e40-188">Для систем Windows 2000 и более поздних версий:</span><span class="sxs-lookup"><span data-stu-id="58e40-188">For Windows 2000 and later systems:</span></span>



|                            |                                                          |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="58e40-189">control.exe папки</span><span class="sxs-lookup"><span data-stu-id="58e40-189">control.exe folders</span></span>        | <span data-ttu-id="58e40-190">Открывает окно " **Свойства папки** ".</span><span class="sxs-lookup"><span data-stu-id="58e40-190">Launches the **Folder Options** window.</span></span>                  |
| <span data-ttu-id="58e40-191">control.exe NetWare</span><span class="sxs-lookup"><span data-stu-id="58e40-191">control.exe netware</span></span>        | <span data-ttu-id="58e40-192">Запускает окно **Novell NetWare** (если установлено).</span><span class="sxs-lookup"><span data-stu-id="58e40-192">Launches the **Novell NetWare** window (if installed).</span></span>   |
| <span data-ttu-id="58e40-193">control.exe телефонии</span><span class="sxs-lookup"><span data-stu-id="58e40-193">control.exe telephony</span></span>      | <span data-ttu-id="58e40-194">Открывает окно **Параметры телефона и модема** .</span><span class="sxs-lookup"><span data-stu-id="58e40-194">Launches the **Phone and Modem Options** window.</span></span>         |
| <span data-ttu-id="58e40-195">control.exe админтулс</span><span class="sxs-lookup"><span data-stu-id="58e40-195">control.exe admintools</span></span>     | <span data-ttu-id="58e40-196">Отображение папки " **Администрирование** ".</span><span class="sxs-lookup"><span data-stu-id="58e40-196">Displays the **Administrative Tools** folder.</span></span>            |
| <span data-ttu-id="58e40-197">control.exe счедтаскс</span><span class="sxs-lookup"><span data-stu-id="58e40-197">control.exe schedtasks</span></span>     | <span data-ttu-id="58e40-198">Отображает папку **Назначенные задания** .</span><span class="sxs-lookup"><span data-stu-id="58e40-198">Displays the **Scheduled Tasks** folder.</span></span>                 |
| <span data-ttu-id="58e40-199">control.exe нетконнектионс</span><span class="sxs-lookup"><span data-stu-id="58e40-199">control.exe netconnections</span></span> | <span data-ttu-id="58e40-200">Отображает папку **Сетевые подключения** .</span><span class="sxs-lookup"><span data-stu-id="58e40-200">Displays the **Network Connections** folder.</span></span>             |
| <span data-ttu-id="58e40-201">control.exe инфракрасной связи</span><span class="sxs-lookup"><span data-stu-id="58e40-201">control.exe infrared</span></span>       | <span data-ttu-id="58e40-202">Запускает окно " **Монитор инфракрасной связи** " (если установлено).</span><span class="sxs-lookup"><span data-stu-id="58e40-202">Launches the **Infrared Monitor** window (if installed).</span></span> |
| <span data-ttu-id="58e40-203">control.exe усерпассвордс</span><span class="sxs-lookup"><span data-stu-id="58e40-203">control.exe userpasswords</span></span>  | <span data-ttu-id="58e40-204">Открывает окно **учетные записи пользователей** .</span><span class="sxs-lookup"><span data-stu-id="58e40-204">Launches the **User Accounts** window.</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="58e40-205">См. также</span><span class="sxs-lookup"><span data-stu-id="58e40-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58e40-206">Элементы панели управления</span><span class="sxs-lookup"><span data-stu-id="58e40-206">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="58e40-207">Руководство по работе пользователей</span><span class="sxs-lookup"><span data-stu-id="58e40-207">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="58e40-208">Регистрация элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="58e40-208">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="58e40-209">Использование Кплапплет</span><span class="sxs-lookup"><span data-stu-id="58e40-209">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="58e40-210">Обработка сообщений в панели управления</span><span class="sxs-lookup"><span data-stu-id="58e40-210">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="58e40-211">Расширение элементов панели управления "система"</span><span class="sxs-lookup"><span data-stu-id="58e40-211">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="58e40-212">Назначение категорий панели управления</span><span class="sxs-lookup"><span data-stu-id="58e40-212">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="58e40-213">Создание ссылок на задачи с возможностью поиска для элемента панели управления</span><span class="sxs-lookup"><span data-stu-id="58e40-213">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="58e40-214">Доступ к панели управления в защищенном режиме в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58e40-214">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
