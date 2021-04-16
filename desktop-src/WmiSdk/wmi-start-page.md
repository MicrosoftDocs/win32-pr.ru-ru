---
description: Инструментарий управления Windows (WMI) (WMI) — это инфраструктура для данных управления и операций в операционных системах на основе Windows.
ms.assetid: 4804152f-2042-4c6a-83c6-75c5e1ab7a04
ms.tgt_platform: multiple
title: Инструментарий управления Windows (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec2313ca7ee744ebe6f14be42a33e2e5878960b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692822"
---
# <a name="windows-management-instrumentation"></a><span data-ttu-id="e7324-103">Инструментарий управления Windows (WMI)</span><span class="sxs-lookup"><span data-stu-id="e7324-103">Windows Management Instrumentation</span></span>

## <a name="purpose"></a><span data-ttu-id="e7324-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="e7324-104">Purpose</span></span>

<span data-ttu-id="e7324-105">Инструментарий управления Windows (WMI) (WMI) — это инфраструктура для данных управления и операций в операционных системах на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="e7324-105">Windows Management Instrumentation (WMI) is the infrastructure for management data and operations on Windows-based operating systems.</span></span> <span data-ttu-id="e7324-106">Можно написать сценарии или приложения WMI для автоматизации задач администрирования на удаленных компьютерах, но Инструментарий WMI также предоставляет данные управления другим частям операционной системы и продуктам, например System Center Operations Manager, ранее Microsoft Operations Manager (MOM) или служба удаленного управления Windows ([WinRM](/windows/desktop/WinRM/portal)).</span><span class="sxs-lookup"><span data-stu-id="e7324-106">You can write WMI scripts or applications to automate administrative tasks on remote computers but WMI also supplies management data to other parts of the operating system and products, for example System Center Operations Manager, formerly Microsoft Operations Manager (MOM), or Windows Remote Management ([WinRM](/windows/desktop/WinRM/portal)).</span></span>

> [!Note]  
> <span data-ttu-id="e7324-107">Следующая документация предназначена для разработчиков и ИТ-администраторов.</span><span class="sxs-lookup"><span data-stu-id="e7324-107">The following documentation is targeted for developers and IT administrators.</span></span> <span data-ttu-id="e7324-108">Если вы являетесь пользователем, имеющим сообщение об ошибке, связанное с WMI, перейдите в [Служба поддержки Майкрософт](https://support.microsoft.com/) и найдите код ошибки, который вы видите в сообщении об ошибке.</span><span class="sxs-lookup"><span data-stu-id="e7324-108">If you are an end-user that has experienced an error message concerning WMI, you should go to [Microsoft Support](https://support.microsoft.com/) and search for the error code you see on the error message.</span></span> <span data-ttu-id="e7324-109">Дополнительные сведения об устранении неполадок со сценариями WMI и службой WMI см. в разделе [инструментарий WMI не работает.](/previous-versions/tn-archive/ff406382(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e7324-109">For more information about troubleshooting problems with WMI scripts and the WMI service, see [WMI Isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10))</span></span>

 

> [!Note]  
> <span data-ttu-id="e7324-110">Инструментарий WMI полностью поддерживается корпорацией Майкрософт; Однако последняя версия административных сценариев и управления доступна в инфраструктуре управления Windows (MI).</span><span class="sxs-lookup"><span data-stu-id="e7324-110">WMI is fully supported by Microsoft; however, the latest version of administrative scripting and control is available through the Windows Management Infrastructure (MI).</span></span> <span data-ttu-id="e7324-111">MI полностью совместима с предыдущими версиями инструментария WMI и предоставляет ряд функций и преимуществ, упрощающих разработку и разработку поставщиков и клиентов проще, чем когда-либо.</span><span class="sxs-lookup"><span data-stu-id="e7324-111">MI is fully compatible with previous versions of WMI, and provides a host of features and benefits that make designing and developing providers and clients easier than ever.</span></span> <span data-ttu-id="e7324-112">Дополнительные сведения см. в разделе [инфраструктура управления Windows (MI)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).</span><span class="sxs-lookup"><span data-stu-id="e7324-112">For more information, see [Windows Management Infrastructure (MI)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="e7324-113">Где применимо</span><span class="sxs-lookup"><span data-stu-id="e7324-113">Where applicable</span></span>

<span data-ttu-id="e7324-114">Инструментарий WMI можно использовать во всех приложениях на основе Windows и наиболее удобен в корпоративных приложениях и административных сценариях.</span><span class="sxs-lookup"><span data-stu-id="e7324-114">WMI can be used in all Windows-based applications, and is most useful in enterprise applications and administrative scripts.</span></span>

<span data-ttu-id="e7324-115">Системные администраторы могут найти сведения об использовании WMI на сайте TechNet [скриптцентер](https://www.microsoft.com/technet/scriptcenter/default.mspx)и в различных книгах об инструментарии WMI.</span><span class="sxs-lookup"><span data-stu-id="e7324-115">System administrators can find information about using WMI at the TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx), and in various books about WMI.</span></span> <span data-ttu-id="e7324-116">Дополнительные сведения см. в разделе Дополнительные [сведения](further-information.md).</span><span class="sxs-lookup"><span data-stu-id="e7324-116">For more information, see [Further Information](further-information.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e7324-117">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="e7324-117">Developer audience</span></span>

<span data-ttu-id="e7324-118">Инструментарий WMI предназначен для программистов, использующих C/C++, приложение Microsoft Visual Basic или язык сценариев, который имеет подсистему Windows и обрабатывает объекты Microsoft ActiveX.</span><span class="sxs-lookup"><span data-stu-id="e7324-118">WMI is designed for programmers who use C/C++, the Microsoft Visual Basic application, or a scripting language that has an engine on Windows and handles Microsoft ActiveX objects.</span></span> <span data-ttu-id="e7324-119">Хотя очень хорошо известно, что программирование COM является полезным, разработчики C++, пишущие приложения, могут найти хорошие примеры для начала работы с [созданием приложения WMI с помощью C++](creating-a-wmi-application-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="e7324-119">While some familiarity with COM programming is helpful, C++ developers who are writing applications can find good examples for getting started at [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md).</span></span>

<span data-ttu-id="e7324-120">Для разработки поставщиков управляемого кода или приложений на C# или Visual Basic .NET с помощью платформа .NET Framework см. раздел [WMI в платформа .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).</span><span class="sxs-lookup"><span data-stu-id="e7324-120">To develop managed code providers or applications in C# or Visual Basic .NET using the .NET Framework, see [WMI in .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).</span></span>

<span data-ttu-id="e7324-121">Многие администраторы и ИТ-специалисты обращаются к WMI с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e7324-121">Many administrators and IT professionals access WMI through PowerShell.</span></span> <span data-ttu-id="e7324-122">Командлет Get-WMI для PowerShell позволяет получить сведения для локального или удаленного репозитория WMI.</span><span class="sxs-lookup"><span data-stu-id="e7324-122">The Get-WMI cmdlet for PowerShell enables you to retrieve information for a local or remote WMI repository.</span></span> <span data-ttu-id="e7324-123">В частности, ряд разделов и классов, особенно в разделе [Создание клиентов WMI](creating-wmi-clients.md) , содержат примеры PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e7324-123">As such, a number of topics and classes, especially in the [Creating WMI Clients](creating-wmi-clients.md) section, contain PowerShell examples.</span></span> <span data-ttu-id="e7324-124">Дополнительные сведения об использовании PowerShell см. в статье [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) и [Создание сценариев с помощью Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).</span><span class="sxs-lookup"><span data-stu-id="e7324-124">For additional information on using PowerShell, see [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) and [Scripting with Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e7324-125">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="e7324-125">Run-time requirements</span></span>

<span data-ttu-id="e7324-126">Дополнительные сведения о том, какая операционная система необходима для использования определенного элемента API или класса WMI, см. в разделе "требования" каждого раздела документации по инструментарию WMI.</span><span class="sxs-lookup"><span data-stu-id="e7324-126">For more information about which operating system is required to use a specific API element or WMI class, see the Requirements section of each topic in the WMI documentation.</span></span>

<span data-ttu-id="e7324-127">Если ожидаемый компонент отсутствует, см. статью [доступность компонентов WMI в операционной системе](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="e7324-127">If an expected component appears to be missing, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

<span data-ttu-id="e7324-128">Для создания сценариев или приложений для WMI не нужно скачивать или устанавливать определенную разработку программного обеспечения (SDK).</span><span class="sxs-lookup"><span data-stu-id="e7324-128">You do not need to download or install a specific software development (SDK) in order to create scripts or applications for WMI.</span></span> <span data-ttu-id="e7324-129">Однако существуют некоторые средства администрирования WMI, которые могут оказаться полезными для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="e7324-129">However, there are some WMI administrative tools that developers find useful.</span></span> <span data-ttu-id="e7324-130">Дополнительные [сведения см. в](further-information.md)разделе "загрузки" этой статьи.</span><span class="sxs-lookup"><span data-stu-id="e7324-130">For more information, see the Downloads section in [Further Information](further-information.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e7324-131">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="e7324-131">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="e7324-132">Сведения об инструментарии WMI</span><span class="sxs-lookup"><span data-stu-id="e7324-132">About WMI</span></span>](about-wmi.md)
</dt> <dd>

<span data-ttu-id="e7324-133">Общие сведения об инструментарии WMI.</span><span class="sxs-lookup"><span data-stu-id="e7324-133">General information about WMI.</span></span>

</dd> <dt>

[<span data-ttu-id="e7324-134">Использование инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="e7324-134">Using WMI</span></span>](using-wmi.md)
</dt> <dd>

<span data-ttu-id="e7324-135">Сведения о разработке приложений для использования WMI, включая сведения о средствах.</span><span class="sxs-lookup"><span data-stu-id="e7324-135">Information about how to develop applications to use WMI, which includes information about tools.</span></span>

</dd> <dt>

[<span data-ttu-id="e7324-136">Справочник по инструментарию WMI</span><span class="sxs-lookup"><span data-stu-id="e7324-136">WMI Reference</span></span>](wmi-reference.md)
</dt> <dd>

<span data-ttu-id="e7324-137">Документация по классам WMI, классам C++ WMI, API WMI COM, API сценариев и другим справочным материалам WMI.</span><span class="sxs-lookup"><span data-stu-id="e7324-137">Documentation about the WMI classes, WMI C++ classes, WMI COM API, Scripting API, and other WMI reference material.</span></span>

</dd> </dl>

 

 
