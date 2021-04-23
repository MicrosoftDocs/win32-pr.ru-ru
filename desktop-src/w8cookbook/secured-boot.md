---
title: Ранний запуск антивредоносного ПО
description: Ранний запуск антивредоносного ПО
ms.assetid: 4064CD44-FC50-48DE-8490-F592ED21CB7E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c3e51d7fb009ffa0e85a59990b321fb38ad196
ms.sourcegitcommit: a93d3abaf4d6d45a6f0b87faed3f576b222b1745
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "104081658"
---
# <a name="early-launch-antimalware"></a><span data-ttu-id="7598f-103">Ранний запуск антивредоносного ПО</span><span class="sxs-lookup"><span data-stu-id="7598f-103">Early launch antimalware</span></span>

## <a name="platforms"></a><span data-ttu-id="7598f-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="7598f-104">Platforms</span></span>

 <span data-ttu-id="7598f-105">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="7598f-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="7598f-106">**Серверы** — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7598f-106">**Servers** - Windows Server 2012</span></span>  

## <a name="description"></a><span data-ttu-id="7598f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7598f-107">Description</span></span>

<span data-ttu-id="7598f-108">По мере того, как антивредоносное по стало более эффективным при обнаружении вредоносных программ во время выполнения, злоумышленники также становятся более эффективными при создании rootkit-программ, которые могут скрываться от обнаружения.</span><span class="sxs-lookup"><span data-stu-id="7598f-108">As antimalware (AM) software has become better and better at detecting runtime malware, attackers are also becoming better at creating rootkits that can hide from detection.</span></span> <span data-ttu-id="7598f-109">Обнаружение вредоносных программ, запускаемых на ранних этапах цикла загрузки, является сложной задачей, которая в большинстве случаев имеет более тщательного решения.</span><span class="sxs-lookup"><span data-stu-id="7598f-109">Detecting malware that starts early in the boot cycle is a challenge that most AM vendors address diligently.</span></span> <span data-ttu-id="7598f-110">Как правило, они создают системные атаки, которые не поддерживаются операционной системой узла, и фактически могут привести к нестабильной работе компьютера.</span><span class="sxs-lookup"><span data-stu-id="7598f-110">Typically, they create system hacks that are not supported by the host operating system and can actually result in placing the computer in an unstable state.</span></span> <span data-ttu-id="7598f-111">До этого момента Windows не предоставила хороший способ обнаружения и устранения угроз с ранним загрузкой.</span><span class="sxs-lookup"><span data-stu-id="7598f-111">Up to this point, Windows has not provided a good way for AM to detect and resolve these early boot threats.</span></span>

<span data-ttu-id="7598f-112">В Windows 8 появилась новая функция, называемая безопасной загрузкой, которая защищает конфигурацию загрузки Windows и компоненты, а также загружает драйвер раннего запуска антивредоносной программы (ELAM).</span><span class="sxs-lookup"><span data-stu-id="7598f-112">Windows 8 introduces a new feature called Secure Boot, which protects the Windows boot configuration and components, and loads an Early Launch Anti-malware (ELAM) driver.</span></span> <span data-ttu-id="7598f-113">Этот драйвер запускается перед другими драйверами загрузки и позволяет оценить эти драйверы и помогает ядру Windows решить, следует ли их инициализировать.</span><span class="sxs-lookup"><span data-stu-id="7598f-113">This driver starts before other boot-start drivers and enables the evaluation of those drivers and helps the Windows kernel decide whether they should be initialized.</span></span>

## <a name="manifestation"></a><span data-ttu-id="7598f-114">Проявление</span><span class="sxs-lookup"><span data-stu-id="7598f-114">Manifestation</span></span>

<span data-ttu-id="7598f-115">При первом запуске ядра ELAM гарантирует запуск до любого стороннего программного обеспечения и, следовательно, сможет обнаружить вредоносные программы в процессе загрузки и предотвратить его инициализацию.</span><span class="sxs-lookup"><span data-stu-id="7598f-115">By being launched first by the kernel, ELAM is ensured to be launched before any third-party software, and is therefore able to detect malware in the boot process and prevent it from initializing.</span></span>

## <a name="mitigation"></a><span data-ttu-id="7598f-116">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="7598f-116">Mitigation</span></span>

<span data-ttu-id="7598f-117">Драйверы загрузки инициализируются на основе классификации, возвращаемой драйвером ELAM в соответствии с политикой инициализации.</span><span class="sxs-lookup"><span data-stu-id="7598f-117">Boot drivers are initialized based on the classification that is returned from the ELAM driver according to an initialization policy.</span></span> <span data-ttu-id="7598f-118">По умолчанию политика инициализирует известные хорошие и неизвестные драйверы, но не инициализирует известные неправильные драйверы.</span><span class="sxs-lookup"><span data-stu-id="7598f-118">By default, the policy initializes known good and unknown drivers, but will not initialize known bad drivers.</span></span> <span data-ttu-id="7598f-119">Системный администратор может указать настраиваемую политику с помощью групповая политика, которая может препятствовать инициализации неизвестных драйверов, или включить драйверы, которые являются критически важными для процесса загрузки, но были незаконно изменены с помощью начальной загрузки.</span><span class="sxs-lookup"><span data-stu-id="7598f-119">A system administrator can specify a custom policy through Group Policy that can prevent unknown drivers from initializing or can enable drivers that are critical to the boot process, but have been tampered with, boot to be initialized.</span></span>

## <a name="solution"></a><span data-ttu-id="7598f-120">Решение</span><span class="sxs-lookup"><span data-stu-id="7598f-120">Solution</span></span>

