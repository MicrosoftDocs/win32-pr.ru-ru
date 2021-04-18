---
title: Windows Deployment Services
description: Развертывание операционных систем Windows. Настройте новые клиенты с помощью сетевой установки, не требуя от администраторов посетить каждый компьютер или установить их непосредственно с компакт-диска или DVD-диска.
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Службы развертывания Windows.
- Службы развертывания Windows, Домашняя страница
- службы развертывания служб развертывания Windows
- Службы развертывания Windows WDS см. в разделе службы развертывания Windows.
- Службы удаленной установки службы развертывания Windows см. в разделе службы развертывания Windows
- Службы развертывания Windows (RIS) см. в разделе службы развертывания Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b35bebb000b383552f12d259ca17552165e9247f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700927"
---
# <a name="windows-deployment-services"></a><span data-ttu-id="35927-110">Windows Deployment Services</span><span class="sxs-lookup"><span data-stu-id="35927-110">Windows Deployment Services</span></span>

## <a name="purpose"></a><span data-ttu-id="35927-111">Назначение</span><span class="sxs-lookup"><span data-stu-id="35927-111">Purpose</span></span>

<span data-ttu-id="35927-112">Службы развертывания Windows (WDS) — это пересмотренная версия служб удаленной установки (RIS).</span><span class="sxs-lookup"><span data-stu-id="35927-112">Windows Deployment Services (WDS) is the revised version of Remote Installation Services (RIS).</span></span> <span data-ttu-id="35927-113">WDS позволяет развертывать операционные системы Windows.</span><span class="sxs-lookup"><span data-stu-id="35927-113">WDS enables the deployment of Windows operating systems.</span></span> <span data-ttu-id="35927-114">WDS можно использовать для настройки новых клиентов с сетевой установкой, не требуя от администраторов посещать каждый компьютер или устанавливать их непосредственно с компакт-диска или DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="35927-114">You can use WDS to set up new clients with a network-based installation without requiring that administrators visit each computer or install directly from CD or DVD media.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="35927-115">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="35927-115">Developer audience</span></span>

<span data-ttu-id="35927-116">Основная аудитория разработчика API WDS предназначена для групп, в которых разрабатываются пользовательские средства и процессы для ИТ и других групп администрирования компьютеров.</span><span class="sxs-lookup"><span data-stu-id="35927-116">The primary developer audience of the WDS API is for groups that develop custom tools and processes for IT and other computer administration groups.</span></span> <span data-ttu-id="35927-117">В средах, в которых нельзя использовать стандартное решение служб развертывания Windows (WDS), API WDS обеспечивает программный доступ к некоторым компонентам WDS.</span><span class="sxs-lookup"><span data-stu-id="35927-117">In environments where the standard Windows Deployment Services (WDS) solution cannot be used, the WDS API enables programmatic access to some WDS components.</span></span>

<span data-ttu-id="35927-118">Изготовителям оборудования (OEM), сборщикам систем и корпоративным ИТ-специалистам требуются сведения о развертывании Windows на новых компьютерах. сведения о стандартном решении служб развертывания Windows (WDS) см. в разделе [Пошаговое руководство по обновлению служб развертывания Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) и [пакет автоматической установки Windows (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).</span><span class="sxs-lookup"><span data-stu-id="35927-118">Original Equipment Manufacturers (OEMs), system builders, and corporate IT professionals looking for information on how to deploy Windows onto new computers, should see the information about the standard Windows Deployment Services (WDS) solution in the [Windows Deployment Services Update Step-by-Step Guide](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) and the [Windows Automated Installation Kit (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="35927-119">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="35927-119">Run-time requirements</span></span>

<span data-ttu-id="35927-120">WDS доступна в качестве надстройки для Windows Server 2003 с пакетом обновления 1 (SP1) и входит в состав операционной системы, начиная с Windows Server 2003 с пакетом обновления 2 (SP2) и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="35927-120">WDS is available as an add-on for Windows Server 2003 with Service Pack 1 (SP1) and is included in the operating system starting with Windows Server 2003 with Service Pack 2 (SP2) and Windows Server 2008.</span></span> <span data-ttu-id="35927-121">API PXE-сервера WDS требует наличия роли сервера WDS на сервере для реализации пользовательских поставщиков PXE.</span><span class="sxs-lookup"><span data-stu-id="35927-121">The WDS PXE Server API requires the WDS server role on the server to implement custom PXE providers.</span></span> <span data-ttu-id="35927-122">Для клиентского API WDS требуется фаза обработки установки Microsoft среда предустановки Windows (Windows PE 2,0).</span><span class="sxs-lookup"><span data-stu-id="35927-122">The WDS Client API requires the Microsoft Windows Preinstallation Environment (Windows PE 2.0) phase of setup processing.</span></span> <span data-ttu-id="35927-123">Загрузочный образ RAMDISK Windows PE 2,0 в. Для реализации пользовательских WDS-клиентов необходимо загрузить формат WIM в рамках процесса сетевой загрузки.</span><span class="sxs-lookup"><span data-stu-id="35927-123">A RAMDISK bootable image of Windows PE 2.0 in the .WIM format must be downloaded as part of the network boot process to implement custom WDS clients.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="35927-124">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="35927-124">In this section</span></span>



| <span data-ttu-id="35927-125">Раздел</span><span class="sxs-lookup"><span data-stu-id="35927-125">Topic</span></span>                                                                                                 | <span data-ttu-id="35927-126">Описание</span><span class="sxs-lookup"><span data-stu-id="35927-126">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="35927-127">Сведения об API служб развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="35927-127">About the Windows Deployment Services API</span></span>](about-the-windows-deployment-services-api.md)<br/> | <span data-ttu-id="35927-128">Общие сведения об API сервера WDS и API клиента WDS.</span><span class="sxs-lookup"><span data-stu-id="35927-128">General information about the WDS Server API and WDS Client API.</span></span><br/>    |
| [<span data-ttu-id="35927-129">Справочник по службам развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="35927-129">Windows Deployment Services Reference</span></span>](windows-deployment-services-reference.md)<br/>         | <span data-ttu-id="35927-130">Описывает функции и структуры служб развертывания Windows.</span><span class="sxs-lookup"><span data-stu-id="35927-130">Describes the Windows Deployment Services functions and structures.</span></span><br/> |



 

 

