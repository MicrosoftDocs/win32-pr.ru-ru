---
description: Создавайте резервные копии томов, пока приложения в системе продолжают запись в тома. Сократите время простоя приложения, быстро создав моментальный снимок (теневое копирование) тома, который дублирует все данные. Выполните многотоме резервное копирование.
ms.assetid: 1eca1e3e-fc86-44b5-b3c4-bcee41bc5a43
title: Служба теневого копирования томов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438ef32f1cbbc5fc82878486d9ad35b549f4535a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692382"
---
# <a name="volume-shadow-copy-service"></a><span data-ttu-id="2308d-105">Служба теневого копирования томов</span><span class="sxs-lookup"><span data-stu-id="2308d-105">Volume Shadow Copy Service</span></span>

## <a name="purpose"></a><span data-ttu-id="2308d-106">Назначение</span><span class="sxs-lookup"><span data-stu-id="2308d-106">Purpose</span></span>

<span data-ttu-id="2308d-107">Служба теневого копирования томов (VSS) — это набор COM-интерфейсов, который реализует платформу, позволяющую выполнять резервное копирование томов, пока приложения в системе продолжают записывать данные на тома.</span><span class="sxs-lookup"><span data-stu-id="2308d-107">The Volume Shadow Copy Service (VSS) is a set of COM interfaces that implements a framework to allow volume backups to be performed while applications on a system continue to write to the volumes.</span></span>

<span data-ttu-id="2308d-108">Общие сведения о службе VSS для системных администраторов см. в разделе [Служба теневого копирования томов](/windows-server/storage/file-server/volume-shadow-copy-service) в библиотеке TechNet.</span><span class="sxs-lookup"><span data-stu-id="2308d-108">For an introduction to VSS for system administrators, see [Volume Shadow Copy Service](/windows-server/storage/file-server/volume-shadow-copy-service) in the TechNet Library.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="2308d-109">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="2308d-109">Run-time requirements</span></span>

<span data-ttu-id="2308d-110">Служба VSS поддерживается в Microsoft Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="2308d-110">VSS is supported on Microsoft Windows XP and later.</span></span> <span data-ttu-id="2308d-111">Сведения о требованиях времени выполнения для определенного программного элемента см. в разделе "требования" документации для этого элемента.</span><span class="sxs-lookup"><span data-stu-id="2308d-111">For information about run-time requirements for a particular programming element, see the Requirements section of the documentation for that element.</span></span>

<span data-ttu-id="2308d-112">Все 32-разрядные приложения VSS (инициаторы запросов, поставщики и модули записи) должны выполняться как собственные 32-разрядные или 64-разрядные приложения.</span><span class="sxs-lookup"><span data-stu-id="2308d-112">All 32-bit VSS applications (requesters, providers, and writers) must run as native 32-bit or 64-bit applications.</span></span> <span data-ttu-id="2308d-113">Их запуск в эмуляторе WOW64 не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2308d-113">Running them under WOW64 is not supported.</span></span> <span data-ttu-id="2308d-114">Дополнительные сведения см. в разделе [Поддерживаемые конфигурации и ограничения](usage-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="2308d-114">For more information, see [Supported Configurations and Restrictions](usage-conventions.md).</span></span>

<span data-ttu-id="2308d-115">**Windows Server 2003 и Windows XP:** Запуск 32-разрядов запросов VSS в эмуляторе WOW64 поддерживается, но не для резервных копий состояния системы.</span><span class="sxs-lookup"><span data-stu-id="2308d-115">**Windows Server 2003 and Windows XP:** Running 32-bit VSS requesters under WOW64 is supported, but not for system-state backups.</span></span> <span data-ttu-id="2308d-116">Запуск 32-разрядных поставщиков VSS и модулей записи в эмуляторе WOW64 не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2308d-116">Running 32-bit VSS providers and writers under WOW64 is not supported.</span></span> <span data-ttu-id="2308d-117">Поддержка запуска 32-разрядных запросов в подсистеме WOW64 была удалена в Windows Vista и последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="2308d-117">Support for running 32-bit requesters under WOW64 was removed in Windows Vista and subsequent versions.</span></span>

