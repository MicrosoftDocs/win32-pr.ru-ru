---
description: Технология энергозависимой памяти (PM Memory) обеспечивает доступ на уровне байт к энергонезависимым носителям, одновременно уменьшая задержку в хранении или получении данных.
ms.assetid: 68BF6074-09CB-4D6E-8BFD-FBA297391286
title: Программирование энергонезависимой памяти в Windows — интеграция НВМЛ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9f033963a8fecded8943eb053781d05a78d568
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272375"
---
# <a name="persistent-memory-programming-in-windows---nvml-integration"></a><span data-ttu-id="54c5b-103">Программирование энергонезависимой памяти в Windows — интеграция НВМЛ</span><span class="sxs-lookup"><span data-stu-id="54c5b-103">Persistent Memory Programming in Windows - NVML Integration</span></span>

<span data-ttu-id="54c5b-104">Технология энергозависимой памяти (PM Memory) обеспечивает доступ на уровне байт к энергонезависимым носителям, одновременно уменьшая задержку в хранении или получении данных.</span><span class="sxs-lookup"><span data-stu-id="54c5b-104">Persistent memory (PM) technology provides byte-level access to non-volatile media while also reducing the latency of storing or retrieving data significantly.</span></span> <span data-ttu-id="54c5b-105">Он создает новый уровень между системной памятью и традиционным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="54c5b-105">It creates a new tier between a system’s memory and traditional storage.</span></span> <span data-ttu-id="54c5b-106">Любая программа, зависящая от или масштабируется с помощью быстрой записи на постоянный носитель, может выиграть от PM.</span><span class="sxs-lookup"><span data-stu-id="54c5b-106">Any program that is dependent on or scales with quick writes to a persistent medium can benefit from PM.</span></span>

<span data-ttu-id="54c5b-107">В этой статье показано, как можно легко интегрировать невременную библиотеку памяти (НВМЛ) в проект Visual Studio для простоты использования.</span><span class="sxs-lookup"><span data-stu-id="54c5b-107">The purpose of this article is to outline how the non-volatile memory library (NVML) can be integrated into a Visual Studio project for easy use.</span></span>

> [!Note]  
> <span data-ttu-id="54c5b-108">Постоянная память иногда также называется памятью класса хранилища (SCM).</span><span class="sxs-lookup"><span data-stu-id="54c5b-108">Persistent Memory is sometimes also referred to as Storage Class Memory (SCM).</span></span>

 

## <a name="pm-and-nvml"></a><span data-ttu-id="54c5b-109">PM и НВМЛ</span><span class="sxs-lookup"><span data-stu-id="54c5b-109">PM and NVML</span></span>

<span data-ttu-id="54c5b-110">Первая поддержка постоянной памяти появилась в Windows Server 2016 и юбилейном обновлении Windows 10 (1607).</span><span class="sxs-lookup"><span data-stu-id="54c5b-110">First support for persistent memory was introduced in Windows Server 2016 and the Windows 10 Anniversary Update (1607).</span></span> <span data-ttu-id="54c5b-111">Чтобы получить краткий обзор, ознакомьтесь с этими двумя видео Channel9:</span><span class="sxs-lookup"><span data-stu-id="54c5b-111">For a quick overview, check out these two Channel9 videos:</span></span>

