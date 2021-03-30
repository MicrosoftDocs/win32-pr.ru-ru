---
description: ICE43 проверяет, что ярлыки, не ссылающиеся на компонент в качестве их целевых (необъявленных ярлыков), находятся в компонентах, где в качестве пути к ключу используется запись реестра HKCU.
ms.assetid: 7e58e303-e512-4707-a0bf-2095ec8ec502
title: ICE43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c9df4a6051557fca3e185f56ca3ad7978c2c0b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156715"
---
# <a name="ice43"></a><span data-ttu-id="e1c90-103">ICE43</span><span class="sxs-lookup"><span data-stu-id="e1c90-103">ICE43</span></span>

<span data-ttu-id="e1c90-104">ICE43 проверяет, что ярлыки, не ссылающиеся на компонент в качестве их целевых (необъявленных ярлыков), находятся в компонентах, где в качестве пути к ключу используется запись реестра HKCU.</span><span class="sxs-lookup"><span data-stu-id="e1c90-104">ICE43 validates that shortcuts that do not reference a feature as their Target (non-advertised shortcuts) are in components having a HKCU registry entry as their key path.</span></span>

## <a name="result"></a><span data-ttu-id="e1c90-105">Результат</span><span class="sxs-lookup"><span data-stu-id="e1c90-105">Result</span></span>

<span data-ttu-id="e1c90-106">ICE43 отправляет сообщение об ошибке, если необъявленный ярлык находится в компоненте, у которого нет записи реестра HKCU в качестве пути к ключу.</span><span class="sxs-lookup"><span data-stu-id="e1c90-106">ICE43 posts an error message if a non-advertised shortcut is in a component that does not have a HKCU registry entry as its key path.</span></span>

## <a name="example"></a><span data-ttu-id="e1c90-107">Пример</span><span class="sxs-lookup"><span data-stu-id="e1c90-107">Example</span></span>

<span data-ttu-id="e1c90-108">ICE43 сообщит о следующих ошибках в приведенном примере.</span><span class="sxs-lookup"><span data-stu-id="e1c90-108">ICE43 would report the following errors for the example shown.</span></span>



