---
description: Таблица свойств содержит имена и значения свойств для всех определенных свойств в установке. Свойства со значениями null отсутствуют в таблице.
ms.assetid: 1f4215b2-dc71-4e6e-bc2e-3b43316806b9
title: Таблица свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612ab63aa36de6cf91ec8176eefec84cef591c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813665"
---
# <a name="property-table"></a><span data-ttu-id="7b222-104">Таблица свойств</span><span class="sxs-lookup"><span data-stu-id="7b222-104">Property Table</span></span>

<span data-ttu-id="7b222-105">Таблица свойств содержит имена и значения свойств для всех определенных свойств в установке.</span><span class="sxs-lookup"><span data-stu-id="7b222-105">The Property table contains the property names and values for all defined properties in the installation.</span></span> <span data-ttu-id="7b222-106">Свойства со значениями null отсутствуют в таблице.</span><span class="sxs-lookup"><span data-stu-id="7b222-106">Properties with Null values are not present in the table.</span></span>

<span data-ttu-id="7b222-107">Таблица свойств содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="7b222-107">The Property table has the following columns.</span></span>



| <span data-ttu-id="7b222-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="7b222-108">Column</span></span>   | <span data-ttu-id="7b222-109">Type</span><span class="sxs-lookup"><span data-stu-id="7b222-109">Type</span></span>                         | <span data-ttu-id="7b222-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="7b222-110">Key</span></span> | <span data-ttu-id="7b222-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="7b222-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="7b222-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="7b222-112">Property</span></span> | [<span data-ttu-id="7b222-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="7b222-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="7b222-114">Да</span><span class="sxs-lookup"><span data-stu-id="7b222-114">Y</span></span>   | <span data-ttu-id="7b222-115">Нет</span><span class="sxs-lookup"><span data-stu-id="7b222-115">N</span></span>        |
| <span data-ttu-id="7b222-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7b222-116">Value</span></span>    | [<span data-ttu-id="7b222-117">Text</span><span class="sxs-lookup"><span data-stu-id="7b222-117">Text</span></span>](text.md)             | <span data-ttu-id="7b222-118">Нет</span><span class="sxs-lookup"><span data-stu-id="7b222-118">N</span></span>   | <span data-ttu-id="7b222-119">Нет</span><span class="sxs-lookup"><span data-stu-id="7b222-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7b222-120">Столбцы</span><span class="sxs-lookup"><span data-stu-id="7b222-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7b222-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Свойства</span><span class="sxs-lookup"><span data-stu-id="7b222-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="7b222-122">Имя свойства.</span><span class="sxs-lookup"><span data-stu-id="7b222-122">The name of a property.</span></span> <span data-ttu-id="7b222-123">См. раздел [Свойства](properties.md).</span><span class="sxs-lookup"><span data-stu-id="7b222-123">See [Properties](properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b222-124"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Значений</span><span class="sxs-lookup"><span data-stu-id="7b222-124"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="7b222-125">Локализуемое строковое значение для свойства.</span><span class="sxs-lookup"><span data-stu-id="7b222-125">A localizable string value for the property.</span></span> <span data-ttu-id="7b222-126">Это значение не может быть равно null или пустой строке.</span><span class="sxs-lookup"><span data-stu-id="7b222-126">This may never be Null or an empty string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b222-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b222-127">Remarks</span></span>

<span data-ttu-id="7b222-128">Обратите внимание, что нельзя использовать таблицу свойств, чтобы задать свойству значение другого свойства.</span><span class="sxs-lookup"><span data-stu-id="7b222-128">Note that you cannot use the Property table to set a property to the value of another property.</span></span> <span data-ttu-id="7b222-129">Программа установки не выполняет никаких действий с текстовой строкой, указанной в столбце значение, перед установкой свойства в столбце свойств.</span><span class="sxs-lookup"><span data-stu-id="7b222-129">The installer does nothing to the text string entered in the Value column before setting the property in the Property column.</span></span> <span data-ttu-id="7b222-130">Если Фирстпроперти входит в столбец свойств и \[ секондпроперти \] в столбце значение, значение фирстпроперти задается как текстовая строка " \[ секондпроперти \] ", а не как значение свойства секондпроперти.</span><span class="sxs-lookup"><span data-stu-id="7b222-130">If FirstProperty is entered into the Property column and \[SecondProperty\] in the Value column, the value of FirstProperty is set to the text string "\[SecondProperty\]" and not to the value of the SecondProperty property.</span></span> <span data-ttu-id="7b222-131">Это необходимо для предотвращения создания циклических ссылок в таблице свойств.</span><span class="sxs-lookup"><span data-stu-id="7b222-131">This is necessary to prevent creating circular references in the Property table.</span></span> <span data-ttu-id="7b222-132">Вместо этого можно установить одно свойство в другое с помощью [пользовательского действия типа 51](custom-action-type-51.md).</span><span class="sxs-lookup"><span data-stu-id="7b222-132">Instead, you can set one property to another by using a [Custom Action Type 51](custom-action-type-51.md).</span></span>

<span data-ttu-id="7b222-133">Обратите внимание, что свойство [**админпропертиес**](adminproperties.md) можно использовать для переопределения значений в таблице свойств во время [административной установки](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="7b222-133">Note that the [**AdminProperties**](adminproperties.md) property can be used to override the values in the Property table during an [Administrative Installation](administrative-installation.md).</span></span>

<span data-ttu-id="7b222-134">Не используйте свойства для паролей и других сведений, которые должны оставаться защищенными.</span><span class="sxs-lookup"><span data-stu-id="7b222-134">Do not use properties for passwords or other information that must remain secure.</span></span> <span data-ttu-id="7b222-135">Установщик может записать значение свойства, созданного в таблице свойств, или во время выполнения, в журнал или системный реестр.</span><span class="sxs-lookup"><span data-stu-id="7b222-135">The installer may write the value of a property authored into the Property table, or created at runtime, into a log or the system registry.</span></span>

## <a name="validation"></a><span data-ttu-id="7b222-136">Проверка</span><span class="sxs-lookup"><span data-stu-id="7b222-136">Validation</span></span>

<dl>

[<span data-ttu-id="7b222-137">ICE03</span><span class="sxs-lookup"><span data-stu-id="7b222-137">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7b222-138">ICE05</span><span class="sxs-lookup"><span data-stu-id="7b222-138">ICE05</span></span>](ice05.md)  
[<span data-ttu-id="7b222-139">ICE06</span><span class="sxs-lookup"><span data-stu-id="7b222-139">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7b222-140">ICE16</span><span class="sxs-lookup"><span data-stu-id="7b222-140">ICE16</span></span>](ice16.md)  
[<span data-ttu-id="7b222-141">ICE24</span><span class="sxs-lookup"><span data-stu-id="7b222-141">ICE24</span></span>](ice24.md)  
[<span data-ttu-id="7b222-142">ICE31</span><span class="sxs-lookup"><span data-stu-id="7b222-142">ICE31</span></span>](ice31.md)  
[<span data-ttu-id="7b222-143">ICE34</span><span class="sxs-lookup"><span data-stu-id="7b222-143">ICE34</span></span>](ice34.md)  
[<span data-ttu-id="7b222-144">ICE36</span><span class="sxs-lookup"><span data-stu-id="7b222-144">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="7b222-145">ICE40</span><span class="sxs-lookup"><span data-stu-id="7b222-145">ICE40</span></span>](ice40.md)  
[<span data-ttu-id="7b222-146">ICE46</span><span class="sxs-lookup"><span data-stu-id="7b222-146">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="7b222-147">ICE48</span><span class="sxs-lookup"><span data-stu-id="7b222-147">ICE48</span></span>](ice48.md)  
[<span data-ttu-id="7b222-148">ICE52</span><span class="sxs-lookup"><span data-stu-id="7b222-148">ICE52</span></span>](ice52.md)  
[<span data-ttu-id="7b222-149">ICE61</span><span class="sxs-lookup"><span data-stu-id="7b222-149">ICE61</span></span>](ice61.md)  
[<span data-ttu-id="7b222-150">ICE73</span><span class="sxs-lookup"><span data-stu-id="7b222-150">ICE73</span></span>](ice73.md)  
[<span data-ttu-id="7b222-151">ICE74</span><span class="sxs-lookup"><span data-stu-id="7b222-151">ICE74</span></span>](ice74.md)  
[<span data-ttu-id="7b222-152">ICE80</span><span class="sxs-lookup"><span data-stu-id="7b222-152">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="7b222-153">ICE87</span><span class="sxs-lookup"><span data-stu-id="7b222-153">ICE87</span></span>](ice87.md)  
[<span data-ttu-id="7b222-154">ICE88</span><span class="sxs-lookup"><span data-stu-id="7b222-154">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="7b222-155">ICE91</span><span class="sxs-lookup"><span data-stu-id="7b222-155">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="7b222-156">ICE99</span><span class="sxs-lookup"><span data-stu-id="7b222-156">ICE99</span></span>](ice99.md)  
</dl>

 

 



