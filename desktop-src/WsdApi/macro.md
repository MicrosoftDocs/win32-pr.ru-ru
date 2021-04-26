---
description: Определяет текст или CDATA для повторного использования элементом include.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: Macro, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f794566b0fd789c463d404289644976c8301a2e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994331"
---
# <a name="macro-element"></a><span data-ttu-id="71c2d-103">Macro, элемент</span><span class="sxs-lookup"><span data-stu-id="71c2d-103">macro element</span></span>

<span data-ttu-id="71c2d-104">Определяет текст или CDATA для повторного использования элементом [**include**](include.md) .</span><span class="sxs-lookup"><span data-stu-id="71c2d-104">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span>

## <a name="usage"></a><span data-ttu-id="71c2d-105">Использование</span><span class="sxs-lookup"><span data-stu-id="71c2d-105">Usage</span></span>

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="71c2d-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="71c2d-106">Attributes</span></span>



| <span data-ttu-id="71c2d-107">attribute</span><span class="sxs-lookup"><span data-stu-id="71c2d-107">Attribute</span></span>           | <span data-ttu-id="71c2d-108">Тип</span><span class="sxs-lookup"><span data-stu-id="71c2d-108">Type</span></span>                         | <span data-ttu-id="71c2d-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="71c2d-109">Required</span></span>       | <span data-ttu-id="71c2d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="71c2d-110">Description</span></span>                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| <span data-ttu-id="71c2d-111">**name**</span><span class="sxs-lookup"><span data-stu-id="71c2d-111">**name**</span></span><br/> | <span data-ttu-id="71c2d-112">Символьная \_ строка</span><span class="sxs-lookup"><span data-stu-id="71c2d-112">character\_string</span></span><br/> | <span data-ttu-id="71c2d-113">Да</span><span class="sxs-lookup"><span data-stu-id="71c2d-113">Yes</span></span><br/> | <span data-ttu-id="71c2d-114">Имя макроса.</span><span class="sxs-lookup"><span data-stu-id="71c2d-114">The name of the macro.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="71c2d-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="71c2d-115">Child elements</span></span>

<span data-ttu-id="71c2d-116">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="71c2d-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="71c2d-117">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="71c2d-117">Parent elements</span></span>



| <span data-ttu-id="71c2d-118">Элемент</span><span class="sxs-lookup"><span data-stu-id="71c2d-118">Element</span></span>                                     | <span data-ttu-id="71c2d-119">Описание</span><span class="sxs-lookup"><span data-stu-id="71c2d-119">Description</span></span>                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="71c2d-120">**всдкодежен**</span><span class="sxs-lookup"><span data-stu-id="71c2d-120">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="71c2d-121">Корневой элемент XML-файла скрипта генератора кода WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="71c2d-121">The root element of a WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="71c2d-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="71c2d-122">Remarks</span></span>

<span data-ttu-id="71c2d-123">Всдкодежен определяет макрос с именем **донотмодифи**.</span><span class="sxs-lookup"><span data-stu-id="71c2d-123">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="71c2d-124">При включении этого макроса созданный код содержит блок комментариев с высокой степенью видимости, который указывает разработчикам не изменять созданный код.</span><span class="sxs-lookup"><span data-stu-id="71c2d-124">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

<span data-ttu-id="71c2d-125">В следующем коде XML показано, как включить макрос **донотмодифи** .</span><span class="sxs-lookup"><span data-stu-id="71c2d-125">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="71c2d-126">Этот XML-код можно добавить в XML-файл конфигурации для Всдкодежен.</span><span class="sxs-lookup"><span data-stu-id="71c2d-126">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="71c2d-127">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="71c2d-127">Element information</span></span>



| <span data-ttu-id="71c2d-128">Метка</span><span class="sxs-lookup"><span data-stu-id="71c2d-128">Label</span></span> | <span data-ttu-id="71c2d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="71c2d-129">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="71c2d-130">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="71c2d-130">Minimum supported system</span></span><br/> | <span data-ttu-id="71c2d-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71c2d-131">Windows Vista</span></span> |
| <span data-ttu-id="71c2d-132">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="71c2d-132">Can be empty</span></span>                        | <span data-ttu-id="71c2d-133">Да</span><span class="sxs-lookup"><span data-stu-id="71c2d-133">Yes</span></span>           |



 

 




