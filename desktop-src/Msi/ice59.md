---
description: ICE59 проверяет, относятся ли объявленные ярлыки к компонентам, установленным целевым компонентом ярлыка.
ms.assetid: 9cd19137-792d-4fde-92d2-7d96942448d6
title: ICE59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5631b723a158bb371fff3211654a70d694b6cb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650702"
---
# <a name="ice59"></a><span data-ttu-id="335f3-103">ICE59</span><span class="sxs-lookup"><span data-stu-id="335f3-103">ICE59</span></span>

<span data-ttu-id="335f3-104">ICE59 проверяет, относятся ли объявленные ярлыки к компонентам, установленным целевым компонентом ярлыка.</span><span class="sxs-lookup"><span data-stu-id="335f3-104">ICE59 checks that advertised shortcuts belong to components that are installed by the target feature of the shortcut.</span></span>

<span data-ttu-id="335f3-105">Ошибки, о которых сообщает ICE59, обычно ведут к следующему поведению:</span><span class="sxs-lookup"><span data-stu-id="335f3-105">Errors reported by ICE59 generally lead to the following behavior:</span></span>

1.  <span data-ttu-id="335f3-106">Объявленный ярлык запустит установщик Windows для установки компонента, указанного в целевом столбце.</span><span class="sxs-lookup"><span data-stu-id="335f3-106">The advertised shortcut will launch the Windows Installer to install the feature listed in the Target column.</span></span>
2.  <span data-ttu-id="335f3-107">Но поскольку [Таблица феатурекомпонентс](featurecomponents-table.md) не сопоставляет целевой компонент с компонентом, содержащим ярлык, файл ключа компонента (который активируется ярлыком) не устанавливается.</span><span class="sxs-lookup"><span data-stu-id="335f3-107">But because the [FeatureComponents table](featurecomponents-table.md) does not map the target feature to the component containing the shortcut, the keyfile of the component (which is activated by the shortcut) is not installed.</span></span>
3.  <span data-ttu-id="335f3-108">Поэтому сочетание клавиш разорвано и не будет выполнять никаких действий.</span><span class="sxs-lookup"><span data-stu-id="335f3-108">Therefore the shortcut is broken and will not do anything.</span></span>

## <a name="result"></a><span data-ttu-id="335f3-109">Результат</span><span class="sxs-lookup"><span data-stu-id="335f3-109">Result</span></span>

<span data-ttu-id="335f3-110">ICE59 отправляет сообщение об ошибке, если объявленный ярлык не относится к компонентам, установленным целевым компонентом ярлыка.</span><span class="sxs-lookup"><span data-stu-id="335f3-110">ICE59 posts an error if an advertised shortcut does not belong to the components that are installed by the target feature of the shortcut.</span></span>

## <a name="example"></a><span data-ttu-id="335f3-111">Пример</span><span class="sxs-lookup"><span data-stu-id="335f3-111">Example</span></span>

<span data-ttu-id="335f3-112">ICE59 сообщает об ошибке в приведенном примере:</span><span class="sxs-lookup"><span data-stu-id="335f3-112">ICE59 reports the following error for the example shown:</span></span>

``` syntax
The shortcut ShortcutB activates component ComponentB and advertises feature FeatureA, but there is no mapping between FeatureA and ComponentB in the FeatureComponents table.
```

<span data-ttu-id="335f3-113">В этом случае Шорткутб объявляет функцию a, а при активации запускает файл ключа Компонентб.</span><span class="sxs-lookup"><span data-stu-id="335f3-113">In this case, ShortcutB advertises FeatureA, and when activated, starts the key file of ComponentB.</span></span> <span data-ttu-id="335f3-114">Однако Компонентб никогда не устанавливается компонентом a, поэтому даже после завершения этапа установки по запросу целевой объект ярлыка не существует.</span><span class="sxs-lookup"><span data-stu-id="335f3-114">Yet ComponentB is never installed by FeatureA, so even after the installation-on-demand phase completes, the target of the shortcut does not exist.</span></span>

<span data-ttu-id="335f3-115">Чтобы устранить эту ошибку, добавьте строку в [таблицу феатурекомпонентс](featurecomponents-table.md) , которая связывает компоненты a и компонентб.</span><span class="sxs-lookup"><span data-stu-id="335f3-115">To fix this error, add a row to the [FeatureComponents table](featurecomponents-table.md) that associates FeatureA and ComponentB.</span></span>

