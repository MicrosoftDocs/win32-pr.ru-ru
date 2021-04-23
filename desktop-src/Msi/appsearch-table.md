---
description: Таблица Аппсеарч содержит свойства, необходимые для поиска файла с определенной подписью файла. Таблицу Аппсеарч также можно использовать, чтобы задать свойству существующее значение записи реестра или INI-файла.
ms.assetid: d560096f-6baa-4fea-8786-f4e3d5ee6bf4
title: Таблица Аппсеарч
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9419a768a51364b4f22444288e6728a87289aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264196"
---
# <a name="appsearch-table"></a><span data-ttu-id="195ee-104">Таблица Аппсеарч</span><span class="sxs-lookup"><span data-stu-id="195ee-104">AppSearch Table</span></span>

<span data-ttu-id="195ee-105">Таблица Аппсеарч содержит свойства, необходимые для поиска файла с определенной подписью файла.</span><span class="sxs-lookup"><span data-stu-id="195ee-105">The AppSearch table contains properties needed to search for a file having a particular file signature.</span></span> <span data-ttu-id="195ee-106">Таблицу Аппсеарч также можно использовать, чтобы задать свойству существующее значение записи реестра или INI-файла.</span><span class="sxs-lookup"><span data-stu-id="195ee-106">The AppSearch table can also be used to set a property to the existing value of a registry or .ini file entry.</span></span>

<span data-ttu-id="195ee-107">Таблица Аппсеарч содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="195ee-107">The AppSearch table has the following columns.</span></span>



