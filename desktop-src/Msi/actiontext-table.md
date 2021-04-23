---
description: Таблица Актионтекст содержит текст, отображаемый в диалоговом окне хода выполнения, и записывает в журнал действия, выполнение которых занимает много времени. Отображаемый текст состоит из описания действия и необязательного форматирования данных из действия.
ms.assetid: 88d18422-77d0-4929-9341-d078843cb2a9
title: Таблица Актионтекст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8071a8542571a3364e151522a7fc4c0b11362045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662965"
---
# <a name="actiontext-table"></a><span data-ttu-id="62113-104">Таблица Актионтекст</span><span class="sxs-lookup"><span data-stu-id="62113-104">ActionText Table</span></span>

<span data-ttu-id="62113-105">Таблица Актионтекст содержит текст, отображаемый в диалоговом окне хода выполнения, и записывает в журнал действия, выполнение которых занимает много времени.</span><span class="sxs-lookup"><span data-stu-id="62113-105">The ActionText Table contains text to be displayed in a progress dialog box, and written to the log for actions that take a long time to execute.</span></span> <span data-ttu-id="62113-106">Отображаемый текст состоит из описания действия и необязательного форматирования данных из действия.</span><span class="sxs-lookup"><span data-stu-id="62113-106">The displayed text consists of the action description and optionally formatted data from the action.</span></span>

<span data-ttu-id="62113-107">Таблица Актионтекст содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="62113-107">The ActionText Table has the following columns.</span></span>



