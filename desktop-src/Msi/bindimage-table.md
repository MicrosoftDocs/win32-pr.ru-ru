---
description: Таблица BindImage содержит сведения о каждом исполняемом файле или библиотеке DLL, которые необходимо привязать к DLL-библиотекам, которые были импортированы.
ms.assetid: 68bf064c-dd85-4796-8e08-6af307f94ad8
title: Таблица BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47b97efc8886d7748d0426a49ed76567810939c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998262"
---
# <a name="bindimage-table"></a><span data-ttu-id="814cd-103">Таблица BindImage</span><span class="sxs-lookup"><span data-stu-id="814cd-103">BindImage Table</span></span>

<span data-ttu-id="814cd-104">Таблица BindImage содержит сведения о каждом исполняемом файле или библиотеке DLL, которые необходимо привязать к DLL-библиотекам, которые были импортированы.</span><span class="sxs-lookup"><span data-stu-id="814cd-104">The BindImage table contains information about each executable or DLL that needs to be bound to the DLLs imported by it.</span></span>

<span data-ttu-id="814cd-105">Таблица BindImage содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="814cd-105">The BindImage table has the following columns.</span></span>



| <span data-ttu-id="814cd-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="814cd-106">Column</span></span> | <span data-ttu-id="814cd-107">Type</span><span class="sxs-lookup"><span data-stu-id="814cd-107">Type</span></span>                         | <span data-ttu-id="814cd-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="814cd-108">Key</span></span> | <span data-ttu-id="814cd-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="814cd-109">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="814cd-110">Файл\_</span><span class="sxs-lookup"><span data-stu-id="814cd-110">File\_</span></span> | [<span data-ttu-id="814cd-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="814cd-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="814cd-112">Да</span><span class="sxs-lookup"><span data-stu-id="814cd-112">Y</span></span>   | <span data-ttu-id="814cd-113">Нет</span><span class="sxs-lookup"><span data-stu-id="814cd-113">N</span></span>        |
| <span data-ttu-id="814cd-114">Путь</span><span class="sxs-lookup"><span data-stu-id="814cd-114">Path</span></span>   | [<span data-ttu-id="814cd-115">Пути</span><span class="sxs-lookup"><span data-stu-id="814cd-115">Paths</span></span>](paths.md)           | <span data-ttu-id="814cd-116">Нет</span><span class="sxs-lookup"><span data-stu-id="814cd-116">N</span></span>   | <span data-ttu-id="814cd-117">Да</span><span class="sxs-lookup"><span data-stu-id="814cd-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="814cd-118">Столбцы</span><span class="sxs-lookup"><span data-stu-id="814cd-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="814cd-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="814cd-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="814cd-120">Внешний ключ для столбца одной [таблицы File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="814cd-120">An external key to column one of the [File table](file-table.md).</span></span> <span data-ttu-id="814cd-121">Это должен быть исполняемый файл или DLL-файл.</span><span class="sxs-lookup"><span data-stu-id="814cd-121">This must be an executable file or a DLL file.</span></span>

</dd> <dt>

<span data-ttu-id="814cd-122"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Путь</span><span class="sxs-lookup"><span data-stu-id="814cd-122"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Path</span></span>
</dt> <dd>

<span data-ttu-id="814cd-123">Список путей, разделенных точкой с запятой, которые представляют пути для поиска импортируемых библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="814cd-123">A list of paths, separated by semicolons, that represent the paths to be searched to find the imported DLLs.</span></span> <span data-ttu-id="814cd-124">Список обычно представляет собой список свойств, в котором каждое свойство заключено в квадратные скобки ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="814cd-124">The list is usually a list of properties, with each property enclosed inside square brackets (\[ \]) .</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="814cd-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="814cd-125">Remarks</span></span>

<span data-ttu-id="814cd-126">Установщик рассчитывает виртуальный адрес каждой функции, которая импортируется из всех библиотек DLL, а вычисленный виртуальный адрес сохраняется в таблице адресов импорта импортируемого образа (IAT).</span><span class="sxs-lookup"><span data-stu-id="814cd-126">The installer computes the virtual address of each function that is imported from all DLLs, and the computed virtual address is then saved in the importing image's Import Address Table (IAT).</span></span>

<span data-ttu-id="814cd-127">Эта таблица упоминается при выполнении [действия BindImage](bindimage-action.md) .</span><span class="sxs-lookup"><span data-stu-id="814cd-127">This table is referred to when the [BindImage action](bindimage-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="814cd-128">Проверка</span><span class="sxs-lookup"><span data-stu-id="814cd-128">Validation</span></span>

<dl>

[<span data-ttu-id="814cd-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="814cd-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="814cd-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="814cd-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="814cd-131">ICE32</span><span class="sxs-lookup"><span data-stu-id="814cd-131">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="814cd-132">ICE46</span><span class="sxs-lookup"><span data-stu-id="814cd-132">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="814cd-133">ICE76</span><span class="sxs-lookup"><span data-stu-id="814cd-133">ICE76</span></span>](ice76.md)  
</dl>

 

 



