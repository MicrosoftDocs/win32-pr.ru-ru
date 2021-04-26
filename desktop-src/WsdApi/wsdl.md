---
description: Указывает WSDL-файл для обработки сведений о контракте.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: элемент WSDL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef4bc7b76ce22184e4c2f1ceaa2131ef163a26d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994711"
---
# <a name="wsdl-element"></a><span data-ttu-id="3f2d1-103">элемент WSDL</span><span class="sxs-lookup"><span data-stu-id="3f2d1-103">wsdl element</span></span>

<span data-ttu-id="3f2d1-104">Указывает WSDL-файл для обработки сведений о контракте.</span><span class="sxs-lookup"><span data-stu-id="3f2d1-104">Specifies a WSDL file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="3f2d1-105">Использование</span><span class="sxs-lookup"><span data-stu-id="3f2d1-105">Usage</span></span>

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a><span data-ttu-id="3f2d1-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3f2d1-106">Attributes</span></span>

<span data-ttu-id="3f2d1-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="3f2d1-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3f2d1-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3f2d1-108">Child elements</span></span>



| <span data-ttu-id="3f2d1-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="3f2d1-109">Element</span></span>                                           | <span data-ttu-id="3f2d1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="3f2d1-110">Description</span></span>                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f2d1-111">**ексклудеимпорт**</span><span class="sxs-lookup"><span data-stu-id="3f2d1-111">**excludeImport**</span></span>](excludeimport.md)<br/> | <span data-ttu-id="3f2d1-112">Предотвращает создание операторов импорта для указанных целевых объектов в \<wsdl:import> ЭЛЕМЕНТЕ WSDL-файла.</span><span class="sxs-lookup"><span data-stu-id="3f2d1-112">Prevents the generation of import statements for specified targets named in a \<wsdl:import> element in a WSDL file.</span></span> <br/> <br/> |
| [<span data-ttu-id="3f2d1-113">**импорсинт**</span><span class="sxs-lookup"><span data-stu-id="3f2d1-113">**importHint**</span></span>](importhint.md)<br/>       | <span data-ttu-id="3f2d1-114">Указывает расположение загрузки для \<wsdl:import> директивы, которая не указывает расположение явным образом.</span><span class="sxs-lookup"><span data-stu-id="3f2d1-114">Specifies the download location for a \<wsdl:import> directive that does not explicitly specify a location.</span></span><br/> <br/>           |
| [<span data-ttu-id="3f2d1-115">**путь**</span><span class="sxs-lookup"><span data-stu-id="3f2d1-115">**path**</span></span>](path.md)<br/>                   | <span data-ttu-id="3f2d1-116">Файл и путь к входному файлу WSDL.</span><span class="sxs-lookup"><span data-stu-id="3f2d1-116">File and path of the WSDL input file.</span></span><br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="3f2d1-117">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="3f2d1-117">Child element sequence</span></span>

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a><span data-ttu-id="3f2d1-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="3f2d1-118">Parent elements</span></span>



| <span data-ttu-id="3f2d1-119">Элемент</span><span class="sxs-lookup"><span data-stu-id="3f2d1-119">Element</span></span>                                     | <span data-ttu-id="3f2d1-120">Описание</span><span class="sxs-lookup"><span data-stu-id="3f2d1-120">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f2d1-121">**всдкодежен**</span><span class="sxs-lookup"><span data-stu-id="3f2d1-121">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="3f2d1-122">Корневой элемент XML-файла скрипта генератора кода WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="3f2d1-122">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="3f2d1-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="3f2d1-123">Remarks</span></span>

<span data-ttu-id="3f2d1-124">Все элементы [**импорсинт**](importhint.md) и [**ексклудеимпорт**](excludeimport.md) , появляющиеся после элемента [**path**](path.md) в XML-файле конфигурации, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="3f2d1-124">Any [**importHint**](importhint.md) or [**excludeImport**](excludeimport.md) elements appearing after the [**path**](path.md) element in an XML configuration file will be ignored.</span></span>

## <a name="element-information"></a><span data-ttu-id="3f2d1-125">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3f2d1-125">Element information</span></span>



| <span data-ttu-id="3f2d1-126">Метка</span><span class="sxs-lookup"><span data-stu-id="3f2d1-126">Label</span></span> | <span data-ttu-id="3f2d1-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3f2d1-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="3f2d1-128">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="3f2d1-128">Minimum supported system</span></span><br/> | <span data-ttu-id="3f2d1-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3f2d1-129">Windows Vista</span></span> |
| <span data-ttu-id="3f2d1-130">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="3f2d1-130">Can be empty</span></span>                        | <span data-ttu-id="3f2d1-131">нет</span><span class="sxs-lookup"><span data-stu-id="3f2d1-131">No</span></span>            |



 

 