| <span data-ttu-id="62113-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="62113-108">Column</span></span>      | <span data-ttu-id="62113-109">Type</span><span class="sxs-lookup"><span data-stu-id="62113-109">Type</span></span>                         | <span data-ttu-id="62113-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="62113-110">Key</span></span> | <span data-ttu-id="62113-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="62113-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="62113-112">Действие</span><span class="sxs-lookup"><span data-stu-id="62113-112">Action</span></span>      | [<span data-ttu-id="62113-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="62113-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="62113-114">Да</span><span class="sxs-lookup"><span data-stu-id="62113-114">Y</span></span>   | <span data-ttu-id="62113-115">Нет</span><span class="sxs-lookup"><span data-stu-id="62113-115">N</span></span>        |
| <span data-ttu-id="62113-116">Описание</span><span class="sxs-lookup"><span data-stu-id="62113-116">Description</span></span> | [<span data-ttu-id="62113-117">Text</span><span class="sxs-lookup"><span data-stu-id="62113-117">Text</span></span>](text.md)             | <span data-ttu-id="62113-118">Нет</span><span class="sxs-lookup"><span data-stu-id="62113-118">N</span></span>   | <span data-ttu-id="62113-119">Да</span><span class="sxs-lookup"><span data-stu-id="62113-119">Y</span></span>        |
| <span data-ttu-id="62113-120">Шаблон</span><span class="sxs-lookup"><span data-stu-id="62113-120">Template</span></span>    | [<span data-ttu-id="62113-121">Шаблон</span><span class="sxs-lookup"><span data-stu-id="62113-121">Template</span></span>](template.md)     | <span data-ttu-id="62113-122">Нет</span><span class="sxs-lookup"><span data-stu-id="62113-122">N</span></span>   | <span data-ttu-id="62113-123">Да</span><span class="sxs-lookup"><span data-stu-id="62113-123">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="62113-124">Столбцы</span><span class="sxs-lookup"><span data-stu-id="62113-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="62113-125"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Поддержки</span><span class="sxs-lookup"><span data-stu-id="62113-125"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="62113-126">Имя действия.</span><span class="sxs-lookup"><span data-stu-id="62113-126">Name of the action.</span></span>

<span data-ttu-id="62113-127">Первичный ключ таблицы.</span><span class="sxs-lookup"><span data-stu-id="62113-127">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="62113-128"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="62113-128"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="62113-129">Локализованное описание, которое отображается в диалоговом окне Ход выполнения, или записывается в журнал при выполнении действия.</span><span class="sxs-lookup"><span data-stu-id="62113-129">Localized description that is displayed in the progress dialog box, or written to the log when the action is executing.</span></span>

</dd> <dt>

<span data-ttu-id="62113-130"><span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Шаблон</span><span class="sxs-lookup"><span data-stu-id="62113-130"><span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Template</span></span>
</dt> <dd>

<span data-ttu-id="62113-131">Шаблон локализованного формата, используемый для форматирования записей данных действий, отображаемых во время выполнения действия.</span><span class="sxs-lookup"><span data-stu-id="62113-131">A localized format template that is used to format action data records to display during action execution.</span></span> <span data-ttu-id="62113-132">Если шаблон не указан, данные действия не отображаются.</span><span class="sxs-lookup"><span data-stu-id="62113-132">If a template is not supplied, then the action data is not displayed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62113-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62113-133">Remarks</span></span>

<span data-ttu-id="62113-134">Как правило, записи в таблице Актионтекст ссылаются на действия в таблицах последовательности.</span><span class="sxs-lookup"><span data-stu-id="62113-134">Typically, the entries in the ActionText table refer to actions in sequence tables.</span></span> <span data-ttu-id="62113-135">Существуют и другие действия, выполняемые установщиком, которые не перечислены в таблице последовательности, но по-прежнему необходимо указывать в таблице.</span><span class="sxs-lookup"><span data-stu-id="62113-135">There are other actions the installer performs that are not listed in the sequence table, but still need to be specified in the table.</span></span> <span data-ttu-id="62113-136">В следующей таблице указаны необходимые записи таблицы, в которых имя и шаблон действия должны быть созданы в точности так, как показано, но описание можно настроить.</span><span class="sxs-lookup"><span data-stu-id="62113-136">The following table identifies the required table entries where the action name and template must be authored exactly as shown, but the description can be customized.</span></span>



| <span data-ttu-id="62113-137">Действие</span><span class="sxs-lookup"><span data-stu-id="62113-137">Action</span></span>          | <span data-ttu-id="62113-138">Описание</span><span class="sxs-lookup"><span data-stu-id="62113-138">Description</span></span>                             | <span data-ttu-id="62113-139">Шаблон</span><span class="sxs-lookup"><span data-stu-id="62113-139">Template</span></span> |
|-----------------|-----------------------------------------|----------|
| <span data-ttu-id="62113-140">Откат</span><span class="sxs-lookup"><span data-stu-id="62113-140">Rollback</span></span>        | <span data-ttu-id="62113-141">Отменяет действия.</span><span class="sxs-lookup"><span data-stu-id="62113-141">Undoes actions.</span></span>                         | <span data-ttu-id="62113-142">\[1\]</span><span class="sxs-lookup"><span data-stu-id="62113-142">\[1\]</span></span>    |
| <span data-ttu-id="62113-143">роллбаккклеануп</span><span class="sxs-lookup"><span data-stu-id="62113-143">RollbackCleanup</span></span> | <span data-ttu-id="62113-144">Удаляет старые файлы.</span><span class="sxs-lookup"><span data-stu-id="62113-144">Removes old files.</span></span>                      | <span data-ttu-id="62113-145">\[1\]</span><span class="sxs-lookup"><span data-stu-id="62113-145">\[1\]</span></span>    |
| <span data-ttu-id="62113-146">женератескрипт</span><span class="sxs-lookup"><span data-stu-id="62113-146">GenerateScript</span></span>  | <span data-ttu-id="62113-147">Создает системные операции для действия.</span><span class="sxs-lookup"><span data-stu-id="62113-147">Generates system operations for action.</span></span> | <span data-ttu-id="62113-148">\[1\]</span><span class="sxs-lookup"><span data-stu-id="62113-148">\[1\]</span></span>    |



 

> [!Note]  
> <span data-ttu-id="62113-149">Текст действия отображается только для действий, выполняемых в скрипте установки.</span><span class="sxs-lookup"><span data-stu-id="62113-149">Action text is only displayed for actions that run within the installation script.</span></span> <span data-ttu-id="62113-150">Таким образом, текст действия отображается только для действий, которые упорядочены между действиями [инсталлинитиализе](installinitialize-action.md) и [функции InstallFinalize](installfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="62113-150">Therefore, action text is only displayed for actions that are sequenced between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) actions.</span></span>

 

<span data-ttu-id="62113-151">Вы можете импортировать локализованную таблицу Актионтекст в базу данных с помощью Msidb.exe или [**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="62113-151">You can import a localized ActionText table into your database by using Msidb.exe or [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="62113-152">Пакет SDK включает локализованную таблицу Актионтекст для каждого из языков, перечисленных в разделе [Локализация таблиц ошибок и актионтекст](localizing-the-error-and-actiontext-tables.md) .</span><span class="sxs-lookup"><span data-stu-id="62113-152">The SDK includes a localized ActionText Table for each of the languages listed in the [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md) section.</span></span> <span data-ttu-id="62113-153">Если таблица Актионтекст не заполнена, установщик загружает локализованные строки для языка, указанного в свойстве [**продуктлангуаже**](productlanguage.md) .</span><span class="sxs-lookup"><span data-stu-id="62113-153">If the ActionText table is not populated, the installer loads localized strings for the language specified by the [**ProductLanguage**](productlanguage.md) property.</span></span>

## <a name="validation"></a><span data-ttu-id="62113-154">Проверка</span><span class="sxs-lookup"><span data-stu-id="62113-154">Validation</span></span>

<dl>

[<span data-ttu-id="62113-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="62113-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="62113-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="62113-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="62113-157">ICE46</span><span class="sxs-lookup"><span data-stu-id="62113-157">ICE46</span></span>](ice46.md)  
</dl>

 

 