| <span data-ttu-id="e1c90-109">ICE43, ошибка</span><span class="sxs-lookup"><span data-stu-id="e1c90-109">ICE43 error</span></span>                                                                                                                             | <span data-ttu-id="e1c90-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e1c90-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1c90-111">Для компонента Component1 имеются необъявленные ярлыки.</span><span class="sxs-lookup"><span data-stu-id="e1c90-111">Component Component1 has non-advertised shortcuts.</span></span> <span data-ttu-id="e1c90-112">Он должен использовать раздел реестра HKCU в качестве ключевого пути, а не файл.</span><span class="sxs-lookup"><span data-stu-id="e1c90-112">It must use a registry key under HKCU as its KeyPath, not a file.</span></span>                    | <span data-ttu-id="e1c90-113">Столбец Attributes объекта Component1 имеет значение 0, означающее, что компонент использует файл в качестве ключевого пути.</span><span class="sxs-lookup"><span data-stu-id="e1c90-113">The attributes column of Component1 is 0, meaning that the component uses a file as its KeyPath.</span></span> <span data-ttu-id="e1c90-114">В результате необъявленные ярлыки в этом компоненте будут установлены только для первого пользователя на компьютере.</span><span class="sxs-lookup"><span data-stu-id="e1c90-114">This causes non-advertised shortcuts in this component to be installed for the first user on the computer ONLY.</span></span> <span data-ttu-id="e1c90-115">Пользователи, которые устанавливают этот компонент, не видят ярлыки, так как компонент отображается установщиком, как уже существует на компьютере.</span><span class="sxs-lookup"><span data-stu-id="e1c90-115">Users who install the component later do not see the shortcuts because the component appear to the installer as already existing on the computer.</span></span> <span data-ttu-id="e1c90-116">Чтобы устранить эту ошибку, установите бит Регистрикэйпас атрибутов, чтобы переключить компонент на запись реестра, а затем измените значение ключевого слова на допустимую запись в таблице реестра.</span><span class="sxs-lookup"><span data-stu-id="e1c90-116">To fix this error, set the RegistryKeyPath bit of the attributes to switch the Component to a Registry entry, then change the KeyPath value to a valid entry in the Registry table.</span></span><br/> |
| <span data-ttu-id="e1c90-117">Для компонента Component2 имеются необъявленные ярлыки.</span><span class="sxs-lookup"><span data-stu-id="e1c90-117">Component Component2 has non-advertised shortcuts.</span></span> <span data-ttu-id="e1c90-118">Он должен использовать раздел реестра в разделе HKCU в качестве ключевого пути.</span><span class="sxs-lookup"><span data-stu-id="e1c90-118">It must use a registry key under HKCU as its KeyPath.</span></span> <span data-ttu-id="e1c90-119">В настоящее время ключевой путь имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="e1c90-119">The KeyPath is currently null.</span></span> | <span data-ttu-id="e1c90-120">Столбец Attributes настроен для использования реестра, но ключевой путь имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="e1c90-120">The Attributes column is set to use the registry, but the KeyPath is null.</span></span> <span data-ttu-id="e1c90-121">Ключевой путь должен ссылаться на запись в таблице реестра.</span><span class="sxs-lookup"><span data-stu-id="e1c90-121">The KeyPath must refer to an entry in the Registry Table.</span></span> <span data-ttu-id="e1c90-122">Чтобы устранить эту ошибку, измените значение ключевого слова на допустимую запись в таблице реестра.</span><span class="sxs-lookup"><span data-stu-id="e1c90-122">To fix this error, change the KeyPath value to a valid entry in the Registry table.</span></span><br/>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="e1c90-123">Для компонента Component3 имеются необъявленные ярлыки.</span><span class="sxs-lookup"><span data-stu-id="e1c90-123">Component Component3 has non-advertised shortcuts.</span></span> <span data-ttu-id="e1c90-124">Его ключевой раздел реестра должен находиться в разделе HKCU.</span><span class="sxs-lookup"><span data-stu-id="e1c90-124">Its KeyPath registry key must fall under HKCU.</span></span>                                       | <span data-ttu-id="e1c90-125">Столбец атрибуты настроен на использование реестра, но указанный параметр реестра не находится в разделе HKCU.</span><span class="sxs-lookup"><span data-stu-id="e1c90-125">The Attributes column is set to use the registry, but the referenced registry entry is not under HKCU.</span></span> <span data-ttu-id="e1c90-126">Чтобы устранить эту ошибку, переключитесь на другую запись реестра в качестве ключевого слова для этого компонента или измените значение корневого параметра записи реестра на-1 или 1.</span><span class="sxs-lookup"><span data-stu-id="e1c90-126">To fix this error, either switch to a different registry entry as the KeyPath for this component, or change the Root value of the Registry entry to either -1 or 1.</span></span><br/>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="e1c90-127">Запись реестра ключевого слова для компонента Component4 не существует.</span><span class="sxs-lookup"><span data-stu-id="e1c90-127">The KeyPath registry entry for component Component4 does not exist.</span></span>                                                                     | <span data-ttu-id="e1c90-128">Запись реестра, на которую ссылается ключевой столбец компонента, отсутствует в таблице реестра.</span><span class="sxs-lookup"><span data-stu-id="e1c90-128">The Registry entry referenced in the KeyPath column of the component is not in the Registry Table.</span></span> <span data-ttu-id="e1c90-129">Чтобы устранить эту ошибку, создайте запись.</span><span class="sxs-lookup"><span data-stu-id="e1c90-129">To fix this error, create an entry.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="e1c90-130">Запись реестра Reg5 задается в качестве ключевого пути для компонента Component5, но эта запись реестра не принадлежит Component5.</span><span class="sxs-lookup"><span data-stu-id="e1c90-130">The Registry Entry Reg5 is set as the KeyPath for component Component5, but that registry entry does not belong to Component5.</span></span>          | <span data-ttu-id="e1c90-131">Имеется запись реестра, на которую ссылается ключевой столбец компонента, который находится в дереве HKCU, но столбец компонента записи реестра \_ не ссылается на тот же компонент, который был указан в качестве ключевого пути.</span><span class="sxs-lookup"><span data-stu-id="e1c90-131">There is a Registry entry referenced in the KeyPath column of the component that lies under the HKCU tree, but the registry entry's Component\_ column does not refer back to the same component that listed it as the KeyPath.</span></span> <span data-ttu-id="e1c90-132">Это означает, что запись реестра, используемая в качестве ключевого параметра компонента, создается только в том случае, если был установлен какой-либо другой компонент.</span><span class="sxs-lookup"><span data-stu-id="e1c90-132">This means that the registry entry used as the KeyPath of the component is only created if some other component was installed.</span></span> <span data-ttu-id="e1c90-133">Чтобы устранить эту ошибку, измените значение ключевого слова так, чтобы оно ссылалось на запись реестра, принадлежащую к компоненту, или измените запись реестра, чтобы она принадлежала компоненту, используя его в качестве ключевого пути.</span><span class="sxs-lookup"><span data-stu-id="e1c90-133">To fix this error, change the KeyPath value to refer to a registry entry that belongs to the component or change the registry entry to belong to the component using it as a KeyPath.</span></span><br/>   |



 

