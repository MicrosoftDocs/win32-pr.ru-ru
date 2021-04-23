---
description: Определяет текст или CDATA для повторного использования элементом include.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: Macro, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8759d4afb61883b8bf41472f276882643cfa552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264789"
---
# <a name="macro-element"></a><span data-ttu-id="a7d6f-103">Macro, элемент</span><span class="sxs-lookup"><span data-stu-id="a7d6f-103">macro element</span></span>

<span data-ttu-id="a7d6f-104">Определяет текст или CDATA для повторного использования элементом [**include**](include.md) .</span><span class="sxs-lookup"><span data-stu-id="a7d6f-104">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span>

## <a name="usage"></a><span data-ttu-id="a7d6f-105">Использование</span><span class="sxs-lookup"><span data-stu-id="a7d6f-105">Usage</span></span>

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="a7d6f-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a7d6f-106">Attributes</span></span>



| <span data-ttu-id="a7d6f-107">attribute</span><span class="sxs-lookup"><span data-stu-id="a7d6f-107">Attribute</span></span>           | <span data-ttu-id="a7d6f-108">Тип</span><span class="sxs-lookup"><span data-stu-id="a7d6f-108">Type</span></span>                         | <span data-ttu-id="a7d6f-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a7d6f-109">Required</span></span>       | <span data-ttu-id="a7d6f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a7d6f-110">Description</span></span>                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| <span data-ttu-id="a7d6f-111">**name**</span><span class="sxs-lookup"><span data-stu-id="a7d6f-111">**name**</span></span><br/> | <span data-ttu-id="a7d6f-112">Символьная \_ строка</span><span class="sxs-lookup"><span data-stu-id="a7d6f-112">character\_string</span></span><br/> | <span data-ttu-id="a7d6f-113">Да</span><span class="sxs-lookup"><span data-stu-id="a7d6f-113">Yes</span></span><br/> | <span data-ttu-id="a7d6f-114">Имя макроса.</span><span class="sxs-lookup"><span data-stu-id="a7d6f-114">The name of the macro.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="a7d6f-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a7d6f-115">Child elements</span></span>

<span data-ttu-id="a7d6f-116">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="a7d6f-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a7d6f-117">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="a7d6f-117">Parent elements</span></span>



| <span data-ttu-id="a7d6f-118">Элемент</span><span class="sxs-lookup"><span data-stu-id="a7d6f-118">Element</span></span>                                     | <span data-ttu-id="a7d6f-119">Описание</span><span class="sxs-lookup"><span data-stu-id="a7d6f-119">Description</span></span>                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7d6f-120">**всдкодежен**</span><span class="sxs-lookup"><span data-stu-id="a7d6f-120">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="a7d6f-121">Корневой элемент XML-файла скрипта генератора кода WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="a7d6f-121">The root element of a WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a7d6f-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7d6f-122">Remarks</span></span>

<span data-ttu-id="a7d6f-123">Всдкодежен определяет макрос с именем **донотмодифи**.</span><span class="sxs-lookup"><span data-stu-id="a7d6f-123">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="a7d6f-124">При включении этого макроса созданный код содержит блок комментариев с высокой степенью видимости, который указывает разработчикам не изменять созданный код.</span><span class="sxs-lookup"><span data-stu-id="a7d6f-124">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

<span data-ttu-id="a7d6f-125">В следующем коде XML показано, как включить макрос **донотмодифи** .</span><span class="sxs-lookup"><span data-stu-id="a7d6f-125">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="a7d6f-126">Этот XML-код можно добавить в XML-файл конфигурации для Всдкодежен.</span><span class="sxs-lookup"><span data-stu-id="a7d6f-126">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="a7d6f-127">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a7d6f-127">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="a7d6f-128">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="a7d6f-128">Minimum supported system</span></span><br/> | <span data-ttu-id="a7d6f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7d6f-129">Windows Vista</span></span> |
| <span data-ttu-id="a7d6f-130">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="a7d6f-130">Can be empty</span></span>                        | <span data-ttu-id="a7d6f-131">Да</span><span class="sxs-lookup"><span data-stu-id="a7d6f-131">Yes</span></span>           |



 

 




