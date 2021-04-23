---
description: Включает в создаваемые выходные данные содержимое макроса или файла.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: включить элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f22cfde339ca218d4cd10525bbca3e57b8d836f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081207"
---
# <a name="include-element"></a><span data-ttu-id="008d4-103">включить элемент</span><span class="sxs-lookup"><span data-stu-id="008d4-103">include element</span></span>

<span data-ttu-id="008d4-104">Включает в создаваемые выходные данные содержимое макроса или файла.</span><span class="sxs-lookup"><span data-stu-id="008d4-104">Includes the contents of a macro or file in the generated output.</span></span>

## <a name="usage"></a><span data-ttu-id="008d4-105">Использование</span><span class="sxs-lookup"><span data-stu-id="008d4-105">Usage</span></span>

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="008d4-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="008d4-106">Attributes</span></span>



| <span data-ttu-id="008d4-107">attribute</span><span class="sxs-lookup"><span data-stu-id="008d4-107">Attribute</span></span>            | <span data-ttu-id="008d4-108">Тип</span><span class="sxs-lookup"><span data-stu-id="008d4-108">Type</span></span>                         | <span data-ttu-id="008d4-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="008d4-109">Required</span></span>      | <span data-ttu-id="008d4-110">Описание</span><span class="sxs-lookup"><span data-stu-id="008d4-110">Description</span></span>                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| <span data-ttu-id="008d4-111">**file**</span><span class="sxs-lookup"><span data-stu-id="008d4-111">**file**</span></span><br/>  | <span data-ttu-id="008d4-112">Символьная \_ строка</span><span class="sxs-lookup"><span data-stu-id="008d4-112">character\_string</span></span><br/> | <span data-ttu-id="008d4-113">Нет</span><span class="sxs-lookup"><span data-stu-id="008d4-113">No</span></span><br/> | <span data-ttu-id="008d4-114">Путь к включаемому файлу.</span><span class="sxs-lookup"><span data-stu-id="008d4-114">The path to the file to include.</span></span><br/> <br/>  |
| <span data-ttu-id="008d4-115">**макровирусах**</span><span class="sxs-lookup"><span data-stu-id="008d4-115">**macro**</span></span><br/> | <span data-ttu-id="008d4-116">Символьная \_ строка</span><span class="sxs-lookup"><span data-stu-id="008d4-116">character\_string</span></span><br/> | <span data-ttu-id="008d4-117">Нет</span><span class="sxs-lookup"><span data-stu-id="008d4-117">No</span></span><br/> | <span data-ttu-id="008d4-118">Имя включаемого макроса.</span><span class="sxs-lookup"><span data-stu-id="008d4-118">The name of the macro to include.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="008d4-119">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="008d4-119">Child elements</span></span>

<span data-ttu-id="008d4-120">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="008d4-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="008d4-121">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="008d4-121">Parent elements</span></span>



| <span data-ttu-id="008d4-122">Элемент</span><span class="sxs-lookup"><span data-stu-id="008d4-122">Element</span></span>                         | <span data-ttu-id="008d4-123">Описание</span><span class="sxs-lookup"><span data-stu-id="008d4-123">Description</span></span>                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="008d4-124">**File**</span><span class="sxs-lookup"><span data-stu-id="008d4-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="008d4-125">Направляет генератору кода создать файл и указать имя выходного файла.</span><span class="sxs-lookup"><span data-stu-id="008d4-125">Directs the code generator to generate a file and specifies the output file name.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="008d4-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="008d4-126">Remarks</span></span>

<span data-ttu-id="008d4-127">Необходимо указать атрибут **макроса** или атрибут **File** .</span><span class="sxs-lookup"><span data-stu-id="008d4-127">Either the **macro** attribute or the **file** attribute must be specified.</span></span> <span data-ttu-id="008d4-128">Не указывайте оба атрибута.</span><span class="sxs-lookup"><span data-stu-id="008d4-128">Do not specify both attributes.</span></span>

<span data-ttu-id="008d4-129">Всдкодежен определяет макрос с именем **донотмодифи**.</span><span class="sxs-lookup"><span data-stu-id="008d4-129">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="008d4-130">При включении этого макроса созданный код содержит блок комментариев с высокой степенью видимости, который указывает разработчикам не изменять созданный код.</span><span class="sxs-lookup"><span data-stu-id="008d4-130">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

## <a name="examples"></a><span data-ttu-id="008d4-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="008d4-131">Examples</span></span>

<span data-ttu-id="008d4-132">В следующем коде XML показано, как включить макрос **донотмодифи** .</span><span class="sxs-lookup"><span data-stu-id="008d4-132">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="008d4-133">Этот XML-код можно добавить в XML-файл конфигурации для Всдкодежен.</span><span class="sxs-lookup"><span data-stu-id="008d4-133">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="008d4-134">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="008d4-134">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="008d4-135">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="008d4-135">Minimum supported system</span></span><br/> | <span data-ttu-id="008d4-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="008d4-136">Windows Vista</span></span> |
| <span data-ttu-id="008d4-137">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="008d4-137">Can be empty</span></span>                        | <span data-ttu-id="008d4-138">Да</span><span class="sxs-lookup"><span data-stu-id="008d4-138">Yes</span></span>           |



 

 




