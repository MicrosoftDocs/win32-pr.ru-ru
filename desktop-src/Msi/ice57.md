---
description: ICE57 проверяет, что отдельные компоненты не сочетают данные для каждого компьютера и пользователя. Это настраиваемое действие ICE проверяет записи реестра, файлы, пути к ключам каталогов и необъявленные ярлыки.
ms.assetid: 3c82efa7-9cf3-4bcd-8ec4-b81d1d7aa0a6
title: ICE57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a59d609e5d7de0011666be0b5cc5e76417d8e67d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265830"
---
# <a name="ice57"></a><span data-ttu-id="a5003-104">ICE57</span><span class="sxs-lookup"><span data-stu-id="a5003-104">ICE57</span></span>

<span data-ttu-id="a5003-105">ICE57 проверяет, что отдельные компоненты не сочетают данные для каждого компьютера и пользователя.</span><span class="sxs-lookup"><span data-stu-id="a5003-105">ICE57 validates that individual components do not mix per-machine and per-user data.</span></span> <span data-ttu-id="a5003-106">Это настраиваемое действие ICE проверяет записи реестра, файлы, пути к ключам каталогов и необъявленные ярлыки.</span><span class="sxs-lookup"><span data-stu-id="a5003-106">This ICE custom action checks registry entries, files, directory key paths, and non-advertised shortcuts.</span></span>

<span data-ttu-id="a5003-107">Смешивание данных на уровне пользователя и на компьютере в одном компоненте может привести к частичной установке компонента только для некоторых пользователей в многопользовательской среде.</span><span class="sxs-lookup"><span data-stu-id="a5003-107">Mixing per-user and per-machine data in the same component could result in only partial installation of the component for some users in a multi-user environment.</span></span>

