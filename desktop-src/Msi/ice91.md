---
description: ICE91 отправляет предупреждение, если файл, ini-файл или файл ярлыка установлен в каталог только для пользователя.
ms.assetid: 1834d841-b1d9-4646-8057-a41dd88310b6
title: ICE91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f5723369c21894817dacbc1755430a31f17199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651058"
---
# <a name="ice91"></a><span data-ttu-id="5ae1c-103">ICE91</span><span class="sxs-lookup"><span data-stu-id="5ae1c-103">ICE91</span></span>

<span data-ttu-id="5ae1c-104">ICE91 отправляет предупреждение, если файл, ini-файл или файл ярлыка установлен в каталог только для пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ae1c-104">ICE91 posts a warning if a file, .ini file, or shortcut file is installed into a per-user only directory.</span></span> <span data-ttu-id="5ae1c-105">Эти предупреждения являются безобидными, если пакет используется только для установки в [контексте установки](installation-context.md) "на пользователя" и никогда не используется для установки на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5ae1c-105">These warnings are harmless if the package is only used for installation in the per-user [installation context](installation-context.md) and never used for per-machine installations.</span></span>

<span data-ttu-id="5ae1c-106">Файлы, ini-файлы или ярлыки в каталогах только для отдельных пользователей устанавливаются в профиль конкретного пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ae1c-106">Files, .ini files, or shortcuts in per-user only directories are installed into a particular user's profile.</span></span> <span data-ttu-id="5ae1c-107">Даже если пользователь задает свойство [**ALLUSERS**](allusers.md) для установки на компьютере, файлы, ini-файлы или ярлыки в каталогах только для отдельных пользователей, не копируются в профиль "все пользователи" и недоступны для других пользователей.</span><span class="sxs-lookup"><span data-stu-id="5ae1c-107">Even if the user sets the [**ALLUSERS**](allusers.md) property for a per-machine installations, files, .ini files, or shortcuts in per-user only directories are not copied in to the "All Users" profile and are not available to other users.</span></span> <span data-ttu-id="5ae1c-108">Каталоги только для пользователей не зависят от свойства **ALLUSERS** .</span><span class="sxs-lookup"><span data-stu-id="5ae1c-108">The per-user only directories do not vary with the **ALLUSERS** property.</span></span> <span data-ttu-id="5ae1c-109">Ниже приведен список каталогов только для пользователей.</span><span class="sxs-lookup"><span data-stu-id="5ae1c-109">The following is a list of the per-user only directories:</span></span>

-   <span data-ttu-id="5ae1c-110">аппдатафолдер</span><span class="sxs-lookup"><span data-stu-id="5ae1c-110">AppDataFolder</span></span>
-   <span data-ttu-id="5ae1c-111">фаворитесфолдер</span><span class="sxs-lookup"><span data-stu-id="5ae1c-111">FavoritesFolder</span></span>
-   <span data-ttu-id="5ae1c-112">несудфолдер</span><span class="sxs-lookup"><span data-stu-id="5ae1c-112">NetHoodFolder</span></span>
-   <span data-ttu-id="5ae1c-113">PersonalFolder</span><span class="sxs-lookup"><span data-stu-id="5ae1c-113">PersonalFolder</span></span>
-   <span data-ttu-id="5ae1c-114">принсудфолдер</span><span class="sxs-lookup"><span data-stu-id="5ae1c-114">PrintHoodFolder</span></span>
-   <span data-ttu-id="5ae1c-115">рецентфолдер</span><span class="sxs-lookup"><span data-stu-id="5ae1c-115">RecentFolder</span></span>
-   <span data-ttu-id="5ae1c-116">сендтофолдер</span><span class="sxs-lookup"><span data-stu-id="5ae1c-116">SendToFolder</span></span>
-   <span data-ttu-id="5ae1c-117">мипиктуресфолдер</span><span class="sxs-lookup"><span data-stu-id="5ae1c-117">MyPicturesFolder</span></span>
-   <span data-ttu-id="5ae1c-118">локалаппдатафолдер</span><span class="sxs-lookup"><span data-stu-id="5ae1c-118">LocalAppDataFolder</span></span>

