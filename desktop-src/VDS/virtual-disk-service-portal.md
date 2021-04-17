---
description: Служба виртуальных дисков (VDS) управляет широким спектром конфигураций хранилища, от рабочих столов на одном диске до внешних массивов хранения данных. Служба предоставляет интерфейс прикладного программирования (API).
ms.assetid: 536aafd2-cc04-48cc-8ee7-920efbba2a5f
title: Служба виртуальных дисков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcfef0c5a73fcb2e6911395c829380c4bdfe56ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673837"
---
# <a name="virtual-disk-service"></a><span data-ttu-id="5000b-104">Служба виртуальных дисков</span><span class="sxs-lookup"><span data-stu-id="5000b-104">Virtual Disk Service</span></span>

<span data-ttu-id="5000b-105">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM службы виртуальных дисков заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5000b-105">\[Beginning with Windows 8 and Windows Server 2012, the Virtual Disk Service COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

## <a name="purpose"></a><span data-ttu-id="5000b-106">Назначение</span><span class="sxs-lookup"><span data-stu-id="5000b-106">Purpose</span></span>

<span data-ttu-id="5000b-107">Служба виртуальных дисков (VDS) управляет широким спектром конфигураций хранилища, от рабочих столов на одном диске до внешних массивов хранения данных.</span><span class="sxs-lookup"><span data-stu-id="5000b-107">The Virtual Disk Service (VDS) manages a wide range of storage configurations, from single-disk desktops to external storage arrays.</span></span> <span data-ttu-id="5000b-108">Служба предоставляет интерфейс прикладного программирования (API).</span><span class="sxs-lookup"><span data-stu-id="5000b-108">The service exposes an application programming interface (API).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="5000b-109">Где применимо</span><span class="sxs-lookup"><span data-stu-id="5000b-109">Where applicable</span></span>

<span data-ttu-id="5000b-110">Начиная с Windows 8 и Windows Server 8, интерфейс COM службы виртуальных дисков заменяется API управления хранением, интерфейсом программирования на основе WMI.</span><span class="sxs-lookup"><span data-stu-id="5000b-110">Beginning with Windows 8 and Windows Server 8, the Virtual Disk Service COM interface is superseded by the Storage Management API, a WMI-based programming interface.</span></span> <span data-ttu-id="5000b-111">Для управления подсистемами хранения, дисками, разделами и томами настоятельно рекомендуется использовать API управления хранилищами.</span><span class="sxs-lookup"><span data-stu-id="5000b-111">For managing storage subsystems, (Windows) disks, partitions, and volumes, we strongly recommend using the Storage Management API.</span></span> <span data-ttu-id="5000b-112">Дополнительные сведения см. в разделе [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).</span><span class="sxs-lookup"><span data-stu-id="5000b-112">For more information, see the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).</span></span>

