---
description: Таблица Комплокатор содержит сведения, необходимые для поиска файла или каталога, использующего данные конфигурации установщика.
ms.assetid: 8b527307-51bf-47b3-a0b2-3421cc5278b7
title: Таблица Комплокатор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9fcb4a3c4f2e2c6f3ca3c92f6dc7466326bd11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547010"
---
# <a name="complocator-table"></a><span data-ttu-id="09f94-103">Таблица Комплокатор</span><span class="sxs-lookup"><span data-stu-id="09f94-103">CompLocator Table</span></span>

<span data-ttu-id="09f94-104">Таблица Комплокатор содержит сведения, необходимые для поиска файла или каталога, использующего данные конфигурации установщика.</span><span class="sxs-lookup"><span data-stu-id="09f94-104">The CompLocator Table contains the information needed to find a file or directory that is using the installer configuration data.</span></span>

<span data-ttu-id="09f94-105">Таблица Комплокатор содержит следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="09f94-105">The CompLocator table contains the following information.</span></span>



| <span data-ttu-id="09f94-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="09f94-106">Column</span></span>      | <span data-ttu-id="09f94-107">Type</span><span class="sxs-lookup"><span data-stu-id="09f94-107">Type</span></span>                         | <span data-ttu-id="09f94-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="09f94-108">Key</span></span> | <span data-ttu-id="09f94-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="09f94-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="09f94-110">Образец\_</span><span class="sxs-lookup"><span data-stu-id="09f94-110">Signature\_</span></span> | [<span data-ttu-id="09f94-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="09f94-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="09f94-112">Да</span><span class="sxs-lookup"><span data-stu-id="09f94-112">Y</span></span>   | <span data-ttu-id="09f94-113">Нет</span><span class="sxs-lookup"><span data-stu-id="09f94-113">N</span></span>        |
| <span data-ttu-id="09f94-114">ComponentId</span><span class="sxs-lookup"><span data-stu-id="09f94-114">ComponentId</span></span> | [<span data-ttu-id="09f94-115">GUID</span><span class="sxs-lookup"><span data-stu-id="09f94-115">GUID</span></span>](guid.md)             | <span data-ttu-id="09f94-116">Нет</span><span class="sxs-lookup"><span data-stu-id="09f94-116">N</span></span>   | <span data-ttu-id="09f94-117">Нет</span><span class="sxs-lookup"><span data-stu-id="09f94-117">N</span></span>        |
| <span data-ttu-id="09f94-118">Тип</span><span class="sxs-lookup"><span data-stu-id="09f94-118">Type</span></span>        | [<span data-ttu-id="09f94-119">Integer</span><span class="sxs-lookup"><span data-stu-id="09f94-119">Integer</span></span>](integer.md)       | <span data-ttu-id="09f94-120">Нет</span><span class="sxs-lookup"><span data-stu-id="09f94-120">N</span></span>   | <span data-ttu-id="09f94-121">Да</span><span class="sxs-lookup"><span data-stu-id="09f94-121">Y</span></span>        |



 

## <a name="column-information"></a><span data-ttu-id="09f94-122">Сведения о столбце</span><span class="sxs-lookup"><span data-stu-id="09f94-122">Column Information</span></span>

<dl> <dt>

<span data-ttu-id="09f94-123"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Образец\_</span><span class="sxs-lookup"><span data-stu-id="09f94-123"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="09f94-124">Этот столбец представляет уникальную сигнатуру файла и является также внешним ключом в [таблице сигнатур](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="09f94-124">This column represents a unique file signature and is also the external key into the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="09f94-125">Если ключ отсутствует в таблице сигнатур, то предполагается, что поиск находится в каталоге, на который указывает таблица Комплокатор.</span><span class="sxs-lookup"><span data-stu-id="09f94-125">If the key is absent from the Signature Table, the search is assumed to be for the presence of a directory pointed to by the CompLocator Table.</span></span>

</dd> <dt>

<span data-ttu-id="09f94-126"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span><span class="sxs-lookup"><span data-stu-id="09f94-126"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span></span>
</dt> <dd>

<span data-ttu-id="09f94-127">Идентификатор компонента компонента, путь к ключу которого должен использоваться для поиска.</span><span class="sxs-lookup"><span data-stu-id="09f94-127">The component ID of the component whose key path is to be used for the search.</span></span> <span data-ttu-id="09f94-128">Это должен быть идентификатор GUID компонента, который отображается в поле ComponentId [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="09f94-128">This should be the GUID of a component that appears in the ComponentId field of the [Component Table](component-table.md).</span></span> <span data-ttu-id="09f94-129">Это может быть идентификатор компонента компонента, принадлежащего другому продукту, установленному на компьютере.</span><span class="sxs-lookup"><span data-stu-id="09f94-129">It may be the component ID of a component belonging to another product installed on the computer.</span></span> <span data-ttu-id="09f94-130">Он не должен быть идентификатором GUID опубликованного компонента, отображаемого в поле ComponentId [таблицы публишкомпонент](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="09f94-130">It should not be the GUID of a published component appearing in the ComponentId field of the [PublishComponent Table](publishcomponent-table.md).</span></span>

<span data-ttu-id="09f94-131">Чтобы найти значение GUID идентификатора компонента для файла, установленного другим продуктом, перейдите в пакет установки продукта.</span><span class="sxs-lookup"><span data-stu-id="09f94-131">To find the component ID GUID value for a file installed by another product, go to the installation package of the product.</span></span> <span data-ttu-id="09f94-132">Перейдите к [таблице File](file-table.md) и найдите строку, содержащую идентификатор файла.</span><span class="sxs-lookup"><span data-stu-id="09f94-132">Go to the [File Table](file-table.md) and find the row that contains the file identifier for the file.</span></span> <span data-ttu-id="09f94-133">Столбец Component \_ этой строки содержит идентификатор компонента для компонента, управляющего файлом.</span><span class="sxs-lookup"><span data-stu-id="09f94-133">The Component\_ column of this row contains the component identifier for the component that controls the file.</span></span> <span data-ttu-id="09f94-134">Перейдите к [таблице Component](component-table.md) и найдите строку, содержащую этот идентификатор компонента, в столбце Component.</span><span class="sxs-lookup"><span data-stu-id="09f94-134">Go to the [Component table](component-table.md) and find the row that contains this component identifier in the Component column.</span></span> <span data-ttu-id="09f94-135">Столбец ComponentId этой строки содержит идентификатор GUID компонента.</span><span class="sxs-lookup"><span data-stu-id="09f94-135">The ComponentId column of this row contains the component ID GUID.</span></span>

</dd> <dt>

<span data-ttu-id="09f94-136"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Тип</span><span class="sxs-lookup"><span data-stu-id="09f94-136"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="09f94-137">Логическое значение, определяющее, является ли путь к ключу компонента именем файла или расположением каталога.</span><span class="sxs-lookup"><span data-stu-id="09f94-137">A Boolean value that determines if the key path of the component is a file name or a directory location.</span></span>

<span data-ttu-id="09f94-138">В следующей таблице перечислены допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="09f94-138">The following table lists valid values.</span></span> <span data-ttu-id="09f94-139">Если он отсутствует, для параметра Тип задано значение 1 (один).</span><span class="sxs-lookup"><span data-stu-id="09f94-139">If absent, Type is set to be 1 (one).</span></span>



| <span data-ttu-id="09f94-140">Константа</span><span class="sxs-lookup"><span data-stu-id="09f94-140">Constant</span></span>                      | <span data-ttu-id="09f94-141">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="09f94-141">Hexadecimal</span></span> | <span data-ttu-id="09f94-142">Decimal</span><span class="sxs-lookup"><span data-stu-id="09f94-142">Decimal</span></span> | <span data-ttu-id="09f94-143">Описание</span><span class="sxs-lookup"><span data-stu-id="09f94-143">Description</span></span>              |
|-------------------------------|-------------|---------|--------------------------|
| <span data-ttu-id="09f94-144">**мсидблокатортипедиректори**</span><span class="sxs-lookup"><span data-stu-id="09f94-144">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="09f94-145">0x000</span><span class="sxs-lookup"><span data-stu-id="09f94-145">0x000</span></span>       | <span data-ttu-id="09f94-146">0</span><span class="sxs-lookup"><span data-stu-id="09f94-146">0</span></span>       | <span data-ttu-id="09f94-147">Путь к разделу — это каталог.</span><span class="sxs-lookup"><span data-stu-id="09f94-147">Key path is a directory.</span></span> |
| <span data-ttu-id="09f94-148">**мсидблокатортипефиленаме**</span><span class="sxs-lookup"><span data-stu-id="09f94-148">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="09f94-149">0x001</span><span class="sxs-lookup"><span data-stu-id="09f94-149">0x001</span></span>       | <span data-ttu-id="09f94-150">1</span><span class="sxs-lookup"><span data-stu-id="09f94-150">1</span></span>       | <span data-ttu-id="09f94-151">Путь к разделу — это имя файла.</span><span class="sxs-lookup"><span data-stu-id="09f94-151">Key path is a file name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09f94-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="09f94-152">Remarks</span></span>

<span data-ttu-id="09f94-153">Эта таблица используется с [таблицей аппсеарч](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="09f94-153">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="09f94-154">Как правило, столбцы в этой таблице не локализуются.</span><span class="sxs-lookup"><span data-stu-id="09f94-154">Typically, the columns in this table are not localized.</span></span> <span data-ttu-id="09f94-155">Если автор решает выполнить поиск продуктов на нескольких языках, в таблице для каждого языка может присутствовать отдельная запись.</span><span class="sxs-lookup"><span data-stu-id="09f94-155">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="09f94-156">Дополнительные сведения см. в разделе [Поиск существующих приложений, файлов, записей реестра или INI-файлов](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="09f94-156">For more information, see [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="09f94-157">Проверка</span><span class="sxs-lookup"><span data-stu-id="09f94-157">Validation</span></span>

<dl>

[<span data-ttu-id="09f94-158">ICE03</span><span class="sxs-lookup"><span data-stu-id="09f94-158">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="09f94-159">ICE06</span><span class="sxs-lookup"><span data-stu-id="09f94-159">ICE06</span></span>](ice06.md)  
</dl>

 

 



