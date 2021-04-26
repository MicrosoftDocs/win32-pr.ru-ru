---
description: Создает определения структуры C для типов сообщений.
ms.assetid: 68459b22-0f35-444a-969e-29695e735774
title: Мессажеструктуредефинитионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a116658fc7ce7f985b7b717c7a7b4ce38be4637
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993671"
---
# <a name="messagestructuredefinitions-element"></a><span data-ttu-id="65061-103">Мессажеструктуредефинитионс, элемент</span><span class="sxs-lookup"><span data-stu-id="65061-103">messageStructureDefinitions element</span></span>

<span data-ttu-id="65061-104">Создает определения структуры C для типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="65061-104">Generates C structure definitions for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="65061-105">Использование</span><span class="sxs-lookup"><span data-stu-id="65061-105">Usage</span></span>

``` syntax
<messageStructureDefinitions>
  child elements
</messageStructureDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="65061-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="65061-106">Attributes</span></span>

<span data-ttu-id="65061-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="65061-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="65061-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="65061-108">Child elements</span></span>



| <span data-ttu-id="65061-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="65061-109">Element</span></span>                                   | <span data-ttu-id="65061-110">Описание</span><span class="sxs-lookup"><span data-stu-id="65061-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="65061-111">**operation**</span><span class="sxs-lookup"><span data-stu-id="65061-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="65061-112">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="65061-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="65061-113">**Порта**</span><span class="sxs-lookup"><span data-stu-id="65061-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="65061-114">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="65061-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="65061-115">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="65061-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="65061-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="65061-116">Parent elements</span></span>



| <span data-ttu-id="65061-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="65061-117">Element</span></span>                         | <span data-ttu-id="65061-118">Описание</span><span class="sxs-lookup"><span data-stu-id="65061-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="65061-119">**File**</span><span class="sxs-lookup"><span data-stu-id="65061-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="65061-120">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="65061-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="65061-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="65061-121">Remarks</span></span>

<span data-ttu-id="65061-122">Ссылки на структуры сообщений создаются прокси-сервером и кодом заглушки.</span><span class="sxs-lookup"><span data-stu-id="65061-122">Message structures are referenced by generated proxy and stub code.</span></span> <span data-ttu-id="65061-123">Этот элемент используется для создания включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="65061-123">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="65061-124">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="65061-124">Element information</span></span>



| <span data-ttu-id="65061-125">Метка</span><span class="sxs-lookup"><span data-stu-id="65061-125">Label</span></span> | <span data-ttu-id="65061-126">Значение</span><span class="sxs-lookup"><span data-stu-id="65061-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="65061-127">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="65061-127">Minimum supported system</span></span><br/> | <span data-ttu-id="65061-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65061-128">Windows Vista</span></span> |
| <span data-ttu-id="65061-129">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="65061-129">Can be empty</span></span>                        | <span data-ttu-id="65061-130">Да</span><span class="sxs-lookup"><span data-stu-id="65061-130">Yes</span></span>           |



 

 




