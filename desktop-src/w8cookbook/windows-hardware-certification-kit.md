---
title: Комплект сертификации оборудования для Windows
description: Комплект сертификации оборудования для Windows
ms.assetid: 99BD2D7D-8F9D-445E-AE04-6A58FFF3DCE6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dba820d62d6766f74549ed23f7a5abdccbca258b
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "104070751"
---
# <a name="windows-hardware-certification-kit"></a><span data-ttu-id="54831-103">Комплект сертификации оборудования для Windows</span><span class="sxs-lookup"><span data-stu-id="54831-103">Windows Hardware Certification Kit</span></span>

## <a name="platforms"></a><span data-ttu-id="54831-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="54831-104">Platforms</span></span>

 <span data-ttu-id="54831-105">**Клиенты** — Windows 7 \| Windows 8</span><span class="sxs-lookup"><span data-stu-id="54831-105">**Clients** - Windows 7 \| Windows 8</span></span>  
<span data-ttu-id="54831-106">**Серверы** — windows Server 2008 R2 \| Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="54831-106">**Servers** - Windows Server 2008 R2 \| Windows Server 2012</span></span>  
<span data-ttu-id="54831-107">**Сервер и контроллер** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="54831-107">**Server/Controller** - Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="54831-108">Описание</span><span class="sxs-lookup"><span data-stu-id="54831-108">Description</span></span>

<span data-ttu-id="54831-109">Комплект сертификации оборудования для Windows позволяет разработчикам, поставщикам программных продуктов, независимым поставщикам оборудования и производителям вычислительных систем сертифицировать свои аппаратные устройства, системы и фильтровать драйверы для последних версий операционных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="54831-109">The Windows Hardware Certification Kit enables developers, ISVs, IHVs, and OEMs to certify their hardware devices, systems, and filter drivers for the latest Windows operating systems.</span></span> <span data-ttu-id="54831-110">Он содержит все средства и документацию, необходимые для сертификации оборудования и фильтрации драйверов для этих операционных систем:</span><span class="sxs-lookup"><span data-stu-id="54831-110">It contains all the tools and documentation that you need to certify your hardware and filter drivers for these operating systems:</span></span>

-   <span data-ttu-id="54831-111">Windows 8</span><span class="sxs-lookup"><span data-stu-id="54831-111">Windows 8</span></span>
-   <span data-ttu-id="54831-112">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="54831-112">Windows Server 2012</span></span>
-   <span data-ttu-id="54831-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="54831-113">Windows 7</span></span>
-   <span data-ttu-id="54831-114">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="54831-114">Windows Server 2008 R2</span></span>

<span data-ttu-id="54831-115">Комплект сертификации оборудования для Windows заменяет комплект Windows Logo и является частью программы сертификации Windows.</span><span class="sxs-lookup"><span data-stu-id="54831-115">The Windows Hardware Certification Kit replaces the Windows Logo Kit and is a part of the Windows Certification Program.</span></span>

## <a name="usage-or-best-practices"></a><span data-ttu-id="54831-116">Использование или рекомендации</span><span class="sxs-lookup"><span data-stu-id="54831-116">Usage or best practices</span></span>

<span data-ttu-id="54831-117">Перед тестированием любого оборудования или драйвера фильтра необходимо настроить правильную тестовую среду на основе оборудования или драйвера фильтра, который вы подтверждаете.</span><span class="sxs-lookup"><span data-stu-id="54831-117">Before you can test any hardware or filter driver, you must set up the proper test environment based on the hardware or filter driver you are certifying.</span></span> <span data-ttu-id="54831-118">Сюда входят контроллер, клиент и потенциально дополнительное оборудование (например, Многофункциональные устройства) или программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="54831-118">This includes the controller, client, and potentially additional hardware (for example, multi-function devices) or software.</span></span> <span data-ttu-id="54831-119">После настройки среды можно протестировать оборудование с помощью средства Studio New ХКК.</span><span class="sxs-lookup"><span data-stu-id="54831-119">After your environment is set up, you can test your hardware using the new HCK’s Studio tool.</span></span> <span data-ttu-id="54831-120">Эти шаги описывают процесс проверки сертификации.</span><span class="sxs-lookup"><span data-stu-id="54831-120">These steps outline the certification test process.</span></span>

1.  <span data-ttu-id="54831-121">Настройка тестовой среды.</span><span class="sxs-lookup"><span data-stu-id="54831-121">Set up test environment.</span></span>
2.  <span data-ttu-id="54831-122">Создайте проект.</span><span class="sxs-lookup"><span data-stu-id="54831-122">Create a project.</span></span>
3.  <span data-ttu-id="54831-123">Создайте один или несколько пулов машин.</span><span class="sxs-lookup"><span data-stu-id="54831-123">Create one or more machine pools.</span></span>
4.  <span data-ttu-id="54831-124">Выберите компоненты для проверки.</span><span class="sxs-lookup"><span data-stu-id="54831-124">Select features to validate.</span></span>
5.  <span data-ttu-id="54831-125">Выберите и запустите тесты для этих функций.</span><span class="sxs-lookup"><span data-stu-id="54831-125">Select and run tests against those features.</span></span>
6.  <span data-ttu-id="54831-126">Просмотр результатов теста.</span><span class="sxs-lookup"><span data-stu-id="54831-126">View test results.</span></span>
7.  <span data-ttu-id="54831-127">Отправьте пакет.</span><span class="sxs-lookup"><span data-stu-id="54831-127">Submit your package.</span></span>

## <a name="resources"></a><span data-ttu-id="54831-128">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="54831-128">Resources</span></span>

-   [<span data-ttu-id="54831-129">Разработка оборудования Windows</span><span class="sxs-lookup"><span data-stu-id="54831-129">Windows Hardware Development</span></span>](https://msdn.microsoft.com/windows/hardware/)
-   <span data-ttu-id="54831-130">[Программа сертификации оборудования для Windows](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="54831-130">[Windows Hardware Certification Program](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))</span></span>
-   <span data-ttu-id="54831-131">[Начало разработки оборудования для Windows](/previous-versions/gg507680(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="54831-131">[Start Developing Hardware for Windows](/previous-versions/gg507680(v=msdn.10))</span></span>

 

 