## <a name="result"></a><span data-ttu-id="5ae1c-119">Результат</span><span class="sxs-lookup"><span data-stu-id="5ae1c-119">Result</span></span>

<span data-ttu-id="5ae1c-120">ICE91 отправляет следующие предупреждения.</span><span class="sxs-lookup"><span data-stu-id="5ae1c-120">ICE91 posts the following warnings.</span></span>



| <span data-ttu-id="5ae1c-121">Предупреждение ICE91</span><span class="sxs-lookup"><span data-stu-id="5ae1c-121">ICE91 warning</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="5ae1c-122">Описание</span><span class="sxs-lookup"><span data-stu-id="5ae1c-122">Description</span></span>                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae1c-123">Файл " \[ 1 \] " будет установлен в каталог "2" для каждого пользователя \[ \] , который не зависит от значения [**ALLUSERS**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="5ae1c-123">The file '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="5ae1c-124">Этот файл не будет копироваться в профиль каждого пользователя, даже если требуется установка на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5ae1c-124">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span>     | <span data-ttu-id="5ae1c-125">Файл устанавливается в каталог только для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ae1c-125">The file is installed into a per-user only directory.</span></span> <span data-ttu-id="5ae1c-126">Он не устанавливается в профиль каждого пользователя во время установки на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5ae1c-126">It is not installed into each user's profile during a per-machine installation.</span></span>      |
| <span data-ttu-id="5ae1c-127">Инифиле " \[ 1 \] " будет установлен в каталог "2" для каждого пользователя \[ \] , который не зависит от значения [**ALLUSERS**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="5ae1c-127">The IniFile '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="5ae1c-128">Этот файл не будет копироваться в профиль каждого пользователя, даже если требуется установка на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5ae1c-128">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span>  | <span data-ttu-id="5ae1c-129">INI-файл устанавливается в каталог только для отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="5ae1c-129">The .ini file is installed into a per-user only directory.</span></span> <span data-ttu-id="5ae1c-130">Он не устанавливается в профиль каждого пользователя во время установки на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5ae1c-130">It is not installed into each user's profile during a per-machine installation.</span></span> |
| <span data-ttu-id="5ae1c-131">Ярлык " \[ 1 \] " будет установлен в каталоге " \[ 2" на пользователя \] , который не зависит от значения [**ALLUSERS**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="5ae1c-131">The shortcut '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="5ae1c-132">Этот файл не будет копироваться в профиль каждого пользователя, даже если требуется установка на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5ae1c-132">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span> | <span data-ttu-id="5ae1c-133">Ярлык устанавливается в каталог только для отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="5ae1c-133">The shortcut is installed into a per-user only directory.</span></span> <span data-ttu-id="5ae1c-134">Он не устанавливается в профиль каждого пользователя во время установки на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5ae1c-134">It is not installed into each user's profile during a per-machine installation.</span></span>  |



 

## <a name="example"></a><span data-ttu-id="5ae1c-135">Пример</span><span class="sxs-lookup"><span data-stu-id="5ae1c-135">Example</span></span>

<span data-ttu-id="5ae1c-136">ICE91 сообщает о следующих предупреждениях для примера:</span><span class="sxs-lookup"><span data-stu-id="5ae1c-136">ICE91 reports the following warnings for the example:</span></span>

``` syntax
The file 'File1' will be installed to the per user directory 'MyPicturesFolder' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The IniFile 'IniFile1' will be installed to the per user directory 'MyIniDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The shortcut 'Shortcut1' will be installed to the per user directory 'MyShortcutDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.
```

<span data-ttu-id="5ae1c-137">[Таблица файлов](file-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="5ae1c-137">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="5ae1c-138">Файл</span><span class="sxs-lookup"><span data-stu-id="5ae1c-138">File</span></span>  | <span data-ttu-id="5ae1c-139">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="5ae1c-139">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="5ae1c-140">Файл1</span><span class="sxs-lookup"><span data-stu-id="5ae1c-140">File1</span></span> | <span data-ttu-id="5ae1c-141">C1</span><span class="sxs-lookup"><span data-stu-id="5ae1c-141">C1</span></span>          |



 

<span data-ttu-id="5ae1c-142">[Таблица Component](component-table.md) (частичная) (частичная) (частичная) (частичная)</span><span class="sxs-lookup"><span data-stu-id="5ae1c-142">[Component Table](component-table.md) (partial) (partial) (partial) (partial)</span></span>



| <span data-ttu-id="5ae1c-143">Компонент</span><span class="sxs-lookup"><span data-stu-id="5ae1c-143">Component</span></span> | <span data-ttu-id="5ae1c-144">Каталог\_</span><span class="sxs-lookup"><span data-stu-id="5ae1c-144">Directory\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="5ae1c-145">C1</span><span class="sxs-lookup"><span data-stu-id="5ae1c-145">C1</span></span>        | <span data-ttu-id="5ae1c-146">MyDir</span><span class="sxs-lookup"><span data-stu-id="5ae1c-146">MyDir</span></span>       |



 

[<span data-ttu-id="5ae1c-147">Таблица Инифиле</span><span class="sxs-lookup"><span data-stu-id="5ae1c-147">IniFile Table</span></span>](inifile-table.md)



| <span data-ttu-id="5ae1c-148">инифиле</span><span class="sxs-lookup"><span data-stu-id="5ae1c-148">IniFile</span></span>  | <span data-ttu-id="5ae1c-149">дирпроперти</span><span class="sxs-lookup"><span data-stu-id="5ae1c-149">DirProperty</span></span> |
|----------|-------------|
| <span data-ttu-id="5ae1c-150">IniFile1</span><span class="sxs-lookup"><span data-stu-id="5ae1c-150">IniFile1</span></span> | <span data-ttu-id="5ae1c-151">минидир</span><span class="sxs-lookup"><span data-stu-id="5ae1c-151">MyIniDir</span></span>    |



 

[<span data-ttu-id="5ae1c-152">Таблица ярлыков</span><span class="sxs-lookup"><span data-stu-id="5ae1c-152">Shortcut Table</span></span>](shortcut-table.md)



| <span data-ttu-id="5ae1c-153">Сочетание клавиш</span><span class="sxs-lookup"><span data-stu-id="5ae1c-153">Shortcut</span></span>  | <span data-ttu-id="5ae1c-154">Каталог\_</span><span class="sxs-lookup"><span data-stu-id="5ae1c-154">Directory\_</span></span>   |
|-----------|---------------|
| <span data-ttu-id="5ae1c-155">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="5ae1c-155">Shortcut1</span></span> | <span data-ttu-id="5ae1c-156">мишорткутдир</span><span class="sxs-lookup"><span data-stu-id="5ae1c-156">MyShortcutDir</span></span> |



 

[<span data-ttu-id="5ae1c-157">Таблица каталога</span><span class="sxs-lookup"><span data-stu-id="5ae1c-157">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="5ae1c-158">Каталог</span><span class="sxs-lookup"><span data-stu-id="5ae1c-158">Directory</span></span>     | <span data-ttu-id="5ae1c-159">\_Родительский каталог</span><span class="sxs-lookup"><span data-stu-id="5ae1c-159">Directory\_Parent</span></span>  |
|---------------|--------------------|
| <span data-ttu-id="5ae1c-160">MyDir</span><span class="sxs-lookup"><span data-stu-id="5ae1c-160">MyDir</span></span>         | <span data-ttu-id="5ae1c-161">фаворитесфолдер</span><span class="sxs-lookup"><span data-stu-id="5ae1c-161">FavoritesFolder</span></span>    |
| <span data-ttu-id="5ae1c-162">минидир</span><span class="sxs-lookup"><span data-stu-id="5ae1c-162">MyIniDir</span></span>      | <span data-ttu-id="5ae1c-163">локалаппдатафолдер</span><span class="sxs-lookup"><span data-stu-id="5ae1c-163">LocalAppDataFolder</span></span> |
| <span data-ttu-id="5ae1c-164">мишорткутдир</span><span class="sxs-lookup"><span data-stu-id="5ae1c-164">MyShortcutDir</span></span> | <span data-ttu-id="5ae1c-165">PersonalFolder</span><span class="sxs-lookup"><span data-stu-id="5ae1c-165">PersonalFolder</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="5ae1c-166">См. также</span><span class="sxs-lookup"><span data-stu-id="5ae1c-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ae1c-167">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="5ae1c-167">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