-   [<span data-ttu-id="54c5b-112">Использование энергонезависимой памяти (NVDIMM-N) в качестве блочного хранилища в Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="54c5b-112">Using Non-volatile Memory (NVDIMM-N) as Block Storage in Windows Server 2016</span></span>](https://channel9.msdn.com/Events/Build/2016/P466)
-   [<span data-ttu-id="54c5b-113">Использование энергонезависимой памяти (NVDIMM-N) в качестве хранилища Byte-Addressable в Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="54c5b-113">Using Non-volatile Memory (NVDIMM-N) as Byte-Addressable Storage in Windows Server 2016</span></span>](https://channel9.msdn.com/Events/Build/2016/P470)

<span data-ttu-id="54c5b-114">Чтобы помочь разработчикам воспользоваться преимуществами постоянных объемов памяти, корпорация Майкрософт также предоставила усилия по переносу библиотеки памяти (нвмл) в Windows.</span><span class="sxs-lookup"><span data-stu-id="54c5b-114">To help developers take advantage of the benefits persistent memory offers, Microsoft has also contributed to the efforts of bringing the non-volatile memory library (NVML) to Windows.</span></span> <span data-ttu-id="54c5b-115">Эта библиотека предоставляет различные средства для создания постоянных приложений с учетом памяти.</span><span class="sxs-lookup"><span data-stu-id="54c5b-115">This library provides various tools to make applications persistent-memory aware.</span></span> <span data-ttu-id="54c5b-116">Например, он содержит код, позволяющий легко создавать хранилище ключей с поддержкой PM для очень быстрого поиска и хранения.</span><span class="sxs-lookup"><span data-stu-id="54c5b-116">For example, it contains code that lets you easily create a PM-aware key-value store for extremely fast look-ups and stores.</span></span> <span data-ttu-id="54c5b-117">Дополнительные сведения о НВМЛ, включая примеры, можно найти в [библиотеке НВМ](https://pmem.io/nvml/).</span><span class="sxs-lookup"><span data-stu-id="54c5b-117">You can find more information on NVML, including samples, at [NVM Library](https://pmem.io/nvml/).</span></span>

## <a name="integrating-nvml-into-a-visual-studio-project"></a><span data-ttu-id="54c5b-118">Интеграция НВМЛ в проект Visual Studio</span><span class="sxs-lookup"><span data-stu-id="54c5b-118">Integrating NVML into a Visual Studio Project</span></span>

1. <span data-ttu-id="54c5b-119">Скачивание файлов и заголовков библиотеки НВМЛ</span><span class="sxs-lookup"><span data-stu-id="54c5b-119">Download NVML library files and headers</span></span>

-   <span data-ttu-id="54c5b-120">НВМЛ сохраняется на GitHub.</span><span class="sxs-lookup"><span data-stu-id="54c5b-120">NVML is maintained on GitHub.</span></span> <span data-ttu-id="54c5b-121">Вы можете либо скомпилировать источник самостоятельно, либо просто загрузить скомпилированные двоичные файлы непосредственно отсюда: [Нвмл версии 1,2 —](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1)Предварительная техническая версия Windows.</span><span class="sxs-lookup"><span data-stu-id="54c5b-121">You can either compile the source yourself, or just download compiled binaries directly from here: [NVML Version 1.2 - Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).</span></span>

2. <span data-ttu-id="54c5b-122">Поместите файлы библиотеки и заголовки в каталог по своему выбору, например "C: \\ нвмл \\ lib" и "c: \\ нвмл \\ Inc" соответственно.</span><span class="sxs-lookup"><span data-stu-id="54c5b-122">Place the library files and headers in a directory of your choosing, for example: “C:\\NVML\\lib” and “C:\\NVML\\inc” respectively.</span></span>

3. <span data-ttu-id="54c5b-123">Настройте проект следующим образом.</span><span class="sxs-lookup"><span data-stu-id="54c5b-123">Configure your project as follows:</span></span>

-   <span data-ttu-id="54c5b-124">Откройте проект Visual Studio и в окне "обозреватель решений" щелкните правой кнопкой мыши имя проекта.</span><span class="sxs-lookup"><span data-stu-id="54c5b-124">Open your visual studio project and in the “Solution Explorer” right-click on your project’s name.</span></span>
-   <span data-ttu-id="54c5b-125">Откройте область параметров проекта в нижней части результирующего всплывающего окна.</span><span class="sxs-lookup"><span data-stu-id="54c5b-125">Open the project’s setting pane at the bottom of the resulting pop-up.</span></span>
-   <span data-ttu-id="54c5b-126">Перейдите к разделу "Свойства конфигурации-> C/C++" и добавьте папку, в которую был сохранен заголовок (C: \\ нвмл \\ Inc), в поле "Дополнительные каталоги включаемых папок".</span><span class="sxs-lookup"><span data-stu-id="54c5b-126">Navigate to “Configuration Properties -> C/C++” and add the folder in which you stored the header (C:\\NVML\\inc) to the “Additional Include Directories” field.</span></span>
-   <span data-ttu-id="54c5b-127">Затем перейдите к разделу "Свойства конфигурации-> компоновщик" и добавьте папку, в которой была сохранена библиотека (C: \\ нвмл \\ lib), в поле "Дополнительные каталоги библиотеки".</span><span class="sxs-lookup"><span data-stu-id="54c5b-127">Next, navigate to “Configuration Properties -> Linker” and add the folder in which you stored the library (C:\\NVML\\lib) to the “Additional Library Directories” field</span></span>

4. <span data-ttu-id="54c5b-128">Затем убедитесь, что вы нацелены на проект для Windows Server 2016 или годовщины обновления Windows 10:</span><span class="sxs-lookup"><span data-stu-id="54c5b-128">Next, make sure you target the project for Windows Server 2016 or Windows 10 Anniversary Update:</span></span>

-   <span data-ttu-id="54c5b-129">Перейдите в раздел "Свойства конфигурации-> Общие" и задайте в поле "версия целевой платформы" значение "10.0.14393.0" и</span><span class="sxs-lookup"><span data-stu-id="54c5b-129">Navigate to “Configuration Properties -> General” and set the “Target Platform Version” field to “10.0.14393.0” and</span></span>
-   <span data-ttu-id="54c5b-130">Перейдите к разделу "Свойства конфигурации-> C/C++" и добавьте "НТДДИ \_ Version = нтдди \_ WIN10 \_ RS1;" в поле "препроцессор".</span><span class="sxs-lookup"><span data-stu-id="54c5b-130">Navigate to “Configuration Properties -> C/C++” and add “NTDDI\_VERSION=NTDDI\_WIN10\_RS1;” to the “Preprocessor” field.</span></span>

5. <span data-ttu-id="54c5b-131">Включение заголовков в код и ссылки на необходимые библиотеки</span><span class="sxs-lookup"><span data-stu-id="54c5b-131">Include the headers in your code and link to the required libraries</span></span>

-   <span data-ttu-id="54c5b-132">На этом этапе можно просто включить файлы заголовков, которые вы хотите использовать в коде, как и любые другие файлы заголовков.</span><span class="sxs-lookup"><span data-stu-id="54c5b-132">At this point, you can simply include the header files you are looking to use in your code like any other header files.</span></span> <span data-ttu-id="54c5b-133">Например, для использования либпмем:</span><span class="sxs-lookup"><span data-stu-id="54c5b-133">For example, to use libpmem:</span></span>
    -   <span data-ttu-id="54c5b-134">Добавьте " \# include <либпмем. h>" и</span><span class="sxs-lookup"><span data-stu-id="54c5b-134">add "\#include <libpmem.h>" and</span></span>
    -   <span data-ttu-id="54c5b-135">Добавьте "либпмем. lib" в "Свойства конфигурации-> компоновщик — > ввод-> дополнительные зависимости"</span><span class="sxs-lookup"><span data-stu-id="54c5b-135">add "libpmem.lib" to "Configuration Properties -> Linker -> Input -> Additional Dependencies"</span></span>

<span data-ttu-id="54c5b-136">На этом этапе вы готовы вызывать функции библиотеки непосредственно в коде и использовать их преимущества.</span><span class="sxs-lookup"><span data-stu-id="54c5b-136">At this point you are ready to call the library’s functions directly in your code and take advantage of them.</span></span>

 

 



