---
description: ICE67 проверяет, что целевой объект необъявленного ярлыка принадлежит к тому же компоненту, что и сам ярлык, или что атрибуты целевого компонента гарантируют, что они не изменяют расположения установки.
ms.assetid: 3fc462e7-4c11-4167-a157-6c1e0791901d
title: ICE67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca140a2d7eace9b693e82763f6bf5824346b51e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999244"
---
# <a name="ice67"></a><span data-ttu-id="07480-103">ICE67</span><span class="sxs-lookup"><span data-stu-id="07480-103">ICE67</span></span>

<span data-ttu-id="07480-104">ICE67 проверяет, что целевой объект необъявленного ярлыка принадлежит к тому же компоненту, что и сам ярлык, или что атрибуты целевого компонента гарантируют, что они не изменяют расположения установки.</span><span class="sxs-lookup"><span data-stu-id="07480-104">ICE67 checks that the target of a non-advertised shortcut belongs to the same component as the shortcut itself, or that the attributes of the target component ensure that it does not change installation locations.</span></span>

<span data-ttu-id="07480-105">Сбой исправления предупреждения или ошибки, о которой сообщает ICE67, может привести к недействительности ярлыка, если целевой компонент изменит состояние, а компонент-Источник — нет.</span><span class="sxs-lookup"><span data-stu-id="07480-105">Failure to fix a warning or error reported by ICE67 can cause the shortcut to be invalid if the target component changes state and the source component does not.</span></span> <span data-ttu-id="07480-106">Например, если компонент целевого файла настроен для запуска из источника, переустановка, которая изменяет компонент на локальные, приводит к установке компонента, содержащего ярлык, который не переустанавливается.</span><span class="sxs-lookup"><span data-stu-id="07480-106">For example, when the target file's component is set to run from source, a reinstallation that changes the component to local results in the component containing the shortcut not being reinstalled.</span></span> <span data-ttu-id="07480-107">Таким же ярлык указывает на недопустимое расположение.</span><span class="sxs-lookup"><span data-stu-id="07480-107">Thus the shortcut points to an invalid location.</span></span>

<span data-ttu-id="07480-108">Обратите внимание, что в некоторых случаях использование другого компонента для ярлыка не позволяет избежать проблем.</span><span class="sxs-lookup"><span data-stu-id="07480-108">Note that in some cases, using a different component for the shortcut is unavoidable.</span></span> <span data-ttu-id="07480-109">Например, если в профиле пользователя создается ярлык и файл устанавливается в каталог без профиля, то, возможно, вы не сможете использовать один и тот же компонент для обоих фрагментов данных.</span><span class="sxs-lookup"><span data-stu-id="07480-109">For example, if the shortcut is created in the user profile and the file is installed to a non-profile directory, you may not be able to use the same component for both pieces of data.</span></span> <span data-ttu-id="07480-110">(Это приводит к сбоям в сценариях с несколькими пользователями, например, описанных в [ICE57](ice57.md)).</span><span class="sxs-lookup"><span data-stu-id="07480-110">(This results in failures in multi-user scenarios – such as those described in [ICE57](ice57.md)).</span></span> <span data-ttu-id="07480-111">В этом случае вы можете использовать объявленные ярлыки для достижения желаемого поведения или просто убедиться, что целевой компонент не может быть изменен с "от-исходного" на локальный.</span><span class="sxs-lookup"><span data-stu-id="07480-111">In this case, you may be able to use advertised shortcuts to achieve the behavior you want, or you can simply ensure that the target component cannot change from run-from-source to local.</span></span>

## <a name="result"></a><span data-ttu-id="07480-112">Результат</span><span class="sxs-lookup"><span data-stu-id="07480-112">Result</span></span>

<span data-ttu-id="07480-113">ICE67 возвращает ошибку или предупреждение, если целевой объект необъявленного ярлыка не принадлежит к тому же компоненту, что и сам ярлык, или если атрибуты целевого компонента не гарантируют, что расположения установки не изменятся.</span><span class="sxs-lookup"><span data-stu-id="07480-113">ICE67 returns an error or a warning if the target of a non-advertised shortcut does not belong to the same component as the shortcut itself, or if the attributes of the target component do not ensure that the installation locations will not change.</span></span>