| <span data-ttu-id="195ee-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="195ee-108">Column</span></span>      | <span data-ttu-id="195ee-109">Type</span><span class="sxs-lookup"><span data-stu-id="195ee-109">Type</span></span>                         | <span data-ttu-id="195ee-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="195ee-110">Key</span></span> | <span data-ttu-id="195ee-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="195ee-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="195ee-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="195ee-112">Property</span></span>    | [<span data-ttu-id="195ee-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="195ee-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="195ee-114">Да</span><span class="sxs-lookup"><span data-stu-id="195ee-114">Y</span></span>   | <span data-ttu-id="195ee-115">Нет</span><span class="sxs-lookup"><span data-stu-id="195ee-115">N</span></span>        |
| <span data-ttu-id="195ee-116">Образец\_</span><span class="sxs-lookup"><span data-stu-id="195ee-116">Signature\_</span></span> | [<span data-ttu-id="195ee-117">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="195ee-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="195ee-118">Да</span><span class="sxs-lookup"><span data-stu-id="195ee-118">Y</span></span>   | <span data-ttu-id="195ee-119">Нет</span><span class="sxs-lookup"><span data-stu-id="195ee-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="195ee-120">Столбцы</span><span class="sxs-lookup"><span data-stu-id="195ee-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="195ee-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Свойства</span><span class="sxs-lookup"><span data-stu-id="195ee-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="195ee-122">При выполнении действия [аппсеарч](appsearch-action.md) этому свойству присваивается расположение файла, указанного в столбце сигнатуры \_ .</span><span class="sxs-lookup"><span data-stu-id="195ee-122">Running the [AppSearch](appsearch-action.md) action sets this property to the location of the file indicated by the Signature\_ column.</span></span> <span data-ttu-id="195ee-123">Это свойство задается, если подпись файла существует на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="195ee-123">This property is set if the file signature exists on the user's computer.</span></span> <span data-ttu-id="195ee-124">Свойства, используемые в этом столбце, должны быть [открытыми](public-properties.md) свойствами и иметь идентификатор, не содержащий строчных букв.</span><span class="sxs-lookup"><span data-stu-id="195ee-124">The properties used in this column must be [public](public-properties.md) properties and have an identifier that contains no lowercase letters.</span></span>

<span data-ttu-id="195ee-125">Свойство, указанное в поле свойства, может быть инициализировано в таблице [свойств](property-table.md) или из командной строки.</span><span class="sxs-lookup"><span data-stu-id="195ee-125">The property listed in the Property field may be initialized in the [Property](property-table.md) table or from a command line.</span></span> <span data-ttu-id="195ee-126">Если действие [аппсеарч](appsearch-action.md) находит подпись, установщик переопределяет инициализированное значение свойства на найденное значение.</span><span class="sxs-lookup"><span data-stu-id="195ee-126">If the [AppSearch](appsearch-action.md) action locates the signature, the installer overrides the initialized property value with the found value.</span></span> <span data-ttu-id="195ee-127">Если подпись не найдена, используется начальное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="195ee-127">If the signature is not found, then the initial property value is used.</span></span> <span data-ttu-id="195ee-128">Если свойство не было инициализировано, свойство будет установлено только в том случае, если сигнатура найдена.</span><span class="sxs-lookup"><span data-stu-id="195ee-128">If the property was never initialized, then the property will only be set if the signature is found.</span></span> <span data-ttu-id="195ee-129">В противном случае свойство не определено.</span><span class="sxs-lookup"><span data-stu-id="195ee-129">Otherwise, the property is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="195ee-130"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Образец\_</span><span class="sxs-lookup"><span data-stu-id="195ee-130"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="195ee-131">Столбец сигнатуры \_ содержит уникальный идентификатор, называемый сигнатурой, который также является внешним ключом в таблицах [реглокатор](reglocator-table.md), [Инилокатор](inilocator-table.md), [комплокатор](complocator-table.md)и [дрлокатор](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="195ee-131">The Signature\_ column contains a unique identifier called a signature and is also an external key into the [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md), and [DrLocator](drlocator-table.md) tables.</span></span> <span data-ttu-id="195ee-132">При поиске файла значение в этом столбце также должно быть внешним ключом в таблице [сигнатур](signature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="195ee-132">When searching for a file, the value in this column must also be a foreign key into the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="195ee-133">Если значение в этом столбце не указано в таблице сигнатур, установщик определяет, что поиск выполняется для каталога.</span><span class="sxs-lookup"><span data-stu-id="195ee-133">If the value in this column is not listed in the Signature table, the installer determines that the search is for a directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="195ee-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="195ee-134">Remarks</span></span>

<span data-ttu-id="195ee-135">Действие [аппсеарч](appsearch-action.md) в [*таблицах последовательностей*](s-gly.md) обрабатывает сведения в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="195ee-135">The [AppSearch](appsearch-action.md) action in [*sequence tables*](s-gly.md) processes the information in this table.</span></span> <span data-ttu-id="195ee-136">Дополнительные сведения об использовании *таблиц последовательности* см. [в разделе Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="195ee-136">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="195ee-137">Действие [аппсеарч](appsearch-action.md) ищет подписи с использованием таблицы [комплокатор](complocator-table.md) First, таблицы [реглокатор](reglocator-table.md) , второй, [Инилокатор](inilocator-table.md) таблицы и, наконец, таблицы [дрлокатор](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="195ee-137">The [AppSearch](appsearch-action.md) action searches for signatures using the [CompLocator](complocator-table.md) table first, the [RegLocator](reglocator-table.md) table second, the [IniLocator](inilocator-table.md) table third, and finally the [DrLocator](drlocator-table.md) table.</span></span> <span data-ttu-id="195ee-138">Подписи файлов перечислены в таблице [сигнатур](signature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="195ee-138">File signatures are listed in the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="195ee-139">Подпись, не указанная в таблице сигнатур, обозначает каталог, а действие задает для свойства путь к каталогу для этой сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="195ee-139">A signature that is not in the Signature table denotes a directory and the action sets the property to the directory path for that signature.</span></span>

<span data-ttu-id="195ee-140">См. раздел [Поиск существующих приложений, файлов, записей реестра или INI-файлов](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="195ee-140">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="195ee-141">Проверка</span><span class="sxs-lookup"><span data-stu-id="195ee-141">Validation</span></span>

<dl>

[<span data-ttu-id="195ee-142">ICE03</span><span class="sxs-lookup"><span data-stu-id="195ee-142">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="195ee-143">ICE06</span><span class="sxs-lookup"><span data-stu-id="195ee-143">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="195ee-144">ICE32</span><span class="sxs-lookup"><span data-stu-id="195ee-144">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="195ee-145">ICE52</span><span class="sxs-lookup"><span data-stu-id="195ee-145">ICE52</span></span>](ice52.md)  
[<span data-ttu-id="195ee-146">ICE88</span><span class="sxs-lookup"><span data-stu-id="195ee-146">ICE88</span></span>](ice88.md)  
</dl>

 

 



