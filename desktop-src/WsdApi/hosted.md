---
description: Определяет элементы ServiceID, Types, Пнпксхардвареид и Пнпкскомпатиблеид для служб, определенных узлом службы.
ms.assetid: f901a88f-7e01-4e7f-a0f2-59f2a01b03cd
title: размещенный элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d46549898f0a95de362467c759c3d95eb806a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702881"
---
# <a name="hosted-element"></a><span data-ttu-id="1d19c-103">размещенный элемент</span><span class="sxs-lookup"><span data-stu-id="1d19c-103">hosted element</span></span>

<span data-ttu-id="1d19c-104">Определяет элементы [**ServiceID**](serviceid.md), [**types**](types.md),[**пнпксхардвареид**](pnpxhardwareid.md)и [**пнпкскомпатиблеид**](pnpxcompatibleid.md) для служб, определенных узлом службы.</span><span class="sxs-lookup"><span data-stu-id="1d19c-104">Defines the [**ServiceID**](serviceid.md), [**Types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md), and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements for the services defined by the service host.</span></span>

## <a name="usage"></a><span data-ttu-id="1d19c-105">Использование</span><span class="sxs-lookup"><span data-stu-id="1d19c-105">Usage</span></span>

``` syntax
<hosted>
  child elements
</hosted>
```

## <a name="attributes"></a><span data-ttu-id="1d19c-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1d19c-106">Attributes</span></span>

<span data-ttu-id="1d19c-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="1d19c-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1d19c-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1d19c-108">Child elements</span></span>



| <span data-ttu-id="1d19c-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="1d19c-109">Element</span></span>                                                 | <span data-ttu-id="1d19c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1d19c-110">Description</span></span>                                                                      |
|---------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="1d19c-111">**пнпкскомпатиблеид**</span><span class="sxs-lookup"><span data-stu-id="1d19c-111">**PnPXCompatibleId**</span></span>](pnpxcompatibleid.md)<br/> | <span data-ttu-id="1d19c-112">Указывает совместимый с PnP-X идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="1d19c-112">Specifies the PnP-X Compatible Identifier of the service.</span></span><br/> <br/> |
| [<span data-ttu-id="1d19c-113">**пнпксхардвареид**</span><span class="sxs-lookup"><span data-stu-id="1d19c-113">**PnPXHardwareId**</span></span>](pnpxhardwareid.md)<br/>     | <span data-ttu-id="1d19c-114">Указывает идентификатор оборудования PnP-X для службы.</span><span class="sxs-lookup"><span data-stu-id="1d19c-114">Specifies the PnP-X Hardware Identifier of the service.</span></span><br/> <br/>   |
| [<span data-ttu-id="1d19c-115">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="1d19c-115">**ServiceID**</span></span>](serviceid.md)<br/>               | <span data-ttu-id="1d19c-116">Определяет идентификатор службы для узла службы.</span><span class="sxs-lookup"><span data-stu-id="1d19c-116">Defines a service identifier for the service host.</span></span><br/> <br/>        |
| [<span data-ttu-id="1d19c-117">**Типы**</span><span class="sxs-lookup"><span data-stu-id="1d19c-117">**Types**</span></span>](types.md)<br/>                       | <span data-ttu-id="1d19c-118">Определяет список полных имен XSD.</span><span class="sxs-lookup"><span data-stu-id="1d19c-118">Defines a list of XSD qualified names.</span></span><br/> <br/>                    |



### <a name="child-element-sequence"></a><span data-ttu-id="1d19c-119">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="1d19c-119">Child element sequence</span></span>

``` syntax
(
  ServiceID, 
  Types, 
  PnPXHardwareId?, 
  PnPXCompatibleId?
)
```

## <a name="parent-elements"></a><span data-ttu-id="1d19c-120">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="1d19c-120">Parent elements</span></span>



| <span data-ttu-id="1d19c-121">Элемент</span><span class="sxs-lookup"><span data-stu-id="1d19c-121">Element</span></span>                                         | <span data-ttu-id="1d19c-122">Описание</span><span class="sxs-lookup"><span data-stu-id="1d19c-122">Description</span></span>                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="1d19c-123">**хостметадата**</span><span class="sxs-lookup"><span data-stu-id="1d19c-123">**hostMetadata**</span></span>](hostmetadata.md)<br/> | <span data-ttu-id="1d19c-124">Метаданные размещения для реализуемого устройства.</span><span class="sxs-lookup"><span data-stu-id="1d19c-124">The hosting metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="1d19c-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d19c-125">Remarks</span></span>

<span data-ttu-id="1d19c-126">Каждая служба, предоставляемая узлом службы, должна иметь собственные сведения о **размещенном** элементе, чтобы обеспечить правильную публикацию службы в ответ на запросы метаданных.</span><span class="sxs-lookup"><span data-stu-id="1d19c-126">Each service provided by a service host should have its own **hosted** element information to ensure that the service is published properly in responses to metadata requests.</span></span>

<span data-ttu-id="1d19c-127">Элементы [**пнпксхардвареид**](pnpxhardwareid.md) и [**пнпкскомпатиблеид**](pnpxcompatibleid.md) необязательны, но при их использовании их необходимо использовать вместе.</span><span class="sxs-lookup"><span data-stu-id="1d19c-127">The [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements are optional, but when used, they must be used together.</span></span> <span data-ttu-id="1d19c-128">Если таковой имеется, также должен присутствовать и другой.</span><span class="sxs-lookup"><span data-stu-id="1d19c-128">If one is present, the other must be present as well.</span></span>

<span data-ttu-id="1d19c-129">Если имеется элемент [**пнпксдевицекатегори**](pnpxdevicecategory.md) , то по крайней мере один **размещенный** элемент должен содержать как элементы [**пнпксхардвареид**](pnpxhardwareid.md) , так и [**пнпкскомпатиблеид**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="1d19c-129">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one **hosted** element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="1d19c-130">Аналогично, если элементы **пнпксхардвареид** и **пнпкскомпатиблеид** находятся в **размещенном** элементе, то внутри элемента [**сисмоделметадата**](thismodelmetadata.md) должен присутствовать хотя бы один элемент **пнпксдевицекатегори** .</span><span class="sxs-lookup"><span data-stu-id="1d19c-130">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element must be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="1d19c-131">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1d19c-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="1d19c-132">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="1d19c-132">Minimum supported system</span></span><br/> | <span data-ttu-id="1d19c-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d19c-133">Windows Vista</span></span> |
| <span data-ttu-id="1d19c-134">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="1d19c-134">Can be empty</span></span>                        | <span data-ttu-id="1d19c-135">Нет</span><span class="sxs-lookup"><span data-stu-id="1d19c-135">No</span></span>            |



 

 




