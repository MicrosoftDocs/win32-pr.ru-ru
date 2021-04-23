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
ms.openlocfilehash: b01a83c3642f49a9fdbe7f8c51f157a154a9843b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068219"
---
# <a name="runtime-registry-entry"></a><span data-ttu-id="e8f71-111">Запись реестра времени выполнения</span><span class="sxs-lookup"><span data-stu-id="e8f71-111">Runtime Registry Entry</span></span>

<span data-ttu-id="e8f71-112">Когда проигрыватель Windows Media обнаруживает пользовательское расширение имени файла, он ищет подраздел реестра, соответствующий этому расширению.</span><span class="sxs-lookup"><span data-stu-id="e8f71-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="e8f71-113">Подраздел описывается в [разделе Параметры реестра расширения имени файла](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="e8f71-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="e8f71-114">Одна из записей реестра, которые могут отображаться в подразделе расширения, — это запись **времени выполнения** .</span><span class="sxs-lookup"><span data-stu-id="e8f71-114">One of the registry entries that can appear under the extension's subkey is the **Runtime** entry.</span></span>

<span data-ttu-id="e8f71-115">Запись **времени выполнения** определяет базовую технологию, которую проигрыватель Windows Media может использовать для воспроизведения или преобразования цифровых файлов мультимедиа с пользовательским расширением.</span><span class="sxs-lookup"><span data-stu-id="e8f71-115">The **Runtime** entry specifies the underlying technology that Windows Media Player can use to play or convert digital media files that have the custom extension.</span></span> <span data-ttu-id="e8f71-116">Запись **времени выполнения** имеет следующую форму.</span><span class="sxs-lookup"><span data-stu-id="e8f71-116">The **Runtime** entry has the following form.</span></span>



|          |                |                                                               |
|----------|----------------|---------------------------------------------------------------|
| <span data-ttu-id="e8f71-117">**имя**;</span><span class="sxs-lookup"><span data-stu-id="e8f71-117">**Name**</span></span> | <span data-ttu-id="e8f71-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e8f71-118">**Type**</span></span>       | <span data-ttu-id="e8f71-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e8f71-119">**Value**</span></span>                                                     |
| <span data-ttu-id="e8f71-120">Параметры выполнения</span><span class="sxs-lookup"><span data-stu-id="e8f71-120">Runtime</span></span>  | <span data-ttu-id="e8f71-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e8f71-121">**REG\_DWORD**</span></span> | <span data-ttu-id="e8f71-122">Положительное целое число, идентифицирующее базовую технологию.</span><span class="sxs-lookup"><span data-stu-id="e8f71-122">A positive integer that identifies the underlying technology.</span></span> |



 

<span data-ttu-id="e8f71-123">Значение записи **времени выполнения** должно быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="e8f71-123">The value of the **Runtime** entry must be one the following.</span></span>



| <span data-ttu-id="e8f71-124">**Значение (десятичное)**</span><span class="sxs-lookup"><span data-stu-id="e8f71-124">**Value (decimal)**</span></span> | <span data-ttu-id="e8f71-125">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e8f71-125">**Description**</span></span>                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8f71-126">6</span><span class="sxs-lookup"><span data-stu-id="e8f71-126">6</span></span>                   | <span data-ttu-id="e8f71-127">Подготовка к просмотру с помощью пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="e8f71-127">Render using the Windows Media Format SDK.</span></span>                                                 |
| <span data-ttu-id="e8f71-128">7</span><span class="sxs-lookup"><span data-stu-id="e8f71-128">7</span></span>                   | <span data-ttu-id="e8f71-129">Подготовка к просмотру с помощью Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e8f71-129">Render using Microsoft DirectShow.</span></span>                                                         |
| <span data-ttu-id="e8f71-130">13</span><span class="sxs-lookup"><span data-stu-id="e8f71-130">13</span></span>                  | <span data-ttu-id="e8f71-131">Преобразование файла с помощью указанного подключаемого модуля преобразования.</span><span class="sxs-lookup"><span data-stu-id="e8f71-131">Convert the file using the specified conversion plug-in.</span></span> <span data-ttu-id="e8f71-132">Требуется проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="e8f71-132">Requires Windows Media Player 11.</span></span> |



 

<span data-ttu-id="e8f71-133">Значения записей реестра **времени выполнения** 6 и 7 поддерживаются в Windows Media Player 9 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="e8f71-133">The **Runtime** registry entry values 6 and 7 are supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="e8f71-134">Значение 13 поддерживается проигрывателем Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="e8f71-134">The value 13 is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8f71-135">См. также</span><span class="sxs-lookup"><span data-stu-id="e8f71-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8f71-136">**Подраздел Конвертплугинклсид**</span><span class="sxs-lookup"><span data-stu-id="e8f71-136">**ConvertPluginCLSID Subkey**</span></span>](convertpluginclsid-subkey.md)
</dt> <dt>

[<span data-ttu-id="e8f71-137">**Параметры реестра для расширения имени файла**</span><span class="sxs-lookup"><span data-stu-id="e8f71-137">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




