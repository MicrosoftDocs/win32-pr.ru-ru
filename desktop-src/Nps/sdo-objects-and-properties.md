---
title: Объекты и свойства
description: Характеристики объекта в SDO определяются свойствами объекта и значениями, связанными с этими свойствами.
ms.assetid: 9faa7759-cad5-4429-94b0-6cba145cfadb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efed7720388e61b9d6131acafd4b9bda17694d29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672335"
---
# <a name="objects-and-properties"></a><span data-ttu-id="20eb9-103">Объекты и свойства</span><span class="sxs-lookup"><span data-stu-id="20eb9-103">Objects and Properties</span></span>

<span data-ttu-id="20eb9-104">Характеристики объекта в SDO определяются свойствами объекта и значениями, связанными с этими свойствами.</span><span class="sxs-lookup"><span data-stu-id="20eb9-104">The characteristics of an object in SDO are determined by the object's properties, and the values associated with those properties.</span></span> <span data-ttu-id="20eb9-105">В отличие от других объектных моделей, объекты SDO сами по себе не имеют методов.</span><span class="sxs-lookup"><span data-stu-id="20eb9-105">Unlike some other object models, SDO objects themselves do not have methods.</span></span> <span data-ttu-id="20eb9-106">Однако объекты SDO предоставляют интерфейсы COM, предоставляющие методы.</span><span class="sxs-lookup"><span data-stu-id="20eb9-106">However, SDO objects do expose COM interfaces that provide methods.</span></span>

