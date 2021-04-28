---
description: Отказоустойчивая куча
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: Отказоустойчивая куча
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17ab2630e6dc28cb84604e48be1aa60bf208a97
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088402"
---
# <a name="fault-tolerant-heap"></a><span data-ttu-id="74532-103">Отказоустойчивая куча</span><span class="sxs-lookup"><span data-stu-id="74532-103">Fault Tolerant Heap</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="74532-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="74532-104">Affected Platforms</span></span>

<span data-ttu-id="74532-105">**Клиенты —** Windows 7</span><span class="sxs-lookup"><span data-stu-id="74532-105">**Clients -** Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="74532-106">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="74532-106">Feature Impact</span></span>

 <span data-ttu-id="74532-107">**Уровень серьезности —** Высокое</span><span class="sxs-lookup"><span data-stu-id="74532-107">**Severity -** Medium</span></span>  
<span data-ttu-id="74532-108">**Частота —** Низшую</span><span class="sxs-lookup"><span data-stu-id="74532-108">**Frequency -** Low</span></span>  


## <a name="description"></a><span data-ttu-id="74532-109">Описание</span><span class="sxs-lookup"><span data-stu-id="74532-109">Description</span></span>

<span data-ttu-id="74532-110">Отказоустойчивая куча (ФС) — это подсистема Windows 7, отвечающая за аварийное отслеживание сбоев приложений, а также автономное применение угроз для предотвращения сбоев в будущем на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="74532-110">The Fault Tolerant Heap (FTH) is a subsystem of Windows 7 responsible for monitoring application crashes and autonomously applying mitigations to prevent future crashes on a per application basis.</span></span> <span data-ttu-id="74532-111">Для большинства пользователей ФС будет работать без необходимости вмешательства или изменения на их части.</span><span class="sxs-lookup"><span data-stu-id="74532-111">For the vast majority of users, FTH will function with no need for intervention or change on their part.</span></span> <span data-ttu-id="74532-112">Однако в некоторых случаях разработчикам приложений и тестерам программного обеспечения может потребоваться переопределить поведение системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="74532-112">However, in some cases, application developers and software testers may need to override the default behavior of this system.</span></span>

## <a name="solution"></a><span data-ttu-id="74532-113">Решение</span><span class="sxs-lookup"><span data-stu-id="74532-113">Solution</span></span>

<span data-ttu-id="74532-114">**Просмотр действия отказоустойчивой кучи**</span><span class="sxs-lookup"><span data-stu-id="74532-114">**Viewing Fault Tolerant Heap activity**</span></span>

<span data-ttu-id="74532-115">Сведения о журналах отказоустойчивой кучи, когда служба запускается, останавливается или начинает устранение проблем для нового приложения.</span><span class="sxs-lookup"><span data-stu-id="74532-115">Fault Tolerant Heap logs information when the service starts, stops, or starts mitigating problems for a new application.</span></span> <span data-ttu-id="74532-116">Чтобы просмотреть эти сведения, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="74532-116">To view this information, follow these steps:</span></span>

1.  <span data-ttu-id="74532-117">Щелкните меню "Запуск".</span><span class="sxs-lookup"><span data-stu-id="74532-117">Click the Start menu.</span></span>
2.  <span data-ttu-id="74532-118">Щелкните правой кнопкой мыши **компьютер** и выберите пункт **Управление**.</span><span class="sxs-lookup"><span data-stu-id="74532-118">Right-click **Computer** and click **Manage**.</span></span>
3.  <span data-ttu-id="74532-119">Щелкните **Просмотр событий**  >  **журналы приложений и служб**  >  **Microsoft**  >  **Windows > отказоустойчивая — куча**</span><span class="sxs-lookup"><span data-stu-id="74532-119">Click **Event Viewer** > **Applications and Services Logs** > **Microsoft** > **Windows > Fault-Tolerant-Heap**</span></span>
4.  <span data-ttu-id="74532-120">Просмотр событий ФС.</span><span class="sxs-lookup"><span data-stu-id="74532-120">View FTH Events.</span></span>

