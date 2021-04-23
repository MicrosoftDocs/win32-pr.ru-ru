---
title: Загрузка файла образа Windows (WimBoot)
description: Загрузка файла образа Windows (WimBoot)
ms.assetid: 1C4EFC42-6698-4981-8C55-D1DFC6309F31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f14ea506226e2c16d771ecec52fa31a8c871b4
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "103797131"
---
# <a name="windows-image-file-boot-wimboot"></a><span data-ttu-id="e633f-103">Загрузка файла образа Windows (WimBoot)</span><span class="sxs-lookup"><span data-stu-id="e633f-103">Windows Image File Boot (WimBoot)</span></span>

## <a name="platform"></a><span data-ttu-id="e633f-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="e633f-104">Platform</span></span>

<span data-ttu-id="e633f-105">**Клиенты:** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e633f-105">**Clients:** Windows 8.1</span></span>  

## <a name="description"></a><span data-ttu-id="e633f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e633f-106">Description</span></span>

<span data-ttu-id="e633f-107">WimBoot — это альтернативный способ развертывания Windows с помощью изготовителей оборудования.</span><span class="sxs-lookup"><span data-stu-id="e633f-107">WimBoot is an alternative way for OEMs to deploy Windows.</span></span> <span data-ttu-id="e633f-108">Развертывание WimBoot загружает и запускает Windows непосредственно из сжатого файла образа Windows (WIM).</span><span class="sxs-lookup"><span data-stu-id="e633f-108">A WimBoot deployment boots and runs Windows directly out of a compressed Windows Image File (WIM).</span></span> <span data-ttu-id="e633f-109">Этот WIM-файл является неизменяемым, и доступ к нему осуществляется с помощью нового драйвера фильтра файловой системы (WoF.sys).</span><span class="sxs-lookup"><span data-stu-id="e633f-109">This WIM file is immutable, and access to it is managed by a new file system filter driver (WoF.sys).</span></span>

<span data-ttu-id="e633f-110">Результатом является значительное сокращение дискового пространства, необходимого для установки Windows.</span><span class="sxs-lookup"><span data-stu-id="e633f-110">The result is a significant reduction in the disk space required to install Windows.</span></span>

## <a name="manifestations"></a><span data-ttu-id="e633f-111">Проявлениями</span><span class="sxs-lookup"><span data-stu-id="e633f-111">Manifestations</span></span>

<span data-ttu-id="e633f-112">На большинство приложений не следует зависеть от WimBoot.</span><span class="sxs-lookup"><span data-stu-id="e633f-112">Most applications should be completely unaffected by WimBoot.</span></span> <span data-ttu-id="e633f-113">Это может повлиять только на приложения, которые обращаются к системным файлам или предварительно загруженным файлам для доступа на запись.</span><span class="sxs-lookup"><span data-stu-id="e633f-113">Only applications that access and unlock system files or pre-loaded files for write access may be affected.</span></span> <span data-ttu-id="e633f-114">Поскольку WIM является неизменяемым, обновления для него (то есть системные или предварительно загруженные файлы) просто хранятся в разделе C: \\ .</span><span class="sxs-lookup"><span data-stu-id="e633f-114">Since the WIM is immutable, updates to it (that is, system or pre-loaded files) are simply stored on the C:\\ partition.</span></span>

<span data-ttu-id="e633f-115">Если приложение разблокировало доступ на запись для всех систем с поддержкой WIM и предварительно загруженных файлов, экономия, которую предоставляет WimBoot, будет полностью утрачена, так как все эти файлы будут распакованы и помещены на диск C: \\ .</span><span class="sxs-lookup"><span data-stu-id="e633f-115">If an application unlocked write access for all WIM-backed system and pre-loaded files, the savings that WimBoot delivers would be completely lost, as all of these files would be decompressed and placed on the C:\\ volume.</span></span>

<span data-ttu-id="e633f-116">Кроме того, для создания резервных копий и восстановления приложений необходимо знать о развертывании WimBoot, так как WIM находится в отдельной секции. то есть, при резервном копировании разделы C: \\ и WIM должны быть сохранены и оба должны быть восстановлены вместе.</span><span class="sxs-lookup"><span data-stu-id="e633f-116">Furthermore, back-up and restore applications need to be aware of WimBoot deployments, as the WIM is present in a separate partition; that is, on back-up, both the C:\\ and WIM partitions must be saved and both must be restored together.</span></span>

## <a name="solution"></a><span data-ttu-id="e633f-117">Решение</span><span class="sxs-lookup"><span data-stu-id="e633f-117">Solution</span></span>

<span data-ttu-id="e633f-118">Появились новые API, позволяющие приложениям напрямую запрашивать, если для определенного тома или файла используется WIM.</span><span class="sxs-lookup"><span data-stu-id="e633f-118">New APIs were introduced that allow applications to directly query if a given volume or file is backed by a WIM.</span></span> <span data-ttu-id="e633f-119">Эти сведения позволяют приложениям принимать соответствующие решения, например открывать эти файлы только для чтения или определять тома и разделы, резервные копии которых должны быть скопированы и восстановлены вместе.</span><span class="sxs-lookup"><span data-stu-id="e633f-119">This information allows applications to make appropriate decisions, such as opening these files only for read access or to identify volumes/partitions that have to be backed up and restored together.</span></span>

## <a name="compatibility-performance-reliability-or-usability-tests"></a><span data-ttu-id="e633f-120">Тесты на совместимость, производительность, надежность и удобство использования</span><span class="sxs-lookup"><span data-stu-id="e633f-120">Compatibility, performance, reliability, or usability tests</span></span>

<span data-ttu-id="e633f-121">Разработчики приложений должны протестировать свое программное обеспечение и соответствующие сценарии в системе WimBoot, особенно если эти приложения обращаются к системным или предварительно загруженным файлам.</span><span class="sxs-lookup"><span data-stu-id="e633f-121">Application developers should test their software and its corresponding scenarios on a WimBoot system, especially if these applications access system or pre-loaded files.</span></span> <span data-ttu-id="e633f-122">Особое внимание следует уделить значительному сокращению свободного места на диске после завершения сценария.</span><span class="sxs-lookup"><span data-stu-id="e633f-122">Special attention should be paid to a significant reduction in available disk space after a scenario has been completed.</span></span>

 

 




