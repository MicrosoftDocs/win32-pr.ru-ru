---
title: Диспетчер перезапуска
description: Создание пользовательских установщиков для устранения перезапусков системы, необходимых для обновления используемого файла. Завершите работу и перезапустите все, но критически важные системные службы из программ.
ms.assetid: 44b7975a-0093-4c8f-9a14-2a6bfd7a68a5
keywords:
- Диспетчер перезапуска диспетчера перезапуска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1244cff7bc22fd2e7b6d2540051bd0984596086
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070341"
---
# <a name="restart-manager"></a><span data-ttu-id="5256f-105">Диспетчер перезапуска</span><span class="sxs-lookup"><span data-stu-id="5256f-105">Restart Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="5256f-106">Назначение</span><span class="sxs-lookup"><span data-stu-id="5256f-106">Purpose</span></span>

<span data-ttu-id="5256f-107">API диспетчера перезапуска может сократить или уменьшить число перезапусков системы, необходимых для завершения установки или обновления.</span><span class="sxs-lookup"><span data-stu-id="5256f-107">The Restart Manager API can eliminate or reduce the number of system restarts that are required to complete an installation or update.</span></span> <span data-ttu-id="5256f-108">Основная причина обновления программного обеспечения требует перезапуска системы во время установки или обновления, поскольку некоторые обновляемые файлы в настоящее время используются запущенным приложением или службой.</span><span class="sxs-lookup"><span data-stu-id="5256f-108">The primary reason software updates require a system restart during an installation or update is that some of the files that are being updated are currently being used by a running application or service.</span></span> <span data-ttu-id="5256f-109">Диспетчер перезапуска позволяет завершить работу всех [системных служб, кроме критических](critical-system-services.md) , и перезапустить их.</span><span class="sxs-lookup"><span data-stu-id="5256f-109">The Restart Manager enables all but the [critical system services](critical-system-services.md) to be shut down and restarted.</span></span> <span data-ttu-id="5256f-110">Это освобождает используемые файлы и позволяет выполнять операции установки.</span><span class="sxs-lookup"><span data-stu-id="5256f-110">This frees files that are in use and allows installation operations to complete.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="5256f-111">Где применимо</span><span class="sxs-lookup"><span data-stu-id="5256f-111">Where applicable</span></span>

<span data-ttu-id="5256f-112">Библиотека DLL диспетчера перезапуска экспортирует общедоступный интерфейс C, который можно загрузить с помощью стандартных или пользовательских установщиков.</span><span class="sxs-lookup"><span data-stu-id="5256f-112">The Restart Manager DLL exports a public C interface that can be loaded by standard or custom installers.</span></span> <span data-ttu-id="5256f-113">Установщик может использовать диспетчер перезапуска для регистрации файлов, которые следует заменить во время установки приложения или обновления.</span><span class="sxs-lookup"><span data-stu-id="5256f-113">The installer can use the Restart Manager to register files that should be replaced during the installation of an application or update.</span></span> <span data-ttu-id="5256f-114">Затем в ходе последующего обновления или установки установщик может использовать диспетчер перезапуска, чтобы определить, какие файлы нельзя обновить, так как они используются в данный момент.</span><span class="sxs-lookup"><span data-stu-id="5256f-114">Then during a subsequent update or installation, the installer can use the Restart Manager to determine which files cannot be updated because they are currently in use.</span></span> <span data-ttu-id="5256f-115">Диспетчер перезапуска может завершить работу и перезапустить некритические службы или приложения, которые в настоящее время используют эти файлы.</span><span class="sxs-lookup"><span data-stu-id="5256f-115">Restart Manager can shut down and restart the non-critical services or applications that are currently using those files.</span></span> <span data-ttu-id="5256f-116">Установщики могут направлять диспетчер перезапуска для завершения работы и перезапуска приложений или служб на основе используемого файла, идентификатора процесса (PID) или короткого имени службы Windows.</span><span class="sxs-lookup"><span data-stu-id="5256f-116">Installers can direct the Restart Manager to shut down and restart applications or services based on the file in use, the process ID (PID), or the short-name of a Windows service.</span></span>

