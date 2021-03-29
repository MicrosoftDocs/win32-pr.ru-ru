---
description: Указывает WSDL-файл для обработки сведений о контракте.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: элемент WSDL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb54f946f32fb4962b8384dea7c6cf4b3c0ebe3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264630"
---
# <a name="wsdl-element"></a><span data-ttu-id="0767d-103">элемент WSDL</span><span class="sxs-lookup"><span data-stu-id="0767d-103">wsdl element</span></span>

<span data-ttu-id="0767d-104">Указывает WSDL-файл для обработки сведений о контракте.</span><span class="sxs-lookup"><span data-stu-id="0767d-104">Specifies a WSDL file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="0767d-105">Использование</span><span class="sxs-lookup"><span data-stu-id="0767d-105">Usage</span></span>

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a><span data-ttu-id="0767d-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0767d-106">Attributes</span></span>

<span data-ttu-id="0767d-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="0767d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0767d-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0767d-108">Child elements</span></span>



| <span data-ttu-id="0767d-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="0767d-109">Element</span></span>                                           | <span data-ttu-id="0767d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0767d-110">Description</span></span>                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0767d-111">**ексклудеимпорт**</span><span class="sxs-lookup"><span data-stu-id="0767d-111">**excludeImport**</span></span>](excludeimport.md)<br/> | <span data-ttu-id="0767d-112">Предотвращает создание операторов импорта для указанных целевых объектов с именем в элементе <WSDL: Import> в WSDL-файле.</span><span class="sxs-lookup"><span data-stu-id="0767d-112">Prevents the generation of import statements for specified targets named in a <wsdl:import> element in a WSDL file.</span></span> <br/> <br/> |
| [<span data-ttu-id="0767d-113">**импорсинт**</span><span class="sxs-lookup"><span data-stu-id="0767d-113">**importHint**</span></span>](importhint.md)<br/>       | <span data-ttu-id="0767d-114">Указывает расположение загрузки для директивы> <WSDL: Import, которая явно не задает расположение.</span><span class="sxs-lookup"><span data-stu-id="0767d-114">Specifies the download location for a <wsdl:import> directive that does not explicitly specify a location.</span></span><br/> <br/>           |
| [<span data-ttu-id="0767d-115">**путь**</span><span class="sxs-lookup"><span data-stu-id="0767d-115">**path**</span></span>](path.md)<br/>                   | <span data-ttu-id="0767d-116">Файл и путь к входному файлу WSDL.</span><span class="sxs-lookup"><span data-stu-id="0767d-116">File and path of the WSDL input file.</span></span><br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="0767d-117">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="0767d-117">Child element sequence</span></span>

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a><span data-ttu-id="0767d-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0767d-118">Parent elements</span></span>



| <span data-ttu-id="0767d-119">Элемент</span><span class="sxs-lookup"><span data-stu-id="0767d-119">Element</span></span>                                     | <span data-ttu-id="0767d-120">Описание</span><span class="sxs-lookup"><span data-stu-id="0767d-120">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="0767d-121">**всдкодежен**</span><span class="sxs-lookup"><span data-stu-id="0767d-121">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="0767d-122">Корневой элемент XML-файла скрипта генератора кода WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="0767d-122">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0767d-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0767d-123">Remarks</span></span>

<span data-ttu-id="0767d-124">Все элементы [**импорсинт**](importhint.md) и [**ексклудеимпорт**](excludeimport.md) , появляющиеся после элемента [**path**](path.md) в XML-файле конфигурации, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="0767d-124">Any [**importHint**](importhint.md) or [**excludeImport**](excludeimport.md) elements appearing after the [**path**](path.md) element in an XML configuration file will be ignored.</span></span>

## <a name="element-information"></a><span data-ttu-id="0767d-125">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0767d-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0767d-126">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="0767d-126">Minimum supported system</span></span><br/> | <span data-ttu-id="0767d-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0767d-127">Windows Vista</span></span> |
| <span data-ttu-id="0767d-128">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="0767d-128">Can be empty</span></span>                        | <span data-ttu-id="0767d-129">Нет</span><span class="sxs-lookup"><span data-stu-id="0767d-129">No</span></span>            |



 

 




