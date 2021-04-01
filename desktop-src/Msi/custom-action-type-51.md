---
description: Разработчики установщик Windowsных пакетов могут использовать настраиваемое действие типа 51, если стандартные действия недостаточны для выполнения установки.
ms.assetid: cdad16ad-426c-4e04-8003-b32c67be7329
title: Тип настраиваемого действия 51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3224add3a425131ee3308bc4f610b086cd99a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999111"
---
# <a name="custom-action-type-51"></a><span data-ttu-id="a0e18-103">Тип настраиваемого действия 51</span><span class="sxs-lookup"><span data-stu-id="a0e18-103">Custom Action Type 51</span></span>

<span data-ttu-id="a0e18-104">Это пользовательское действие задает свойство из форматированной текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="a0e18-104">This custom action sets a property from a formatted text string.</span></span>

<span data-ttu-id="a0e18-105">Чтобы изменить свойство, используемое в условии компонента или функции, пользовательское действие должно быть перед [действием костфинализе](costfinalize-action.md) в последовательности действий.</span><span class="sxs-lookup"><span data-stu-id="a0e18-105">To affect a property used in a condition on a component or feature, the custom action must come before the [CostFinalize action](costfinalize-action.md) in the action sequence.</span></span>

## <a name="source"></a><span data-ttu-id="a0e18-106">Источник</span><span class="sxs-lookup"><span data-stu-id="a0e18-106">Source</span></span>

<span data-ttu-id="a0e18-107">Исходное поле [таблицы CustomAction](customaction-table.md) может содержать либо имя свойства, либо ключ для [таблицы свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="a0e18-107">The Source field of the [CustomAction table](customaction-table.md) can contain either the name of a property or a key to the [Property table](property-table.md).</span></span> <span data-ttu-id="a0e18-108">Это свойство задается форматированной строкой в целевом поле с помощью [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya).</span><span class="sxs-lookup"><span data-stu-id="a0e18-108">This property is set by the formatted string in the Target field using [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya).</span></span>

## <a name="type-value"></a><span data-ttu-id="a0e18-109">Значение типа</span><span class="sxs-lookup"><span data-stu-id="a0e18-109">Type Value</span></span>

<span data-ttu-id="a0e18-110">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип.</span><span class="sxs-lookup"><span data-stu-id="a0e18-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="a0e18-111">Константы</span><span class="sxs-lookup"><span data-stu-id="a0e18-111">Constants</span></span>                                                             | <span data-ttu-id="a0e18-112">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="a0e18-112">Hexadecimal</span></span> | <span data-ttu-id="a0e18-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="a0e18-113">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="a0e18-114">**мсидбкустомактионтипетекстдата**  +  **мсидбкустомактионтипепроперти**</span><span class="sxs-lookup"><span data-stu-id="a0e18-114">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="a0e18-115">0x033</span><span class="sxs-lookup"><span data-stu-id="a0e18-115">0x033</span></span>       | <span data-ttu-id="a0e18-116">51</span><span class="sxs-lookup"><span data-stu-id="a0e18-116">51</span></span>      |



 

## <a name="target"></a><span data-ttu-id="a0e18-117">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="a0e18-117">Target</span></span>

<span data-ttu-id="a0e18-118">Целевой столбец [таблицы CustomAction](customaction-table.md) содержит текстовую строку, отформатированную с помощью функций, указанных в [**мсиформатрекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (без описателей числовых полей).</span><span class="sxs-lookup"><span data-stu-id="a0e18-118">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="a0e18-119">Заменяемые параметры заключаются в квадратные скобки,.. \[ . \] и могут быть свойствами, переменными среды (% prefix), путями к файлам ( \# префиксом) или путями к каталогам компонентов ($ prefix).</span><span class="sxs-lookup"><span data-stu-id="a0e18-119">Parameters to be replaced are enclosed in square brackets, \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="a0e18-120">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="a0e18-120">Return Processing Options</span></span>

<span data-ttu-id="a0e18-121">Пользовательское действие не использует эти параметры.</span><span class="sxs-lookup"><span data-stu-id="a0e18-121">The custom action does not use these options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="a0e18-122">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="a0e18-122">Execution Scheduling Options</span></span>

<span data-ttu-id="a0e18-123">Включите дополнительные биты флагов в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры планирования выполнения.</span><span class="sxs-lookup"><span data-stu-id="a0e18-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="a0e18-124">Эти параметры управляют несколькими выполнениями пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="a0e18-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="a0e18-125">Описание параметров см. в разделе [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="a0e18-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="a0e18-126">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="a0e18-126">In-Script Execution Options</span></span>

<span data-ttu-id="a0e18-127">Пользовательское действие не использует эти параметры.</span><span class="sxs-lookup"><span data-stu-id="a0e18-127">The custom action does not use these options.</span></span>

## <a name="return-values"></a><span data-ttu-id="a0e18-128">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a0e18-128">Return Values</span></span>

<span data-ttu-id="a0e18-129">См. раздел [возвращаемые значения пользовательских действий](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a0e18-129">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a0e18-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0e18-130">Remarks</span></span>

<span data-ttu-id="a0e18-131">Если задать [свойство Private](private-properties.md) в последовательности пользовательского интерфейса путем создания настраиваемого действия в одной из таблиц последовательности пользовательского интерфейса, это свойство не будет задано в последовательности выполнения.</span><span class="sxs-lookup"><span data-stu-id="a0e18-131">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="a0e18-132">Чтобы задать свойство в последовательности выполнения, необходимо также добавить пользовательское действие в таблицу последовательности выполнения.</span><span class="sxs-lookup"><span data-stu-id="a0e18-132">To set the property in the execution sequence, you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="a0e18-133">Кроме того, можно сделать свойство [общедоступным](public-properties.md) и включить его в [**свойство секурекустомпропертиес**](securecustomproperties.md).</span><span class="sxs-lookup"><span data-stu-id="a0e18-133">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties property**](securecustomproperties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0e18-134">См. также</span><span class="sxs-lookup"><span data-stu-id="a0e18-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0e18-135">Настраиваемые \_ действия</span><span class="sxs-lookup"><span data-stu-id="a0e18-135">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="a0e18-136">Настраиваемые действия форматированного текста</span><span class="sxs-lookup"><span data-stu-id="a0e18-136">Formatted Text Custom Actions</span></span>](formatted-text-custom-actions.md)
</dt> </dl>

 

 



