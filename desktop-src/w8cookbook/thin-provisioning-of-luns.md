---
title: Тонкая подготовка логических устройств
description: Тонкая подготовка логических устройств
ms.assetid: D64ECA7B-62AC-4C14-BE4B-84DA2E20C16B
keywords:
- LUN
- РЕЖИМА
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4abb6fa3cec112737b23e3cd658a48984cb0fcd1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "104070759"
---
# <a name="thin-provisioning-of-logical-units"></a><span data-ttu-id="481b4-105">Тонкая подготовка логических устройств</span><span class="sxs-lookup"><span data-stu-id="481b4-105">Thin provisioning of logical units</span></span>

## <a name="platforms"></a><span data-ttu-id="481b4-106">Платформы</span><span class="sxs-lookup"><span data-stu-id="481b4-106">Platforms</span></span>

<span data-ttu-id="481b4-107">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="481b4-107">**Clients** – Windows 8</span></span>  
<span data-ttu-id="481b4-108">**Серверы** — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="481b4-108">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="481b4-109">Описание</span><span class="sxs-lookup"><span data-stu-id="481b4-109">Description</span></span>

<span data-ttu-id="481b4-110">Тонкая подготовка Windows — это интерфейс к комплексному решению для подготовки хранилища.</span><span class="sxs-lookup"><span data-stu-id="481b4-110">Windows Thin Provisioning is an interface to the end-to-end storage provisioning solution.</span></span> <span data-ttu-id="481b4-111">Для доставки высокодоступной, масштабируемой и удобной для пользователя службы подготовки хранилища требуются надежные реализации с узла сервера на целевое устройство хранения.</span><span class="sxs-lookup"><span data-stu-id="481b4-111">To deliver a highly available, scalable and user-friendly storage provisioning service requires robust implementations from the server host to the storage target device.</span></span> <span data-ttu-id="481b4-112">Функция тонкой подготовки Windows обеспечивает синхронное представление запоминающих устройств с тонкой подготовкой к системному администратору, ИТ-менеджеру и администратору хранилища посредством идентификации LUN с тонкой подготовкой, порогового уведомления, обработки нехватки ресурсов, реорганизации пространства и получения состояния логической адресации блоков (LBA).</span><span class="sxs-lookup"><span data-stu-id="481b4-112">The Windows thin provisioning feature provides a synchronous view of the thin provisioning storage devices to the system administrator, IT manager, and storage administrator through the thinly provisioned logical unit’s (LUN’s) identification, threshold notification, resource exhaustion handling, space reclamation, and logical block addressing (LBA) state retrieval.</span></span> <span data-ttu-id="481b4-113">Функция тонкой подготовки Windows представляет собой надежную модель службы подготовки хранилища, которая может применяться к системам хранения данных клиента и сервера, хранилищу виртуализации и службам облачного хранилища.</span><span class="sxs-lookup"><span data-stu-id="481b4-113">The Windows thin provisioning feature presents a robust storage provisioning service model that can be applied to client-server storage systems, virtualization storage, and cloud storage services.</span></span> <span data-ttu-id="481b4-114">Корпорация Майкрософт обеспечит высокое качество функции тонкой подготовки, применяя требования к комплекту сертификации оборудования для тонкой подготовки Windows для продуктов массивов хранения данных.</span><span class="sxs-lookup"><span data-stu-id="481b4-114">Microsoft will ensure the high quality of the thin provisioning feature by enforcing the Windows Thin Provisioning Hardware Certification Kit requirements for storage array products.</span></span>

<span data-ttu-id="481b4-115">Решение для хранения тонкой подготовки Windows:</span><span class="sxs-lookup"><span data-stu-id="481b4-115">The Windows Thin Provisioning storage solution:</span></span>

-   <span data-ttu-id="481b4-116">Позволяет администраторам хранилища создавать больший LUN с меньшим объемом ресурсов физического диска.</span><span class="sxs-lookup"><span data-stu-id="481b4-116">Allows storage administrators to create a larger LUN with fewer physical disk resources</span></span>
-   <span data-ttu-id="481b4-117">Добавляет или удаляет ресурс физического диска без прерывания работы службы подготовки хранилища.</span><span class="sxs-lookup"><span data-stu-id="481b4-117">Adds or removes physical disk resource without interrupting the storage provisioning service</span></span>
-   <span data-ttu-id="481b4-118">Предупреждает пользователей об использовании тома хранилища с помощью порогового значения</span><span class="sxs-lookup"><span data-stu-id="481b4-118">Alerts users to the storage volume usage through the threshold setting</span></span>
-   <span data-ttu-id="481b4-119">Поддерживает подготовку хранилища с помощью конфигурации общего пула носителей</span><span class="sxs-lookup"><span data-stu-id="481b4-119">Supports storage provisioning through the shared storage pool configuration</span></span>
-   <span data-ttu-id="481b4-120">Увеличение или уменьшение размера пула носителей в соответствии с потребностями и использованием дискового пространства</span><span class="sxs-lookup"><span data-stu-id="481b4-120">Increases or decreases the size of the storage pool according to the demand and usage of storage space</span></span>

<span data-ttu-id="481b4-121">Сводка функций тонкой подготовки Windows:</span><span class="sxs-lookup"><span data-stu-id="481b4-121">Summary of the Windows Thin Provisioning features:</span></span>

