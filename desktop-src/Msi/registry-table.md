---
description: В таблице реестра содержатся сведения о реестре, которые приложение должно задать в системном реестре.
ms.assetid: 809ffd02-cf97-42d8-aed9-c13a14dcd8b4
title: Таблица реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16cb2084716ea8cb9830056808e9c6be7da667f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998416"
---
# <a name="registry-table"></a><span data-ttu-id="8d3c0-103">Таблица реестра</span><span class="sxs-lookup"><span data-stu-id="8d3c0-103">Registry Table</span></span>

<span data-ttu-id="8d3c0-104">В таблице реестра содержатся сведения о реестре, которые приложение должно задать в системном реестре.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-104">The Registry table holds the registry information that the application needs to set in the system registry.</span></span>

<span data-ttu-id="8d3c0-105">Таблица реестра содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-105">The Registry table has the following columns.</span></span>



| <span data-ttu-id="8d3c0-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="8d3c0-106">Column</span></span>      | <span data-ttu-id="8d3c0-107">Type</span><span class="sxs-lookup"><span data-stu-id="8d3c0-107">Type</span></span>                         | <span data-ttu-id="8d3c0-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="8d3c0-108">Key</span></span> | <span data-ttu-id="8d3c0-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="8d3c0-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="8d3c0-110">Реестр</span><span class="sxs-lookup"><span data-stu-id="8d3c0-110">Registry</span></span>    | [<span data-ttu-id="8d3c0-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="8d3c0-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="8d3c0-112">Да</span><span class="sxs-lookup"><span data-stu-id="8d3c0-112">Y</span></span>   | <span data-ttu-id="8d3c0-113">Нет</span><span class="sxs-lookup"><span data-stu-id="8d3c0-113">N</span></span>        |
| <span data-ttu-id="8d3c0-114">Root</span><span class="sxs-lookup"><span data-stu-id="8d3c0-114">Root</span></span>        | [<span data-ttu-id="8d3c0-115">Integer</span><span class="sxs-lookup"><span data-stu-id="8d3c0-115">Integer</span></span>](integer.md)       | <span data-ttu-id="8d3c0-116">Нет</span><span class="sxs-lookup"><span data-stu-id="8d3c0-116">N</span></span>   | <span data-ttu-id="8d3c0-117">Нет</span><span class="sxs-lookup"><span data-stu-id="8d3c0-117">N</span></span>        |
| <span data-ttu-id="8d3c0-118">Ключ</span><span class="sxs-lookup"><span data-stu-id="8d3c0-118">Key</span></span>         | [<span data-ttu-id="8d3c0-119">регпас</span><span class="sxs-lookup"><span data-stu-id="8d3c0-119">RegPath</span></span>](regpath.md)       | <span data-ttu-id="8d3c0-120">Нет</span><span class="sxs-lookup"><span data-stu-id="8d3c0-120">N</span></span>   | <span data-ttu-id="8d3c0-121">Нет</span><span class="sxs-lookup"><span data-stu-id="8d3c0-121">N</span></span>        |
| <span data-ttu-id="8d3c0-122">Имя</span><span class="sxs-lookup"><span data-stu-id="8d3c0-122">Name</span></span>        | [<span data-ttu-id="8d3c0-123">Формате</span><span class="sxs-lookup"><span data-stu-id="8d3c0-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="8d3c0-124">Нет</span><span class="sxs-lookup"><span data-stu-id="8d3c0-124">N</span></span>   | <span data-ttu-id="8d3c0-125">Да</span><span class="sxs-lookup"><span data-stu-id="8d3c0-125">Y</span></span>        |
| <span data-ttu-id="8d3c0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="8d3c0-126">Value</span></span>       | [<span data-ttu-id="8d3c0-127">Формате</span><span class="sxs-lookup"><span data-stu-id="8d3c0-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="8d3c0-128">Нет</span><span class="sxs-lookup"><span data-stu-id="8d3c0-128">N</span></span>   | <span data-ttu-id="8d3c0-129">Да</span><span class="sxs-lookup"><span data-stu-id="8d3c0-129">Y</span></span>        |
| <span data-ttu-id="8d3c0-130">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="8d3c0-130">Component\_</span></span> | [<span data-ttu-id="8d3c0-131">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="8d3c0-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="8d3c0-132">Нет</span><span class="sxs-lookup"><span data-stu-id="8d3c0-132">N</span></span>   | <span data-ttu-id="8d3c0-133">Нет</span><span class="sxs-lookup"><span data-stu-id="8d3c0-133">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8d3c0-134">Столбцы</span><span class="sxs-lookup"><span data-stu-id="8d3c0-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8d3c0-135"><span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Реестра</span><span class="sxs-lookup"><span data-stu-id="8d3c0-135"><span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Registry</span></span>
</dt> <dd>

<span data-ttu-id="8d3c0-136">Первичный ключ, используемый для задания записи реестра.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-136">Primary key used to identify a registry record.</span></span>

</dd> <dt>

<span data-ttu-id="8d3c0-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Корневой</span><span class="sxs-lookup"><span data-stu-id="8d3c0-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="8d3c0-138">Предопределенный корневой ключ для значения реестра.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-138">The predefined root key for the registry value.</span></span> <span data-ttu-id="8d3c0-139">В этом поле введите значение-1, чтобы сделать корневой ключ зависимым от типа установки.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-139">Enter a value of -1 in this field to make the root key dependent on the type of installation.</span></span> <span data-ttu-id="8d3c0-140">Введите одно из других значений в следующей таблице, чтобы принудительно записать значение реестра с определенным корневым ключом.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-140">Enter one of the other values in the following table to force the registry value to be written under a particular root key.</span></span>



| <span data-ttu-id="8d3c0-141">Константа</span><span class="sxs-lookup"><span data-stu-id="8d3c0-141">Constant</span></span>                          | <span data-ttu-id="8d3c0-142">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="8d3c0-142">Hexadecimal</span></span> | <span data-ttu-id="8d3c0-143">Decimal</span><span class="sxs-lookup"><span data-stu-id="8d3c0-143">Decimal</span></span> | <span data-ttu-id="8d3c0-144">Корневой ключ</span><span class="sxs-lookup"><span data-stu-id="8d3c0-144">Root key</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d3c0-145">(нет)</span><span class="sxs-lookup"><span data-stu-id="8d3c0-145">(none)</span></span>                            | <span data-ttu-id="8d3c0-146">\- 0x001</span><span class="sxs-lookup"><span data-stu-id="8d3c0-146">\- 0x001</span></span>    | <span data-ttu-id="8d3c0-147">-1</span><span class="sxs-lookup"><span data-stu-id="8d3c0-147">-1</span></span>      | <span data-ttu-id="8d3c0-148">Если это установка на уровне пользователя, значение реестра записывается в разделе **hKey \_ текущий \_ пользователь**.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-148">If this is a per-user installation, the registry value is written under **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="8d3c0-149">Если это установка на компьютере, значение реестра записывается на **\_ локальный \_ компьютер hKey**.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-149">If this is a per-machine installation, the registry value is written under **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="8d3c0-150">Обратите внимание, что установка для отдельного компьютера задается путем присвоения свойству [**ALLUSERS**](allusers.md) значения 1.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-150">Note that a per-machine installation is specified by setting the [**ALLUSERS**](allusers.md) property to 1.</span></span><br/>                |
| <span data-ttu-id="8d3c0-151">**мсидбрегистрирутклассесрут**</span><span class="sxs-lookup"><span data-stu-id="8d3c0-151">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="8d3c0-152">0x000</span><span class="sxs-lookup"><span data-stu-id="8d3c0-152">0x000</span></span>       | <span data-ttu-id="8d3c0-153">0</span><span class="sxs-lookup"><span data-stu-id="8d3c0-153">0</span></span>       | <span data-ttu-id="8d3c0-154">**HKey \_ \_Корень классов**. установщик записывает или удаляет значение из **\\ \\ классов программного обеспечения HKCU** во время установки в [контексте установки](installation-context.md)на уровне пользователя.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-154">**HKEY\_CLASSES\_ROOT** The installer writes or removes the value from the **HKCU\\Software\\Classes** hive during installation in the per-user [installation context](installation-context.md).</span></span><br/> <span data-ttu-id="8d3c0-155">Установщик записывает или удаляет значение из **\\ \\ классов программного обеспечения HKLM** во время установки на компьютере.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-155">The installer writes or removes the value from the **HKLM\\Software\\Classes** hive during per-machine installations.</span></span><br/> |
| <span data-ttu-id="8d3c0-156">**мсидбрегистрируткуррентусер**</span><span class="sxs-lookup"><span data-stu-id="8d3c0-156">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="8d3c0-157">0x001</span><span class="sxs-lookup"><span data-stu-id="8d3c0-157">0x001</span></span>       | <span data-ttu-id="8d3c0-158">1</span><span class="sxs-lookup"><span data-stu-id="8d3c0-158">1</span></span>       | <span data-ttu-id="8d3c0-159">**HKEY \_ текущего \_ пользователя**</span><span class="sxs-lookup"><span data-stu-id="8d3c0-159">**HKEY\_CURRENT\_USER**</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="8d3c0-160">**мсидбрегистрирутлокалмачине**</span><span class="sxs-lookup"><span data-stu-id="8d3c0-160">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="8d3c0-161">0x002</span><span class="sxs-lookup"><span data-stu-id="8d3c0-161">0x002</span></span>       | <span data-ttu-id="8d3c0-162">2</span><span class="sxs-lookup"><span data-stu-id="8d3c0-162">2</span></span>       | <span data-ttu-id="8d3c0-163">**HKEY \_ локальный \_ компьютер**</span><span class="sxs-lookup"><span data-stu-id="8d3c0-163">**HKEY\_LOCAL\_MACHINE**</span></span>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="8d3c0-164">**мсидбрегистрирутусерс**</span><span class="sxs-lookup"><span data-stu-id="8d3c0-164">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="8d3c0-165">0x003</span><span class="sxs-lookup"><span data-stu-id="8d3c0-165">0x003</span></span>       | <span data-ttu-id="8d3c0-166">3</span><span class="sxs-lookup"><span data-stu-id="8d3c0-166">3</span></span>       | <span data-ttu-id="8d3c0-167">**\_Пользователи hKey**</span><span class="sxs-lookup"><span data-stu-id="8d3c0-167">**HKEY\_USERS**</span></span>                                                                                                                                                                                                                                                                                                                              |



 

<span data-ttu-id="8d3c0-168">Обратите внимание, что записи реестра, записанные в куст **HKCU** , должны ссылаться на компонент, для которого установлен бит регистрикэйпас в столбце Attributes [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="8d3c0-168">Note that it is recommended that registry entries written to the **HKCU** hive reference a component having the RegistryKeyPath bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="8d3c0-169">Это гарантирует, что установщик запишет необходимые записи реестра при наличии нескольких пользователей на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-169">This ensures that the installer writes the necessary registry entries when there are multiple users on the same computer.</span></span>

</dd> <dt>

<span data-ttu-id="8d3c0-170"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Раздел</span><span class="sxs-lookup"><span data-stu-id="8d3c0-170"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="8d3c0-171">Локализуемый ключ для значения реестра.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-171">The localizable key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="8d3c0-172"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Безымян</span><span class="sxs-lookup"><span data-stu-id="8d3c0-172"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="8d3c0-173">Этот столбец содержит имя значения реестра (локализуемое).</span><span class="sxs-lookup"><span data-stu-id="8d3c0-173">This column contains the registry value name (localizable).</span></span> <span data-ttu-id="8d3c0-174">Если это значение равно null, то данные, указанные в столбце значение, записываются в раздел реестра по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-174">If this is Null, then the data entered into the Value column are written to the default registry key.</span></span>

<span data-ttu-id="8d3c0-175">Если столбец значение имеет значение null, то строки, приведенные в следующей таблице в столбце имя, имеют особое значение.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-175">If the Value column is Null, then the strings shown in the following table in the Name column have special significance.</span></span>



| <span data-ttu-id="8d3c0-176">Строка</span><span class="sxs-lookup"><span data-stu-id="8d3c0-176">String</span></span> | <span data-ttu-id="8d3c0-177">Значение</span><span class="sxs-lookup"><span data-stu-id="8d3c0-177">Meaning</span></span>                                                                                                                                                                                          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \+     | <span data-ttu-id="8d3c0-178">Ключ будет создан, если он отсутствует, при установке компонента.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-178">The key is to be created, if absent, when the component is installed.</span></span>                                                                                                                            |
| \-     | <span data-ttu-id="8d3c0-179">Ключ должен быть удален, если он есть, со всеми его значениями и подразделами при удалении компонента.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-179">The key is to be deleted, if present, with all of its values and subkeys, when the component is uninstalled.</span></span>                                                                                     |
| \*     | <span data-ttu-id="8d3c0-180">Ключ будет создан, если он отсутствует, при установке компонента.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-180">The key is to be created, if absent, when the component is installed.</span></span> <span data-ttu-id="8d3c0-181">Кроме того, ключ должен быть удален (если он есть) со всеми его значениями и подразделами при удалении компонента.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-181">Additionally, the key is to be deleted, if present, with all of its values and subkeys, when the component is uninstalled.</span></span> |



 

<span data-ttu-id="8d3c0-182">Обратите внимание, что необходимо использовать [таблицу ремоверегистри](removeregistry-table.md) , если установленный раздел реестра необходимо удалить вместе со своими значениями и подразделами при установке компонента.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-182">Note that the [RemoveRegistry table](removeregistry-table.md) must be used if an installed registry key is to be deleted, with its values and subkeys, when the component is installed.</span></span>

</dd> <dt>

<span data-ttu-id="8d3c0-183"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Значений</span><span class="sxs-lookup"><span data-stu-id="8d3c0-183"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="8d3c0-184">Этот столбец представляет собой локализуемое значение реестра.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-184">This column is the localizable registry value.</span></span> <span data-ttu-id="8d3c0-185">Поле [форматируется](formatted.md).</span><span class="sxs-lookup"><span data-stu-id="8d3c0-185">The field is [Formatted](formatted.md).</span></span> <span data-ttu-id="8d3c0-186">Если значение прикрепляется к одному из следующих префиксов (т. е. \# % *значение*), то значение интерпретируется, как описано в таблице.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-186">If the value is attached to one of the following prefixes (i.e. \#%*value*) then the value is interpreted as described in the table.</span></span> <span data-ttu-id="8d3c0-187">Обратите внимание, что каждый префикс начинается со знака решетки ( \# ).</span><span class="sxs-lookup"><span data-stu-id="8d3c0-187">Note that each prefix begins with a number sign (\#).</span></span> <span data-ttu-id="8d3c0-188">Если значение начинается с двух или более последовательных знаков числа ( \# ), первый \# игнорируется, а значение интерпретируется и сохраняется как строка.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-188">If the value begins with two or more consecutive number signs (\#), the first \# is ignored and value is interpreted and stored as a string.</span></span>



| <span data-ttu-id="8d3c0-189">Prefix</span><span class="sxs-lookup"><span data-stu-id="8d3c0-189">Prefix</span></span> | <span data-ttu-id="8d3c0-190">Значение</span><span class="sxs-lookup"><span data-stu-id="8d3c0-190">Meaning</span></span>                                                                        |
|--------|--------------------------------------------------------------------------------|
| <span data-ttu-id="8d3c0-191">\#x</span><span class="sxs-lookup"><span data-stu-id="8d3c0-191">\#x</span></span>    | <span data-ttu-id="8d3c0-192">Значение интерпретируется и сохраняется как шестнадцатеричное значение ( \_ двоичный формат reg).</span><span class="sxs-lookup"><span data-stu-id="8d3c0-192">The value is interpreted and stored as a hexadecimal value (REG\_BINARY).</span></span>      |
| \#%    | <span data-ttu-id="8d3c0-193">Значение интерпретируется и сохраняется как расширяемая строка (REG \_ expand \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="8d3c0-193">The value is interpreted and stored as an expandable string (REG\_EXPAND\_SZ).</span></span> |
| \#     | <span data-ttu-id="8d3c0-194">Значение интерпретируется и сохраняется как целое число (REG \_ DWORD).</span><span class="sxs-lookup"><span data-stu-id="8d3c0-194">The value is interpreted and stored as an integer (REG\_DWORD).</span></span>                |



 

-   <span data-ttu-id="8d3c0-195">Если значение содержит последовательность тильда \[ ~ \] , то значение интерпретируется как список строк, разделенных символами NULL (REG \_ Multi \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="8d3c0-195">If the value contains the sequence tilde \[~\], then the value is interpreted as a Null-delimited list of strings (REG\_MULTI\_SZ).</span></span> <span data-ttu-id="8d3c0-196">Например, чтобы указать список, содержащий три строки a, b и c, используйте "a \[ ~ \] b \[ ~ \] c".</span><span class="sxs-lookup"><span data-stu-id="8d3c0-196">For example, to specify a list containing the three strings a, b and c, use "a\[~\]b\[~\]c".</span></span>
-   <span data-ttu-id="8d3c0-197">Последовательность \[ ~ \] в значении разделяет отдельные строки и интерпретируется и сохраняется как символ null.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-197">The sequence \[~\] within the value separates the individual strings and is interpreted and stored as a Null character.</span></span>
-   <span data-ttu-id="8d3c0-198">Если \[ ~ \] перед списком строк стоит строка, строки будут добавлены к любым существующим строкам значений реестра.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-198">If a \[~\] precedes the string list, the strings are to be appended to any existing registry value strings.</span></span> <span data-ttu-id="8d3c0-199">Если добавляемая строка уже содержится в значении реестра, исходное вхождение строки удаляется.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-199">If an appending string already occurs in the registry value, the original occurrence of the string is removed.</span></span>
-   <span data-ttu-id="8d3c0-200">Если \[ ~ \] после конца списка строк, строки будут добавляться в начало всех существующих строк значений реестра.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-200">If a \[~\] follows the end of the string list, the strings are to be prepended to any existing registry value strings.</span></span> <span data-ttu-id="8d3c0-201">Если в значении реестра уже есть строка, которая находится в состоянии ожидания, то исходное вхождение строки удаляется.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-201">If a prepending string already occurs in the registry value, the original occurrence of the string is removed.</span></span>
-   <span data-ttu-id="8d3c0-202">Если объект a \[ ~ \] находится как в начале, так и в конце строки или не в начале списка строк, строки должны заменять все существующие строки значений реестра.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-202">If a \[~\] is at both the beginning and the end or at neither the beginning nor the end of the string list, the strings are to replace any existing registry value strings.</span></span>
-   <span data-ttu-id="8d3c0-203">В противном случае значение интерпретируется и сохраняется в виде строки (REG \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="8d3c0-203">Otherwise, the value is interpreted and stored as a string (REG\_SZ).</span></span>

</dd> <dt>

<span data-ttu-id="8d3c0-204"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="8d3c0-204"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="8d3c0-205">Внешний ключ в первый столбец [таблицы Component](component-table.md) , ссылающийся на компонент, который управляет установкой значения реестра.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-205">External key into the first column of the [Component table](component-table.md) referencing the component that controls the installation of the registry value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d3c0-206">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d3c0-206">Remarks</span></span>

<span data-ttu-id="8d3c0-207">Действия [вритерегистривалуес](writeregistryvalues-action.md) и [ремоверегистривалуес](removeregistryvalues-action.md) в [*таблицах последовательностей*](s-gly.md) обрабатывают сведения, приведенные в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-207">The [WriteRegistryValues](writeregistryvalues-action.md) and [RemoveRegistryValues](removeregistryvalues-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="8d3c0-208">Дополнительные сведения об использовании *таблиц последовательности* см. [в разделе Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="8d3c0-208">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="8d3c0-209">Данные реестра записываются в системный реестр, когда соответствующий компонент был выбран для локальной установки или запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-209">The registry information is written out to the system registry when the corresponding component has been selected to be installed locally or run from source.</span></span>

<span data-ttu-id="8d3c0-210">Обратите внимание, что установщик удаляет раздел реестра после удаления последнего значения или подраздела раздела.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-210">Note that the installer removes a registry key after removing the last value or subkey under the key.</span></span> <span data-ttu-id="8d3c0-211">Чтобы предотвратить удаление пустого раздела реестра при удалении, напишите фиктивное значение с ключом, который необходимо сохранить, и введите + в столбце имя.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-211">To prevent an empty registry key from being removed when uninstalling, write a dummy value under the key you need to keep and enter + in the Name column.</span></span> <span data-ttu-id="8d3c0-212">Если \* параметр находится в столбце имя, ключ удаляется со всеми его значениями и подразделами при удалении компонента.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-212">If \* is in the Name column, the key is deleted, with all of its values and subkeys, when the component is removed.</span></span>

<span data-ttu-id="8d3c0-213">Пользовательское действие можно использовать для добавления строк в таблицу реестра во время установки, удаления или восстановления транзакции.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-213">A custom action can be used to add rows to the Registry table during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="8d3c0-214">Эти строки не сохраняются в таблице реестра, и эти данные доступны только во время текущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-214">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="8d3c0-215">Поэтому пользовательское действие должно выполняться при каждой установке, удалении или исправлении транзакций, для которых требуется информация в этих дополнительных строках.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-215">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="8d3c0-216">Пользовательское действие должно предшествовать действиям [ремоверегистривалуес](removeregistryvalues-action.md) и [вритерегистривалуес](writeregistryvalues-action.md) в последовательности действий.</span><span class="sxs-lookup"><span data-stu-id="8d3c0-216">The custom action must come before the [RemoveRegistryValues](removeregistryvalues-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions in the action sequence.</span></span>

<span data-ttu-id="8d3c0-217">Сведения о том, как защитить раздел реестра, см. в [таблице мсилоккпермиссионсекс](msilockpermissionsex-table.md) и таблице [локкпермиссионс](lockpermissions-table.md).</span><span class="sxs-lookup"><span data-stu-id="8d3c0-217">For information on how to secure a registry key see the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) and [LockPermissions Table](lockpermissions-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="8d3c0-218">Проверка</span><span class="sxs-lookup"><span data-stu-id="8d3c0-218">Validation</span></span>

<dl>

[<span data-ttu-id="8d3c0-219">ICE02</span><span class="sxs-lookup"><span data-stu-id="8d3c0-219">ICE02</span></span>](ice02.md)  
[<span data-ttu-id="8d3c0-220">ICE03</span><span class="sxs-lookup"><span data-stu-id="8d3c0-220">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8d3c0-221">ICE06</span><span class="sxs-lookup"><span data-stu-id="8d3c0-221">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8d3c0-222">ICE32</span><span class="sxs-lookup"><span data-stu-id="8d3c0-222">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="8d3c0-223">ICE38</span><span class="sxs-lookup"><span data-stu-id="8d3c0-223">ICE38</span></span>](ice38.md)  
[<span data-ttu-id="8d3c0-224">ICE43</span><span class="sxs-lookup"><span data-stu-id="8d3c0-224">ICE43</span></span>](ice43.md)  
[<span data-ttu-id="8d3c0-225">ICE46</span><span class="sxs-lookup"><span data-stu-id="8d3c0-225">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="8d3c0-226">ICE49</span><span class="sxs-lookup"><span data-stu-id="8d3c0-226">ICE49</span></span>](ice49.md)  
[<span data-ttu-id="8d3c0-227">ICE53</span><span class="sxs-lookup"><span data-stu-id="8d3c0-227">ICE53</span></span>](ice53.md)  
[<span data-ttu-id="8d3c0-228">ICE55</span><span class="sxs-lookup"><span data-stu-id="8d3c0-228">ICE55</span></span>](ice55.md)  
[<span data-ttu-id="8d3c0-229">ICE57</span><span class="sxs-lookup"><span data-stu-id="8d3c0-229">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="8d3c0-230">ICE70</span><span class="sxs-lookup"><span data-stu-id="8d3c0-230">ICE70</span></span>](ice70.md)  
[<span data-ttu-id="8d3c0-231">ICE80</span><span class="sxs-lookup"><span data-stu-id="8d3c0-231">ICE80</span></span>](ice80.md)  
</dl>

 

 




