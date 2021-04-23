---
description: Определяет число создаваемых слоев кода.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: Лайернумбер, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c22a20db7817e449b05c943c9016b6002f35b54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264790"
---
# <a name="layernumber-element"></a><span data-ttu-id="428a5-103">Лайернумбер, элемент</span><span class="sxs-lookup"><span data-stu-id="428a5-103">layerNumber element</span></span>

<span data-ttu-id="428a5-104">Определяет число создаваемых слоев кода.</span><span class="sxs-lookup"><span data-stu-id="428a5-104">Defines the number of the code layer to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="428a5-105">Использование</span><span class="sxs-lookup"><span data-stu-id="428a5-105">Usage</span></span>

``` syntax
<layerNumber/>
```

## <a name="attributes"></a><span data-ttu-id="428a5-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="428a5-106">Attributes</span></span>

<span data-ttu-id="428a5-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="428a5-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="428a5-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="428a5-108">Child elements</span></span>

<span data-ttu-id="428a5-109">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="428a5-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="428a5-110">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="428a5-110">Parent elements</span></span>



| <span data-ttu-id="428a5-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="428a5-111">Element</span></span>                                     | <span data-ttu-id="428a5-112">Описание</span><span class="sxs-lookup"><span data-stu-id="428a5-112">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="428a5-113">**всдкодежен**</span><span class="sxs-lookup"><span data-stu-id="428a5-113">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="428a5-114">Корневой элемент XML-файла скрипта генератора кода WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="428a5-114">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="428a5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="428a5-115">Remarks</span></span>

<span data-ttu-id="428a5-116">Номера слоев используются в таблицах среды выполнения для различения одного уровня кода для другого.</span><span class="sxs-lookup"><span data-stu-id="428a5-116">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="428a5-117">WSDAPI сам использует сформированный код с номером уровня 0.</span><span class="sxs-lookup"><span data-stu-id="428a5-117">WSDAPI itself uses generated code that has a layer number of 0.</span></span>

<span data-ttu-id="428a5-118">Как правило, это значение равно 1, что означает, что созданный код будет разноситься поверх WSDAPI и без другого слоя.</span><span class="sxs-lookup"><span data-stu-id="428a5-118">Typically, this value will be 1, indicating that the generated code is layered on top of WSDAPI and no other layer.</span></span> <span data-ttu-id="428a5-119">В некоторых случаях можно использовать более высокие значения.</span><span class="sxs-lookup"><span data-stu-id="428a5-119">In some cases, higher numbers may be used.</span></span> <span data-ttu-id="428a5-120">Например, если одна компания создает код для класса устройств (нумерованный уровень 1), конкретному поставщику оборудования может потребоваться добавить дополнительный слой с номером 2.</span><span class="sxs-lookup"><span data-stu-id="428a5-120">For example, if one company produces code for a device class (numbered layer 1), a particular hardware vendor may want to add an additional layer numbered layer 2.</span></span>

<span data-ttu-id="428a5-121">Допустимые значения, за исключением случая, когда WSDAPI имеет значение, больше 0 и меньше 16.</span><span class="sxs-lookup"><span data-stu-id="428a5-121">Legal values, except in the case of WSDAPI itself are greater than 0 and less than 16.</span></span>

## <a name="element-information"></a><span data-ttu-id="428a5-122">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="428a5-122">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="428a5-123">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="428a5-123">Minimum supported system</span></span><br/> | <span data-ttu-id="428a5-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="428a5-124">Windows Vista</span></span> |
| <span data-ttu-id="428a5-125">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="428a5-125">Can be empty</span></span>                        | <span data-ttu-id="428a5-126">Да</span><span class="sxs-lookup"><span data-stu-id="428a5-126">Yes</span></span>           |



 

 




