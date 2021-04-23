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
ms.openlocfilehash: 577d318292081dddf4e2839967642c6115a474d6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069060"
---
# <a name="string-element"></a><span data-ttu-id="0b101-104">Строковый элемент</span><span class="sxs-lookup"><span data-stu-id="0b101-104">String element</span></span>

<span data-ttu-id="0b101-105">Представляет строковый ресурс.</span><span class="sxs-lookup"><span data-stu-id="0b101-105">Represents a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="0b101-106">Использование</span><span class="sxs-lookup"><span data-stu-id="0b101-106">Usage</span></span>

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
```

## <a name="attributes"></a><span data-ttu-id="0b101-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0b101-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0b101-108">attribute</span><span class="sxs-lookup"><span data-stu-id="0b101-108">Attribute</span></span></th>
<th><span data-ttu-id="0b101-109">Тип</span><span class="sxs-lookup"><span data-stu-id="0b101-109">Type</span></span></th>
<th><span data-ttu-id="0b101-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="0b101-110">Required</span></span></th>
<th><span data-ttu-id="0b101-111">Описание</span><span class="sxs-lookup"><span data-stu-id="0b101-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0b101-112"><strong>Содержимое</strong></span><span class="sxs-lookup"><span data-stu-id="0b101-112"><strong>Content</strong></span></span><br/></td>
<td><span data-ttu-id="0b101-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="0b101-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="0b101-114">Нет</span><span class="sxs-lookup"><span data-stu-id="0b101-114">No</span></span><br/></td>
<td><span data-ttu-id="0b101-115"><dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="0b101-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0b101-116">Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="0b101-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b101-117"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="0b101-117"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="0b101-118">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="0b101-118">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="0b101-119">Нет</span><span class="sxs-lookup"><span data-stu-id="0b101-119">No</span></span><br/></td>
<td><span data-ttu-id="0b101-120">Уникальный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="0b101-120">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="0b101-121">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="0b101-121">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0b101-122">Целочисленное значение в диапазоне от 2 до 59999, включительно или 0x2 и 0xea5f в шестнадцатеричном, включающем.</span><span class="sxs-lookup"><span data-stu-id="0b101-122">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="0b101-123">Максимальная длина — 10 символов, включая необязательные нули в начале.</span><span class="sxs-lookup"><span data-stu-id="0b101-123">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b101-124"><strong>Символ</strong></span><span class="sxs-lookup"><span data-stu-id="0b101-124"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="0b101-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="0b101-125">xs:string</span></span><br/></td>
<td><span data-ttu-id="0b101-126">Нет</span><span class="sxs-lookup"><span data-stu-id="0b101-126">No</span></span><br/></td>
<td><span data-ttu-id="0b101-127">Символ ресурса для строки.</span><span class="sxs-lookup"><span data-stu-id="0b101-127">The resource symbol for the string.</span></span><br/> <br/><span data-ttu-id="0b101-128">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="0b101-128">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0b101-129">Буква или символ подчеркивания, за которым следует любая последовательность букв, цифр или знаков подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="0b101-129">A letter or underscore followed by any sequence of letters, digits, or underscores.</span></span><br/> <span data-ttu-id="0b101-130">Максимальная длина — 100 символов.</span><span class="sxs-lookup"><span data-stu-id="0b101-130">The maximum length is 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="0b101-131">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0b101-131">Child elements</span></span>



| <span data-ttu-id="0b101-132">Элемент</span><span class="sxs-lookup"><span data-stu-id="0b101-132">Element</span></span>                                                                   | <span data-ttu-id="0b101-133">Описание</span><span class="sxs-lookup"><span data-stu-id="0b101-133">Description</span></span>                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="0b101-134">**String. Content**</span><span class="sxs-lookup"><span data-stu-id="0b101-134">**String.Content**</span></span>](windowsribbon-element-string-content.md)<br/> | <span data-ttu-id="0b101-135">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="0b101-135">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="0b101-136">**String.Id**</span><span class="sxs-lookup"><span data-stu-id="0b101-136">**String.Id**</span></span>](windowsribbon-element-string-id.md)<br/>           | <span data-ttu-id="0b101-137">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="0b101-137">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="0b101-138">**String. Symbol**</span><span class="sxs-lookup"><span data-stu-id="0b101-138">**String.Symbol**</span></span>](windowsribbon-element-string-symbol.md)<br/>   | <span data-ttu-id="0b101-139">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="0b101-139">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="0b101-140">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0b101-140">Parent elements</span></span>



| <span data-ttu-id="0b101-141">Элемент</span><span class="sxs-lookup"><span data-stu-id="0b101-141">Element</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b101-142">**Command. keytip**</span><span class="sxs-lookup"><span data-stu-id="0b101-142">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                         |
| [<span data-ttu-id="0b101-143">**Command. Лабелдескриптион**</span><span class="sxs-lookup"><span data-stu-id="0b101-143">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>     |
| [<span data-ttu-id="0b101-144">**Command. Лабелтитле**</span><span class="sxs-lookup"><span data-stu-id="0b101-144">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [<span data-ttu-id="0b101-145">**Command. Тултипдескриптион**</span><span class="sxs-lookup"><span data-stu-id="0b101-145">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [<span data-ttu-id="0b101-146">**Command. Тултиптитле**</span><span class="sxs-lookup"><span data-stu-id="0b101-146">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a><span data-ttu-id="0b101-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b101-147">Remarks</span></span>

<span data-ttu-id="0b101-148">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="0b101-148">Optional.</span></span>

<span data-ttu-id="0b101-149">Может встречаться не более одного раза для каждой [**команды Command. лабелтитле**](windowsribbon-element-command-labeltitle.md), [**Command. лабелдескриптион**](windowsribbon-element-command-labeldescription.md), [**Command. KeyTip**](windowsribbon-element-command-keytip.md), [**Command. тултиптитле**](windowsribbon-element-command-tooltiptitle.md)или элемента [**Command. тултипдескриптион**](windowsribbon-element-command-tooltipdescription.md) .</span><span class="sxs-lookup"><span data-stu-id="0b101-149">May occur at most once for each [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command.Keytip**](windowsribbon-element-command-keytip.md), [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), or [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) element.</span></span>

<span data-ttu-id="0b101-150">Определение строки добавляется в файл заголовка ленты, например `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="0b101-150">The string definition is added to the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="0b101-151">Строка добавляется в таблицу строк в файле ресурсов ленты, где платформа Ribbon создает имя и идентификатор, если они не объявлены.</span><span class="sxs-lookup"><span data-stu-id="0b101-151">The string is added to a string table in the Ribbon resource file where a name and ID are generated by the Ribbon framework if none are declared.</span></span>

## <a name="examples"></a><span data-ttu-id="0b101-152">Примеры</span><span class="sxs-lookup"><span data-stu-id="0b101-152">Examples</span></span>

<span data-ttu-id="0b101-153">В следующем примере показана разметка для элемента [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) с объявлением **строки** .</span><span class="sxs-lookup"><span data-stu-id="0b101-153">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a><span data-ttu-id="0b101-154">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0b101-154">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="0b101-155">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="0b101-155">Minimum supported system</span></span><br/> | <span data-ttu-id="0b101-156">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b101-156">Windows 7</span></span> |
| <span data-ttu-id="0b101-157">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="0b101-157">Can be empty</span></span>                        | <span data-ttu-id="0b101-158">Нет</span><span class="sxs-lookup"><span data-stu-id="0b101-158">No</span></span>        |



 

 





