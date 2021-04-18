---
description: Создает определения структуры C для типов сообщений.
ms.assetid: 68459b22-0f35-444a-969e-29695e735774
title: Мессажеструктуредефинитионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8840e4493cb97d33cb0dac8ce1ace97cc1789e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692814"
---
# <a name="messagestructuredefinitions-element"></a><span data-ttu-id="0e5b0-103">Мессажеструктуредефинитионс, элемент</span><span class="sxs-lookup"><span data-stu-id="0e5b0-103">messageStructureDefinitions element</span></span>

<span data-ttu-id="0e5b0-104">Создает определения структуры C для типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-104">Generates C structure definitions for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="0e5b0-105">Использование</span><span class="sxs-lookup"><span data-stu-id="0e5b0-105">Usage</span></span>

``` syntax
<messageStructureDefinitions>
  child elements
</messageStructureDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="0e5b0-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0e5b0-106">Attributes</span></span>

<span data-ttu-id="0e5b0-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0e5b0-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0e5b0-108">Child elements</span></span>



| <span data-ttu-id="0e5b0-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="0e5b0-109">Element</span></span>                                   | <span data-ttu-id="0e5b0-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0e5b0-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="0e5b0-111">**операцию**</span><span class="sxs-lookup"><span data-stu-id="0e5b0-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="0e5b0-112">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="0e5b0-113">**Порта**</span><span class="sxs-lookup"><span data-stu-id="0e5b0-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="0e5b0-114">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="0e5b0-115">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="0e5b0-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="0e5b0-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0e5b0-116">Parent elements</span></span>



| <span data-ttu-id="0e5b0-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="0e5b0-117">Element</span></span>                         | <span data-ttu-id="0e5b0-118">Описание</span><span class="sxs-lookup"><span data-stu-id="0e5b0-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="0e5b0-119">**File**</span><span class="sxs-lookup"><span data-stu-id="0e5b0-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="0e5b0-120">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0e5b0-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e5b0-121">Remarks</span></span>

<span data-ttu-id="0e5b0-122">Ссылки на структуры сообщений создаются прокси-сервером и кодом заглушки.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-122">Message structures are referenced by generated proxy and stub code.</span></span> <span data-ttu-id="0e5b0-123">Этот элемент используется для создания включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-123">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="0e5b0-124">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0e5b0-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0e5b0-125">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="0e5b0-125">Minimum supported system</span></span><br/> | <span data-ttu-id="0e5b0-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e5b0-126">Windows Vista</span></span> |
| <span data-ttu-id="0e5b0-127">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="0e5b0-127">Can be empty</span></span>                        | <span data-ttu-id="0e5b0-128">Да</span><span class="sxs-lookup"><span data-stu-id="0e5b0-128">Yes</span></span>           |



 

 