## <a name="example"></a><span data-ttu-id="07480-114">Пример</span><span class="sxs-lookup"><span data-stu-id="07480-114">Example</span></span>

<span data-ttu-id="07480-115">ICE67 сообщает о следующих предупреждениях и ошибках в приведенном примере.</span><span class="sxs-lookup"><span data-stu-id="07480-115">ICE67 reports the following warning and errors for the example shown.</span></span>

``` syntax
The shortcut 'Shortcut1' is a non-advertised shortcut with a file target. The shortcut and target are installed by different components, and the target component can run locally or from source.
```

<span data-ttu-id="07480-116">Shortcut1 устанавливается с помощью Component2, но его целевой файл file1 устанавливается Component1.</span><span class="sxs-lookup"><span data-stu-id="07480-116">Shortcut1 is installed by Component2, but its target file, File1, is installed by component1.</span></span> <span data-ttu-id="07480-117">Целевой компонент помечается как необязательный (это означает, что он может быть локальным или запущенным из исходного кода).</span><span class="sxs-lookup"><span data-stu-id="07480-117">The target component is marked optional (meaning that it can be local or run-from-source).</span></span> <span data-ttu-id="07480-118">Одна из возможных ситуаций, которая привела бы к возникновению проблемы, заключается в том, что Component1 меняется с Run-from-Source на локальную.</span><span class="sxs-lookup"><span data-stu-id="07480-118">One possible situation that would cause a problem is if Component1 changes from run-from-source to local.</span></span> <span data-ttu-id="07480-119">Это приведет к тому, что Shortcut1 будет указывать на недопустимое расположение.</span><span class="sxs-lookup"><span data-stu-id="07480-119">This would cause Shortcut1 to point to an invalid location.</span></span>

<span data-ttu-id="07480-120">Чтобы устранить это предупреждение, установите ярлык в составе Component1 или пометьте Component1 как LocalOnly или Саурцеонли.</span><span class="sxs-lookup"><span data-stu-id="07480-120">To fix this warning, Install the shortcut as part of Component1, or mark Component1 as LocalOnly or SourceOnly.</span></span>

<span data-ttu-id="07480-121">[Таблица файлов](file-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="07480-121">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="07480-122">Файл</span><span class="sxs-lookup"><span data-stu-id="07480-122">File</span></span>  | <span data-ttu-id="07480-123">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="07480-123">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="07480-124">Файл1</span><span class="sxs-lookup"><span data-stu-id="07480-124">File1</span></span> | <span data-ttu-id="07480-125">Component1</span><span class="sxs-lookup"><span data-stu-id="07480-125">Component1</span></span>  |



 

<span data-ttu-id="07480-126">[Таблица ярлыков](shortcut-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="07480-126">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="07480-127">Сочетание клавиш</span><span class="sxs-lookup"><span data-stu-id="07480-127">Shortcut</span></span>  | <span data-ttu-id="07480-128">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="07480-128">Component\_</span></span> | <span data-ttu-id="07480-129">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="07480-129">Target</span></span>      |
|-----------|-------------|-------------|
| <span data-ttu-id="07480-130">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="07480-130">Shortcut1</span></span> | <span data-ttu-id="07480-131">Component2</span><span class="sxs-lookup"><span data-stu-id="07480-131">Component2</span></span>  | <span data-ttu-id="07480-132">\[\#File1\]</span><span class="sxs-lookup"><span data-stu-id="07480-132">\[\#File1\]</span></span> |



 

<span data-ttu-id="07480-133">[Таблица Component](component-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="07480-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="07480-134">Компонент</span><span class="sxs-lookup"><span data-stu-id="07480-134">Component</span></span>  | <span data-ttu-id="07480-135">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="07480-135">Attributes</span></span> |
|------------|------------|
| <span data-ttu-id="07480-136">Component1</span><span class="sxs-lookup"><span data-stu-id="07480-136">Component1</span></span> | <span data-ttu-id="07480-137">2</span><span class="sxs-lookup"><span data-stu-id="07480-137">2</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="07480-138">См. также</span><span class="sxs-lookup"><span data-stu-id="07480-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07480-139">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="07480-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



