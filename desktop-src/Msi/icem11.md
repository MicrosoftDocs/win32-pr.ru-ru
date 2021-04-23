---
description: ICEM11 проверяет, что настраиваемый модуль слияния содержит таблицу Модулеконфигуратион и таблицу Модулесубститутион в таблице Модулеигноретабле модуля.
ms.assetid: f0199137-0a40-40ca-b3cf-ff8eef4309cc
title: ICEM11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403a36435ce2367fc356934740e6d022f5457698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265419"
---
# <a name="icem11"></a><span data-ttu-id="59221-103">ICEM11</span><span class="sxs-lookup"><span data-stu-id="59221-103">ICEM11</span></span>

<span data-ttu-id="59221-104">ICEM11 проверяет, что настраиваемый модуль слияния содержит [таблицу модулеконфигуратион](moduleconfiguration-table.md) и [таблицу Модулесубститутион](modulesubstitution-table.md) в [таблице модулеигноретабле](moduleignoretable-table.md) модуля.</span><span class="sxs-lookup"><span data-stu-id="59221-104">ICEM11 verifies that a Configurable Merge Module lists the [ModuleConfiguration table](moduleconfiguration-table.md) and [ModuleSubstitution table](modulesubstitution-table.md) in the [ModuleIgnoreTable table](moduleignoretable-table.md) of the module.</span></span> <span data-ttu-id="59221-105">Это гарантирует, что средства слияния, которые не распознают настраиваемые модули слияния (меньше версии 2,0), не копируют эти таблицы в целевую базу данных.</span><span class="sxs-lookup"><span data-stu-id="59221-105">This ensures that merge tools that do not recognize configurable merge modules(less than version 2.0) do not copy these tables into the target database.</span></span>