<span data-ttu-id="a5003-108">См. свойство [**ALLUSERS**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="a5003-108">See the [**ALLUSERS**](allusers.md) property.</span></span>

## <a name="result"></a><span data-ttu-id="a5003-109">Результат</span><span class="sxs-lookup"><span data-stu-id="a5003-109">Result</span></span>

<span data-ttu-id="a5003-110">ICE57 отправляет сообщение об ошибке, если обнаруживает любой компонент, содержащий записи реестра для компьютера и пользователя, файлы, пути к ключам каталогов или необъявленные ярлыки.</span><span class="sxs-lookup"><span data-stu-id="a5003-110">ICE57 posts an error if it finds any component that contains both a per-machine and per-user registry entries, files, directory key paths, or non-advertised shortcuts.</span></span>

## <a name="example"></a><span data-ttu-id="a5003-111">Пример</span><span class="sxs-lookup"><span data-stu-id="a5003-111">Example</span></span>

<span data-ttu-id="a5003-112">ICE57reports следующие ошибки для показанного примера.</span><span class="sxs-lookup"><span data-stu-id="a5003-112">ICE57reports the following errors for the example shown.</span></span>

``` syntax
Component 'Component1' has both per-user and per-machine 
    data with a per-machine KeyPath. 
 
WARNING: Component 'Component2' has both per-user and 
    per-machine data with an HKCU Registry KeyPath. 
 
Component 'Component3' has a registry entry that 
    can be either per-user or per-machine and a per-machine KeyPath. 
 
Component 'Component4' has both per-user data and 
    a keypath that can be either per-user or per-machine.
```

<span data-ttu-id="a5003-113">[Таблица Component](component-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="a5003-113">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="a5003-114">Компонент</span><span class="sxs-lookup"><span data-stu-id="a5003-114">Component</span></span>  | <span data-ttu-id="a5003-115">Каталог</span><span class="sxs-lookup"><span data-stu-id="a5003-115">Directory</span></span>  | <span data-ttu-id="a5003-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a5003-116">Attributes</span></span> | <span data-ttu-id="a5003-117">Путь</span><span class="sxs-lookup"><span data-stu-id="a5003-117">KeyPath</span></span> |
|------------|------------|------------|---------|
| <span data-ttu-id="a5003-118">Component1</span><span class="sxs-lookup"><span data-stu-id="a5003-118">Component1</span></span> | <span data-ttu-id="a5003-119">Каталог а</span><span class="sxs-lookup"><span data-stu-id="a5003-119">DirectoryA</span></span> | <span data-ttu-id="a5003-120">0</span><span class="sxs-lookup"><span data-stu-id="a5003-120">0</span></span>          | <span data-ttu-id="a5003-121">Файл а</span><span class="sxs-lookup"><span data-stu-id="a5003-121">FileA</span></span>   |
| <span data-ttu-id="a5003-122">Component2</span><span class="sxs-lookup"><span data-stu-id="a5003-122">Component2</span></span> | <span data-ttu-id="a5003-123">Каталог а</span><span class="sxs-lookup"><span data-stu-id="a5003-123">DirectoryA</span></span> | <span data-ttu-id="a5003-124">4</span><span class="sxs-lookup"><span data-stu-id="a5003-124">4</span></span>          | <span data-ttu-id="a5003-125">регкэйб</span><span class="sxs-lookup"><span data-stu-id="a5003-125">RegKeyB</span></span> |
| <span data-ttu-id="a5003-126">Component3</span><span class="sxs-lookup"><span data-stu-id="a5003-126">Component3</span></span> | <span data-ttu-id="a5003-127">Каталог а</span><span class="sxs-lookup"><span data-stu-id="a5003-127">DirectoryA</span></span> | <span data-ttu-id="a5003-128">0</span><span class="sxs-lookup"><span data-stu-id="a5003-128">0</span></span>          | <span data-ttu-id="a5003-129">филек</span><span class="sxs-lookup"><span data-stu-id="a5003-129">FileC</span></span>   |
| <span data-ttu-id="a5003-130">Component4</span><span class="sxs-lookup"><span data-stu-id="a5003-130">Component4</span></span> | <span data-ttu-id="a5003-131">Каталог а</span><span class="sxs-lookup"><span data-stu-id="a5003-131">DirectoryA</span></span> | <span data-ttu-id="a5003-132">4</span><span class="sxs-lookup"><span data-stu-id="a5003-132">4</span></span>          | <span data-ttu-id="a5003-133">регкэйд</span><span class="sxs-lookup"><span data-stu-id="a5003-133">RegKeyD</span></span> |



 

<span data-ttu-id="a5003-134">[Таблица реестра](registry-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="a5003-134">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="a5003-135">Реестр</span><span class="sxs-lookup"><span data-stu-id="a5003-135">Registry</span></span> | <span data-ttu-id="a5003-136">Root</span><span class="sxs-lookup"><span data-stu-id="a5003-136">Root</span></span> | <span data-ttu-id="a5003-137">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="a5003-137">Component\_</span></span> |
|----------|------|-------------|
| <span data-ttu-id="a5003-138">регкэйа</span><span class="sxs-lookup"><span data-stu-id="a5003-138">RegKeyA</span></span>  | <span data-ttu-id="a5003-139">1</span><span class="sxs-lookup"><span data-stu-id="a5003-139">1</span></span>    | <span data-ttu-id="a5003-140">Component1</span><span class="sxs-lookup"><span data-stu-id="a5003-140">Component1</span></span>  |
| <span data-ttu-id="a5003-141">регкэйб</span><span class="sxs-lookup"><span data-stu-id="a5003-141">RegKeyB</span></span>  | <span data-ttu-id="a5003-142">1</span><span class="sxs-lookup"><span data-stu-id="a5003-142">1</span></span>    | <span data-ttu-id="a5003-143">Component2</span><span class="sxs-lookup"><span data-stu-id="a5003-143">Component2</span></span>  |
| <span data-ttu-id="a5003-144">регкэйк</span><span class="sxs-lookup"><span data-stu-id="a5003-144">RegKeyC</span></span>  | <span data-ttu-id="a5003-145">-1</span><span class="sxs-lookup"><span data-stu-id="a5003-145">-1</span></span>   | <span data-ttu-id="a5003-146">Component3</span><span class="sxs-lookup"><span data-stu-id="a5003-146">Component3</span></span>  |
| <span data-ttu-id="a5003-147">регкэйд</span><span class="sxs-lookup"><span data-stu-id="a5003-147">RegKeyD</span></span>  | <span data-ttu-id="a5003-148">-1</span><span class="sxs-lookup"><span data-stu-id="a5003-148">-1</span></span>   | <span data-ttu-id="a5003-149">Component4</span><span class="sxs-lookup"><span data-stu-id="a5003-149">Component4</span></span>  |



 

<span data-ttu-id="a5003-150">[Таблица файлов](file-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="a5003-150">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="a5003-151">Файл</span><span class="sxs-lookup"><span data-stu-id="a5003-151">File</span></span>  | <span data-ttu-id="a5003-152">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="a5003-152">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="a5003-153">Файл а</span><span class="sxs-lookup"><span data-stu-id="a5003-153">FileA</span></span> | <span data-ttu-id="a5003-154">Component1</span><span class="sxs-lookup"><span data-stu-id="a5003-154">Component1</span></span>  |
| <span data-ttu-id="a5003-155">филеб</span><span class="sxs-lookup"><span data-stu-id="a5003-155">FileB</span></span> | <span data-ttu-id="a5003-156">Component2</span><span class="sxs-lookup"><span data-stu-id="a5003-156">Component2</span></span>  |
| <span data-ttu-id="a5003-157">филек</span><span class="sxs-lookup"><span data-stu-id="a5003-157">FileC</span></span> | <span data-ttu-id="a5003-158">Component3</span><span class="sxs-lookup"><span data-stu-id="a5003-158">Component3</span></span>  |
| <span data-ttu-id="a5003-159">Подан</span><span class="sxs-lookup"><span data-stu-id="a5003-159">FileD</span></span> | <span data-ttu-id="a5003-160">Component4</span><span class="sxs-lookup"><span data-stu-id="a5003-160">Component4</span></span>  |



 

[<span data-ttu-id="a5003-161">Таблица каталога</span><span class="sxs-lookup"><span data-stu-id="a5003-161">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="a5003-162">Каталог</span><span class="sxs-lookup"><span data-stu-id="a5003-162">Directory</span></span>  | <span data-ttu-id="a5003-163">\_Родительский каталог</span><span class="sxs-lookup"><span data-stu-id="a5003-163">Directory\_Parent</span></span> | <span data-ttu-id="a5003-164">дефаултдир</span><span class="sxs-lookup"><span data-stu-id="a5003-164">DefaultDir</span></span> |
|------------|-------------------|------------|
| <span data-ttu-id="a5003-165">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="a5003-165">TARGETDIR</span></span>  |                   | <span data-ttu-id="a5003-166">SourceDir</span><span class="sxs-lookup"><span data-stu-id="a5003-166">SourceDir</span></span>  |
| <span data-ttu-id="a5003-167">Каталог а</span><span class="sxs-lookup"><span data-stu-id="a5003-167">DirectoryA</span></span> | <span data-ttu-id="a5003-168">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="a5003-168">TARGETDIR</span></span>         | <span data-ttu-id="a5003-169">Каталог а</span><span class="sxs-lookup"><span data-stu-id="a5003-169">DirectoryA</span></span> |



 

<span data-ttu-id="a5003-170">Чтобы устранить ошибки, реорганизуйте приложение таким способом, чтобы каждый компонент содержал только ресурсы для отдельных пользователей или компьютеров, а не оба.</span><span class="sxs-lookup"><span data-stu-id="a5003-170">To fix the errors, reorganize the application such that each component contains only per-user or per-machine resources, and not both.</span></span>

<span data-ttu-id="a5003-171">Первое сообщение об ошибке публикуется, так как Component1 содержит файл a (для компьютера) и раздел реестра HKCU Регкэйа (для каждого пользователя).</span><span class="sxs-lookup"><span data-stu-id="a5003-171">The first error message is posted because Component1 contains FileA (per-machine) and the HKCU registry key RegKeyA (per user).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5003-172">См. также</span><span class="sxs-lookup"><span data-stu-id="a5003-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5003-173">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="a5003-173">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



