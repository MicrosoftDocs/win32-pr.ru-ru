---
description: Описание использования объекта Пенинпутпанел для программирования панели ввода планшетного ПК на уровне системы.
ms.assetid: f83c7709-86dc-4c64-ad17-2ad660eb57b7
title: Программирование панели ввода с помощью класса Пенинпутпанел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e00d1cb10983255ab2e532aa08de6e9e6a0fb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349392"
---
# <a name="programming-the-input-panel-using-the-peninputpanel-class"></a><span data-ttu-id="684aa-103">Программирование панели ввода с помощью класса Пенинпутпанел</span><span class="sxs-lookup"><span data-stu-id="684aa-103">Programming the Input Panel Using the PenInputPanel Class</span></span>

<span data-ttu-id="684aa-104">\[[**Пенинпутпанел**](peninputpanel-class.md) был заменен [Microsoft. Ink. TextInput](/previous-versions/ms581554(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="684aa-104">\[[**PenInputPanel**](peninputpanel-class.md) has been replaced by [Microsoft.Ink.TextInput](/previous-versions/ms581554(v=vs.100)).</span></span> <span data-ttu-id="684aa-105">Дополнительные сведения см. в разделе [Программирование панели ввода текста](programming-the-text-input-panel.md).\]</span><span class="sxs-lookup"><span data-stu-id="684aa-105">Please refer to [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="684aa-106">Описание использования объекта [**пенинпутпанел**](peninputpanel-class.md) для программирования панели ввода планшетного ПК на уровне системы.</span><span class="sxs-lookup"><span data-stu-id="684aa-106">Description of using the [**PenInputPanel**](peninputpanel-class.md) object to program the system-level Tablet PC Input Panel.</span></span>

## <a name="input-panel-vs-the-peninputpanel-object"></a><span data-ttu-id="684aa-107">Панель ввода и объект Пенинпутпанел</span><span class="sxs-lookup"><span data-stu-id="684aa-107">Input Panel vs. the PenInputPanel Object</span></span>

<span data-ttu-id="684aa-108">В Microsoft Windows XP Tablet PC Edition версии 1,0 панель ввода Tablet PC на уровне системы предоставляет универсальный механизм для выполнения ввода текста на платформе Windows, но не предоставляет программный доступ.</span><span class="sxs-lookup"><span data-stu-id="684aa-108">In Microsoft Windows XP Tablet PC Edition version 1.0, the system-level Tablet PC Input Panel provides a universal mechanism to accomplish text input across the Windows platform, but it does not provide programmatic access.</span></span> <span data-ttu-id="684aa-109">В пакете средств разработки программного обеспечения (SDK) для Windows XP Tablet PC Edition 1,5 и более поздних версий объект [**пенинпутпанел**](peninputpanel-class.md) позволяет интегрировать средства ввода текста непосредственно в приложения и предоставлять уровень контроля, который ранее не был доступен.</span><span class="sxs-lookup"><span data-stu-id="684aa-109">In Windows XP Tablet PC Edition Software Development Kit (SDK) version 1.5 and later, the [**PenInputPanel**](peninputpanel-class.md) object enables you to integrate text input tools directly into your applications, and provide a level of control not previously available.</span></span> <span data-ttu-id="684aa-110">Начиная с Windows XP Tablet PC Edition 2005, системная панель ввода была обновлена, чтобы включать встроенные функции ввода, предоставляемые объектом **пенинпутпанел** , и многое другое.</span><span class="sxs-lookup"><span data-stu-id="684aa-110">Starting with the Windows XP Tablet PC Edition 2005, the system-level Input Panel has been upgraded to include the in-place input functionality provided by the **PenInputPanel** object and more.</span></span>

<span data-ttu-id="684aa-111">На следующем рисунке показана панель ввода, отображаемая на [примере образца Auto Claims](auto-claims-form-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="684aa-111">The following graphic shows Input Panel displayed over the [Auto Claims Form Sample](auto-claims-form-sample.md) sample.</span></span>

![панель ввода, отображаемая в форме, используемой для утверждений автомобилей](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

<span data-ttu-id="684aa-113">Панель ввода заменяет [**пенинпутпанел**](peninputpanel-class.md) , предоставляя те же функции ввода на месте для любого приложения, работающего под управлением Windows XP Tablet PC Edition 2005 или более поздней версии, без необходимости дополнительного кода.</span><span class="sxs-lookup"><span data-stu-id="684aa-113">Input Panel supersedes the [**PenInputPanel**](peninputpanel-class.md) by supplying the same in-place input functionality to any application running on Windows XP Tablet PC Edition 2005 or later without the need for additional code.</span></span> <span data-ttu-id="684aa-114">Эта статья об использовании объекта **пенинпутпанел** предоставляется для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="684aa-114">This article on using the **PenInputPanel** object is provided for backward compatibility.</span></span> <span data-ttu-id="684aa-115">Приложения, которые уже используют объект **пенинпутпанел** , будут работать одинаково, за исключением того, что панель ввода будет отображаться вместо **пенинпутпанел** при запуске приложения в Windows XP Tablet PC Edition 2005 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="684aa-115">Applications that already utilize the **PenInputPanel** object will function the same except that Input Panel will be displayed instead of the **PenInputPanel** when the application is run on Windows XP Tablet PC Edition 2005 or later.</span></span>

<span data-ttu-id="684aa-116">Если вы разрабатываете новое приложение для планшетного ПК и хотите использовать встроенное решение для ввода данных, панель ввода обеспечивается автоматически в Windows XP Tablet PC Edition 2005 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="684aa-116">If you are developing a new application for the Tablet PC and want to have an in-place user input solution, Input Panel provides this automatically on Windows XP Tablet PC Edition 2005 or later.</span></span> <span data-ttu-id="684aa-117">Создавать экземпляр объекта [**пенинпутпанел**](peninputpanel-class.md) не требуется.</span><span class="sxs-lookup"><span data-stu-id="684aa-117">There is no need to instantiate the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>

## <a name="disabling-the-input-panel"></a><span data-ttu-id="684aa-118">Отключение панели ввода</span><span class="sxs-lookup"><span data-stu-id="684aa-118">Disabling the Input Panel</span></span>

<span data-ttu-id="684aa-119">Возможны случаи, когда необходимо отключить панель ввода.</span><span class="sxs-lookup"><span data-stu-id="684aa-119">There may be cases where you want to disable Input Panel.</span></span> <span data-ttu-id="684aa-120">Этого можно добиться двумя следующими способами.</span><span class="sxs-lookup"><span data-stu-id="684aa-120">There are two ways to accomplish this.</span></span> <span data-ttu-id="684aa-121">Это можно сделать программно или путем установки записи реестра, которая отключает панель ввода для всего приложения.</span><span class="sxs-lookup"><span data-stu-id="684aa-121">You can accomplish this programmatically or by setting a registry entry that disables Input Panel for your entire application.</span></span>

### <a name="disabling-input-panel-programmatically"></a><span data-ttu-id="684aa-122">Отключение панели ввода программными средствами</span><span class="sxs-lookup"><span data-stu-id="684aa-122">Disabling Input Panel Programmatically</span></span>

<span data-ttu-id="684aa-123">Чтобы отключить панель ввода программным путем, создайте экземпляр [**пенинпутпанел**](peninputpanel-class.md) и задайте для его свойства [**автоотображения**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) значение **false**.</span><span class="sxs-lookup"><span data-stu-id="684aa-123">To disable Input Panel programmatically, instantiate the [**PenInputPanel**](peninputpanel-class.md) and set its [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) property to **False**.</span></span>


```C++
using Microsoft.Ink;

// ...

private PenInputPanel theInputPanel;

// ...

private void Form1_Load(object sender, System.EventArgs e)
{
// Attach the Input Panel to a specific TextBox control.
theInputPanel = new PenInputPanel(textBox1);

// Disable the Input Panel for the TextBox.
theInputPanel.AutoShow = false;
}
```



<span data-ttu-id="684aa-124">Чтобы отключить панель ввода для нескольких элементов управления в одном приложении, создайте экземпляр объекта [**пенинпутпанел**](peninputpanel-class.md) для каждого элемента управления и присвойте свойству " [**Автопросмотр**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)" **значение false** для каждого или создайте экземпляр одного **пенинпутпанел** и переместите его из элемента управления в элемент управления в качестве фокуса ввода.</span><span class="sxs-lookup"><span data-stu-id="684aa-124">To disable Input Panel for multiple controls in a single application, either instantiate a [**PenInputPanel**](peninputpanel-class.md) object for each control and set the [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)property to **False** for each or instantiate a single **PenInputPanel** and move it from control to control as input focus changes.</span></span> <span data-ttu-id="684aa-125">Дополнительные сведения об этих двух методах см. в [образце раздела пенинпутпанел](peninputpanel-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="684aa-125">For more information about these two techniques, see the [PenInputPanel Sample](peninputpanel-sample.md) topic.</span></span>

### <a name="disabling-input-panel-through-the-registry"></a><span data-ttu-id="684aa-126">Отключение панели ввода в реестре</span><span class="sxs-lookup"><span data-stu-id="684aa-126">Disabling Input Panel Through the Registry</span></span>

<span data-ttu-id="684aa-127">Можно задать параметр реестра, чтобы отключить панель ввода для всего приложения.</span><span class="sxs-lookup"><span data-stu-id="684aa-127">You can set a registry entry to disable Input Panel for your entire application.</span></span> <span data-ttu-id="684aa-128">Однако это также приведет к отключению для общих диалоговых окон, таких как диалоговое окно **открытия файла** , диалоговое окно **Печать** и диалоговое окно **Сохранение файла** .</span><span class="sxs-lookup"><span data-stu-id="684aa-128">However, this will also disable it for common dialog boxes such as the **File Open** dialog box, the **Print** dialog box, and the **File Save** dialog box.</span></span> <span data-ttu-id="684aa-129">Это может сделать работу пользователя в приложении несовместимой с другими приложениями для планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="684aa-129">This may make the user experience in your application inconsistent with other Tablet PC applications.</span></span>

<span data-ttu-id="684aa-130">Если задать `DisableInPlace` для раздела реестра значение нуль, Пользовательский интерфейс панели ввода не будет отображаться в приложении.</span><span class="sxs-lookup"><span data-stu-id="684aa-130">Setting the `DisableInPlace` registry key to zero prevents Input Panel user interface (UI) from appearing in an application.</span></span> <span data-ttu-id="684aa-131">Раздел реестра необходимо разместить `DisableInPlace` по адресу `HKEY_LOCAL_MACHINE\Software\Microsoft\TabletTip\` .</span><span class="sxs-lookup"><span data-stu-id="684aa-131">You must place the `DisableInPlace` registry key at `HKEY_LOCAL_MACHINE\Software\Microsoft\TabletTip\`.</span></span> <span data-ttu-id="684aa-132">Затем добавьте новое значение реестра, используя полный путь к приложению, в котором необходимо отключить панель ввода.</span><span class="sxs-lookup"><span data-stu-id="684aa-132">Then, add a new registry value by using the full path of the application in which you want to disable Input Panel.</span></span> <span data-ttu-id="684aa-133">В следующем примере запись реестра отключает панель ввода в приложении с именем MyApp:</span><span class="sxs-lookup"><span data-stu-id="684aa-133">The following example registry entry disables Input Panel in an application called MyApp:</span></span>

`[HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\WindowsNT\TabletTIP\DisableInPlace]``"C:\Program Files\My App\MyApp.exe"=dword:00000000`

<span data-ttu-id="684aa-134">Если вы по-прежнему видите проблему в приложении после отключения пользовательского интерфейса панели ввода, может потребоваться отключить базовую платформу, которая запрашивает ваше приложение на предмет расположения курсора.</span><span class="sxs-lookup"><span data-stu-id="684aa-134">If you still see a problem in your application after you disable the Input Panel UI, it may be necessary to disable the underlying framework, which queries your application for the caret location.</span></span> <span data-ttu-id="684aa-135">Например, панель ввода может предоставлять ошибку в коде отслеживания курсора приложения.</span><span class="sxs-lookup"><span data-stu-id="684aa-135">For example, Input Panel may expose a bug in your application's caret tracking code.</span></span> <span data-ttu-id="684aa-136">Отключение запроса на отслеживание курсора также не повлечет за собой отображение пользовательского интерфейса панели ввода.</span><span class="sxs-lookup"><span data-stu-id="684aa-136">Turning off the caret tracking query also prevents the Input Panel UI from appearing.</span></span> <span data-ttu-id="684aa-137">Чтобы отключить платформу, присвойте `EnableCaretTracking` разделу реестра значение 0.</span><span class="sxs-lookup"><span data-stu-id="684aa-137">To disable the framework, set the `EnableCaretTracking` registry key to zero.</span></span> <span data-ttu-id="684aa-138">Путь к этому разделу находится в разделе `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\AppCompatFlags\CaretTracking\` .</span><span class="sxs-lookup"><span data-stu-id="684aa-138">Locate this key at `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\AppCompatFlags\CaretTracking\`.</span></span>

> [!Note]  
> <span data-ttu-id="684aa-139">Средства специальных возможностей и голосовые технологии в Windows XP также используют эту платформу, поэтому отключение запроса также отключает эти функции в приложении.</span><span class="sxs-lookup"><span data-stu-id="684aa-139">Accessibility tools and speech technology in Windows XP also use this framework, so disabling the query also disables these features in your application.</span></span>

 

## <a name="the-input-panel-and-web-pages"></a><span data-ttu-id="684aa-140">Панель ввода и веб-страницы</span><span class="sxs-lookup"><span data-stu-id="684aa-140">The Input Panel and Web Pages</span></span>

<span data-ttu-id="684aa-141">Чтобы использовать API на веб-странице, он должен работать в среде с частичным доверием.</span><span class="sxs-lookup"><span data-stu-id="684aa-141">In order to use an API on a Web page, it must function in a partial trust environment.</span></span> <span data-ttu-id="684aa-142">Все члены класса [**пенинпутпанел**](peninputpanel-class.md) должны иметь полное доверие, за исключением следующих:</span><span class="sxs-lookup"><span data-stu-id="684aa-142">All [**PenInputPanel**](peninputpanel-class.md) class members require full trust except the following:</span></span>

-   <span data-ttu-id="684aa-143">[Конструкторы пенинпутпанел](/previous-versions/dotnet/netframework-3.5/ms571341(v=vs.90)) (только управляемый код)</span><span class="sxs-lookup"><span data-stu-id="684aa-143">[PenInputPanel Constructors](/previous-versions/dotnet/netframework-3.5/ms571341(v=vs.90)) (managed code only)</span></span>
-   <span data-ttu-id="684aa-144">[Метод Dispose](/previous-versions/dotnet/netframework-3.5/ms571343(v=vs.90)) (только управляемый код)</span><span class="sxs-lookup"><span data-stu-id="684aa-144">[Dispose Method](/previous-versions/dotnet/netframework-3.5/ms571343(v=vs.90)) (managed code only)</span></span>
-   <span data-ttu-id="684aa-145">[Свойство аттачедедитконтрол](/previous-versions/ms582239(v=vs.100)) (только управляемый код)</span><span class="sxs-lookup"><span data-stu-id="684aa-145">[AttachedEditControl Property](/previous-versions/ms582239(v=vs.100)) (managed code only)</span></span>
-   [<span data-ttu-id="684aa-146">**Свойство "Автоотображение"**</span><span class="sxs-lookup"><span data-stu-id="684aa-146">**AutoShow Property**</span></span>](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)

<span data-ttu-id="684aa-147">Эти интерфейсы API работают в среде с частичным доверием, например на веб-странице, позволяя создавать экземпляры объекта [**пенинпутпанел**](peninputpanel-class.md) , подключать его к элементу управления и отключать панель ввода для этого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="684aa-147">These APIs function in a partial trust environment, such as a Web page, enabling you to instantiate a [**PenInputPanel**](peninputpanel-class.md) object, attach it to a control, and disable Input Panel for that control.</span></span> <span data-ttu-id="684aa-148">Дополнительные сведения см. в разделе Программирование панели ввода с помощью класса Пенинпутпанел и [рукописного ввода в Интернете](ink-on-the-web.md).</span><span class="sxs-lookup"><span data-stu-id="684aa-148">For more information, see Programming the Input Panel Using the PenInputPanel Class and [Ink on the Web](ink-on-the-web.md).</span></span>

## <a name="the-peninputpanel-object"></a><span data-ttu-id="684aa-149">Объект Пенинпутпанел</span><span class="sxs-lookup"><span data-stu-id="684aa-149">The PenInputPanel Object</span></span>

<span data-ttu-id="684aa-150">В оставшейся части этого раздела описывается, как использовать объект [**пенинпутпанел**](peninputpanel-class.md) в приложениях с поддержкой планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="684aa-150">The rest of this topic describes how to use the [**PenInputPanel**](peninputpanel-class.md) object in your Tablet PC–enabled applications.</span></span> <span data-ttu-id="684aa-151">В частности, этот раздел относится к объекту **пенинпутпанел** при обсуждении программного объекта, панели ввода пера при ссылке на элемент пользовательского интерфейса, а также панели ввода ПК (или панели ввода) при ссылке на глобальную панель ввода, обычно находящейся в боковой части экрана Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="684aa-151">More specifically, this topic refers to the **PenInputPanel** object when discussing the programming object, the pen input panel when referring to the UI element, and the PC Input Panel (or Input Panel) when referring to the global input panel typically found on the side of the Tablet PC screen.</span></span>

<span data-ttu-id="684aa-152">В следующих разделах описывается объект [**пенинпутпанел**](peninputpanel-class.md) и пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="684aa-152">The following sections describe the [**PenInputPanel**](peninputpanel-class.md) object and UI.</span></span>

-   [<span data-ttu-id="684aa-153">Сведения о панели ввода</span><span class="sxs-lookup"><span data-stu-id="684aa-153">About the Input Panel</span></span>](about-the-input-panel.md)
-   [<span data-ttu-id="684aa-154">Создание экземпляра класса Пенинпутпанел</span><span class="sxs-lookup"><span data-stu-id="684aa-154">Instantiating the PenInputPanel Class</span></span>](instantiating-the-peninputpanel-class.md)
-   [<span data-ttu-id="684aa-155">Поддержка фактоид</span><span class="sxs-lookup"><span data-stu-id="684aa-155">Factoid Support</span></span>](factoid-support.md)
-   [<span data-ttu-id="684aa-156">инфраструктуры текстовых служб (TSF)</span><span class="sxs-lookup"><span data-stu-id="684aa-156">Text Services Framework</span></span>](text-services-framework.md)
-   [<span data-ttu-id="684aa-157">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="684aa-157">Best Practices</span></span>](best-practices.md)

 

 
