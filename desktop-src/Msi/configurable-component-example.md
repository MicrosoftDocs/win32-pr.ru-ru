---
description: Этот пример позволяет потребителю модуля независимо настраивать элемент управления правки, атрибут CHECKSUM и сжатый атрибут.
ms.assetid: f0500856-18d0-45e5-992a-57e01fb2cca5
title: Пример настраиваемого компонента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971b2a7c442acb96d7ba00a444c8c3a038c339f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662581"
---
# <a name="configurable-component-example"></a><span data-ttu-id="c2fc2-103">Пример настраиваемого компонента</span><span class="sxs-lookup"><span data-stu-id="c2fc2-103">Configurable Component Example</span></span>

<span data-ttu-id="c2fc2-104">В этом примере следующие таблицы Модулеконфигуратион и Модулесубститутион позволяют потребителю модуля независимо настраивать атрибут Password для элемента управления Edit, атрибут CHECKSUM для файла и сжатый атрибут для одного и того же файла.</span><span class="sxs-lookup"><span data-stu-id="c2fc2-104">In this example, the following ModuleConfiguration and ModuleSubstitution tables allows the module consumer to independently configure the Password attribute for an edit control, the checksum attribute for a file, and the compressed attribute for the same file.</span></span>

[<span data-ttu-id="c2fc2-105">Таблица Модулесубститутион</span><span class="sxs-lookup"><span data-stu-id="c2fc2-105">ModuleSubstitution Table</span></span>](modulesubstitution-table.md)



| <span data-ttu-id="c2fc2-106">Таблица</span><span class="sxs-lookup"><span data-stu-id="c2fc2-106">Table</span></span>   | <span data-ttu-id="c2fc2-107">Строка</span><span class="sxs-lookup"><span data-stu-id="c2fc2-107">Row</span></span>           | <span data-ttu-id="c2fc2-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="c2fc2-108">Column</span></span>     | <span data-ttu-id="c2fc2-109">Значение</span><span class="sxs-lookup"><span data-stu-id="c2fc2-109">Value</span></span>                        |
|---------|---------------|------------|------------------------------|
| <span data-ttu-id="c2fc2-110">Control</span><span class="sxs-lookup"><span data-stu-id="c2fc2-110">Control</span></span> | <span data-ttu-id="c2fc2-111">Dialog1; Edit1</span><span class="sxs-lookup"><span data-stu-id="c2fc2-111">Dialog1;Edit1</span></span> | <span data-ttu-id="c2fc2-112">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c2fc2-112">Attributes</span></span> | <span data-ttu-id="c2fc2-113">\[= Пароль\]</span><span class="sxs-lookup"><span data-stu-id="c2fc2-113">\[=Password\]</span></span>                |
| <span data-ttu-id="c2fc2-114">Файл</span><span class="sxs-lookup"><span data-stu-id="c2fc2-114">File</span></span>    | <span data-ttu-id="c2fc2-115">Файл1</span><span class="sxs-lookup"><span data-stu-id="c2fc2-115">File1</span></span>         | <span data-ttu-id="c2fc2-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c2fc2-116">Attributes</span></span> | <span data-ttu-id="c2fc2-117">\[= CHECKSUM \] \[ = сжатый\]</span><span class="sxs-lookup"><span data-stu-id="c2fc2-117">\[=Checksum\]\[=Compressed\]</span></span> |



 

[<span data-ttu-id="c2fc2-118">Таблица Модулеконфигуратион</span><span class="sxs-lookup"><span data-stu-id="c2fc2-118">ModuleConfiguration Table</span></span>](moduleconfiguration-table.md)



| <span data-ttu-id="c2fc2-119">Имя</span><span class="sxs-lookup"><span data-stu-id="c2fc2-119">Name</span></span>       | <span data-ttu-id="c2fc2-120">Формат</span><span class="sxs-lookup"><span data-stu-id="c2fc2-120">Format</span></span>   | <span data-ttu-id="c2fc2-121">Тип</span><span class="sxs-lookup"><span data-stu-id="c2fc2-121">Type</span></span> | <span data-ttu-id="c2fc2-122">контекстдата</span><span class="sxs-lookup"><span data-stu-id="c2fc2-122">ContextData</span></span>                              | <span data-ttu-id="c2fc2-123">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c2fc2-123">DefaultValue</span></span> | <span data-ttu-id="c2fc2-124">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c2fc2-124">Attributes</span></span> | <span data-ttu-id="c2fc2-125">DisplayName</span><span class="sxs-lookup"><span data-stu-id="c2fc2-125">DisplayName</span></span> | <span data-ttu-id="c2fc2-126">Описание</span><span class="sxs-lookup"><span data-stu-id="c2fc2-126">Description</span></span> |
|------------|----------|------|------------------------------------------|--------------|------------|-------------|-------------|
| <span data-ttu-id="c2fc2-127">Пароль</span><span class="sxs-lookup"><span data-stu-id="c2fc2-127">Password</span></span>   | <span data-ttu-id="c2fc2-128">Битами</span><span class="sxs-lookup"><span data-stu-id="c2fc2-128">Bitfield</span></span> |      | <span data-ttu-id="c2fc2-129">2097152; True = 2097152; False = 0</span><span class="sxs-lookup"><span data-stu-id="c2fc2-129">2097152;True=2097152;False=0</span></span>             | <span data-ttu-id="c2fc2-130">0</span><span class="sxs-lookup"><span data-stu-id="c2fc2-130">0</span></span>            | <span data-ttu-id="c2fc2-131">0</span><span class="sxs-lookup"><span data-stu-id="c2fc2-131">0</span></span>          |             |             |
| <span data-ttu-id="c2fc2-132">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="c2fc2-132">Checksum</span></span>   | <span data-ttu-id="c2fc2-133">Битами</span><span class="sxs-lookup"><span data-stu-id="c2fc2-133">Bitfield</span></span> |      | <span data-ttu-id="c2fc2-134">1024; CHECKSUM = 1024; Без контрольной суммы = 0</span><span class="sxs-lookup"><span data-stu-id="c2fc2-134">1024;Checksum=1024;No Checksum=0</span></span>         | <span data-ttu-id="c2fc2-135">0</span><span class="sxs-lookup"><span data-stu-id="c2fc2-135">0</span></span>            | <span data-ttu-id="c2fc2-136">0</span><span class="sxs-lookup"><span data-stu-id="c2fc2-136">0</span></span>          |             |             |
| <span data-ttu-id="c2fc2-137">Compressed</span><span class="sxs-lookup"><span data-stu-id="c2fc2-137">Compressed</span></span> | <span data-ttu-id="c2fc2-138">Битами</span><span class="sxs-lookup"><span data-stu-id="c2fc2-138">Bitfield</span></span> |      | <span data-ttu-id="c2fc2-139">24576; Сжатый = 16384; Без сжатия = 8192</span><span class="sxs-lookup"><span data-stu-id="c2fc2-139">24576;Compressed=16384;Uncompressed=8192</span></span> | <span data-ttu-id="c2fc2-140">8192</span><span class="sxs-lookup"><span data-stu-id="c2fc2-140">8192</span></span>         | <span data-ttu-id="c2fc2-141">0</span><span class="sxs-lookup"><span data-stu-id="c2fc2-141">0</span></span>          |             |             |



 

 

 