<span data-ttu-id="20eb9-107">Объекты SDO предоставляют интерфейс [**исдо**](/windows/desktop/api/sdoias/nn-sdoias-isdo) , предоставляющий методы для управления свойствами объектов.</span><span class="sxs-lookup"><span data-stu-id="20eb9-107">Objects in SDO expose the [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface that provides methods for manipulating the objects properties.</span></span> <span data-ttu-id="20eb9-108">Чтобы получить доступ к свойствам объекта, получите интерфейс **исдо** для объекта и используйте методы интерфейса GetObject [**и**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) [**putproperty изменил**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) для получения и установки значений свойств.</span><span class="sxs-lookup"><span data-stu-id="20eb9-108">To access the object's properties, obtain an **ISdo** interface for the object, and use the [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) and [**PutProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) interface methods to retrieve and set values for the properties.</span></span> <span data-ttu-id="20eb9-109">В разделе [Получение ПОЛЬЗОВАТЕЛЬСКОГО SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) содержится пример кода, демонстрирующий получение интерфейса **Исдо** для объекта пользователя.</span><span class="sxs-lookup"><span data-stu-id="20eb9-109">The topic [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contains sample code that demonstrates obtaining the **ISdo** interface for a User object.</span></span>

<span data-ttu-id="20eb9-110">После внесения изменений в свойства объекта используйте метод [**исдо:: Apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) , чтобы записать изменения в постоянное хранилище для объекта.</span><span class="sxs-lookup"><span data-stu-id="20eb9-110">After making changes to the properties of an object, use the [**ISdo::Apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) method to write the changes to persistent storage for the object.</span></span> <span data-ttu-id="20eb9-111">Вы можете отменить изменения, внесенные в свойства объекта перед вызовом **исдо:: Apply** путем вызова метода [**исдо:: Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) .</span><span class="sxs-lookup"><span data-stu-id="20eb9-111">You can cancel changes made to an object's properties before you call **ISdo::Apply** by calling the [**ISdo::Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) method.</span></span> <span data-ttu-id="20eb9-112">Этот метод восстанавливает значения свойств объекта из постоянного хранилища.</span><span class="sxs-lookup"><span data-stu-id="20eb9-112">This method restores the values of an object's properties from persistent storage.</span></span>

<span data-ttu-id="20eb9-113">В следующей таблице показаны типы перечислений, которые перечисляют свойства некоторых объектов в SDO.</span><span class="sxs-lookup"><span data-stu-id="20eb9-113">The following table shows the enumeration types that enumerate the properties of some of the objects in SDO.</span></span>



| <span data-ttu-id="20eb9-114">Объект</span><span class="sxs-lookup"><span data-stu-id="20eb9-114">Object</span></span>                                 | <span data-ttu-id="20eb9-115">Тип перечисления</span><span class="sxs-lookup"><span data-stu-id="20eb9-115">Enumeration type</span></span>                                       |
|----------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="20eb9-116">Все объекты SDO</span><span class="sxs-lookup"><span data-stu-id="20eb9-116">All SDO objects</span></span>                        | [<span data-ttu-id="20eb9-117">**иаскоммонпропертиес**</span><span class="sxs-lookup"><span data-stu-id="20eb9-117">**IASCOMMONPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties) |
| <span data-ttu-id="20eb9-118">Объект User</span><span class="sxs-lookup"><span data-stu-id="20eb9-118">User Object</span></span>                            | [<span data-ttu-id="20eb9-119">**усерпропертиес**</span><span class="sxs-lookup"><span data-stu-id="20eb9-119">**USERPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-userproperties)           |
| <span data-ttu-id="20eb9-120">Объект службы (сервер политики сети)</span><span class="sxs-lookup"><span data-stu-id="20eb9-120">Service Object (Network Policy Server)</span></span> | [<span data-ttu-id="20eb9-121">**иаспропертиес**</span><span class="sxs-lookup"><span data-stu-id="20eb9-121">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)             |
| <span data-ttu-id="20eb9-122">Объект протокола Microsoft RADIUS</span><span class="sxs-lookup"><span data-stu-id="20eb9-122">Microsoft RADIUS Protocol Object</span></span>       | [<span data-ttu-id="20eb9-123">**радиуспропертиес**</span><span class="sxs-lookup"><span data-stu-id="20eb9-123">**RADIUSPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-radiusproperties)       |



 

> [!Note]  
> <span data-ttu-id="20eb9-124">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="20eb9-124">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

## <a name="collections"></a><span data-ttu-id="20eb9-125">Коллекции</span><span class="sxs-lookup"><span data-stu-id="20eb9-125">Collections</span></span>

<span data-ttu-id="20eb9-126">Объекты часто группируются в коллекции.</span><span class="sxs-lookup"><span data-stu-id="20eb9-126">Objects are often grouped into collections.</span></span> <span data-ttu-id="20eb9-127">API SDO предоставляет функциональные возможности через интерфейс [**сбора исдо**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) для перечисления объектов в коллекции и добавления и удаления объектов из коллекции.</span><span class="sxs-lookup"><span data-stu-id="20eb9-127">The SDO API provides functionality, through the [**ISdo Collection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) interface, to enumerate the objects in a collection and to add and delete objects from a collection.</span></span>

<span data-ttu-id="20eb9-128">Доступ к коллекции получается путем получения свойства коллекции для объекта, содержащего коллекцию.</span><span class="sxs-lookup"><span data-stu-id="20eb9-128">Access to a collection is obtained by retrieving a collection property on the object that contains the collection.</span></span> <span data-ttu-id="20eb9-129">Дополнительные сведения см. в разделе [Иерархия объектной модели](/windows/desktop/Nps/sdo-object-model-hierarchy).</span><span class="sxs-lookup"><span data-stu-id="20eb9-129">For more information, see the section [Object Model Hierarchy](/windows/desktop/Nps/sdo-object-model-hierarchy).</span></span>

<span data-ttu-id="20eb9-130">Тип данных для всех свойств, соответствующих коллекциям, — это VT \_ Dispatch.</span><span class="sxs-lookup"><span data-stu-id="20eb9-130">The data type for all properties that correspond to collections is VT\_DISPATCH.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20eb9-131">См. также</span><span class="sxs-lookup"><span data-stu-id="20eb9-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20eb9-132">Иерархия объектной модели SDO</span><span class="sxs-lookup"><span data-stu-id="20eb9-132">SDO Object Model Hierarchy</span></span>](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[<span data-ttu-id="20eb9-133">Поддерживаемые в SDO атрибуты</span><span class="sxs-lookup"><span data-stu-id="20eb9-133">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 