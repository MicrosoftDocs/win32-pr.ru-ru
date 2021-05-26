---
title: Запись реестра времени выполнения
description: Запись реестра времени выполнения
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Проигрыватель Windows Media, записи реестра времени выполнения
- Проигрыватель Windows Media, расширения имен файлов
- Проигрыватель Windows Media, реестр
- реестр, расширения имен файлов
- реестр, записи времени выполнения
- реестр, параметры для проигрывателя Windows Media
- параметры реестра для расширения имени файла
- записи реестра среды выполнения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf485038965184add320e49c29482672c770f48
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424113"
---
# <a name="runtime-registry-entry"></a><span data-ttu-id="50b92-111">Запись реестра времени выполнения</span><span class="sxs-lookup"><span data-stu-id="50b92-111">Runtime Registry Entry</span></span>

<span data-ttu-id="50b92-112">Когда проигрыватель Windows Media обнаруживает пользовательское расширение имени файла, он ищет подраздел реестра, соответствующий этому расширению.</span><span class="sxs-lookup"><span data-stu-id="50b92-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="50b92-113">Подраздел описывается в [разделе Параметры реестра расширения имени файла](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="50b92-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="50b92-114">Одна из записей реестра, которые могут отображаться в подразделе расширения, — это запись **времени выполнения** .</span><span class="sxs-lookup"><span data-stu-id="50b92-114">One of the registry entries that can appear under the extension's subkey is the **Runtime** entry.</span></span>

<span data-ttu-id="50b92-115">Запись **времени выполнения** определяет базовую технологию, которую проигрыватель Windows Media может использовать для воспроизведения или преобразования цифровых файлов мультимедиа с пользовательским расширением.</span><span class="sxs-lookup"><span data-stu-id="50b92-115">The **Runtime** entry specifies the underlying technology that Windows Media Player can use to play or convert digital media files that have the custom extension.</span></span> <span data-ttu-id="50b92-116">Запись **времени выполнения** имеет следующую форму.</span><span class="sxs-lookup"><span data-stu-id="50b92-116">The **Runtime** entry has the following form.</span></span>



|   <span data-ttu-id="50b92-117">Имя</span><span class="sxs-lookup"><span data-stu-id="50b92-117">Name</span></span>   |   <span data-ttu-id="50b92-118">Тип</span><span class="sxs-lookup"><span data-stu-id="50b92-118">Type</span></span>         |   <span data-ttu-id="50b92-119">Значение</span><span class="sxs-lookup"><span data-stu-id="50b92-119">Value</span></span>                                                       |
|----------|----------------|---------------------------------------------------------------|
| <span data-ttu-id="50b92-120">Параметры выполнения</span><span class="sxs-lookup"><span data-stu-id="50b92-120">Runtime</span></span>  | <span data-ttu-id="50b92-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="50b92-121">**REG\_DWORD**</span></span> | <span data-ttu-id="50b92-122">Положительное целое число, идентифицирующее базовую технологию.</span><span class="sxs-lookup"><span data-stu-id="50b92-122">A positive integer that identifies the underlying technology.</span></span> |



 

<span data-ttu-id="50b92-123">Значение записи **времени выполнения** должно быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="50b92-123">The value of the **Runtime** entry must be one the following.</span></span>



| <span data-ttu-id="50b92-124">**Значение (десятичное)**</span><span class="sxs-lookup"><span data-stu-id="50b92-124">**Value (decimal)**</span></span> | <span data-ttu-id="50b92-125">**Описание**</span><span class="sxs-lookup"><span data-stu-id="50b92-125">**Description**</span></span>                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="50b92-126">6</span><span class="sxs-lookup"><span data-stu-id="50b92-126">6</span></span>                   | <span data-ttu-id="50b92-127">Подготовка к просмотру с помощью пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="50b92-127">Render using the Windows Media Format SDK.</span></span>                                                 |
| <span data-ttu-id="50b92-128">7</span><span class="sxs-lookup"><span data-stu-id="50b92-128">7</span></span>                   | <span data-ttu-id="50b92-129">Подготовка к просмотру с помощью Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="50b92-129">Render using Microsoft DirectShow.</span></span>                                                         |
| <span data-ttu-id="50b92-130">13</span><span class="sxs-lookup"><span data-stu-id="50b92-130">13</span></span>                  | <span data-ttu-id="50b92-131">Преобразование файла с помощью указанного подключаемого модуля преобразования.</span><span class="sxs-lookup"><span data-stu-id="50b92-131">Convert the file using the specified conversion plug-in.</span></span> <span data-ttu-id="50b92-132">Требуется проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="50b92-132">Requires Windows Media Player 11.</span></span> |



 

<span data-ttu-id="50b92-133">Значения записей реестра **времени выполнения** 6 и 7 поддерживаются в Windows Media Player 9 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="50b92-133">The **Runtime** registry entry values 6 and 7 are supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="50b92-134">Значение 13 поддерживается проигрывателем Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="50b92-134">The value 13 is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50b92-135">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="50b92-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50b92-136">**Подраздел Конвертплугинклсид**</span><span class="sxs-lookup"><span data-stu-id="50b92-136">**ConvertPluginCLSID Subkey**</span></span>](convertpluginclsid-subkey.md)
</dt> <dt>

[<span data-ttu-id="50b92-137">**Параметры реестра для расширения имени файла**</span><span class="sxs-lookup"><span data-stu-id="50b92-137">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