<span data-ttu-id="335f3-116">[Таблица ярлыков](shortcut-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="335f3-116">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="335f3-117">Сочетание клавиш</span><span class="sxs-lookup"><span data-stu-id="335f3-117">Shortcut</span></span>  | <span data-ttu-id="335f3-118">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="335f3-118">Target</span></span>   | <span data-ttu-id="335f3-119">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="335f3-119">Component\_</span></span> |
|-----------|----------|-------------|
| <span data-ttu-id="335f3-120">шорткутб</span><span class="sxs-lookup"><span data-stu-id="335f3-120">ShortcutB</span></span> | <span data-ttu-id="335f3-121">Компонент а</span><span class="sxs-lookup"><span data-stu-id="335f3-121">FeatureA</span></span> | <span data-ttu-id="335f3-122">компонентб</span><span class="sxs-lookup"><span data-stu-id="335f3-122">ComponentB</span></span>  |



 

[<span data-ttu-id="335f3-123">Таблица Феатурекомпонентс</span><span class="sxs-lookup"><span data-stu-id="335f3-123">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="335f3-124">Функция\_</span><span class="sxs-lookup"><span data-stu-id="335f3-124">Feature\_</span></span> | <span data-ttu-id="335f3-125">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="335f3-125">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="335f3-126">Компонент а</span><span class="sxs-lookup"><span data-stu-id="335f3-126">FeatureA</span></span>  | <span data-ttu-id="335f3-127">Компонент а</span><span class="sxs-lookup"><span data-stu-id="335f3-127">ComponentA</span></span>  |



 

<span data-ttu-id="335f3-128">[Таблица компонентов](feature-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="335f3-128">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="335f3-129">Функция</span><span class="sxs-lookup"><span data-stu-id="335f3-129">Feature</span></span>  | <span data-ttu-id="335f3-130">Level</span><span class="sxs-lookup"><span data-stu-id="335f3-130">Level</span></span> |
|----------|-------|
| <span data-ttu-id="335f3-131">Компонент а</span><span class="sxs-lookup"><span data-stu-id="335f3-131">FeatureA</span></span> | <span data-ttu-id="335f3-132">10</span><span class="sxs-lookup"><span data-stu-id="335f3-132">10</span></span>    |



 

<span data-ttu-id="335f3-133">[Таблица Component](component-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="335f3-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="335f3-134">Компонент</span><span class="sxs-lookup"><span data-stu-id="335f3-134">Component</span></span>  | <span data-ttu-id="335f3-135">Путь</span><span class="sxs-lookup"><span data-stu-id="335f3-135">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="335f3-136">Компонент а</span><span class="sxs-lookup"><span data-stu-id="335f3-136">ComponentA</span></span> | <span data-ttu-id="335f3-137">Файл а</span><span class="sxs-lookup"><span data-stu-id="335f3-137">FileA</span></span>   |
| <span data-ttu-id="335f3-138">компонентб</span><span class="sxs-lookup"><span data-stu-id="335f3-138">ComponentB</span></span> | <span data-ttu-id="335f3-139">филеб</span><span class="sxs-lookup"><span data-stu-id="335f3-139">FileB</span></span>   |



 

<span data-ttu-id="335f3-140">[Таблица файлов](file-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="335f3-140">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="335f3-141">Файл</span><span class="sxs-lookup"><span data-stu-id="335f3-141">File</span></span>  | <span data-ttu-id="335f3-142">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="335f3-142">Component\_</span></span> | <span data-ttu-id="335f3-143">Последовательность</span><span class="sxs-lookup"><span data-stu-id="335f3-143">Sequence</span></span> |
|-------|-------------|----------|
| <span data-ttu-id="335f3-144">Файл а</span><span class="sxs-lookup"><span data-stu-id="335f3-144">FileA</span></span> | <span data-ttu-id="335f3-145">Компонент а</span><span class="sxs-lookup"><span data-stu-id="335f3-145">ComponentA</span></span>  | <span data-ttu-id="335f3-146">1</span><span class="sxs-lookup"><span data-stu-id="335f3-146">1</span></span>        |
| <span data-ttu-id="335f3-147">филеб</span><span class="sxs-lookup"><span data-stu-id="335f3-147">FileB</span></span> | <span data-ttu-id="335f3-148">компонентб</span><span class="sxs-lookup"><span data-stu-id="335f3-148">ComponentB</span></span>  | <span data-ttu-id="335f3-149">2</span><span class="sxs-lookup"><span data-stu-id="335f3-149">2</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="335f3-150">См. также</span><span class="sxs-lookup"><span data-stu-id="335f3-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="335f3-151">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="335f3-151">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



