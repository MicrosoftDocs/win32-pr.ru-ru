---
description: Определяет элементы ServiceID, Types, Пнпксхардвареид и Пнпкскомпатиблеид для служб, определенных узлом службы.
ms.assetid: f901a88f-7e01-4e7f-a0f2-59f2a01b03cd
title: размещенный элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3d281b5e058f8716c12c655ebcdb9a17bdfa4fb
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994891"
---
# <a name="hosted-element"></a><span data-ttu-id="9a3f0-103">размещенный элемент</span><span class="sxs-lookup"><span data-stu-id="9a3f0-103">hosted element</span></span>

<span data-ttu-id="9a3f0-104">Определяет элементы [**ServiceID**](serviceid.md), [**types**](types.md),[**пнпксхардвареид**](pnpxhardwareid.md)и [**пнпкскомпатиблеид**](pnpxcompatibleid.md) для служб, определенных узлом службы.</span><span class="sxs-lookup"><span data-stu-id="9a3f0-104">Defines the [**ServiceID**](serviceid.md), [**Types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md), and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements for the services defined by the service host.</span></span>

## <a name="usage"></a><span data-ttu-id="9a3f0-105">Использование</span><span class="sxs-lookup"><span data-stu-id="9a3f0-105">Usage</span></span>

``` syntax
<hosted>
  child elements
</hosted>
```

## <a name="attributes"></a><span data-ttu-id="9a3f0-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9a3f0-106">Attributes</span></span>

<span data-ttu-id="9a3f0-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="9a3f0-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9a3f0-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9a3f0-108">Child elements</span></span>



| <span data-ttu-id="9a3f0-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="9a3f0-109">Element</span></span>                                                 | <span data-ttu-id="9a3f0-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9a3f0-110">Description</span></span>                                                                      |
|---------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="9a3f0-111">**пнпкскомпатиблеид**</span><span class="sxs-lookup"><span data-stu-id="9a3f0-111">**PnPXCompatibleId**</span></span>](pnpxcompatibleid.md)<br/> | <span data-ttu-id="9a3f0-112">Указывает совместимый с PnP-X идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="9a3f0-112">Specifies the PnP-X Compatible Identifier of the service.</span></span><br/> <br/> |
| [<span data-ttu-id="9a3f0-113">**пнпксхардвареид**</span><span class="sxs-lookup"><span data-stu-id="9a3f0-113">**PnPXHardwareId**</span></span>](pnpxhardwareid.md)<br/>     | <span data-ttu-id="9a3f0-114">Указывает идентификатор оборудования PnP-X для службы.</span><span class="sxs-lookup"><span data-stu-id="9a3f0-114">Specifies the PnP-X Hardware Identifier of the service.</span></span><br/> <br/>   |
| [<span data-ttu-id="9a3f0-115">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="9a3f0-115">**ServiceID**</span></span>](serviceid.md)<br/>               | <span data-ttu-id="9a3f0-116">Определяет идентификатор службы для узла службы.</span><span class="sxs-lookup"><span data-stu-id="9a3f0-116">Defines a service identifier for the service host.</span></span><br/> <br/>        |
| [<span data-ttu-id="9a3f0-117">**Типы**</span><span class="sxs-lookup"><span data-stu-id="9a3f0-117">**Types**</span></span>](types.md)<br/>                       | <span data-ttu-id="9a3f0-118">Определяет список полных имен XSD.</span><span class="sxs-lookup"><span data-stu-id="9a3f0-118">Defines a list of XSD qualified names.</span></span><br/> <br/>                    |



### <a name="child-element-sequence"></a><span data-ttu-id="9a3f0-119">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="9a3f0-119">Child element sequence</span></span>

``` syntax
(
  ServiceID, 
  Types, 
  PnPXHardwareId?, 
  PnPXCompatibleId?
)
```

## <a name="parent-elements"></a><span data-ttu-id="9a3f0-120">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="9a3f0-120">Parent elements</span></span>



| <span data-ttu-id="9a3f0-121">Элемент</span><span class="sxs-lookup"><span data-stu-id="9a3f0-121">Element</span></span>                                         | <span data-ttu-id="9a3f0-122">Описание</span><span class="sxs-lookup"><span data-stu-id="9a3f0-122">Description</span></span>                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="9a3f0-123">**хостметадата**</span><span class="sxs-lookup"><span data-stu-id="9a3f0-123">**hostMetadata**</span></span>](hostmetadata.md)<br/> | <span data-ttu-id="9a3f0-124">Метаданные размещения для реализуемого устройства.</span><span class="sxs-lookup"><span data-stu-id="9a3f0-124">The hosting metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="9a3f0-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="9a3f0-125">Remarks</span></span>

<span data-ttu-id="9a3f0-126">Каждая служба, предоставляемая узлом службы, должна иметь собственные сведения о **размещенном** элементе, чтобы обеспечить правильную публикацию службы в ответ на запросы метаданных.</span><span class="sxs-lookup"><span data-stu-id="9a3f0-126">Each service provided by a service host should have its own **hosted** element information to ensure that the service is published properly in responses to metadata requests.</span></span>

<span data-ttu-id="9a3f0-127">Элементы [**пнпксхардвареид**](pnpxhardwareid.md) и [**пнпкскомпатиблеид**](pnpxcompatibleid.md) необязательны, но при их использовании их необходимо использовать вместе.</span><span class="sxs-lookup"><span data-stu-id="9a3f0-127">The [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements are optional, but when used, they must be used together.</span></span> <span data-ttu-id="9a3f0-128">Если таковой имеется, также должен присутствовать и другой.</span><span class="sxs-lookup"><span data-stu-id="9a3f0-128">If one is present, the other must be present as well.</span></span>

<span data-ttu-id="9a3f0-129">Если имеется элемент [**пнпксдевицекатегори**](pnpxdevicecategory.md) , то по крайней мере один **размещенный** элемент должен содержать как элементы [**пнпксхардвареид**](pnpxhardwareid.md) , так и [**пнпкскомпатиблеид**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="9a3f0-129">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one **hosted** element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="9a3f0-130">Аналогично, если элементы **пнпксхардвареид** и **пнпкскомпатиблеид** находятся в **размещенном** элементе, то внутри элемента [**сисмоделметадата**](thismodelmetadata.md) должен присутствовать хотя бы один элемент **пнпксдевицекатегори** .</span><span class="sxs-lookup"><span data-stu-id="9a3f0-130">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element must be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="9a3f0-131">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9a3f0-131">Element information</span></span>



| <span data-ttu-id="9a3f0-132">Метка</span><span class="sxs-lookup"><span data-stu-id="9a3f0-132">Label</span></span> | <span data-ttu-id="9a3f0-133">Значение</span><span class="sxs-lookup"><span data-stu-id="9a3f0-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="9a3f0-134">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="9a3f0-134">Minimum supported system</span></span><br/> | <span data-ttu-id="9a3f0-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a3f0-135">Windows Vista</span></span> |
| <span data-ttu-id="9a3f0-136">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="9a3f0-136">Can be empty</span></span>                        | <span data-ttu-id="9a3f0-137">нет</span><span class="sxs-lookup"><span data-stu-id="9a3f0-137">No</span></span>            |



 

 




