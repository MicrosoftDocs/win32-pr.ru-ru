---
description: Включает в создаваемые выходные данные содержимое макроса или файла.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: включить элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8237ec865cd3cfbb80f500358e8f363be8f230
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995781"
---
# <a name="include-element"></a><span data-ttu-id="82e3a-103">включить элемент</span><span class="sxs-lookup"><span data-stu-id="82e3a-103">include element</span></span>

<span data-ttu-id="82e3a-104">Включает в создаваемые выходные данные содержимое макроса или файла.</span><span class="sxs-lookup"><span data-stu-id="82e3a-104">Includes the contents of a macro or file in the generated output.</span></span>

## <a name="usage"></a><span data-ttu-id="82e3a-105">Использование</span><span class="sxs-lookup"><span data-stu-id="82e3a-105">Usage</span></span>

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="82e3a-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="82e3a-106">Attributes</span></span>



| <span data-ttu-id="82e3a-107">attribute</span><span class="sxs-lookup"><span data-stu-id="82e3a-107">Attribute</span></span>            | <span data-ttu-id="82e3a-108">Тип</span><span class="sxs-lookup"><span data-stu-id="82e3a-108">Type</span></span>                         | <span data-ttu-id="82e3a-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="82e3a-109">Required</span></span>      | <span data-ttu-id="82e3a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="82e3a-110">Description</span></span>                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| <span data-ttu-id="82e3a-111">**file**</span><span class="sxs-lookup"><span data-stu-id="82e3a-111">**file**</span></span><br/>  | <span data-ttu-id="82e3a-112">Символьная \_ строка</span><span class="sxs-lookup"><span data-stu-id="82e3a-112">character\_string</span></span><br/> | <span data-ttu-id="82e3a-113">нет</span><span class="sxs-lookup"><span data-stu-id="82e3a-113">No</span></span><br/> | <span data-ttu-id="82e3a-114">Путь к включаемому файлу.</span><span class="sxs-lookup"><span data-stu-id="82e3a-114">The path to the file to include.</span></span><br/> <br/>  |
| <span data-ttu-id="82e3a-115">**макровирусах**</span><span class="sxs-lookup"><span data-stu-id="82e3a-115">**macro**</span></span><br/> | <span data-ttu-id="82e3a-116">Символьная \_ строка</span><span class="sxs-lookup"><span data-stu-id="82e3a-116">character\_string</span></span><br/> | <span data-ttu-id="82e3a-117">нет</span><span class="sxs-lookup"><span data-stu-id="82e3a-117">No</span></span><br/> | <span data-ttu-id="82e3a-118">Имя включаемого макроса.</span><span class="sxs-lookup"><span data-stu-id="82e3a-118">The name of the macro to include.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="82e3a-119">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="82e3a-119">Child elements</span></span>

<span data-ttu-id="82e3a-120">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="82e3a-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="82e3a-121">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="82e3a-121">Parent elements</span></span>



| <span data-ttu-id="82e3a-122">Элемент</span><span class="sxs-lookup"><span data-stu-id="82e3a-122">Element</span></span>                         | <span data-ttu-id="82e3a-123">Описание</span><span class="sxs-lookup"><span data-stu-id="82e3a-123">Description</span></span>                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82e3a-124">**File**</span><span class="sxs-lookup"><span data-stu-id="82e3a-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="82e3a-125">Направляет генератору кода создать файл и указать имя выходного файла.</span><span class="sxs-lookup"><span data-stu-id="82e3a-125">Directs the code generator to generate a file and specifies the output file name.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="82e3a-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="82e3a-126">Remarks</span></span>

<span data-ttu-id="82e3a-127">Необходимо указать атрибут **макроса** или атрибут **File** .</span><span class="sxs-lookup"><span data-stu-id="82e3a-127">Either the **macro** attribute or the **file** attribute must be specified.</span></span> <span data-ttu-id="82e3a-128">Не указывайте оба атрибута.</span><span class="sxs-lookup"><span data-stu-id="82e3a-128">Do not specify both attributes.</span></span>

<span data-ttu-id="82e3a-129">Всдкодежен определяет макрос с именем **донотмодифи**.</span><span class="sxs-lookup"><span data-stu-id="82e3a-129">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="82e3a-130">При включении этого макроса созданный код содержит блок комментариев с высокой степенью видимости, который указывает разработчикам не изменять созданный код.</span><span class="sxs-lookup"><span data-stu-id="82e3a-130">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

## <a name="examples"></a><span data-ttu-id="82e3a-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="82e3a-131">Examples</span></span>

<span data-ttu-id="82e3a-132">В следующем коде XML показано, как включить макрос **донотмодифи** .</span><span class="sxs-lookup"><span data-stu-id="82e3a-132">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="82e3a-133">Этот XML-код можно добавить в XML-файл конфигурации для Всдкодежен.</span><span class="sxs-lookup"><span data-stu-id="82e3a-133">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="82e3a-134">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="82e3a-134">Element information</span></span>



| <span data-ttu-id="82e3a-135">Метка</span><span class="sxs-lookup"><span data-stu-id="82e3a-135">Label</span></span> | <span data-ttu-id="82e3a-136">Значение</span><span class="sxs-lookup"><span data-stu-id="82e3a-136">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="82e3a-137">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="82e3a-137">Minimum supported system</span></span><br/> | <span data-ttu-id="82e3a-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82e3a-138">Windows Vista</span></span> |
| <span data-ttu-id="82e3a-139">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="82e3a-139">Can be empty</span></span>                        | <span data-ttu-id="82e3a-140">Да</span><span class="sxs-lookup"><span data-stu-id="82e3a-140">Yes</span></span>           |



 

 




