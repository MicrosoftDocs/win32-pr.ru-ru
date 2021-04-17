---
description: Таблица Реглокатор содержит сведения, необходимые для поиска файла или каталога с помощью реестра, или для поиска определенного параметра реестра. Эта таблица содержит следующие столбцы.
ms.assetid: dc88b083-cc1d-46d7-9be8-29ebbf3767a0
title: Таблица Реглокатор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db5084b8c6fd8d10372759bdba65abbb4dfe7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663057"
---
# <a name="reglocator-table"></a><span data-ttu-id="3d95a-104">Таблица Реглокатор</span><span class="sxs-lookup"><span data-stu-id="3d95a-104">RegLocator Table</span></span>

<span data-ttu-id="3d95a-105">Таблица Реглокатор содержит сведения, необходимые для поиска файла или каталога с помощью реестра, или для поиска определенного параметра реестра.</span><span class="sxs-lookup"><span data-stu-id="3d95a-105">The RegLocator table holds the information needed to search for a file or directory using the registry, or to search for a particular registry entry itself.</span></span> <span data-ttu-id="3d95a-106">Эта таблица содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="3d95a-106">This table has the following columns.</span></span>



| <span data-ttu-id="3d95a-107">Столбец</span><span class="sxs-lookup"><span data-stu-id="3d95a-107">Column</span></span>      | <span data-ttu-id="3d95a-108">Type</span><span class="sxs-lookup"><span data-stu-id="3d95a-108">Type</span></span>                         | <span data-ttu-id="3d95a-109">Ключ</span><span class="sxs-lookup"><span data-stu-id="3d95a-109">Key</span></span> | <span data-ttu-id="3d95a-110">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="3d95a-110">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="3d95a-111">Образец\_</span><span class="sxs-lookup"><span data-stu-id="3d95a-111">Signature\_</span></span> | [<span data-ttu-id="3d95a-112">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="3d95a-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="3d95a-113">Да</span><span class="sxs-lookup"><span data-stu-id="3d95a-113">Y</span></span>   | <span data-ttu-id="3d95a-114">Нет</span><span class="sxs-lookup"><span data-stu-id="3d95a-114">N</span></span>        |
| <span data-ttu-id="3d95a-115">Root</span><span class="sxs-lookup"><span data-stu-id="3d95a-115">Root</span></span>        | [<span data-ttu-id="3d95a-116">Integer</span><span class="sxs-lookup"><span data-stu-id="3d95a-116">Integer</span></span>](integer.md)       | <span data-ttu-id="3d95a-117">Нет</span><span class="sxs-lookup"><span data-stu-id="3d95a-117">N</span></span>   | <span data-ttu-id="3d95a-118">Нет</span><span class="sxs-lookup"><span data-stu-id="3d95a-118">N</span></span>        |
| <span data-ttu-id="3d95a-119">Ключ</span><span class="sxs-lookup"><span data-stu-id="3d95a-119">Key</span></span>         | [<span data-ttu-id="3d95a-120">регпас</span><span class="sxs-lookup"><span data-stu-id="3d95a-120">RegPath</span></span>](regpath.md)       | <span data-ttu-id="3d95a-121">Нет</span><span class="sxs-lookup"><span data-stu-id="3d95a-121">N</span></span>   | <span data-ttu-id="3d95a-122">Нет</span><span class="sxs-lookup"><span data-stu-id="3d95a-122">N</span></span>        |
| <span data-ttu-id="3d95a-123">Имя</span><span class="sxs-lookup"><span data-stu-id="3d95a-123">Name</span></span>        | [<span data-ttu-id="3d95a-124">Формате</span><span class="sxs-lookup"><span data-stu-id="3d95a-124">Formatted</span></span>](formatted.md)   | <span data-ttu-id="3d95a-125">Нет</span><span class="sxs-lookup"><span data-stu-id="3d95a-125">N</span></span>   | <span data-ttu-id="3d95a-126">Да</span><span class="sxs-lookup"><span data-stu-id="3d95a-126">Y</span></span>        |
| <span data-ttu-id="3d95a-127">Тип</span><span class="sxs-lookup"><span data-stu-id="3d95a-127">Type</span></span>        | [<span data-ttu-id="3d95a-128">Integer</span><span class="sxs-lookup"><span data-stu-id="3d95a-128">Integer</span></span>](integer.md)       | <span data-ttu-id="3d95a-129">Нет</span><span class="sxs-lookup"><span data-stu-id="3d95a-129">N</span></span>   | <span data-ttu-id="3d95a-130">Да</span><span class="sxs-lookup"><span data-stu-id="3d95a-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3d95a-131">Столбцы</span><span class="sxs-lookup"><span data-stu-id="3d95a-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3d95a-132"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Образец\_</span><span class="sxs-lookup"><span data-stu-id="3d95a-132"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="3d95a-133">Значение в \_ поле Signature представляет собой уникальную сигнатуру, которая является внешним ключом в столбце одной из таблиц [сигнатур](signature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="3d95a-133">The value in the Signature\_ field represents a unique signature that is an external key into column one of the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="3d95a-134">Если эта подпись содержится в таблице сигнатур, то поиск выполняется для файла.</span><span class="sxs-lookup"><span data-stu-id="3d95a-134">If this signature is present in the Signature table, the search is for a file.</span></span> <span data-ttu-id="3d95a-135">Если эта подпись отсутствует в таблице сигнатур, а значение столбца Type — **мсидблокатортипераввалуе**, то поиск будет указывать на имя раздела реестра, на который указывает таблица реглокатор.</span><span class="sxs-lookup"><span data-stu-id="3d95a-135">If this signature is absent from the Signature table, and the value of the Type column is **msidbLocatorTypeRawValue**, the search is for the registry key name pointed to by the RegLocator table.</span></span> <span data-ttu-id="3d95a-136">В противном случае поиск осуществляется для каталога, на который указывает таблица Реглокатор.</span><span class="sxs-lookup"><span data-stu-id="3d95a-136">Otherwise the search is for a directory pointed to by the RegLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="3d95a-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Корневой</span><span class="sxs-lookup"><span data-stu-id="3d95a-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="3d95a-138">Предопределенный корневой ключ для значения реестра.</span><span class="sxs-lookup"><span data-stu-id="3d95a-138">The predefined root key for the registry value.</span></span>



| <span data-ttu-id="3d95a-139">Константа</span><span class="sxs-lookup"><span data-stu-id="3d95a-139">Constant</span></span>                          | <span data-ttu-id="3d95a-140">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="3d95a-140">Hexadecimal</span></span> | <span data-ttu-id="3d95a-141">Decimal</span><span class="sxs-lookup"><span data-stu-id="3d95a-141">Decimal</span></span> | <span data-ttu-id="3d95a-142">Корневой ключ</span><span class="sxs-lookup"><span data-stu-id="3d95a-142">Root key</span></span>             |
|-----------------------------------|-------------|---------|----------------------|
| <span data-ttu-id="3d95a-143">**мсидбрегистрирутклассесрут**</span><span class="sxs-lookup"><span data-stu-id="3d95a-143">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="3d95a-144">0x000</span><span class="sxs-lookup"><span data-stu-id="3d95a-144">0x000</span></span>       | <span data-ttu-id="3d95a-145">0</span><span class="sxs-lookup"><span data-stu-id="3d95a-145">0</span></span>       | <span data-ttu-id="3d95a-146">\_корневой узел классов hKey \_</span><span class="sxs-lookup"><span data-stu-id="3d95a-146">HKEY\_CLASSES\_ROOT</span></span>  |
| <span data-ttu-id="3d95a-147">**мсидбрегистрируткуррентусер**</span><span class="sxs-lookup"><span data-stu-id="3d95a-147">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="3d95a-148">0x001</span><span class="sxs-lookup"><span data-stu-id="3d95a-148">0x001</span></span>       | <span data-ttu-id="3d95a-149">1</span><span class="sxs-lookup"><span data-stu-id="3d95a-149">1</span></span>       | <span data-ttu-id="3d95a-150">HKEY \_ текущего \_ пользователя</span><span class="sxs-lookup"><span data-stu-id="3d95a-150">HKEY\_CURRENT\_USER</span></span>  |
| <span data-ttu-id="3d95a-151">**мсидбрегистрирутлокалмачине**</span><span class="sxs-lookup"><span data-stu-id="3d95a-151">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="3d95a-152">0x002</span><span class="sxs-lookup"><span data-stu-id="3d95a-152">0x002</span></span>       | <span data-ttu-id="3d95a-153">2</span><span class="sxs-lookup"><span data-stu-id="3d95a-153">2</span></span>       | <span data-ttu-id="3d95a-154">HKEY \_ локальный \_ компьютер</span><span class="sxs-lookup"><span data-stu-id="3d95a-154">HKEY\_LOCAL\_MACHINE</span></span> |
| <span data-ttu-id="3d95a-155">**мсидбрегистрирутусерс**</span><span class="sxs-lookup"><span data-stu-id="3d95a-155">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="3d95a-156">0x003</span><span class="sxs-lookup"><span data-stu-id="3d95a-156">0x003</span></span>       | <span data-ttu-id="3d95a-157">3</span><span class="sxs-lookup"><span data-stu-id="3d95a-157">3</span></span>       | <span data-ttu-id="3d95a-158">\_Пользователи hKey</span><span class="sxs-lookup"><span data-stu-id="3d95a-158">HKEY\_USERS</span></span>          |



 

</dd> <dt>

<span data-ttu-id="3d95a-159"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Раздел</span><span class="sxs-lookup"><span data-stu-id="3d95a-159"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="3d95a-160">Ключ для значения реестра.</span><span class="sxs-lookup"><span data-stu-id="3d95a-160">The key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="3d95a-161"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Безымян</span><span class="sxs-lookup"><span data-stu-id="3d95a-161"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="3d95a-162">Имя значения реестра.</span><span class="sxs-lookup"><span data-stu-id="3d95a-162">The registry value name.</span></span> <span data-ttu-id="3d95a-163">Если это значение равно null, то извлекается значение из безымянного ключа или значения по умолчанию (при его наличии).</span><span class="sxs-lookup"><span data-stu-id="3d95a-163">If this value is null, then the value from the key's unnamed or default value, if any, is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="3d95a-164"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Тип</span><span class="sxs-lookup"><span data-stu-id="3d95a-164"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="3d95a-165">Значение, определяющее, является ли значение реестра именем файла, расположением каталога или необработанным значением реестра.</span><span class="sxs-lookup"><span data-stu-id="3d95a-165">A value that determines if the registry value is a file name, a directory location, or raw registry value.</span></span>

<span data-ttu-id="3d95a-166">В следующей таблице перечислены допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="3d95a-166">The following table lists valid values.</span></span> <span data-ttu-id="3d95a-167">При необходимости задайте одно из первых трех значений и **msidbLocatorType64bit** .</span><span class="sxs-lookup"><span data-stu-id="3d95a-167">Set one of the first three values and **msidbLocatorType64bit** if necessary.</span></span> <span data-ttu-id="3d95a-168">Если запись в этом поле отсутствует, для параметра Тип задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="3d95a-168">If the entry in this field is absent, Type is set to be 1.</span></span>



| <span data-ttu-id="3d95a-169">Константа</span><span class="sxs-lookup"><span data-stu-id="3d95a-169">Constant</span></span>                      | <span data-ttu-id="3d95a-170">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="3d95a-170">Hexadecimal</span></span> | <span data-ttu-id="3d95a-171">Decimal</span><span class="sxs-lookup"><span data-stu-id="3d95a-171">Decimal</span></span> | <span data-ttu-id="3d95a-172">Описание</span><span class="sxs-lookup"><span data-stu-id="3d95a-172">Description</span></span>                                                                                                                                                        |
|-------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d95a-173">**мсидблокатортипедиректори**</span><span class="sxs-lookup"><span data-stu-id="3d95a-173">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="3d95a-174">0x000</span><span class="sxs-lookup"><span data-stu-id="3d95a-174">0x000</span></span>       | <span data-ttu-id="3d95a-175">0</span><span class="sxs-lookup"><span data-stu-id="3d95a-175">0</span></span>       | <span data-ttu-id="3d95a-176">Путь к разделу — это каталог.</span><span class="sxs-lookup"><span data-stu-id="3d95a-176">Key path is a directory.</span></span>                                                                                                                                           |
| <span data-ttu-id="3d95a-177">**мсидблокатортипефиленаме**</span><span class="sxs-lookup"><span data-stu-id="3d95a-177">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="3d95a-178">0x001</span><span class="sxs-lookup"><span data-stu-id="3d95a-178">0x001</span></span>       | <span data-ttu-id="3d95a-179">1</span><span class="sxs-lookup"><span data-stu-id="3d95a-179">1</span></span>       | <span data-ttu-id="3d95a-180">Путь к разделу — это имя файла.</span><span class="sxs-lookup"><span data-stu-id="3d95a-180">Key path is a file name.</span></span>                                                                                                                                           |
| <span data-ttu-id="3d95a-181">**мсидблокатортипераввалуе**</span><span class="sxs-lookup"><span data-stu-id="3d95a-181">**msidbLocatorTypeRawValue**</span></span>  | <span data-ttu-id="3d95a-182">0x002</span><span class="sxs-lookup"><span data-stu-id="3d95a-182">0x002</span></span>       | <span data-ttu-id="3d95a-183">2</span><span class="sxs-lookup"><span data-stu-id="3d95a-183">2</span></span>       | <span data-ttu-id="3d95a-184">Путь к разделу — это значение реестра.</span><span class="sxs-lookup"><span data-stu-id="3d95a-184">Key path is a registry value.</span></span>                                                                                                                                      |
| <span data-ttu-id="3d95a-185">**msidbLocatorType64bit**</span><span class="sxs-lookup"><span data-stu-id="3d95a-185">**msidbLocatorType64bit**</span></span>     | <span data-ttu-id="3d95a-186">0x010</span><span class="sxs-lookup"><span data-stu-id="3d95a-186">0x010</span></span>       | <span data-ttu-id="3d95a-187">16</span><span class="sxs-lookup"><span data-stu-id="3d95a-187">16</span></span>      | <span data-ttu-id="3d95a-188">Установите этот бит, чтобы установщик выполнил Поиск в 64-разрядной части реестра.</span><span class="sxs-lookup"><span data-stu-id="3d95a-188">Set this bit to have the installer search the 64-bit portion of the registry.</span></span> <span data-ttu-id="3d95a-189">Не устанавливайте этот бит, чтобы установщик выполнил Поиск 32-разрядной части реестра.</span><span class="sxs-lookup"><span data-stu-id="3d95a-189">Do not set this bit to have the installer search the 32-bit portion of the registry.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d95a-190">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d95a-190">Remarks</span></span>

<span data-ttu-id="3d95a-191">Обратите внимание, что если значение в поле Type равно **мсидблокатортипераввалуе**, установщик устанавливает значение свойства, указанного в поле Property таблицы [аппсеарч](appsearch-table.md) , в значение реестра.</span><span class="sxs-lookup"><span data-stu-id="3d95a-191">Note that if the value in the Type field is **msidbLocatorTypeRawValue**, the installer sets the value of the property specified in the Property field of the [AppSearch](appsearch-table.md) table to the registry value.</span></span> <span data-ttu-id="3d95a-192">Установщик добавляет префикс в значение реестра, определяющее тип значения реестра.</span><span class="sxs-lookup"><span data-stu-id="3d95a-192">The installer adds a prefix to the registry value that identifies the type of registry value.</span></span> <span data-ttu-id="3d95a-193">Дополнительные сведения о типах значений реестра см. в разделе [типы значений реестра](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="3d95a-193">For more information about types of registry values, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>



| <span data-ttu-id="3d95a-194">Тип реестра</span><span class="sxs-lookup"><span data-stu-id="3d95a-194">Registry type</span></span>   | <span data-ttu-id="3d95a-195">Префикс, добавленный установщиком</span><span class="sxs-lookup"><span data-stu-id="3d95a-195">Prefix added by Installer</span></span>                                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d95a-196">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="3d95a-196">REG\_SZ</span></span>         | <span data-ttu-id="3d95a-197">Нет, но если первый символ в значении реестра равен \# , программа установки помещает символ в escape-последовательность другого \# .</span><span class="sxs-lookup"><span data-stu-id="3d95a-197">None, but if the first character of the registry value is \#, the installer escapes the character by prefixing a another \#.</span></span>            |
| <span data-ttu-id="3d95a-198">DWORD</span><span class="sxs-lookup"><span data-stu-id="3d95a-198">DWORD</span></span>           | <span data-ttu-id="3d95a-199">" \# " (необязательно), за которым следует символ "+" или "-"</span><span class="sxs-lookup"><span data-stu-id="3d95a-199">"\#" optionally followed by '+' or '-'</span></span>                                                                                                  |
| <span data-ttu-id="3d95a-200">\_распаковать \_ SZ</span><span class="sxs-lookup"><span data-stu-id="3d95a-200">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="3d95a-201">"\#%"</span><span class="sxs-lookup"><span data-stu-id="3d95a-201">"\#%"</span></span>                                                                                                                                   |
| <span data-ttu-id="3d95a-202">REG \_ Multi \_ SZ</span><span class="sxs-lookup"><span data-stu-id="3d95a-202">REG\_MULTI\_SZ</span></span>  | <span data-ttu-id="3d95a-203">NULL.</span><span class="sxs-lookup"><span data-stu-id="3d95a-203">Null.</span></span> <span data-ttu-id="3d95a-204">Установщик присваивает свойству значение, начинающееся со значения NULL и заканчивающееся значением NULL.</span><span class="sxs-lookup"><span data-stu-id="3d95a-204">The installer sets the property to a value beginning with a null and ending with a null.</span></span>                                          |
| <span data-ttu-id="3d95a-205">\_двоичный файл REG</span><span class="sxs-lookup"><span data-stu-id="3d95a-205">REG\_BINARY</span></span>     | <span data-ttu-id="3d95a-206">" \# x" в случае \_ двоичного файла reg программа установки преобразует и сохраняет каждую шестнадцатеричную цифру (на части) в виде символа ASCII с префиксом " \# x".</span><span class="sxs-lookup"><span data-stu-id="3d95a-206">"\#x" In case of REG\_BINARY, the installer converts and saves each hexadecimal digit (nibble) as an ASCII character prefixed by "\#x".</span></span> |



 

<span data-ttu-id="3d95a-207">Как правило, столбцы в этой таблице не локализуются.</span><span class="sxs-lookup"><span data-stu-id="3d95a-207">Typically, the columns in this table are not localized.</span></span> <span data-ttu-id="3d95a-208">Если автор решает выполнить поиск продуктов на нескольких языках, для каждого языка должна быть включена отдельная запись в таблицу.</span><span class="sxs-lookup"><span data-stu-id="3d95a-208">If an author decides to search for products in multiple languages, then there must be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="3d95a-209">Обратите внимание, что невозможно использовать таблицу Реглокатор для проверки только наличия ключа.</span><span class="sxs-lookup"><span data-stu-id="3d95a-209">Note that it is not possible to use the RegLocator table to check only for the presence of the key.</span></span> <span data-ttu-id="3d95a-210">Однако можно найти значение по умолчанию для ключа и получить его значение, если оно не пустое.</span><span class="sxs-lookup"><span data-stu-id="3d95a-210">However, you can search for the default value of a key and retrieve its value if it is not empty.</span></span>

<span data-ttu-id="3d95a-211">Дополнительные сведения см. в разделе [Поиск существующих приложений, файлов, записей реестра или INI-файлов](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="3d95a-211">For more information, see [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="3d95a-212">Проверка</span><span class="sxs-lookup"><span data-stu-id="3d95a-212">Validation</span></span>

<dl>

[<span data-ttu-id="3d95a-213">ICE03</span><span class="sxs-lookup"><span data-stu-id="3d95a-213">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3d95a-214">ICE06</span><span class="sxs-lookup"><span data-stu-id="3d95a-214">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3d95a-215">ICE46</span><span class="sxs-lookup"><span data-stu-id="3d95a-215">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="3d95a-216">ICE80</span><span class="sxs-lookup"><span data-stu-id="3d95a-216">ICE80</span></span>](ice80.md)  
</dl>

 

 