<span data-ttu-id="74532-121">События останавливает и запустить службы не содержат дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="74532-121">The service stop and start events contain no additional data.</span></span> <span data-ttu-id="74532-122">Событие ФС Enabled содержит идентификатор процесса (PID), имя образа процесса и время запуска экземпляра процесса.</span><span class="sxs-lookup"><span data-stu-id="74532-122">The FTH Enabled event contains the Process ID (PID), the process image name, and the process instance start time.</span></span>

<span data-ttu-id="74532-123">**Отключение отказоустойчивой кучи**</span><span class="sxs-lookup"><span data-stu-id="74532-123">**Disabling Fault Tolerant Heap**</span></span>

<span data-ttu-id="74532-124">**Внимание!** При неправильном изменении реестра с помощью редактора реестра или другого метода могут возникнуть серьезные проблемы.</span><span class="sxs-lookup"><span data-stu-id="74532-124">**Caution** Serious problems may occur if you modify the registry incorrectly by using Registry Editor or by using another method.</span></span> <span data-ttu-id="74532-125">Эти проблемы могут потребовать переустановки операционной системы.</span><span class="sxs-lookup"><span data-stu-id="74532-125">These problems may require you to reinstall the operating system.</span></span> <span data-ttu-id="74532-126">Корпорация Майкрософт не гарантирует, что такие неполадки могут быть устранены.</span><span class="sxs-lookup"><span data-stu-id="74532-126">Microsoft cannot guarantee that these problems can be solved.</span></span> <span data-ttu-id="74532-127">Ответственность за изменение реестра лежит на пользователе.</span><span class="sxs-lookup"><span data-stu-id="74532-127">Modify the registry at your own risk.</span></span>  
 <span data-ttu-id="74532-128">Чтобы полностью отключить отказоустойчивую кучу в системе, установите \_ параметр reg DWORD **HKLM \\ Software \\ Microsoft \\ ФС \\ Enabled** в значение **0**.</span><span class="sxs-lookup"><span data-stu-id="74532-128">To disable Fault Tolerant Heap entirely on a system, set the REG\_DWORD value **HKLM\\Software\\Microsoft\\FTH\\Enabled** to **0**.</span></span>

<span data-ttu-id="74532-129">После изменения этого значения перезапустите систему.</span><span class="sxs-lookup"><span data-stu-id="74532-129">After changing this value, restart the system.</span></span> <span data-ttu-id="74532-130">ФС больше не будет активироваться для новых приложений.</span><span class="sxs-lookup"><span data-stu-id="74532-130">FTH will no longer activate for new applications.</span></span>

<span data-ttu-id="74532-131">**Сброс списка приложений, отслеживаний ФС**</span><span class="sxs-lookup"><span data-stu-id="74532-131">**Resetting the list of applications tracked by FTH**</span></span>

<span data-ttu-id="74532-132">Отказоустойчивая куча является самоуправляемой и будет автономно приостанавливаться в случае, если меры по предотвращению неэффективны для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="74532-132">Fault Tolerant heap is self-managing and will autonomously stop applying in the case that mitigations are not effective for a given application.</span></span> <span data-ttu-id="74532-133">Однако если необходимо сбросить список приложений, для которых ФС проблемы с устранением неполадок (например, при тестировании приложения и необходимости воспроизведения сбоя ФС), можно выполнить следующую команду из командной строки с повышенными привилегиями:  **Rundll32.exe fthsvc.dll, фссиспрепспеЦиализе**</span><span class="sxs-lookup"><span data-stu-id="74532-133">However, if you need to reset the list of applications for which FTH is mitigating problems (for example, if you are testing an application and need to reproduce a crash that FTH is mitigating), you can run the following command from an elevated command prompt:  **Rundll32.exe fthsvc.dll,FthSysprepSpecialize**</span></span>  
<span data-ttu-id="74532-134">**Внимание!** При выполнении этой команды будут удалены все ФС приложения, поэтому приложения, работающие в данный момент, могут снова завершить работу после выполнения этой команды.</span><span class="sxs-lookup"><span data-stu-id="74532-134">**Caution** Running this command will clear all FTH applications, so applications that are currently functioning properly may begin to crash again after running this command.</span></span>  

 

 