> [!Note]  
> <span data-ttu-id="2308d-118">Теневую копию, созданную в Windows Server 2003 R2 или Windows Server 2003, нельзя использовать на компьютере под Windows Server 2008 R2 или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="2308d-118">A shadow copy that was created on Windows Server 2003 R2 or Windows Server 2003 cannot be used on a computer that is running Windows Server 2008 R2 or Windows Server 2008.</span></span> <span data-ttu-id="2308d-119">Теневую копию, созданную в Windows Server 2008 R2 или Windows Server 2008, нельзя использовать на компьютере под Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2308d-119">A shadow copy that was created on Windows Server 2008 R2 or Windows Server 2008 cannot be used on a computer that is running Windows Server 2003.</span></span> <span data-ttu-id="2308d-120">Однако теневую копию, созданную в Windows Server 2008, можно использовать на компьютере, работающем под Windows Server 2008 R2, и наоборот.</span><span class="sxs-lookup"><span data-stu-id="2308d-120">However, a shadow copy that was created on Windows Server 2008 can be used on a computer that is running Windows Server 2008 R2, and vice versa.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="2308d-121">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="2308d-121">In this section</span></span>



| <span data-ttu-id="2308d-122">Раздел</span><span class="sxs-lookup"><span data-stu-id="2308d-122">Topic</span></span>                                                          | <span data-ttu-id="2308d-123">Описание</span><span class="sxs-lookup"><span data-stu-id="2308d-123">Description</span></span>                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2308d-124">Обзор</span><span class="sxs-lookup"><span data-stu-id="2308d-124">Overview</span></span>](volume-shadow-copy-service-overview.md)<br/> | <span data-ttu-id="2308d-125">Описывает объектную модель VSS, стратегии резервного копирования и восстановления, а также способы создания поставщиков VSS, запрашивающих объектов и модулей записи.</span><span class="sxs-lookup"><span data-stu-id="2308d-125">Describes the VSS object model, backup and restore strategies, and how to create VSS providers, requesters, and writers.</span></span><br/> |
| [<span data-ttu-id="2308d-126">Ссылки</span><span class="sxs-lookup"><span data-stu-id="2308d-126">Reference</span></span>](volume-shadow-copy-reference.md)<br/>       | <span data-ttu-id="2308d-127">Описание классов VSS, типов данных, перечислений, функций, интерфейсов и структур.</span><span class="sxs-lookup"><span data-stu-id="2308d-127">Describes VSS classes, data types, enumerations, functions, interfaces, and structures.</span></span><br/>                                  |



 

## <a name="additional-resources"></a><span data-ttu-id="2308d-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2308d-128">Additional resources</span></span>



|                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2308d-129">Windows Vista и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="2308d-129">Windows Vista and later</span></span>            | <span data-ttu-id="2308d-130">Служба VSS доступна в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2308d-130">VSS is available in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2308d-131">Пакет SDK для Windows 7 и Windows Server 2008 R2 можно установить из [центра загрузки Windows](https://www.microsoft.com/download/details.aspx?id=8279).</span><span class="sxs-lookup"><span data-stu-id="2308d-131">You can install the SDK for Windows 7 and Windows Server 2008 R2 from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span> <span data-ttu-id="2308d-132">Версию пакета SDK для [ISO](https://www.microsoft.com/download/details.aspx?id=8442) также можно загрузить из центра загрузки Windows.</span><span class="sxs-lookup"><span data-stu-id="2308d-132">You can also download the [ISO version](https://www.microsoft.com/download/details.aspx?id=8442) of the SDK from the Windows Download Center.</span></span> <span data-ttu-id="2308d-133">Предыдущие версии пакета SDK можно скачать на [странице загрузки Windows SDK](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2308d-133">Previous versions of the SDK can be downloaded from the [Windows SDK Download Page](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span> |
| <span data-ttu-id="2308d-134">Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="2308d-134">Windows Server 2003 and Windows XP</span></span> | <span data-ttu-id="2308d-135">Служба VSS доступна в пакете SDK для служба теневого копирования томов 7,2, который можно скачать в [центре загрузки Windows](https://www.microsoft.com/download/details.aspx?id=23490).</span><span class="sxs-lookup"><span data-stu-id="2308d-135">VSS is available in the Volume Shadow Copy Service 7.2 SDK, which you can download from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=23490).</span></span> <span data-ttu-id="2308d-136">Обратите внимание, что \\ для 64-разрядных версий Windows Server 2003 и Windows XP можно использовать 64-битные файлы вссапи. lib в каталогах, которые находятся в каталоге файлов Win2003 obj.</span><span class="sxs-lookup"><span data-stu-id="2308d-136">Note that the 64-bit vssapi.lib files in the directories under the Win2003\\Obj directory can be used for the 64-bit versions of Windows Server 2003 and Windows XP.</span></span>                                                                                                                                                                 |



 

 

 
