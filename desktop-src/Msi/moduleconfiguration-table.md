---
description: В таблице Модулеконфигуратион указаны настраиваемые атрибуты модуля. Эта таблица не объединяется с базой данных.
ms.assetid: 3b77cc23-c104-4adc-868c-3aa2b5794bc7
title: Таблица Модулеконфигуратион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa187c10b5d3376a9bec78eb897b4982445ff01f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265045"
---
# <a name="moduleconfiguration-table"></a><span data-ttu-id="a8206-104">Таблица Модулеконфигуратион</span><span class="sxs-lookup"><span data-stu-id="a8206-104">ModuleConfiguration Table</span></span>

<span data-ttu-id="a8206-105">В таблице Модулеконфигуратион указаны настраиваемые атрибуты модуля.</span><span class="sxs-lookup"><span data-stu-id="a8206-105">The ModuleConfiguration table identifies the configurable attributes of the module.</span></span> <span data-ttu-id="a8206-106">Эта таблица не объединяется с базой данных.</span><span class="sxs-lookup"><span data-stu-id="a8206-106">This table is not merged into the database.</span></span>

<span data-ttu-id="a8206-107">Таблица Модулеконфигуратион содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="a8206-107">The ModuleConfiguration table has the following columns.</span></span>



| <span data-ttu-id="a8206-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="a8206-108">Column</span></span>       | <span data-ttu-id="a8206-109">Type</span><span class="sxs-lookup"><span data-stu-id="a8206-109">Type</span></span>                         | <span data-ttu-id="a8206-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="a8206-110">Key</span></span> | <span data-ttu-id="a8206-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="a8206-111">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="a8206-112">Имя</span><span class="sxs-lookup"><span data-stu-id="a8206-112">Name</span></span>         | [<span data-ttu-id="a8206-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="a8206-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="a8206-114">Да</span><span class="sxs-lookup"><span data-stu-id="a8206-114">Y</span></span>   | <span data-ttu-id="a8206-115">Нет</span><span class="sxs-lookup"><span data-stu-id="a8206-115">N</span></span>        |
| <span data-ttu-id="a8206-116">Формат</span><span class="sxs-lookup"><span data-stu-id="a8206-116">Format</span></span>       | [<span data-ttu-id="a8206-117">Integer</span><span class="sxs-lookup"><span data-stu-id="a8206-117">Integer</span></span>](integer.md)       | <span data-ttu-id="a8206-118">Нет</span><span class="sxs-lookup"><span data-stu-id="a8206-118">N</span></span>   | <span data-ttu-id="a8206-119">Нет</span><span class="sxs-lookup"><span data-stu-id="a8206-119">N</span></span>        |
| <span data-ttu-id="a8206-120">Тип</span><span class="sxs-lookup"><span data-stu-id="a8206-120">Type</span></span>         | [<span data-ttu-id="a8206-121">Text</span><span class="sxs-lookup"><span data-stu-id="a8206-121">Text</span></span>](text.md)             | <span data-ttu-id="a8206-122">Нет</span><span class="sxs-lookup"><span data-stu-id="a8206-122">N</span></span>   | <span data-ttu-id="a8206-123">Да</span><span class="sxs-lookup"><span data-stu-id="a8206-123">Y</span></span>        |
| <span data-ttu-id="a8206-124">контекстдата</span><span class="sxs-lookup"><span data-stu-id="a8206-124">ContextData</span></span>  | [<span data-ttu-id="a8206-125">Text</span><span class="sxs-lookup"><span data-stu-id="a8206-125">Text</span></span>](text.md)             | <span data-ttu-id="a8206-126">Нет</span><span class="sxs-lookup"><span data-stu-id="a8206-126">N</span></span>   | <span data-ttu-id="a8206-127">Да</span><span class="sxs-lookup"><span data-stu-id="a8206-127">Y</span></span>        |
| <span data-ttu-id="a8206-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a8206-128">DefaultValue</span></span> | [<span data-ttu-id="a8206-129">Text</span><span class="sxs-lookup"><span data-stu-id="a8206-129">Text</span></span>](text.md)             | <span data-ttu-id="a8206-130">Нет</span><span class="sxs-lookup"><span data-stu-id="a8206-130">N</span></span>   | <span data-ttu-id="a8206-131">Да</span><span class="sxs-lookup"><span data-stu-id="a8206-131">Y</span></span>        |
| <span data-ttu-id="a8206-132">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a8206-132">Attributes</span></span>   | [<span data-ttu-id="a8206-133">Integer</span><span class="sxs-lookup"><span data-stu-id="a8206-133">Integer</span></span>](integer.md)       | <span data-ttu-id="a8206-134">Нет</span><span class="sxs-lookup"><span data-stu-id="a8206-134">N</span></span>   | <span data-ttu-id="a8206-135">Да</span><span class="sxs-lookup"><span data-stu-id="a8206-135">Y</span></span>        |
| <span data-ttu-id="a8206-136">DisplayName</span><span class="sxs-lookup"><span data-stu-id="a8206-136">DisplayName</span></span>  | [<span data-ttu-id="a8206-137">Text</span><span class="sxs-lookup"><span data-stu-id="a8206-137">Text</span></span>](text.md)             | <span data-ttu-id="a8206-138">Нет</span><span class="sxs-lookup"><span data-stu-id="a8206-138">N</span></span>   | <span data-ttu-id="a8206-139">Да</span><span class="sxs-lookup"><span data-stu-id="a8206-139">Y</span></span>        |
| <span data-ttu-id="a8206-140">Описание</span><span class="sxs-lookup"><span data-stu-id="a8206-140">Description</span></span>  | [<span data-ttu-id="a8206-141">Text</span><span class="sxs-lookup"><span data-stu-id="a8206-141">Text</span></span>](text.md)             | <span data-ttu-id="a8206-142">Нет</span><span class="sxs-lookup"><span data-stu-id="a8206-142">N</span></span>   | <span data-ttu-id="a8206-143">Да</span><span class="sxs-lookup"><span data-stu-id="a8206-143">Y</span></span>        |
| <span data-ttu-id="a8206-144">HelpLocation</span><span class="sxs-lookup"><span data-stu-id="a8206-144">HelpLocation</span></span> | [<span data-ttu-id="a8206-145">Text</span><span class="sxs-lookup"><span data-stu-id="a8206-145">Text</span></span>](text.md)             | <span data-ttu-id="a8206-146">Нет</span><span class="sxs-lookup"><span data-stu-id="a8206-146">N</span></span>   | <span data-ttu-id="a8206-147">Да</span><span class="sxs-lookup"><span data-stu-id="a8206-147">Y</span></span>        |
| <span data-ttu-id="a8206-148">Данным</span><span class="sxs-lookup"><span data-stu-id="a8206-148">HelpKeyword</span></span>  | [<span data-ttu-id="a8206-149">Text</span><span class="sxs-lookup"><span data-stu-id="a8206-149">Text</span></span>](text.md)             | <span data-ttu-id="a8206-150">Нет</span><span class="sxs-lookup"><span data-stu-id="a8206-150">N</span></span>   | <span data-ttu-id="a8206-151">Да</span><span class="sxs-lookup"><span data-stu-id="a8206-151">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a8206-152">Столбцы</span><span class="sxs-lookup"><span data-stu-id="a8206-152">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a8206-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Безымян</span><span class="sxs-lookup"><span data-stu-id="a8206-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="a8206-154">Это поле определяет имя настраиваемого элемента.</span><span class="sxs-lookup"><span data-stu-id="a8206-154">This field defines the name of the configurable item.</span></span> <span data-ttu-id="a8206-155">На это имя ссылается шаблон форматирования в столбце значение [таблицы модулесубститутион](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="a8206-155">This name is referenced in the formatting template in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8206-156"><span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Формат</span><span class="sxs-lookup"><span data-stu-id="a8206-156"><span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Format</span></span>
</dt> <dd>

<span data-ttu-id="a8206-157">В этом столбце указывается формат изменяемых данных.</span><span class="sxs-lookup"><span data-stu-id="a8206-157">This column specifies the format of the data being changed.</span></span>



| <span data-ttu-id="a8206-158">Формат</span><span class="sxs-lookup"><span data-stu-id="a8206-158">Format</span></span>                                       | <span data-ttu-id="a8206-159">Значение</span><span class="sxs-lookup"><span data-stu-id="a8206-159">Value</span></span> |
|----------------------------------------------|-------|
| [<span data-ttu-id="a8206-160">Текст</span><span class="sxs-lookup"><span data-stu-id="a8206-160">Text</span></span>](text-format-types.md)                | <span data-ttu-id="a8206-161">0</span><span class="sxs-lookup"><span data-stu-id="a8206-161">0</span></span>     |
| [<span data-ttu-id="a8206-162">Ключ</span><span class="sxs-lookup"><span data-stu-id="a8206-162">Key</span></span>](key-format-types.md)                  | <span data-ttu-id="a8206-163">1</span><span class="sxs-lookup"><span data-stu-id="a8206-163">1</span></span>     |
| [<span data-ttu-id="a8206-164">Integer</span><span class="sxs-lookup"><span data-stu-id="a8206-164">Integer</span></span>](integer-format-types.md)          | <span data-ttu-id="a8206-165">2</span><span class="sxs-lookup"><span data-stu-id="a8206-165">2</span></span>     |
| [<span data-ttu-id="a8206-166">Формат битового поля</span><span class="sxs-lookup"><span data-stu-id="a8206-166">Bitfield Format</span></span>](bitfield-format-types.md) | <span data-ttu-id="a8206-167">3</span><span class="sxs-lookup"><span data-stu-id="a8206-167">3</span></span>     |



 

</dd> <dt>

<span data-ttu-id="a8206-168"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Тип</span><span class="sxs-lookup"><span data-stu-id="a8206-168"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="a8206-169">В этом столбце указывается тип изменяемых данных.</span><span class="sxs-lookup"><span data-stu-id="a8206-169">This column specifies the type for the data being changed.</span></span> <span data-ttu-id="a8206-170">Этот тип используется для предоставления контекста для любого пользовательского интерфейса и не используется в процессе слияния.</span><span class="sxs-lookup"><span data-stu-id="a8206-170">This type is used to provide a context for any user-interface and is not used in the merge process.</span></span> <span data-ttu-id="a8206-171">Допустимые значения для этого столбца зависят от значения в столбце формат.</span><span class="sxs-lookup"><span data-stu-id="a8206-171">The valid values for this column depend on the value in the Format column.</span></span>

</dd> <dt>

<span data-ttu-id="a8206-172"><span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>контекстдата</span><span class="sxs-lookup"><span data-stu-id="a8206-172"><span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>ContextData</span></span>
</dt> <dd>

<span data-ttu-id="a8206-173">В этом столбце указывается семантический контекст для запрошенных данных.</span><span class="sxs-lookup"><span data-stu-id="a8206-173">This column specifies a semantic context for the requested data.</span></span> <span data-ttu-id="a8206-174">Тип используется для предоставления контекста для любого пользовательского интерфейса и не используется в процессе слияния.</span><span class="sxs-lookup"><span data-stu-id="a8206-174">The type is used to provide a context for any user-interface and is not used in the merge process.</span></span> <span data-ttu-id="a8206-175">Допустимые значения для этого столбца зависят от значений в столбцах Format и Type.</span><span class="sxs-lookup"><span data-stu-id="a8206-175">The valid values for this column depend on the values in the Format and Type columns.</span></span>

</dd> <dt>

<span data-ttu-id="a8206-176"><span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>Максимально</span><span class="sxs-lookup"><span data-stu-id="a8206-176"><span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>DefaultValue</span></span>
</dt> <dd>

<span data-ttu-id="a8206-177">В этом столбце указывается значение по умолчанию для элемента в этой записи, если средство слияния отклоняет предоставление значения.</span><span class="sxs-lookup"><span data-stu-id="a8206-177">This column specifies a default value for the item in this record if the merge tool declines to provide a value.</span></span> <span data-ttu-id="a8206-178">Это значение должно иметь формат, тип и контекст элемента.</span><span class="sxs-lookup"><span data-stu-id="a8206-178">This value must have the format, type, and context of the item.</span></span> <span data-ttu-id="a8206-179">Если это элемент формата "ключ", внешний ключ должен быть допустимым ключом в таблицах модуля.</span><span class="sxs-lookup"><span data-stu-id="a8206-179">If this is a "Key" format item, the foreign key must be a valid key into the tables of the module.</span></span> <span data-ttu-id="a8206-180">Значение NULL может быть допустимым для этого столбца в зависимости от элемента.</span><span class="sxs-lookup"><span data-stu-id="a8206-180">Null may be a valid value for this column depending on the item.</span></span> <span data-ttu-id="a8206-181">Для элементов формата "Key" это значение находится в [специальном формате кмсм](cmsm-special-format.md).</span><span class="sxs-lookup"><span data-stu-id="a8206-181">For "Key" format items, this value is in [CMSM special format](cmsm-special-format.md).</span></span> <span data-ttu-id="a8206-182">Для всех остальных типов значение считается буквально.</span><span class="sxs-lookup"><span data-stu-id="a8206-182">For all other types, the value is treated literally.</span></span>

<span data-ttu-id="a8206-183">Авторы модулей должны убедиться, что модуль является допустимым в состоянии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a8206-183">Module authors must ensure that the module is valid in its default state.</span></span> <span data-ttu-id="a8206-184">Это гарантирует, что версии Mergemod.dll, предшествующие версии 2,0, по-прежнему смогут использовать модуль в состоянии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a8206-184">This ensures that versions of Mergemod.dll earlier than version 2.0 can still use the module in its default state.</span></span>

</dd> <dt>

<span data-ttu-id="a8206-185"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибута</span><span class="sxs-lookup"><span data-stu-id="a8206-185"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="a8206-186">Этот столбец является битовым полем, содержащим атрибуты для этого настраиваемого элемента.</span><span class="sxs-lookup"><span data-stu-id="a8206-186">This column is a bit field containing attributes for this configurable item.</span></span> <span data-ttu-id="a8206-187">Значение NULL эквивалентно 0.</span><span class="sxs-lookup"><span data-stu-id="a8206-187">Null is equivalent to 0.</span></span> <span data-ttu-id="a8206-188">Все остальные биты в этом столбце зарезервированы для будущего использования и должны быть равны 0.</span><span class="sxs-lookup"><span data-stu-id="a8206-188">All other bits in this column are reserved for future use and must be 0.</span></span>



| <span data-ttu-id="a8206-189">Имя</span><span class="sxs-lookup"><span data-stu-id="a8206-189">Name</span></span>                             | <span data-ttu-id="a8206-190">Decimal</span><span class="sxs-lookup"><span data-stu-id="a8206-190">Decimal</span></span> | <span data-ttu-id="a8206-191">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="a8206-191">Hexadecimal</span></span> | <span data-ttu-id="a8206-192">Описание</span><span class="sxs-lookup"><span data-stu-id="a8206-192">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------|---------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8206-193">мсмконфигураблеоптионкэйнурфан</span><span class="sxs-lookup"><span data-stu-id="a8206-193">msmConfigurableOptionKeyNoOrphan</span></span> | <span data-ttu-id="a8206-194">1</span><span class="sxs-lookup"><span data-stu-id="a8206-194">1</span></span>       | <span data-ttu-id="a8206-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a8206-195">0x00000001</span></span>  | <span data-ttu-id="a8206-196">Этот атрибут применяется только к записям со списком внешних ключей для таблицы модулей в поле DefaultValue.</span><span class="sxs-lookup"><span data-stu-id="a8206-196">This attribute only applies to records that list a foreign key to a module table in their DefaultValue field.</span></span> <span data-ttu-id="a8206-197">Средство слияния игнорирует атрибут для любых форматов, кроме [типов форматов ключей](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="a8206-197">The merge tool ignores the attribute for any formats other than the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="a8206-198">Элементы, не перечисленные в [таблице модулесубститутион](modulesubstitution-table.md) , исключаются из следующей проверки.</span><span class="sxs-lookup"><span data-stu-id="a8206-198">Items not listed in the [ModuleSubstitution table](modulesubstitution-table.md) are excluded from the following check.</span></span> <span data-ttu-id="a8206-199">Средство слияния не объединяет строку, на которую ссылается столбец DefaultValue, в целевую базу данных, если после завершения всех параметров конфигурации удовлетворяются следующие условия.</span><span class="sxs-lookup"><span data-stu-id="a8206-199">The merge tool does not merge the row referenced by the DefaultValue column into the target database if the following conditions are satisfied after completing all configuration options.</span></span><br/> <span data-ttu-id="a8206-200">Каждая строка в таблице Модулеконфигуратион с тем же DefaultValue имеет набор Мсмконфигуратионитемскэйнурфан.</span><span class="sxs-lookup"><span data-stu-id="a8206-200">Every row in the ModuleConfiguration table with the same DefaultValue has the msmConfigurationItemsKeyNoOrphan set.</span></span><br/> <span data-ttu-id="a8206-201">Ни одна из строк не использует DefaultValue, так как средство разработки отклонило предоставление значения.</span><span class="sxs-lookup"><span data-stu-id="a8206-201">No rows use the DefaultValue because the authoring tool declined to provide a value.</span></span><br/> <span data-ttu-id="a8206-202">Средство слияния выполняет слияние строки, если выполняется одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="a8206-202">The merge tool merges the row if any of the following conditions are satisfied.</span></span><br/> <span data-ttu-id="a8206-203">Средство слияния находит любую строку, в которой не установлен Мсмконфигитемскэйнурфан.</span><span class="sxs-lookup"><span data-stu-id="a8206-203">The merge tool finds any row that does not have msmConfigItemsKeyNoOrphan set.</span></span><br/> <span data-ttu-id="a8206-204">Значение, если средство слияния находит любую строку по умолчанию, так как средство разработки отклонило предоставление значения.</span><span class="sxs-lookup"><span data-stu-id="a8206-204">If the merge tool finds any row using DefaultValue because the authoring tool declined to provide a value.</span></span><br/> |
| <span data-ttu-id="a8206-205">мсмконфигураблеоптионноннуллабле</span><span class="sxs-lookup"><span data-stu-id="a8206-205">msmConfigurableOptionNonNullable</span></span> | <span data-ttu-id="a8206-206">2</span><span class="sxs-lookup"><span data-stu-id="a8206-206">2</span></span>       | <span data-ttu-id="a8206-207">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a8206-207">0x00000002</span></span>  | <span data-ttu-id="a8206-208">Если этот атрибут задан, значение NULL не является допустимым ответом для этого элемента.</span><span class="sxs-lookup"><span data-stu-id="a8206-208">When this attribute is set, null is not a valid response for this item.</span></span> <span data-ttu-id="a8206-209">Этот атрибут не действует для [целочисленных типов](integer-format-types.md) или [типов битового](bitfield-format-types.md)формата.</span><span class="sxs-lookup"><span data-stu-id="a8206-209">This attribute has no effect for [Integer Format Types](integer-format-types.md) or [Bitfield Format Types](bitfield-format-types.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="a8206-210"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName</span><span class="sxs-lookup"><span data-stu-id="a8206-210"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName</span></span>
</dt> <dd>

<span data-ttu-id="a8206-211">Этот столбец содержит краткое описание этого элемента, которое может использоваться средством Authoring Tool в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="a8206-211">This column provides a short description of this item that the authoring tool may use in the user interface.</span></span> <span data-ttu-id="a8206-212">Этот столбец не может быть локализован.</span><span class="sxs-lookup"><span data-stu-id="a8206-212">This column may not be localized.</span></span> <span data-ttu-id="a8206-213">Присвойте этому столбцу значение null, чтобы модуль запрашивал, что средство разработки не раскрывает это свойство в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="a8206-213">Set this column to null to have the module is request that the authoring tool not expose this property in the UI.</span></span> <span data-ttu-id="a8206-214">Средство может игнорировать значение в этом поле.</span><span class="sxs-lookup"><span data-stu-id="a8206-214">The tool may disregard the value in this field.</span></span>

</dd> <dt>

<span data-ttu-id="a8206-215"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="a8206-215"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="a8206-216">В этом столбце содержится описание этого элемента, которое может использоваться средством Authoring Tool в элементах пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a8206-216">This column provides a description of this item that the authoring tool may use in UI elements.</span></span> <span data-ttu-id="a8206-217">Эта строка может быть локализована при преобразовании языка модуля.</span><span class="sxs-lookup"><span data-stu-id="a8206-217">This string may be localized by the module's language transform.</span></span> <span data-ttu-id="a8206-218">Этот столбец может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="a8206-218">This column may be null.</span></span>

</dd> <dt>

<span data-ttu-id="a8206-219"><span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation</span><span class="sxs-lookup"><span data-stu-id="a8206-219"><span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation</span></span>
</dt> <dd>

<span data-ttu-id="a8206-220">В этом столбце содержится либо имя файла справки (без расширения CHM), либо список пространств имен справки с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="a8206-220">This column provides either the name of a help file (without the .chm extension) or a semicolon delimited list of help namespaces.</span></span> <span data-ttu-id="a8206-221">Если справка недоступна, этот столбец может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="a8206-221">This column can be null if no help is available.</span></span> <span data-ttu-id="a8206-222">Этот столбец может иметь значение null, только если столбец HelpKeyword имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="a8206-222">This column can be null only if the HelpKeyword column is null.</span></span>

</dd> <dt>

<span data-ttu-id="a8206-223"><span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>Данным</span><span class="sxs-lookup"><span data-stu-id="a8206-223"><span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>HelpKeyword</span></span>
</dt> <dd>

<span data-ttu-id="a8206-224">Этот столбец содержит ключевое слово в файл справки или пространство имен из столбца HelpLocation.</span><span class="sxs-lookup"><span data-stu-id="a8206-224">This column provides a keyword into the help file or namespace from the HelpLocation column.</span></span> <span data-ttu-id="a8206-225">Интерпретация этого ключевого слова зависит от столбца HelpLocation.</span><span class="sxs-lookup"><span data-stu-id="a8206-225">The interpretation of this keyword depends on the HelpLocation column.</span></span> <span data-ttu-id="a8206-226">Этот столбец может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="a8206-226">This column may be null.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8206-227">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8206-227">Remarks</span></span>

<span data-ttu-id="a8206-228">Таблица Модулеконфигуратион используется [настраиваемыми модулями слияния](configurable-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="a8206-228">The ModuleConfiguration table is used by [Configurable Merge Modules](configurable-merge-modules.md).</span></span> <span data-ttu-id="a8206-229">Для создания настраиваемого модуля слияния требуется Mergemod.dll 2,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a8206-229">Mergemod.dll 2.0 or later is required to create a configurable merge module.</span></span>

<span data-ttu-id="a8206-230">Чтобы обеспечить совместимость с более старыми версиями Mergemod.dll, таблицы Модулеконфигуратион и [модулесубститутион](modulesubstitution-table.md) должны быть добавлены в [таблицу модулеигноретабле](moduleignoretable-table.md) каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="a8206-230">To ensure compatibility with older versions of Mergemod.dll, the ModuleConfiguration table and [ModuleSubstitution table](modulesubstitution-table.md) should be added to the [ModuleIgnoreTable table](moduleignoretable-table.md) of every module.</span></span>

## <a name="validation"></a><span data-ttu-id="a8206-231">Проверка</span><span class="sxs-lookup"><span data-stu-id="a8206-231">Validation</span></span>

<dl>

[<span data-ttu-id="a8206-232">ICE03</span><span class="sxs-lookup"><span data-stu-id="a8206-232">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a8206-233">ICE06</span><span class="sxs-lookup"><span data-stu-id="a8206-233">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a8206-234">ICE25</span><span class="sxs-lookup"><span data-stu-id="a8206-234">ICE25</span></span>](ice25.md)  
[<span data-ttu-id="a8206-235">ICE45</span><span class="sxs-lookup"><span data-stu-id="a8206-235">ICE45</span></span>](ice45.md)  
</dl>

 

 