<span data-ttu-id="5256f-117">Диспетчер перезапуска предназначен для разработки приложений в стиле рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="5256f-117">Restart Manager is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="5256f-118">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="5256f-118">Developer audience</span></span>

<span data-ttu-id="5256f-119">Эта документация предназначена для разработчиков приложений установки, желающих воспользоваться преимуществами возможностей установщика в Windows Vista или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5256f-119">This documentation is intended for developers of installation applications who want to take advantage of the installer capabilities in Windows Vista or Windows Server 2008.</span></span> <span data-ttu-id="5256f-120">Приложения, использующие [установщик Windows](/windows/desktop/Msi/windows-installer-portal) версии 4,0 для установки и обслуживания, автоматически используют диспетчер перезапуска для уменьшения числа перезапусков системы.</span><span class="sxs-lookup"><span data-stu-id="5256f-120">Applications that use the [Windows Installer](/windows/desktop/Msi/windows-installer-portal) version 4.0 for installation and servicing automatically use the Restart Manager to reduce system restarts.</span></span> <span data-ttu-id="5256f-121">Пользовательские установщики также могут вызывать API диспетчера перезапуска для завершения работы и перезапуска приложений и служб.</span><span class="sxs-lookup"><span data-stu-id="5256f-121">Custom installers can also be designed to call the Restart Manager API to shut down and restart applications and services.</span></span> <span data-ttu-id="5256f-122">В случаях, когда перезапуск системы недоступен, установщики могут использовать API диспетчера перезапуска, чтобы запланировать перезапуск таким образом, чтобы минимизировать перебои в работе потока пользователя.</span><span class="sxs-lookup"><span data-stu-id="5256f-122">In cases where a system restart is unavoidable, installers can use the Restart Manager API to schedule restarts in such a way that it minimizes the disruption of the user's work flow.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5256f-123">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="5256f-123">Run-time requirements</span></span>

<span data-ttu-id="5256f-124">API диспетчера перезапуска доступен начиная с Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5256f-124">The Restart Manager API is available beginning with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="5256f-125">Диспетчер перезапуска состоит из одной библиотеки DLL, которую приложения могут загрузить для доступа к API диспетчера перезапуска.</span><span class="sxs-lookup"><span data-stu-id="5256f-125">Restart Manager consists of a single DLL that applications can load to access the Restart Manager API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5256f-126">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="5256f-126">In this section</span></span>



| <span data-ttu-id="5256f-127">Раздел</span><span class="sxs-lookup"><span data-stu-id="5256f-127">Topic</span></span>                                                                 | <span data-ttu-id="5256f-128">Описание</span><span class="sxs-lookup"><span data-stu-id="5256f-128">Description</span></span>                                                     |
|-----------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="5256f-129">О диспетчере перезапуска</span><span class="sxs-lookup"><span data-stu-id="5256f-129">About Restart Manager</span></span>](about-restart-manager.md)<br/>         | <span data-ttu-id="5256f-130">Обзорные разделы, описывающие диспетчер перезапуска.</span><span class="sxs-lookup"><span data-stu-id="5256f-130">Overview topics that describe the Restart Manager.</span></span><br/>   |
| [<span data-ttu-id="5256f-131">Использование диспетчера перезапуска</span><span class="sxs-lookup"><span data-stu-id="5256f-131">Using Restart Manager</span></span>](using-restart-manager.md)<br/>         | <span data-ttu-id="5256f-132">Обзорные разделы об использовании API диспетчера перезапуска.</span><span class="sxs-lookup"><span data-stu-id="5256f-132">Overview topics about using the Restart Manager API.</span></span><br/> |
| [<span data-ttu-id="5256f-133">Справочник по диспетчеру перезапуска</span><span class="sxs-lookup"><span data-stu-id="5256f-133">Restart Manager Reference</span></span>](restart-manager-reference.md)<br/> | <span data-ttu-id="5256f-134">Справочные разделы по API диспетчера перезапуска.</span><span class="sxs-lookup"><span data-stu-id="5256f-134">Reference topics for the Restart Manager API.</span></span><br/>        |



 

 