-   <span data-ttu-id="481b4-122">Идентификация LUN с тонкой подготовкой</span><span class="sxs-lookup"><span data-stu-id="481b4-122">Thin Provisioning LUN identification</span></span>
-   <span data-ttu-id="481b4-123">Обработка пороговых уведомлений, нехватки ресурсов и постоянного расходования ресурсов</span><span class="sxs-lookup"><span data-stu-id="481b4-123">Handles for threshold notification, temporary resource exhaustion, and permanent resource exhaustion</span></span>
-   <span data-ttu-id="481b4-124">Освобождение дискового пространства</span><span class="sxs-lookup"><span data-stu-id="481b4-124">Storage space reclamation</span></span>
-   <span data-ttu-id="481b4-125">Сопоставление запросов о состоянии логических блоков</span><span class="sxs-lookup"><span data-stu-id="481b4-125">Mapping state queries of logical blocks</span></span>

## <a name="manifestation"></a><span data-ttu-id="481b4-126">Проявление</span><span class="sxs-lookup"><span data-stu-id="481b4-126">Manifestation</span></span>

<span data-ttu-id="481b4-127">Без правильного понимания дескрипторов Windows для тонкой подготовки LUN приложение может завершиться с непредвиденным поведением или по неизвестной причине.</span><span class="sxs-lookup"><span data-stu-id="481b4-127">Without the proper understanding of the Windows handles for thin provisioning LUN, the app could fail with unexpected behavior or for an unknown cause.</span></span>

## <a name="using-thin-provisioning-luns"></a><span data-ttu-id="481b4-128">Использование LUN с тонкой подготовкой</span><span class="sxs-lookup"><span data-stu-id="481b4-128">Using thin provisioning LUNs</span></span>

<span data-ttu-id="481b4-129">Чтобы использовать устройства LUN с тонкой подготовкой в Windows 8 или Windows Server 2012, администратор системы и хранилища должен иметь в виду следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="481b4-129">To use thinly provisioned LUNs in Windows 8 or Windows Server 2012, system and storage administrators should be aware of these matters:</span></span>

-   <span data-ttu-id="481b4-130">Идентификация LUN с тонкой подготовкой; Системные администраторы или конечные пользователи могут использовать Defrag и служебную программу оптимизатора хранилища для обнаружения типа носителя устройства хранения.</span><span class="sxs-lookup"><span data-stu-id="481b4-130">Thin provisioning LUN identification; system administrators or end users can use Defrag and the Storage Optimizer utility to identify the media type of the storage device</span></span>
-   <span data-ttu-id="481b4-131">При достижении порогового значения или события нехватки ресурсов Windows регистрирует системное событие для предупреждения системного администратора.</span><span class="sxs-lookup"><span data-stu-id="481b4-131">When a threshold or a permanent resource exhaustion event is hit, Windows will log a system event to alert the system administrator</span></span>
-   <span data-ttu-id="481b4-132">Возможность реорганизации дискового пространства может выполняться вручную или автоматически при помощи уведомления об удалении файлов или планировщика оптимизатора хранилища.</span><span class="sxs-lookup"><span data-stu-id="481b4-132">Storage space reclamation can be performed manually or automatically by file delete notification or the scheduler of the storage optimizer</span></span>
-   <span data-ttu-id="481b4-133">Администратор хранилища должен реализовать пороговое уведомление для оповещения системного администратора или конечного пользователя и избежать непредвиденных прерываний службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="481b4-133">Storage administrator should implement the threshold notification to alert system administrator or end user and avoid any unexpected storage service interruption</span></span>

## <a name="tests"></a><span data-ttu-id="481b4-134">Тесты</span><span class="sxs-lookup"><span data-stu-id="481b4-134">Tests</span></span>

-   <span data-ttu-id="481b4-135">Массив хранения данных должен получить сертификат тонкой подготовки Windows 8 для поддержки функций тонкой подготовки Windows</span><span class="sxs-lookup"><span data-stu-id="481b4-135">Storage array must receive Windows 8 Thin Provisioning certificate to support Windows Thin Provisioning features</span></span>
-   <span data-ttu-id="481b4-136">Комплект сертификации оборудования для тонкой подготовки Windows для массива хранения данных будет полезным средством тестирования для проверки возможности массива хранения данных для поддержки функций тонкой подготовки Windows.</span><span class="sxs-lookup"><span data-stu-id="481b4-136">Windows Thin Provisioning Hardware Certification Kit for storage array will be a useful test tool to verify storage array’s capability for Windows Thin Provisioning feature support</span></span>
-   <span data-ttu-id="481b4-137">Windows ждет, что LUN тонкой подготовки и LUN полной подготовки будут работать в одной системе без каких бы то ни было проблем.</span><span class="sxs-lookup"><span data-stu-id="481b4-137">Windows expects the Thin Provisioning LUN and Full Provisioning LUN to work in the same system without any issue</span></span>

## <a name="resources"></a><span data-ttu-id="481b4-138">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="481b4-138">Resources</span></span>

-   [<span data-ttu-id="481b4-139">Спецификация команды T10 SCSI Block (SBC3r27)</span><span class="sxs-lookup"><span data-stu-id="481b4-139">T10 SCSI Block Command Spec (SBC3r27)</span></span>](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r27.pdf)
-   [<span data-ttu-id="481b4-140">Службы панели мониторинга оборудования</span><span class="sxs-lookup"><span data-stu-id="481b4-140">Hardware Dashboard Services</span></span>](/windows-hardware/drivers/dashboard/)

 

 