<span data-ttu-id="59221-106">Этот ИЦЕМ доступен в файле Мержемод. CUB, который входит в состав пакета SDK для установщик Windows 2,0 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="59221-106">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="59221-107">Дополнительные сведения см. в разделе [Windows SDK компонентов для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="59221-107">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="59221-108">Результат</span><span class="sxs-lookup"><span data-stu-id="59221-108">Result</span></span>

<span data-ttu-id="59221-109">ICEM11 отправляет ошибку, если модуль содержит таблицу Модулеконфигуратион или Модулесубститутион, не указанную в таблице Модулеигноретабле.</span><span class="sxs-lookup"><span data-stu-id="59221-109">ICEM11 posts an error if the module contains a ModuleConfiguration or ModuleSubstitution table not listed in the ModuleIgnoreTable table.</span></span>

## <a name="example"></a><span data-ttu-id="59221-110">Пример</span><span class="sxs-lookup"><span data-stu-id="59221-110">Example</span></span>

<span data-ttu-id="59221-111">ICEM11 отправляет следующие сообщения об ошибках для модуля, содержащего записи базы данных, показанные ниже.</span><span class="sxs-lookup"><span data-stu-id="59221-111">ICEM11 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
Error The module contains a ModuleConfiguration or ModuleSubstitution 
table. These tables must be listed in the ModuleIgnoreTable table.
```

<span data-ttu-id="59221-112">[Модулеконфигуратион](moduleconfiguration-table.md) (частичный)</span><span class="sxs-lookup"><span data-stu-id="59221-112">[ModuleConfiguration](moduleconfiguration-table.md) (partial)</span></span>



| <span data-ttu-id="59221-113">Имя</span><span class="sxs-lookup"><span data-stu-id="59221-113">Name</span></span>     | <span data-ttu-id="59221-114">Формат</span><span class="sxs-lookup"><span data-stu-id="59221-114">Format</span></span> | <span data-ttu-id="59221-115">Тип</span><span class="sxs-lookup"><span data-stu-id="59221-115">Type</span></span>   | <span data-ttu-id="59221-116">контекстдата</span><span class="sxs-lookup"><span data-stu-id="59221-116">ContextData</span></span> | <span data-ttu-id="59221-117">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="59221-117">DefaultValue</span></span> |
|----------|--------|--------|-------------|--------------|
| <span data-ttu-id="59221-118">IconKey1</span><span class="sxs-lookup"><span data-stu-id="59221-118">IconKey1</span></span> | <span data-ttu-id="59221-119">1</span><span class="sxs-lookup"><span data-stu-id="59221-119">1</span></span>      | <span data-ttu-id="59221-120">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="59221-120">Binary</span></span> | <span data-ttu-id="59221-121">Значок</span><span class="sxs-lookup"><span data-stu-id="59221-121">Icon</span></span>        | <span data-ttu-id="59221-122">дефаултикон</span><span class="sxs-lookup"><span data-stu-id="59221-122">DefaultIcon</span></span>  |



 

[<span data-ttu-id="59221-123">модулесубститутион</span><span class="sxs-lookup"><span data-stu-id="59221-123">ModuleSubstitution</span></span>](modulesubstitution-table.md)



| <span data-ttu-id="59221-124">Таблица</span><span class="sxs-lookup"><span data-stu-id="59221-124">Table</span></span>   | <span data-ttu-id="59221-125">Строка</span><span class="sxs-lookup"><span data-stu-id="59221-125">Row</span></span>              | <span data-ttu-id="59221-126">Столбец</span><span class="sxs-lookup"><span data-stu-id="59221-126">Column</span></span> | <span data-ttu-id="59221-127">Значение</span><span class="sxs-lookup"><span data-stu-id="59221-127">Value</span></span>        |
|---------|------------------|--------|--------------|
| <span data-ttu-id="59221-128">Control</span><span class="sxs-lookup"><span data-stu-id="59221-128">Control</span></span> | <span data-ttu-id="59221-129">Dialog1; Control1</span><span class="sxs-lookup"><span data-stu-id="59221-129">Dialog1;Control1</span></span> | <span data-ttu-id="59221-130">Текст</span><span class="sxs-lookup"><span data-stu-id="59221-130">Text</span></span>   | <span data-ttu-id="59221-131">\[IconKey1\]</span><span class="sxs-lookup"><span data-stu-id="59221-131">\[IconKey1\]</span></span> |



 

[<span data-ttu-id="59221-132">модулеигноретабле</span><span class="sxs-lookup"><span data-stu-id="59221-132">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)



| <span data-ttu-id="59221-133">Таблица</span><span class="sxs-lookup"><span data-stu-id="59221-133">Table</span></span>               |
|---------------------|
| <span data-ttu-id="59221-134">модулеконфигуратион</span><span class="sxs-lookup"><span data-stu-id="59221-134">ModuleConfiguration</span></span> |



 

<span data-ttu-id="59221-135">Чтобы устранить эту ошибку, включите в таблицу Модулеигноретабле таблицы Модулесубститутион и Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="59221-135">To fix this error include both the ModuleSubstitution and ModuleConfiguration tables in the ModuleIgnoreTable table.</span></span>

## <a name="table-used-during-execution"></a><span data-ttu-id="59221-136">Таблица, используемая во время выполнения</span><span class="sxs-lookup"><span data-stu-id="59221-136">Table Used During Execution</span></span>

[<span data-ttu-id="59221-137">модулесубститутион</span><span class="sxs-lookup"><span data-stu-id="59221-137">ModuleSubstitution</span></span>](modulesubstitution-table.md)

[<span data-ttu-id="59221-138">модулеконфигуратион</span><span class="sxs-lookup"><span data-stu-id="59221-138">ModuleConfiguration</span></span>](moduleconfiguration-table.md)

[<span data-ttu-id="59221-139">модулеигноретабле</span><span class="sxs-lookup"><span data-stu-id="59221-139">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)

## <a name="related-topics"></a><span data-ttu-id="59221-140">См. также</span><span class="sxs-lookup"><span data-stu-id="59221-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59221-141">Ссылка на модуль слияния ICE</span><span class="sxs-lookup"><span data-stu-id="59221-141">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