<span data-ttu-id="7598f-121">Драйвер ELAM должен зарегистрироваться для обратных вызовов ядра, чтобы получить сведения о каждом драйвере загрузки при инициализации.</span><span class="sxs-lookup"><span data-stu-id="7598f-121">An ELAM driver must register for kernel callbacks to get info about each boot-start driver as it is initializing.</span></span> <span data-ttu-id="7598f-122">После этого драйвер ELAM может возвращать классификацию для каждого драйвера.</span><span class="sxs-lookup"><span data-stu-id="7598f-122">The ELAM driver can then return a classification for each driver.</span></span> <span data-ttu-id="7598f-123">Эти функции являются обязательными:</span><span class="sxs-lookup"><span data-stu-id="7598f-123">These functions are required:</span></span>

-   [<span data-ttu-id="7598f-124">иорегистербутдриверкаллбакк</span><span class="sxs-lookup"><span data-stu-id="7598f-124">IoRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [<span data-ttu-id="7598f-125">иаунрегистербутдриверкаллбакк</span><span class="sxs-lookup"><span data-stu-id="7598f-125">IoUnRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)

<span data-ttu-id="7598f-126">Драйвер ELAM также может зарегистрироваться для обратных вызовов реестра.</span><span class="sxs-lookup"><span data-stu-id="7598f-126">An ELAM driver can also register for registry callbacks.</span></span> <span data-ttu-id="7598f-127">Это позволит драйверу ELAM проверить данные конфигурации, используемые каждым драйвером загрузки.</span><span class="sxs-lookup"><span data-stu-id="7598f-127">Doing so enables the ELAM driver to inspect the configuration data that is used by each boot-start driver.</span></span> <span data-ttu-id="7598f-128">После этого драйвер ELAM может блокировать или изменять данные перед использованием драйверов, запускаемых при загрузке, при необходимости.</span><span class="sxs-lookup"><span data-stu-id="7598f-128">The ELAM driver can then block or modify the data before it is used by the boot-start drivers, if necessary.</span></span> <span data-ttu-id="7598f-129">Эти функции являются обязательными:</span><span class="sxs-lookup"><span data-stu-id="7598f-129">These functions are required:</span></span>

-   [<span data-ttu-id="7598f-130">кмрегистеркаллбаккекс</span><span class="sxs-lookup"><span data-stu-id="7598f-130">CmRegisterCallbackEx</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [<span data-ttu-id="7598f-131">кмунрегистеркаллбакк</span><span class="sxs-lookup"><span data-stu-id="7598f-131">CmUnRegisterCallback</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)

<span data-ttu-id="7598f-132">Дополнительные сведения о требованиях к драйверу ELAM и использовании API см. в статье [ранний запуск антивредоносной программы](/windows-hardware/drivers/install/early-launch-antimalware).</span><span class="sxs-lookup"><span data-stu-id="7598f-132">For more details about ELAM driver requirements and API usage, see [Early Launch Antimalware](/windows-hardware/drivers/install/early-launch-antimalware).</span></span>

## <a name="tests"></a><span data-ttu-id="7598f-133">Тесты</span><span class="sxs-lookup"><span data-stu-id="7598f-133">Tests</span></span>

<span data-ttu-id="7598f-134">Драйверы ELAM должны быть специально подписаны корпорацией Майкрософт, чтобы гарантировать их запуск ядром Windows на ранних этапах процесса загрузки.</span><span class="sxs-lookup"><span data-stu-id="7598f-134">ELAM drivers must be specially signed by Microsoft to ensure they are started by the Windows kernel early in the boot process.</span></span> <span data-ttu-id="7598f-135">Чтобы получить подпись, драйверы ELAM должны пройти набор тестов сертификации для проверки производительности и другого поведения.</span><span class="sxs-lookup"><span data-stu-id="7598f-135">To get the signature, ELAM drivers must pass a set of certification tests to verify performance and other behavior.</span></span> <span data-ttu-id="7598f-136">Эти тесты включены в комплект сертификации оборудования для Windows.</span><span class="sxs-lookup"><span data-stu-id="7598f-136">These tests are included in the Windows Hardware Certification Kit.</span></span>

## <a name="resources"></a><span data-ttu-id="7598f-137">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="7598f-137">Resources</span></span>

-   [<span data-ttu-id="7598f-138">Ранний запуск антивредоносной программы</span><span class="sxs-lookup"><span data-stu-id="7598f-138">Early Launch Antimalware</span></span>](/windows-hardware/drivers/install/early-launch-antimalware)
-   [<span data-ttu-id="7598f-139">кмрегистеркаллбаккекс</span><span class="sxs-lookup"><span data-stu-id="7598f-139">CmRegisterCallbackEx</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [<span data-ttu-id="7598f-140">кмунрегистеркаллбакк</span><span class="sxs-lookup"><span data-stu-id="7598f-140">CmUnRegisterCallback</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)
-   [<span data-ttu-id="7598f-141">иорегистербутдриверкаллбакк</span><span class="sxs-lookup"><span data-stu-id="7598f-141">IoRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [<span data-ttu-id="7598f-142">иаунрегистербутдриверкаллбакк</span><span class="sxs-lookup"><span data-stu-id="7598f-142">IoUnRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)
-   [<span data-ttu-id="7598f-143">Сертификация оборудования с помощью Конференции сборки комплекта сертификации оборудования для Windows</span><span class="sxs-lookup"><span data-stu-id="7598f-143">Certifying hardware with the Windows Hardware Certification Kit Build Conference presentation</span></span>](https://channel9.msdn.com/events/BUILD/BUILD2011/HW-659T)
-   [<span data-ttu-id="7598f-144">Загрузка комплектов и средств</span><span class="sxs-lookup"><span data-stu-id="7598f-144">Download Kits and Tools</span></span>](https://msdn.microsoft.com/windows/hardware/br259105)

 

 
