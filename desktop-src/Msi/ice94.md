---
description: ICE94 проверяет таблицу ярлыков, таблицу компонентов и таблицу Мсиассембли и отправляет предупреждение, если есть необъявленные ярлыки, указывающие на файл сборки в глобальном кэше сборок.
ms.assetid: 9b1b25b5-b190-47c2-8d43-fa3964e87a6f
title: ICE94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ce52e88a31e246eb4d69defba77b64c2955eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266130"
---
# <a name="ice94"></a><span data-ttu-id="4618e-103">ICE94</span><span class="sxs-lookup"><span data-stu-id="4618e-103">ICE94</span></span>

<span data-ttu-id="4618e-104">ICE94 проверяет [таблицу ярлыков](shortcut-table.md), [таблицу компонентов](feature-table.md)и [таблицу мсиассембли](msiassembly-table.md) и отправляет предупреждение, если есть необъявленные ярлыки, указывающие на файл сборки в глобальном кэше сборок.</span><span class="sxs-lookup"><span data-stu-id="4618e-104">ICE94 checks the [Shortcut table](shortcut-table.md), [Feature table](feature-table.md), and [MsiAssembly table](msiassembly-table.md) and posts a warning if there are any unadvertised shortcuts pointing to an assembly file in the global assembly cache.</span></span> <span data-ttu-id="4618e-105">Если запись в целевом поле в таблице ярлыков не является функцией в таблице Feature, это сочетание не объявляется.</span><span class="sxs-lookup"><span data-stu-id="4618e-105">If the entry in the Target field of the Shortcut table is not a feature in the Feature table, the shortcut is unadvertised.</span></span> <span data-ttu-id="4618e-106">Если запись в \_ поле Component Таблицы ярлыков также указана в таблице мсиассембли, ярлык указывает на файл сборки.</span><span class="sxs-lookup"><span data-stu-id="4618e-106">If the entry in the Component\_ field of the Shortcut table is also listed in the MsiAssembly table, the shortcut points to an assembly file.</span></span> <span data-ttu-id="4618e-107">Если запись в поле файлового \_ приложения в таблице мсиассембли пуста, файл сборки находится в глобальном кэше сборок.</span><span class="sxs-lookup"><span data-stu-id="4618e-107">If the entry in the File\_Application field in the MsiAssembly table is empty, the assembly file is in the global assembly cache.</span></span>

## <a name="result"></a><span data-ttu-id="4618e-108">Результат</span><span class="sxs-lookup"><span data-stu-id="4618e-108">Result</span></span>

<span data-ttu-id="4618e-109">ICE94 отправляет следующее предупреждение.</span><span class="sxs-lookup"><span data-stu-id="4618e-109">ICE94 posts the following warning.</span></span>



| <span data-ttu-id="4618e-110">Предупреждение ICE94</span><span class="sxs-lookup"><span data-stu-id="4618e-110">ICE94 warning</span></span>                                                                                | <span data-ttu-id="4618e-111">Описание</span><span class="sxs-lookup"><span data-stu-id="4618e-111">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4618e-112">Необъявленный ярлык " \[ 2 \] " указывает на файл сборки в глобальном кэше сборок.</span><span class="sxs-lookup"><span data-stu-id="4618e-112">The non-advertised shortcut '\[2\]' points to an assembly file in the global assembly cache.</span></span> | <span data-ttu-id="4618e-113">Необъявленный ярлык указывает на файл сборки в глобальном кэше сборок.</span><span class="sxs-lookup"><span data-stu-id="4618e-113">An unadvertised shortcut is pointing to an assembly file in the global assembly cache.</span></span> |



 

## <a name="example"></a><span data-ttu-id="4618e-114">Пример</span><span class="sxs-lookup"><span data-stu-id="4618e-114">Example</span></span>

<span data-ttu-id="4618e-115">ICE94 сообщает о следующей ошибке в примере:</span><span class="sxs-lookup"><span data-stu-id="4618e-115">ICE94 reports the following error for the example:</span></span>

``` syntax
The non-advertised shortcut 'shortcut1' points to an assembly file in the global assembly cache.
```

<span data-ttu-id="4618e-116">[Таблица ярлыков](shortcut-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="4618e-116">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="4618e-117">Сочетание клавиш</span><span class="sxs-lookup"><span data-stu-id="4618e-117">Shortcut</span></span>  | <span data-ttu-id="4618e-118">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="4618e-118">Component\_</span></span> | <span data-ttu-id="4618e-119">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="4618e-119">Target</span></span>    |
|-----------|-------------|-----------|
| <span data-ttu-id="4618e-120">shortcut1</span><span class="sxs-lookup"><span data-stu-id="4618e-120">shortcut1</span></span> | <span data-ttu-id="4618e-121">c1</span><span class="sxs-lookup"><span data-stu-id="4618e-121">c1</span></span>          | <span data-ttu-id="4618e-122">\[file1\]</span><span class="sxs-lookup"><span data-stu-id="4618e-122">\[file1\]</span></span> |
| <span data-ttu-id="4618e-123">shortcut2</span><span class="sxs-lookup"><span data-stu-id="4618e-123">shortcut2</span></span> | <span data-ttu-id="4618e-124">c2</span><span class="sxs-lookup"><span data-stu-id="4618e-124">c2</span></span>          | <span data-ttu-id="4618e-125">Feature1</span><span class="sxs-lookup"><span data-stu-id="4618e-125">feature1</span></span>  |
| <span data-ttu-id="4618e-126">shortcut3</span><span class="sxs-lookup"><span data-stu-id="4618e-126">shortcut3</span></span> | <span data-ttu-id="4618e-127">c3</span><span class="sxs-lookup"><span data-stu-id="4618e-127">c3</span></span>          | <span data-ttu-id="4618e-128">\[file2\]</span><span class="sxs-lookup"><span data-stu-id="4618e-128">\[file2\]</span></span> |



 

<span data-ttu-id="4618e-129">[Таблица компонентов](feature-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="4618e-129">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="4618e-130">Функция</span><span class="sxs-lookup"><span data-stu-id="4618e-130">Feature</span></span>  |
|----------|
| <span data-ttu-id="4618e-131">Feature1</span><span class="sxs-lookup"><span data-stu-id="4618e-131">feature1</span></span> |



 

<span data-ttu-id="4618e-132">[Таблица мсиассембли](msiassembly-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="4618e-132">[MsiAssembly Table](msiassembly-table.md) (partial)</span></span>



| <span data-ttu-id="4618e-133">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="4618e-133">Component\_</span></span> | <span data-ttu-id="4618e-134">\_Приложение файла</span><span class="sxs-lookup"><span data-stu-id="4618e-134">File\_Application</span></span> |
|-------------|-------------------|
| <span data-ttu-id="4618e-135">c1</span><span class="sxs-lookup"><span data-stu-id="4618e-135">c1</span></span>          |                   |
| <span data-ttu-id="4618e-136">c2</span><span class="sxs-lookup"><span data-stu-id="4618e-136">c2</span></span>          |                   |
| <span data-ttu-id="4618e-137">c3</span><span class="sxs-lookup"><span data-stu-id="4618e-137">c3</span></span>          | <span data-ttu-id="4618e-138">fa1</span><span class="sxs-lookup"><span data-stu-id="4618e-138">fa1</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="4618e-139">См. также</span><span class="sxs-lookup"><span data-stu-id="4618e-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4618e-140">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="4618e-140">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



