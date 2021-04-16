---
description: Таблица Креатефолдер содержит ссылки на папки, которые необходимо явно создать для конкретного компонента.
ms.assetid: b17b470b-6971-4124-8ec3-73914fdea95f
title: Таблица Креатефолдер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc286b32b48e0db9e5b991ab10af663c51538bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265656"
---
# <a name="createfolder-table"></a><span data-ttu-id="0ac9a-103">Таблица Креатефолдер</span><span class="sxs-lookup"><span data-stu-id="0ac9a-103">CreateFolder Table</span></span>

<span data-ttu-id="0ac9a-104">Таблица Креатефолдер содержит ссылки на папки, которые необходимо явно создать для конкретного компонента.</span><span class="sxs-lookup"><span data-stu-id="0ac9a-104">The CreateFolder table contains references to folders that need to be created explicitly for a particular component.</span></span>

<span data-ttu-id="0ac9a-105">Таблица Креатефолдер содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="0ac9a-105">The CreateFolder table has the following columns.</span></span>



| <span data-ttu-id="0ac9a-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="0ac9a-106">Column</span></span>      | <span data-ttu-id="0ac9a-107">Type</span><span class="sxs-lookup"><span data-stu-id="0ac9a-107">Type</span></span>                         | <span data-ttu-id="0ac9a-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="0ac9a-108">Key</span></span> | <span data-ttu-id="0ac9a-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="0ac9a-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="0ac9a-110">Каталог\_</span><span class="sxs-lookup"><span data-stu-id="0ac9a-110">Directory\_</span></span> | [<span data-ttu-id="0ac9a-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0ac9a-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="0ac9a-112">Да</span><span class="sxs-lookup"><span data-stu-id="0ac9a-112">Y</span></span>   | <span data-ttu-id="0ac9a-113">Нет</span><span class="sxs-lookup"><span data-stu-id="0ac9a-113">N</span></span>        |
| <span data-ttu-id="0ac9a-114">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="0ac9a-114">Component\_</span></span> | [<span data-ttu-id="0ac9a-115">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0ac9a-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="0ac9a-116">Да</span><span class="sxs-lookup"><span data-stu-id="0ac9a-116">Y</span></span>   | <span data-ttu-id="0ac9a-117">Нет</span><span class="sxs-lookup"><span data-stu-id="0ac9a-117">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="0ac9a-118">Столбцы</span><span class="sxs-lookup"><span data-stu-id="0ac9a-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="0ac9a-119"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Каталоги\_</span><span class="sxs-lookup"><span data-stu-id="0ac9a-119"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="0ac9a-120">Внешний ключ в первом столбце [таблицы Directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="0ac9a-120">External key into the first column of the [Directory table](directory-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ac9a-121"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="0ac9a-121"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="0ac9a-122">Внешний ключ в первый столбец [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="0ac9a-122">External key into the first column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ac9a-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ac9a-123">Remarks</span></span>

<span data-ttu-id="0ac9a-124">Папки в этой таблице создаются при установке компонента.</span><span class="sxs-lookup"><span data-stu-id="0ac9a-124">The folders in this table are created when the component is installed.</span></span> <span data-ttu-id="0ac9a-125">Предпринята попытка удалить эти папки только в том случае, если компонент удален или перемещен в исходный код запуска.</span><span class="sxs-lookup"><span data-stu-id="0ac9a-125">An attempt is made to remove these folders only when the component is uninstalled or moved to run-from-source.</span></span> <span data-ttu-id="0ac9a-126">Автоматическое удаление не запускается, если папки становятся пустыми.</span><span class="sxs-lookup"><span data-stu-id="0ac9a-126">No automatic removal is triggered if the folders become empty.</span></span> <span data-ttu-id="0ac9a-127">В отличие от этого, папки, созданные установщиком, но не перечисленные в этой таблице, удаляются, когда они становятся пустыми.</span><span class="sxs-lookup"><span data-stu-id="0ac9a-127">In contrast, folders created by the installer but not listed in this table are removed when they become empty.</span></span>

<span data-ttu-id="0ac9a-128">Поскольку папки, созданные установщиком, удаляются, когда они становятся пустыми, необходимо создать запись в таблице Креатефолдер, чтобы установить компонент, состоящий из пустой папки.</span><span class="sxs-lookup"><span data-stu-id="0ac9a-128">Because folders created by the installer are deleted when they become empty, you must author an entry into the CreateFolder table to install a component that consists of an empty folder.</span></span>

<span data-ttu-id="0ac9a-129">Эта таблица упоминается при вызове действия [креатефолдерс](createfolders-action.md) или [ремовефолдерс](removefolders-action.md) .</span><span class="sxs-lookup"><span data-stu-id="0ac9a-129">This table is referred to when the [CreateFolders](createfolders-action.md) action or the [RemoveFolders](removefolders-action.md) action is called.</span></span>

<span data-ttu-id="0ac9a-130">Сведения о том, как защитить папку, см. в [таблице мсилоккпермиссионсекс](msilockpermissionsex-table.md) и таблице [локкпермиссионс](lockpermissions-table.md).</span><span class="sxs-lookup"><span data-stu-id="0ac9a-130">For information on how to secure a folder see the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) and [LockPermissions Table](lockpermissions-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="0ac9a-131">Проверка</span><span class="sxs-lookup"><span data-stu-id="0ac9a-131">Validation</span></span>

<dl>

[<span data-ttu-id="0ac9a-132">ICE03</span><span class="sxs-lookup"><span data-stu-id="0ac9a-132">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="0ac9a-133">ICE06</span><span class="sxs-lookup"><span data-stu-id="0ac9a-133">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="0ac9a-134">ICE18</span><span class="sxs-lookup"><span data-stu-id="0ac9a-134">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="0ac9a-135">ICE32</span><span class="sxs-lookup"><span data-stu-id="0ac9a-135">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="0ac9a-136">ICE55</span><span class="sxs-lookup"><span data-stu-id="0ac9a-136">ICE55</span></span>](ice55.md)  
</dl>

 

 



