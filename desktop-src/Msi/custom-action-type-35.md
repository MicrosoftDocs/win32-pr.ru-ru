---
description: Разработчики установщик Windowsных пакетов могут использовать настраиваемое действие типа 35, если стандартные действия недостаточны для выполнения установки.
ms.assetid: b88b5f48-5353-4876-9dda-2eeda288fa4b
title: Тип настраиваемого действия 35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8401f26f40ccc7de811ea0d290d556789284680f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664489"
---
# <a name="custom-action-type-35"></a><span data-ttu-id="a9be0-103">Тип настраиваемого действия 35</span><span class="sxs-lookup"><span data-stu-id="a9be0-103">Custom Action Type 35</span></span>

<span data-ttu-id="a9be0-104">Это пользовательское действие задает каталог установки из форматированной текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="a9be0-104">This custom action sets the install directory from a formatted text string.</span></span> <span data-ttu-id="a9be0-105">Дополнительные сведения см. [в разделе изменение целевого расположения каталога](changing-the-target-location-for-a-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="a9be0-105">For more information, see [Changing the Target Location for a Directory](changing-the-target-location-for-a-directory.md)</span></span>

## <a name="source"></a><span data-ttu-id="a9be0-106">Источник</span><span class="sxs-lookup"><span data-stu-id="a9be0-106">Source</span></span>

<span data-ttu-id="a9be0-107">Исходное поле [таблицы CustomAction](customaction-table.md) содержит ключ к [таблице каталога](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="a9be0-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Directory table](directory-table.md).</span></span> <span data-ttu-id="a9be0-108">Указанный каталог задается форматированной строкой в целевом поле с помощью [**мсисеттаржетпас**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha).</span><span class="sxs-lookup"><span data-stu-id="a9be0-108">The designated directory is set by the formatted string in the Target field using [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha).</span></span> <span data-ttu-id="a9be0-109">Этот параметр задает для целевого пути и связанного свойства расширенное значение форматированной текстовой строки в целевом поле.</span><span class="sxs-lookup"><span data-stu-id="a9be0-109">This sets the target path and associated property to the expanded value of the formatted text string in the Target field.</span></span> <span data-ttu-id="a9be0-110">Не пытайтесь изменить расположение целевого каталога во время [установки обслуживания](maintenance-installation.md).</span><span class="sxs-lookup"><span data-stu-id="a9be0-110">Do not attempt to change the location of a target directory during a [maintenance installation](maintenance-installation.md).</span></span> <span data-ttu-id="a9be0-111">Не пытайтесь изменить путь к целевому каталогу, если некоторые компоненты, использующие этот путь, уже установлены для любого пользователя.</span><span class="sxs-lookup"><span data-stu-id="a9be0-111">Do not attempt to change the target directory path if some components using that path are already installed for any user.</span></span>

## <a name="type-value"></a><span data-ttu-id="a9be0-112">Значение типа</span><span class="sxs-lookup"><span data-stu-id="a9be0-112">Type Value</span></span>

<span data-ttu-id="a9be0-113">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип.</span><span class="sxs-lookup"><span data-stu-id="a9be0-113">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="a9be0-114">Константы</span><span class="sxs-lookup"><span data-stu-id="a9be0-114">Constants</span></span>                                                              | <span data-ttu-id="a9be0-115">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="a9be0-115">Hexadecimal</span></span> | <span data-ttu-id="a9be0-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="a9be0-116">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="a9be0-117">**мсидбкустомактионтипетекстдата**  +  **мсидбкустомактионтипедиректори**</span><span class="sxs-lookup"><span data-stu-id="a9be0-117">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="a9be0-118">0x023</span><span class="sxs-lookup"><span data-stu-id="a9be0-118">0x023</span></span>       | <span data-ttu-id="a9be0-119">35</span><span class="sxs-lookup"><span data-stu-id="a9be0-119">35</span></span>      |



 

## <a name="target"></a><span data-ttu-id="a9be0-120">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="a9be0-120">Target</span></span>

<span data-ttu-id="a9be0-121">Целевой столбец [таблицы CustomAction](customaction-table.md) содержит текстовую строку, отформатированную с помощью функций, указанных в [**мсиформатрекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (без описателей числовых полей).</span><span class="sxs-lookup"><span data-stu-id="a9be0-121">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="a9be0-122">Заменяющие параметры заключаются в квадратные скобки \[ ... \] и могут быть свойствами, переменными среды (% prefix), путями к файлам ( \# префиксом) или путями к каталогам компонентов ($ prefix).</span><span class="sxs-lookup"><span data-stu-id="a9be0-122">Parameters to be replaced are enclosed in square brackets \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span> <span data-ttu-id="a9be0-123">Обратите внимание, что пути к каталогу всегда заканчиваются разделителем каталогов.</span><span class="sxs-lookup"><span data-stu-id="a9be0-123">Note that directory paths always end with a directory separator.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="a9be0-124">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="a9be0-124">Return Processing Options</span></span>

<span data-ttu-id="a9be0-125">Пользовательское действие не использует эти параметры.</span><span class="sxs-lookup"><span data-stu-id="a9be0-125">The custom action does not use these options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="a9be0-126">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="a9be0-126">Execution Scheduling Options</span></span>

<span data-ttu-id="a9be0-127">Включите дополнительные биты флагов в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры планирования выполнения.</span><span class="sxs-lookup"><span data-stu-id="a9be0-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="a9be0-128">Эти параметры управляют несколькими выполнениями пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="a9be0-128">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="a9be0-129">Описание параметров см. в разделе [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="a9be0-129">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="a9be0-130">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="a9be0-130">In-Script Execution Options</span></span>

<span data-ttu-id="a9be0-131">Пользовательское действие не использует эти параметры.</span><span class="sxs-lookup"><span data-stu-id="a9be0-131">The custom action does not use these options.</span></span>

## <a name="return-values"></a><span data-ttu-id="a9be0-132">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a9be0-132">Return Values</span></span>

<span data-ttu-id="a9be0-133">См. раздел [возвращаемые значения пользовательских действий](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a9be0-133">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a9be0-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9be0-134">Remarks</span></span>

<span data-ttu-id="a9be0-135">Если задать [свойство Private](private-properties.md) в последовательности пользовательского интерфейса путем создания настраиваемого действия в одной из таблиц последовательности пользовательского интерфейса, это свойство не будет задано в последовательности выполнения.</span><span class="sxs-lookup"><span data-stu-id="a9be0-135">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="a9be0-136">Чтобы задать свойство в последовательности выполнения, необходимо также добавить пользовательское действие в таблицу последовательности выполнения.</span><span class="sxs-lookup"><span data-stu-id="a9be0-136">To set the property in the execution sequence you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="a9be0-137">Кроме того, можно сделать свойство [общедоступным](public-properties.md) и включить его в [**свойство секурекустомпропертиес**](securecustomproperties.md).</span><span class="sxs-lookup"><span data-stu-id="a9be0-137">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties property**](securecustomproperties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9be0-138">См. также</span><span class="sxs-lookup"><span data-stu-id="a9be0-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9be0-139">Настраиваемые \_ действия</span><span class="sxs-lookup"><span data-stu-id="a9be0-139">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="a9be0-140">Настраиваемые действия форматированного текста</span><span class="sxs-lookup"><span data-stu-id="a9be0-140">Formatted Text Custom Actions</span></span>](formatted-text-custom-actions.md)
</dt> </dl>

 

 



