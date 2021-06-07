---
title: Строковый элемент
description: Представляет строковый ресурс.
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- Лента для строковых элементов Windows
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b0dab5d7ce1485aad5fe1e15442069c488933aa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443905"
---
# <a name="string-element"></a><span data-ttu-id="e32bf-104">Строковый элемент</span><span class="sxs-lookup"><span data-stu-id="e32bf-104">String element</span></span>

<span data-ttu-id="e32bf-105">Представляет строковый ресурс.</span><span class="sxs-lookup"><span data-stu-id="e32bf-105">Represents a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="e32bf-106">Использование</span><span class="sxs-lookup"><span data-stu-id="e32bf-106">Usage</span></span>

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
```

## <a name="attributes"></a><span data-ttu-id="e32bf-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e32bf-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e32bf-108">attribute</span><span class="sxs-lookup"><span data-stu-id="e32bf-108">Attribute</span></span></th>
<th><span data-ttu-id="e32bf-109">Тип</span><span class="sxs-lookup"><span data-stu-id="e32bf-109">Type</span></span></th>
<th><span data-ttu-id="e32bf-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="e32bf-110">Required</span></span></th>
<th><span data-ttu-id="e32bf-111">Описание</span><span class="sxs-lookup"><span data-stu-id="e32bf-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e32bf-112"><strong>Содержимое</strong></span><span class="sxs-lookup"><span data-stu-id="e32bf-112"><strong>Content</strong></span></span><br/></td>
<td><span data-ttu-id="e32bf-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="e32bf-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="e32bf-114">Нет</span><span class="sxs-lookup"><span data-stu-id="e32bf-114">No</span></span><br/></td>
<td><span data-ttu-id="e32bf-115"><dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="e32bf-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e32bf-116">Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="e32bf-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e32bf-117"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="e32bf-117"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="e32bf-118">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="e32bf-118">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="e32bf-119">Нет</span><span class="sxs-lookup"><span data-stu-id="e32bf-119">No</span></span><br/></td>
<td><span data-ttu-id="e32bf-120">Уникальный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="e32bf-120">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="e32bf-121">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="e32bf-121">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e32bf-122">Целочисленное значение в диапазоне от 2 до 59999, включительно или 0x2 и 0xea5f в шестнадцатеричном, включающем.</span><span class="sxs-lookup"><span data-stu-id="e32bf-122">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="e32bf-123">Максимальная длина — 10 символов, включая необязательные нули в начале.</span><span class="sxs-lookup"><span data-stu-id="e32bf-123">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e32bf-124"><strong>Символ</strong></span><span class="sxs-lookup"><span data-stu-id="e32bf-124"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="e32bf-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="e32bf-125">xs:string</span></span><br/></td>
<td><span data-ttu-id="e32bf-126">Нет</span><span class="sxs-lookup"><span data-stu-id="e32bf-126">No</span></span><br/></td>
<td><span data-ttu-id="e32bf-127">Символ ресурса для строки.</span><span class="sxs-lookup"><span data-stu-id="e32bf-127">The resource symbol for the string.</span></span><br/> <br/><span data-ttu-id="e32bf-128">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="e32bf-128">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e32bf-129">Буква или символ подчеркивания, за которым следует любая последовательность букв, цифр или знаков подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="e32bf-129">A letter or underscore followed by any sequence of letters, digits, or underscores.</span></span><br/> <span data-ttu-id="e32bf-130">Максимальная длина — 100 символов.</span><span class="sxs-lookup"><span data-stu-id="e32bf-130">The maximum length is 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="e32bf-131">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e32bf-131">Child elements</span></span>



| <span data-ttu-id="e32bf-132">Элемент</span><span class="sxs-lookup"><span data-stu-id="e32bf-132">Element</span></span>                                                                   | <span data-ttu-id="e32bf-133">Описание</span><span class="sxs-lookup"><span data-stu-id="e32bf-133">Description</span></span>                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="e32bf-134">**String. Content**</span><span class="sxs-lookup"><span data-stu-id="e32bf-134">**String.Content**</span></span>](windowsribbon-element-string-content.md)<br/> | <span data-ttu-id="e32bf-135">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="e32bf-135">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="e32bf-136">**String.Id**</span><span class="sxs-lookup"><span data-stu-id="e32bf-136">**String.Id**</span></span>](windowsribbon-element-string-id.md)<br/>           | <span data-ttu-id="e32bf-137">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="e32bf-137">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="e32bf-138">**String. Symbol**</span><span class="sxs-lookup"><span data-stu-id="e32bf-138">**String.Symbol**</span></span>](windowsribbon-element-string-symbol.md)<br/>   | <span data-ttu-id="e32bf-139">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="e32bf-139">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="e32bf-140">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e32bf-140">Parent elements</span></span>



| <span data-ttu-id="e32bf-141">Элемент</span><span class="sxs-lookup"><span data-stu-id="e32bf-141">Element</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e32bf-142">**Command. keytip**</span><span class="sxs-lookup"><span data-stu-id="e32bf-142">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                         |
| [<span data-ttu-id="e32bf-143">**Command. Лабелдескриптион**</span><span class="sxs-lookup"><span data-stu-id="e32bf-143">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>     |
| [<span data-ttu-id="e32bf-144">**Command. Лабелтитле**</span><span class="sxs-lookup"><span data-stu-id="e32bf-144">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [<span data-ttu-id="e32bf-145">**Command. Тултипдескриптион**</span><span class="sxs-lookup"><span data-stu-id="e32bf-145">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [<span data-ttu-id="e32bf-146">**Command. Тултиптитле**</span><span class="sxs-lookup"><span data-stu-id="e32bf-146">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a><span data-ttu-id="e32bf-147">Remarks</span><span class="sxs-lookup"><span data-stu-id="e32bf-147">Remarks</span></span>

<span data-ttu-id="e32bf-148">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e32bf-148">Optional.</span></span>

<span data-ttu-id="e32bf-149">Может встречаться не более одного раза для каждой [**команды Command. лабелтитле**](windowsribbon-element-command-labeltitle.md), [**Command. лабелдескриптион**](windowsribbon-element-command-labeldescription.md), [**Command. KeyTip**](windowsribbon-element-command-keytip.md), [**Command. тултиптитле**](windowsribbon-element-command-tooltiptitle.md)или элемента [**Command. тултипдескриптион**](windowsribbon-element-command-tooltipdescription.md) .</span><span class="sxs-lookup"><span data-stu-id="e32bf-149">May occur at most once for each [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command.Keytip**](windowsribbon-element-command-keytip.md), [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), or [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) element.</span></span>

<span data-ttu-id="e32bf-150">Определение строки добавляется в файл заголовка ленты, например `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="e32bf-150">The string definition is added to the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="e32bf-151">Строка добавляется в таблицу строк в файле ресурсов ленты, где платформа Ribbon создает имя и идентификатор, если они не объявлены.</span><span class="sxs-lookup"><span data-stu-id="e32bf-151">The string is added to a string table in the Ribbon resource file where a name and ID are generated by the Ribbon framework if none are declared.</span></span>

## <a name="examples"></a><span data-ttu-id="e32bf-152">Примеры</span><span class="sxs-lookup"><span data-stu-id="e32bf-152">Examples</span></span>

<span data-ttu-id="e32bf-153">В следующем примере показана разметка для элемента [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) с объявлением **строки** .</span><span class="sxs-lookup"><span data-stu-id="e32bf-153">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a><span data-ttu-id="e32bf-154">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e32bf-154">Element information</span></span>

- <span data-ttu-id="e32bf-155">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="e32bf-155">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="e32bf-156">**Может быть пустым**: нет</span><span class="sxs-lookup"><span data-stu-id="e32bf-156">**Can be empty**: No</span></span>



 

 





