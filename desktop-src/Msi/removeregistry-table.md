---
description: Таблица Ремоверегистри содержит сведения реестра, которые приложению необходимо удалить из системного реестра.
ms.assetid: 8be382f1-f5ab-4a9d-bf0e-05275310c5b5
title: Таблица Ремоверегистри
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de39edd15484ac4bcda675ec8bffaca0540a0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998744"
---
# <a name="removeregistry-table"></a><span data-ttu-id="c16d2-103">Таблица Ремоверегистри</span><span class="sxs-lookup"><span data-stu-id="c16d2-103">RemoveRegistry Table</span></span>

<span data-ttu-id="c16d2-104">Таблица Ремоверегистри содержит сведения реестра, которые приложению необходимо удалить из системного реестра.</span><span class="sxs-lookup"><span data-stu-id="c16d2-104">The RemoveRegistry table contains the registry information the application needs to delete from the system registry.</span></span>

<span data-ttu-id="c16d2-105">Таблица Ремоверегистри содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="c16d2-105">The RemoveRegistry table has the following columns.</span></span>



| <span data-ttu-id="c16d2-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="c16d2-106">Column</span></span>         | <span data-ttu-id="c16d2-107">Type</span><span class="sxs-lookup"><span data-stu-id="c16d2-107">Type</span></span>                         | <span data-ttu-id="c16d2-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="c16d2-108">Key</span></span> | <span data-ttu-id="c16d2-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="c16d2-109">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="c16d2-110">ремоверегистри</span><span class="sxs-lookup"><span data-stu-id="c16d2-110">RemoveRegistry</span></span> | [<span data-ttu-id="c16d2-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="c16d2-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="c16d2-112">Да</span><span class="sxs-lookup"><span data-stu-id="c16d2-112">Y</span></span>   | <span data-ttu-id="c16d2-113">Нет</span><span class="sxs-lookup"><span data-stu-id="c16d2-113">N</span></span>        |
| <span data-ttu-id="c16d2-114">Root</span><span class="sxs-lookup"><span data-stu-id="c16d2-114">Root</span></span>           | [<span data-ttu-id="c16d2-115">Integer</span><span class="sxs-lookup"><span data-stu-id="c16d2-115">Integer</span></span>](integer.md)       | <span data-ttu-id="c16d2-116">Нет</span><span class="sxs-lookup"><span data-stu-id="c16d2-116">N</span></span>   | <span data-ttu-id="c16d2-117">Нет</span><span class="sxs-lookup"><span data-stu-id="c16d2-117">N</span></span>        |
| <span data-ttu-id="c16d2-118">Ключ</span><span class="sxs-lookup"><span data-stu-id="c16d2-118">Key</span></span>            | [<span data-ttu-id="c16d2-119">регпас</span><span class="sxs-lookup"><span data-stu-id="c16d2-119">RegPath</span></span>](regpath.md)       | <span data-ttu-id="c16d2-120">Нет</span><span class="sxs-lookup"><span data-stu-id="c16d2-120">N</span></span>   | <span data-ttu-id="c16d2-121">Нет</span><span class="sxs-lookup"><span data-stu-id="c16d2-121">N</span></span>        |
| <span data-ttu-id="c16d2-122">Имя</span><span class="sxs-lookup"><span data-stu-id="c16d2-122">Name</span></span>           | [<span data-ttu-id="c16d2-123">Формате</span><span class="sxs-lookup"><span data-stu-id="c16d2-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="c16d2-124">Нет</span><span class="sxs-lookup"><span data-stu-id="c16d2-124">N</span></span>   | <span data-ttu-id="c16d2-125">Да</span><span class="sxs-lookup"><span data-stu-id="c16d2-125">Y</span></span>        |
| <span data-ttu-id="c16d2-126">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="c16d2-126">Component\_</span></span>    | [<span data-ttu-id="c16d2-127">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="c16d2-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="c16d2-128">Нет</span><span class="sxs-lookup"><span data-stu-id="c16d2-128">N</span></span>   | <span data-ttu-id="c16d2-129">Нет</span><span class="sxs-lookup"><span data-stu-id="c16d2-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c16d2-130">Столбцы</span><span class="sxs-lookup"><span data-stu-id="c16d2-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c16d2-131"><span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>ремоверегистри</span><span class="sxs-lookup"><span data-stu-id="c16d2-131"><span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry</span></span>
</dt> <dd>

<span data-ttu-id="c16d2-132">Ключ для этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="c16d2-132">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="c16d2-133"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Корневой</span><span class="sxs-lookup"><span data-stu-id="c16d2-133"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="c16d2-134">Предопределенный корневой ключ для значения реестра.</span><span class="sxs-lookup"><span data-stu-id="c16d2-134">The predefined root key for the registry value.</span></span>



| <span data-ttu-id="c16d2-135">Константа</span><span class="sxs-lookup"><span data-stu-id="c16d2-135">Constant</span></span>                          | <span data-ttu-id="c16d2-136">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="c16d2-136">Hexadecimal</span></span> | <span data-ttu-id="c16d2-137">Decimal</span><span class="sxs-lookup"><span data-stu-id="c16d2-137">Decimal</span></span> | <span data-ttu-id="c16d2-138">Корневой ключ</span><span class="sxs-lookup"><span data-stu-id="c16d2-138">Root key</span></span>                                                                                                                                                                                                           |
|-----------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c16d2-139">(нет)</span><span class="sxs-lookup"><span data-stu-id="c16d2-139">(none)</span></span>                            | <span data-ttu-id="c16d2-140">\- 0x001</span><span class="sxs-lookup"><span data-stu-id="c16d2-140">\- 0x001</span></span>    | <span data-ttu-id="c16d2-141">-1</span><span class="sxs-lookup"><span data-stu-id="c16d2-141">-1</span></span>      | <span data-ttu-id="c16d2-142">**HKey \_ ТЕКУЩИЙ установщик \_ пользователя** задает этот ключ при выполнении установки на уровне пользователя.</span><span class="sxs-lookup"><span data-stu-id="c16d2-142">**HKEY\_CURRENT\_USER** Installer sets this key while doing a per-user installation.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="c16d2-143">(нет)</span><span class="sxs-lookup"><span data-stu-id="c16d2-143">(none)</span></span>                            | <span data-ttu-id="c16d2-144">-0x001</span><span class="sxs-lookup"><span data-stu-id="c16d2-144">-0x001</span></span>      | <span data-ttu-id="c16d2-145">-1</span><span class="sxs-lookup"><span data-stu-id="c16d2-145">-1</span></span>      | <span data-ttu-id="c16d2-146">**HKey \_ Установщик ЛОКАЛЬНОГО \_ компьютера** задает этот ключ при установке всех пользователей с параметром [**ALLUSERS**](allusers.md) , имеющим значение 1.</span><span class="sxs-lookup"><span data-stu-id="c16d2-146">**HKEY\_LOCAL\_MACHINE** Installer sets this key while doing an all-users installation with [**ALLUSERS**](allusers.md) set to 1.</span></span><br/>                                                                       |
| <span data-ttu-id="c16d2-147">**мсидбрегистрирутклассесрут**</span><span class="sxs-lookup"><span data-stu-id="c16d2-147">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="c16d2-148">0x000</span><span class="sxs-lookup"><span data-stu-id="c16d2-148">0x000</span></span>       | <span data-ttu-id="c16d2-149">0</span><span class="sxs-lookup"><span data-stu-id="c16d2-149">0</span></span>       | <span data-ttu-id="c16d2-150">**HKey \_ \_Корень классов** установщик удаляет значение из куста **\\ программных \\ классов HKCU** во время установки в [контексте установки](installation-context.md)на уровне пользователя и на компьютере.</span><span class="sxs-lookup"><span data-stu-id="c16d2-150">**HKEY\_CLASSES\_ROOT** The installer removes the value from the **HKCU\\Software\\Classes** hive during installations in the per-user and per-machine [installation context](installation-context.md).</span></span><br/> |
| <span data-ttu-id="c16d2-151">**мсидбрегистрируткуррентусер**</span><span class="sxs-lookup"><span data-stu-id="c16d2-151">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="c16d2-152">0x001</span><span class="sxs-lookup"><span data-stu-id="c16d2-152">0x001</span></span>       | <span data-ttu-id="c16d2-153">1</span><span class="sxs-lookup"><span data-stu-id="c16d2-153">1</span></span>       | <span data-ttu-id="c16d2-154">**HKEY \_ текущего \_ пользователя**</span><span class="sxs-lookup"><span data-stu-id="c16d2-154">**HKEY\_CURRENT\_USER**</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="c16d2-155">**мсидбрегистрирутлокалмачине**</span><span class="sxs-lookup"><span data-stu-id="c16d2-155">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="c16d2-156">0x002</span><span class="sxs-lookup"><span data-stu-id="c16d2-156">0x002</span></span>       | <span data-ttu-id="c16d2-157">2</span><span class="sxs-lookup"><span data-stu-id="c16d2-157">2</span></span>       | <span data-ttu-id="c16d2-158">**HKEY \_ локальный \_ компьютер**</span><span class="sxs-lookup"><span data-stu-id="c16d2-158">**HKEY\_LOCAL\_MACHINE**</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="c16d2-159">**мсидбрегистрирутусерс**</span><span class="sxs-lookup"><span data-stu-id="c16d2-159">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="c16d2-160">0x003</span><span class="sxs-lookup"><span data-stu-id="c16d2-160">0x003</span></span>       | <span data-ttu-id="c16d2-161">3</span><span class="sxs-lookup"><span data-stu-id="c16d2-161">3</span></span>       | <span data-ttu-id="c16d2-162">**\_Пользователи hKey**</span><span class="sxs-lookup"><span data-stu-id="c16d2-162">**HKEY\_USERS**</span></span>                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="c16d2-163"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Раздел</span><span class="sxs-lookup"><span data-stu-id="c16d2-163"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="c16d2-164">Локализуемый ключ для значения реестра.</span><span class="sxs-lookup"><span data-stu-id="c16d2-164">The localizable key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="c16d2-165"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Безымян</span><span class="sxs-lookup"><span data-stu-id="c16d2-165"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="c16d2-166">Имя локализуемого значения реестра.</span><span class="sxs-lookup"><span data-stu-id="c16d2-166">The localizable registry value name.</span></span>

<span data-ttu-id="c16d2-167">Следующая строка в столбце Name имеет особое значение.</span><span class="sxs-lookup"><span data-stu-id="c16d2-167">The following string in the Name column has special significance.</span></span>



| <span data-ttu-id="c16d2-168">Строка</span><span class="sxs-lookup"><span data-stu-id="c16d2-168">String</span></span> | <span data-ttu-id="c16d2-169">Значение</span><span class="sxs-lookup"><span data-stu-id="c16d2-169">Meaning</span></span>                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c16d2-170">"-"</span><span class="sxs-lookup"><span data-stu-id="c16d2-170">"-"</span></span>    | <span data-ttu-id="c16d2-171">Ключ должен быть удален, если он есть, со всеми его значениями и подразделами при установке компонента.</span><span class="sxs-lookup"><span data-stu-id="c16d2-171">The key is to be deleted, if present, with all of its values and subkeys, when the component is installed.</span></span> |



 

<span data-ttu-id="c16d2-172">Обратите внимание, что для создания или удаления раздела реестра при удалении компонента следует использовать [таблицу реестра](registry-table.md) .</span><span class="sxs-lookup"><span data-stu-id="c16d2-172">Note that the [Registry table](registry-table.md) should be used to create or remove a registry key when the component is removed.</span></span>

</dd> <dt>

<span data-ttu-id="c16d2-173"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="c16d2-173"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="c16d2-174">Внешний ключ в первый столбец [таблицы Component](component-table.md) , ссылающийся на компонент, который управляет удалением значения реестра.</span><span class="sxs-lookup"><span data-stu-id="c16d2-174">External key into the first column of the [Component table](component-table.md) referencing the component that controls the deletion of the registry value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c16d2-175">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c16d2-175">Remarks</span></span>

<span data-ttu-id="c16d2-176">Сведения из реестра удаляются из системного реестра, если соответствующий компонент выбран для локальной установки или запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="c16d2-176">The registry information is deleted from the system registry when the corresponding component has been selected to be installed locally or run from source.</span></span>

<span data-ttu-id="c16d2-177">Эта таблица упоминается при выполнении [действия ремоверегистривалуес](removeregistryvalues-action.md) .</span><span class="sxs-lookup"><span data-stu-id="c16d2-177">This table is referred to when the [RemoveRegistryValues action](removeregistryvalues-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="c16d2-178">Проверка</span><span class="sxs-lookup"><span data-stu-id="c16d2-178">Validation</span></span>

<dl>

[<span data-ttu-id="c16d2-179">ICE03</span><span class="sxs-lookup"><span data-stu-id="c16d2-179">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c16d2-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="c16d2-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c16d2-181">ICE32</span><span class="sxs-lookup"><span data-stu-id="c16d2-181">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="c16d2-182">ICE46</span><span class="sxs-lookup"><span data-stu-id="c16d2-182">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="c16d2-183">ICE69</span><span class="sxs-lookup"><span data-stu-id="c16d2-183">ICE69</span></span>](ice69.md)  
</dl>

 

 