<span data-ttu-id="e1c90-134">[Таблица Component](component-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="e1c90-134">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="e1c90-135">Компонент</span><span class="sxs-lookup"><span data-stu-id="e1c90-135">Component</span></span>  | <span data-ttu-id="e1c90-136">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e1c90-136">Attributes</span></span> | <span data-ttu-id="e1c90-137">Путь</span><span class="sxs-lookup"><span data-stu-id="e1c90-137">KeyPath</span></span> |
|------------|------------|---------|
| <span data-ttu-id="e1c90-138">Component1</span><span class="sxs-lookup"><span data-stu-id="e1c90-138">Component1</span></span> | <span data-ttu-id="e1c90-139">0</span><span class="sxs-lookup"><span data-stu-id="e1c90-139">0</span></span>          | <span data-ttu-id="e1c90-140">Файл1</span><span class="sxs-lookup"><span data-stu-id="e1c90-140">File1</span></span>   |
| <span data-ttu-id="e1c90-141">Component2</span><span class="sxs-lookup"><span data-stu-id="e1c90-141">Component2</span></span> | <span data-ttu-id="e1c90-142">4</span><span class="sxs-lookup"><span data-stu-id="e1c90-142">4</span></span>          |         |
| <span data-ttu-id="e1c90-143">Component3</span><span class="sxs-lookup"><span data-stu-id="e1c90-143">Component3</span></span> | <span data-ttu-id="e1c90-144">4</span><span class="sxs-lookup"><span data-stu-id="e1c90-144">4</span></span>          | <span data-ttu-id="e1c90-145">Reg3</span><span class="sxs-lookup"><span data-stu-id="e1c90-145">Reg3</span></span>    |
| <span data-ttu-id="e1c90-146">Component4</span><span class="sxs-lookup"><span data-stu-id="e1c90-146">Component4</span></span> | <span data-ttu-id="e1c90-147">4</span><span class="sxs-lookup"><span data-stu-id="e1c90-147">4</span></span>          | <span data-ttu-id="e1c90-148">Reg4</span><span class="sxs-lookup"><span data-stu-id="e1c90-148">Reg4</span></span>    |
| <span data-ttu-id="e1c90-149">Component5</span><span class="sxs-lookup"><span data-stu-id="e1c90-149">Component5</span></span> | <span data-ttu-id="e1c90-150">4</span><span class="sxs-lookup"><span data-stu-id="e1c90-150">4</span></span>          | <span data-ttu-id="e1c90-151">Reg5</span><span class="sxs-lookup"><span data-stu-id="e1c90-151">Reg5</span></span>    |



 

<span data-ttu-id="e1c90-152">[Таблица реестра](registry-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="e1c90-152">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="e1c90-153">Реестр</span><span class="sxs-lookup"><span data-stu-id="e1c90-153">Registry</span></span> | <span data-ttu-id="e1c90-154">Root</span><span class="sxs-lookup"><span data-stu-id="e1c90-154">Root</span></span> | <span data-ttu-id="e1c90-155">Значение</span><span class="sxs-lookup"><span data-stu-id="e1c90-155">Value</span></span> | <span data-ttu-id="e1c90-156">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="e1c90-156">Component\_</span></span> |
|----------|------|-------|-------------|
| <span data-ttu-id="e1c90-157">Reg3</span><span class="sxs-lookup"><span data-stu-id="e1c90-157">Reg3</span></span>     | <span data-ttu-id="e1c90-158">2</span><span class="sxs-lookup"><span data-stu-id="e1c90-158">2</span></span>    |       | <span data-ttu-id="e1c90-159">Component3</span><span class="sxs-lookup"><span data-stu-id="e1c90-159">Component3</span></span>  |
| <span data-ttu-id="e1c90-160">Reg5</span><span class="sxs-lookup"><span data-stu-id="e1c90-160">Reg5</span></span>     | <span data-ttu-id="e1c90-161">0</span><span class="sxs-lookup"><span data-stu-id="e1c90-161">0</span></span>    |       | <span data-ttu-id="e1c90-162">Component4</span><span class="sxs-lookup"><span data-stu-id="e1c90-162">Component4</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="e1c90-163">См. также</span><span class="sxs-lookup"><span data-stu-id="e1c90-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1c90-164">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="e1c90-164">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




