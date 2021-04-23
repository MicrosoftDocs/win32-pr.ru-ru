---
description: ICE36 проверяет, что каждый значок в таблице значков указан по крайней мере один раз в свойстве АРППРОДУКТИКОН или в таблицах класса, ProgId или ярлыков.
ms.assetid: d502c0a9-17e5-467a-8b02-8b254e77b96b
title: ICE36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f24eebc1b591edde418c59b6765d7ee91a00dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081064"
---
# <a name="ice36"></a><span data-ttu-id="e1252-103">ICE36</span><span class="sxs-lookup"><span data-stu-id="e1252-103">ICE36</span></span>

<span data-ttu-id="e1252-104">ICE36 проверяет, что каждый значок в таблице значков указан по крайней мере один раз в свойстве [**арппродуктикон**](arpproducticon.md) или в таблицах [класса](class-table.md), [ProgID](progid-table.md)или [ярлыков](shortcut-table.md) .</span><span class="sxs-lookup"><span data-stu-id="e1252-104">ICE36 validates that every icon in the Icon table is listed at least once in the [**ARPPRODUCTICON**](arpproducticon.md) property or the [Class](class-table.md), [ProgId](progid-table.md), or [Shortcut](shortcut-table.md) tables.</span></span>

<span data-ttu-id="e1252-105">Во время объявления установщик устанавливает все значки, перечисленные в [таблице значков](icon-table.md) на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="e1252-105">During advertisement, the installer installs all the icons listed in the [Icon table](icon-table.md) on the user's computer.</span></span> <span data-ttu-id="e1252-106">Наличие неиспользуемых значков в таблице значков не препятствует запуску установки, однако при этом размер MSI-файла необязательно увеличится, а время и пространство, необходимое для объявления функции.</span><span class="sxs-lookup"><span data-stu-id="e1252-106">Having unused icons in the Icon table does not prevent the installation from running, however it does unnecessarily increase the size of the .msi file and the time and space required to advertise a feature.</span></span>

<span data-ttu-id="e1252-107">Если на значок нет ссылки в свойстве или в таблице и отсутствует пользовательский интерфейс для создания ссылки во время выполнения, следует удалить значок, чтобы добиться лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="e1252-107">If an icon is not referenced in the property or table and there is no UI provided to create a reference at run time, you should remove the icon to achieve better performance.</span></span>

## <a name="result"></a><span data-ttu-id="e1252-108">Результат</span><span class="sxs-lookup"><span data-stu-id="e1252-108">Result</span></span>

<span data-ttu-id="e1252-109">ICE36 отправляет сообщение, если в таблице значков имеется значок, на который нет ссылок в таблицах [классов](class-table.md), [ProgID](progid-table.md)или [ярлыков](shortcut-table.md) , и если для создания такой ссылки во время выполнения не предусмотрен пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="e1252-109">ICE36 posts a message if there is a icon in the Icon table that is not referenced in the [Class](class-table.md), [ProgId](progid-table.md), or [Shortcut](shortcut-table.md) tables and if there is no UI provided to create such a reference at run time.</span></span>

## <a name="example"></a><span data-ttu-id="e1252-110">Пример</span><span class="sxs-lookup"><span data-stu-id="e1252-110">Example</span></span>

<span data-ttu-id="e1252-111">ICE36 сообщает об ошибке в приведенном примере.</span><span class="sxs-lookup"><span data-stu-id="e1252-111">ICE36 reports the following error for the example shown.</span></span>

``` syntax
Icon Bloat. Icon Icon4 is not used in the Class, Shortcut, or ProgID table. This adversely affects performance.
```

<span data-ttu-id="e1252-112">[Таблица значков](icon-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="e1252-112">[Icon Table](icon-table.md) (partial)</span></span>



| <span data-ttu-id="e1252-113">Имя</span><span class="sxs-lookup"><span data-stu-id="e1252-113">Name</span></span>  | <span data-ttu-id="e1252-114">Данные</span><span class="sxs-lookup"><span data-stu-id="e1252-114">Data</span></span>     |
|-------|----------|
| <span data-ttu-id="e1252-115">Icon1</span><span class="sxs-lookup"><span data-stu-id="e1252-115">Icon1</span></span> | <span data-ttu-id="e1252-116">Control1</span><span class="sxs-lookup"><span data-stu-id="e1252-116">Control1</span></span> |
| <span data-ttu-id="e1252-117">Icon2</span><span class="sxs-lookup"><span data-stu-id="e1252-117">Icon2</span></span> | <span data-ttu-id="e1252-118">Control2</span><span class="sxs-lookup"><span data-stu-id="e1252-118">Control2</span></span> |
| <span data-ttu-id="e1252-119">Icon3</span><span class="sxs-lookup"><span data-stu-id="e1252-119">Icon3</span></span> | <span data-ttu-id="e1252-120">Control3</span><span class="sxs-lookup"><span data-stu-id="e1252-120">Control3</span></span> |
| <span data-ttu-id="e1252-121">Icon4</span><span class="sxs-lookup"><span data-stu-id="e1252-121">Icon4</span></span> | <span data-ttu-id="e1252-122">Control4</span><span class="sxs-lookup"><span data-stu-id="e1252-122">Control4</span></span> |



 

<span data-ttu-id="e1252-123">[Таблица ProgID](progid-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="e1252-123">[ProgID Table](progid-table.md) (partial)</span></span>



| <span data-ttu-id="e1252-124">ProgID:</span><span class="sxs-lookup"><span data-stu-id="e1252-124">ProgID</span></span>    |
|-----------|
| <span data-ttu-id="e1252-125">Property1</span><span class="sxs-lookup"><span data-stu-id="e1252-125">Property1</span></span> |



 

<span data-ttu-id="e1252-126">[Таблица классов](class-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="e1252-126">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="e1252-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="e1252-127">CLSID</span></span>                                  |
|----------------------------------------|
| <span data-ttu-id="e1252-128">{3E469ABA-3644-11d2-8892-00A0C981B015}</span><span class="sxs-lookup"><span data-stu-id="e1252-128">{3E469ABA-3644-11d2-8892-00A0C981B015}</span></span> |



 

<span data-ttu-id="e1252-129">[Таблица ярлыков](shortcut-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="e1252-129">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="e1252-130">Сочетание клавиш</span><span class="sxs-lookup"><span data-stu-id="e1252-130">Shortcut</span></span>  | <span data-ttu-id="e1252-131">Значок\_</span><span class="sxs-lookup"><span data-stu-id="e1252-131">Icon\_</span></span> |
|-----------|--------|
| <span data-ttu-id="e1252-132">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="e1252-132">Shortcut1</span></span> | <span data-ttu-id="e1252-133">Icon2</span><span class="sxs-lookup"><span data-stu-id="e1252-133">Icon2</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="e1252-134">См. также</span><span class="sxs-lookup"><span data-stu-id="e1252-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1252-135">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="e1252-135">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



