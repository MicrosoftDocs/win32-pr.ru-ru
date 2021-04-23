---
description: ICE02 проверяет, что определенные ссылки между компонентами, файлами и таблицами реестра являются обратными. Чтобы установщик правильно определил состояние установки компонентов, эти ссылки должны быть обратными.
ms.assetid: 864404f1-439d-49a2-973d-4e6e1618863e
title: ICE02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975203825d079d5eeb1ec5e4183767dd68625bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808752"
---
# <a name="ice02"></a><span data-ttu-id="68d56-104">ICE02</span><span class="sxs-lookup"><span data-stu-id="68d56-104">ICE02</span></span>

<span data-ttu-id="68d56-105">ICE02 проверяет, что определенные ссылки между [компонентами](component-table.md), [файлами](file-table.md)и таблицами [реестра](registry-table.md) являются обратными.</span><span class="sxs-lookup"><span data-stu-id="68d56-105">ICE02 validates that certain references between the [Component](component-table.md), [File](file-table.md), and [Registry](registry-table.md) tables are reciprocal.</span></span> <span data-ttu-id="68d56-106">Чтобы установщик правильно определил состояние установки компонентов, эти ссылки должны быть обратными.</span><span class="sxs-lookup"><span data-stu-id="68d56-106">These references must to be reciprocal for the installer to correctly determine the installation state of components.</span></span>

<span data-ttu-id="68d56-107">Установщик использует столбец ключевого пути в таблице Component для определения наличия компонента, указанного в столбце Component.</span><span class="sxs-lookup"><span data-stu-id="68d56-107">The installer uses the KeyPath column of the Component table to detect the presence of the component listed in the Component column.</span></span> <span data-ttu-id="68d56-108">Ключевой столбец содержит ключ в реестре или файловые таблицы.</span><span class="sxs-lookup"><span data-stu-id="68d56-108">The KeyPath column contains a key into the Registry or File tables.</span></span> <span data-ttu-id="68d56-109">Обе эти таблицы имеют \_ столбец Component, который содержит ключ обратно в таблицу Component, указывающую на компонент, управляющий записью или файлом реестра.</span><span class="sxs-lookup"><span data-stu-id="68d56-109">Both of these tables have a Component\_ column that contains a key back into the Component table pointing to the component that controls the registry entry or file.</span></span> <span data-ttu-id="68d56-110">Эти ссылки должны быть обратными.</span><span class="sxs-lookup"><span data-stu-id="68d56-110">These references must be reciprocal.</span></span>

## <a name="result"></a><span data-ttu-id="68d56-111">Результат</span><span class="sxs-lookup"><span data-stu-id="68d56-111">Result</span></span>

<span data-ttu-id="68d56-112">ICE02 отправляет сообщение об ошибке, если обнаруживает ссылку, которая должна быть обратной и не является.</span><span class="sxs-lookup"><span data-stu-id="68d56-112">ICE02 posts an error message if it finds a reference that should be reciprocal and is not.</span></span>

## <a name="example"></a><span data-ttu-id="68d56-113">Пример</span><span class="sxs-lookup"><span data-stu-id="68d56-113">Example</span></span>

<span data-ttu-id="68d56-114">ICE02 будет размещать следующее сообщение об ошибке для MSI-файла, содержащего отображаемые записи базы данных.</span><span class="sxs-lookup"><span data-stu-id="68d56-114">ICE02 would post the following error message for a .msi file containing the database entries shown.</span></span>

``` syntax
File: 'Red_File' cannot be the key file for Component: 'Blue'. The file belongs to Component: 'Red'
```

<span data-ttu-id="68d56-115">[Таблица Component](component-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="68d56-115">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="68d56-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="68d56-116">Component</span></span> | <span data-ttu-id="68d56-117">Путь</span><span class="sxs-lookup"><span data-stu-id="68d56-117">KeyPath</span></span>   |
|-----------|-----------|
| <span data-ttu-id="68d56-118">Красный</span><span class="sxs-lookup"><span data-stu-id="68d56-118">Red</span></span>       | <span data-ttu-id="68d56-119">Красный \_ файл</span><span class="sxs-lookup"><span data-stu-id="68d56-119">Red\_File</span></span> |
| <span data-ttu-id="68d56-120">Синий</span><span class="sxs-lookup"><span data-stu-id="68d56-120">Blue</span></span>      | <span data-ttu-id="68d56-121">Красный \_ файл</span><span class="sxs-lookup"><span data-stu-id="68d56-121">Red\_File</span></span> |



 

<span data-ttu-id="68d56-122">[Таблица файлов](file-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="68d56-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="68d56-123">Столбец файла</span><span class="sxs-lookup"><span data-stu-id="68d56-123">File Column</span></span> | <span data-ttu-id="68d56-124">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="68d56-124">Component\_</span></span> |
|-------------|-------------|
| <span data-ttu-id="68d56-125">Красный \_ файл</span><span class="sxs-lookup"><span data-stu-id="68d56-125">Red\_File</span></span>   | <span data-ttu-id="68d56-126">Красный</span><span class="sxs-lookup"><span data-stu-id="68d56-126">Red</span></span>         |
| <span data-ttu-id="68d56-127">Синий \_ файл</span><span class="sxs-lookup"><span data-stu-id="68d56-127">Blue\_File</span></span>  | <span data-ttu-id="68d56-128">Синий</span><span class="sxs-lookup"><span data-stu-id="68d56-128">Blue</span></span>        |



 

<span data-ttu-id="68d56-129">Компонент Blue ссылается на красный \_ файл, но красный \_ файл не управляется синим компонентом и, следовательно, не может быть файлом ключевого файла.</span><span class="sxs-lookup"><span data-stu-id="68d56-129">Component Blue references Red\_File, but Red\_File is not controlled by Component Blue and therefore cannot be the KeyPath file.</span></span> <span data-ttu-id="68d56-130">Если установщик был вызван для получения состояния установки Blue, он неправильно проверяет \_ , установлен ли красный файл.</span><span class="sxs-lookup"><span data-stu-id="68d56-130">If the installer were called to get the installation state of Blue it would incorrectly check whether Red\_File was installed.</span></span> <span data-ttu-id="68d56-131">Изменение поля ключевого пути синего в таблице Component (компонент) на «синий» \_ файл устраняет ошибку.</span><span class="sxs-lookup"><span data-stu-id="68d56-131">Changing the KeyPath field for Blue in the Component Table to Blue\_File fixes the error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68d56-132">См. также</span><span class="sxs-lookup"><span data-stu-id="68d56-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68d56-133">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="68d56-133">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