<span data-ttu-id="5000b-113">Для всех случаев использования, за исключением зеркальных томов загрузки (с использованием зеркального тома для размещения операционной системы), динамические диски являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="5000b-113">For all usages except mirror boot volumes (using a mirror volume to host the operating system ), dynamic disks are deprecated.</span></span> <span data-ttu-id="5000b-114">Для данных, требующих устойчивости к сбою диска, используйте дисковые пространства — отказоустойчивое решение для виртуализации хранилища.</span><span class="sxs-lookup"><span data-stu-id="5000b-114">For data that requires resiliency against drive failure, use Storage Spaces, a resilient storage virtualization solution.</span></span> <span data-ttu-id="5000b-115">Дополнительные сведения см. в статье [Предварительная версия дисковых пространств](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="5000b-115">For more information, see [Storage Spaces Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).</span></span>

<span data-ttu-id="5000b-116">Разработчики приложений, использующие интерфейсы, описанные в этом разделе, могут запрашивать и настраивать разнородный набор предоставляемых поставщиком и внутренним образом управляемого хранилища.</span><span class="sxs-lookup"><span data-stu-id="5000b-116">Application developers who use the interfaces described in this guide can query and configure a heterogeneous set of vendor-supplied and internally managed storage.</span></span> <span data-ttu-id="5000b-117">Служба VDS скрывает от приложений сложности, связанные с хранилищем, делая службу независимой от поставщика и технологии.</span><span class="sxs-lookup"><span data-stu-id="5000b-117">VDS hides from applications the complexities associated with storage, making the service both vendor and technology neutral.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="5000b-118">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="5000b-118">Developer audience</span></span>

<span data-ttu-id="5000b-119">Эта документация предназначена для разработчиков приложений, знакомых с возможностями хранения данных на платформах Microsoft Windows и тех, кто знает о разработке в модели COM.</span><span class="sxs-lookup"><span data-stu-id="5000b-119">This documentation is intended for application developers who are familiar with the storage capabilities of Microsoft Windows platforms and who are knowledgeable about COM development.</span></span>

<span data-ttu-id="5000b-120">Данное руководством также предназначено для производителей аппаратных подсистем, которые разрабатывают и поддерживают программы поставщиков оборудования VDS.</span><span class="sxs-lookup"><span data-stu-id="5000b-120">The guide is also intended for hardware subsystem manufacturers who develop and support VDS hardware provider programs.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5000b-121">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="5000b-121">Run-time requirements</span></span>

<span data-ttu-id="5000b-122">Служба VDS поддерживается в Windows Server 2003, Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="5000b-122">VDS is supported on Windows Server 2003, Windows Vista, and later.</span></span> <span data-ttu-id="5000b-123">Сведения о требованиях времени выполнения для определенного программного элемента см. в разделе "требования" документации для этого элемента.</span><span class="sxs-lookup"><span data-stu-id="5000b-123">For information about run-time requirements for a particular programming element, see the Requirements section of the documentation for that element.</span></span>

<span data-ttu-id="5000b-124">Запуск 32-разрядных приложений VDS в WOW64 поддерживается, но 64-разрядные поставщики VDS должны работать как собственные приложения в 64-разрядных версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="5000b-124">Running 32-bit VDS applications under WOW64 is supported, but 64-bit VDS providers must run as native applications on 64-bit Windows versions.</span></span>

<span data-ttu-id="5000b-125">Служба VDS доступна в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5000b-125">VDS is available in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5000b-126">Пакет SDK для Windows 7 и Windows Server 2008 R2 можно установить из [центра загрузки Windows](https://www.microsoft.com/download/details.aspx?id=8279).</span><span class="sxs-lookup"><span data-stu-id="5000b-126">You can install the SDK for Windows 7 and Windows Server 2008 R2 from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span> <span data-ttu-id="5000b-127">Эту версию Windows SDK можно использовать для разработки приложений VDS для Windows Server 2003, Windows Vista и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="5000b-127">This version of the Windows SDK can be used to develop VDS applications for Windows Server 2003, Windows Vista, and later.</span></span> <span data-ttu-id="5000b-128">Версию пакета SDK для [ISO](https://www.microsoft.com/download/details.aspx?id=8442) также можно загрузить из центра загрузки Windows.</span><span class="sxs-lookup"><span data-stu-id="5000b-128">You can also download the [ISO version](https://www.microsoft.com/download/details.aspx?id=8442) of the SDK from the Windows Download Center.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5000b-129">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="5000b-129">In this section</span></span>



| <span data-ttu-id="5000b-130">Раздел</span><span class="sxs-lookup"><span data-stu-id="5000b-130">Topic</span></span>                                         | <span data-ttu-id="5000b-131">Описание</span><span class="sxs-lookup"><span data-stu-id="5000b-131">Description</span></span>                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5000b-132">О службе VDS</span><span class="sxs-lookup"><span data-stu-id="5000b-132">About VDS</span></span>](about-vds.md)<br/>         | <span data-ttu-id="5000b-133">Описание объектной модели VDS, стратегий конфигурации хранилища и уведомлений службы VDS.</span><span class="sxs-lookup"><span data-stu-id="5000b-133">Describes the VDS object model, storage-configuration strategies, and VDS notifications.</span></span><br/>    |
| [<span data-ttu-id="5000b-134">Использование VDS</span><span class="sxs-lookup"><span data-stu-id="5000b-134">Using VDS</span></span>](using-vds.md)<br/>         | <span data-ttu-id="5000b-135">Описание использования службы VDS для запроса и настройки устройств хранения.</span><span class="sxs-lookup"><span data-stu-id="5000b-135">Describes how to use VDS to query and configure storage devices.</span></span><br/>                            |
| [<span data-ttu-id="5000b-136">Ссылка на службу VDS</span><span class="sxs-lookup"><span data-stu-id="5000b-136">VDS Reference</span></span>](vds-reference.md)<br/> | <span data-ttu-id="5000b-137">Описывает константы VDS, типы данных, перечисления, интерфейсы, структуры и коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="5000b-137">Describes VDS constants, data types, enumerations, interfaces, structures, and error codes.</span></span><br/> |



 

 

