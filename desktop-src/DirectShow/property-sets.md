---
description: Наборы свойств
ms.assetid: 4b8a917f-7a6c-4433-83f4-b83ef6d26115
title: Наборы свойств (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdc65efbc99eeed3a5f94ab33ce5ec982975852
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416644"
---
# <a name="property-sets-directshow"></a><span data-ttu-id="d74a5-103">Наборы свойств (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="d74a5-103">Property Sets (DirectShow)</span></span>

<span data-ttu-id="d74a5-104">Microsoft DirectShow использует наборы свойств для поддержки расширенных служб, предлагаемых оборудованием и связанными с ним драйверами и фильтрами.</span><span class="sxs-lookup"><span data-stu-id="d74a5-104">Microsoft DirectShow uses property sets to support extended services offered by hardware and its associated drivers and filters.</span></span> <span data-ttu-id="d74a5-105">Поставщики оборудования и фильтров могут определять новые возможности в качестве свойств, упорядочивать их в наборах свойств и публиковать спецификацию для этих наборов свойств.</span><span class="sxs-lookup"><span data-stu-id="d74a5-105">Hardware and filter vendors can define new capabilities as properties, arrange them in property sets, and publish the specification for these property sets.</span></span> <span data-ttu-id="d74a5-106">Разработчик приложения может использовать методы интерфейса [**икспропертисет**](ikspropertyset.md) , чтобы определить, поддерживает ли драйвер или фильтр определенный набор свойств, а также извлечь или задать эти свойства.</span><span class="sxs-lookup"><span data-stu-id="d74a5-106">As the application developer, you can use the methods of the [**IKsPropertySet**](ikspropertyset.md) interface to determine whether a driver or filter supports a particular set of properties, and retrieve or set those properties.</span></span>

<span data-ttu-id="d74a5-107">Для всех методов, предоставляемых **икспропертисет** , требуется **идентификатор GUID** , определяющий набор свойств (параметр *гуидпропсет* ), и **DWORD** , определяющий свойство в наборе свойств (параметр *dwPropID* ).</span><span class="sxs-lookup"><span data-stu-id="d74a5-107">All the methods exposed by **IKsPropertySet** require a **GUID** that identifies the property set (the *guidPropSet* parameter) and a **DWORD** that identifies the property within the property set (the *dwPropID* parameter).</span></span> <span data-ttu-id="d74a5-108">Параметр *dwPropID* обычно является членом перечислимого типа данных.</span><span class="sxs-lookup"><span data-stu-id="d74a5-108">The *dwPropID* parameter is typically a member of an enumerated data type.</span></span>

<span data-ttu-id="d74a5-109">Отдельные свойства могут иметь связанные данные, указанные в параметре *ппропдата* в методах [**Икспропертисет:: Set**](ikspropertyset-set.md) и [**икспропертисет:: Get**](ikspropertyset-get.md) .</span><span class="sxs-lookup"><span data-stu-id="d74a5-109">Individual properties can have associated data that you specify in the *pPropData* parameter in the [**IKsPropertySet::Set**](ikspropertyset-set.md) and [**IKsPropertySet::Get**](ikspropertyset-get.md) methods.</span></span> <span data-ttu-id="d74a5-110">В этих методах данные свойства вводятся как указатель на `void` .</span><span class="sxs-lookup"><span data-stu-id="d74a5-110">In these methods, the property data is typed as a pointer to `void`.</span></span> <span data-ttu-id="d74a5-111">Тип данных и значение данных указываются в определении набора свойств.</span><span class="sxs-lookup"><span data-stu-id="d74a5-111">The data type and the meaning of the data are specified in the definition of the property set.</span></span>

<span data-ttu-id="d74a5-112">Следующие разделы содержат сведения о наборах свойств, поддерживаемых в DirectShow:</span><span class="sxs-lookup"><span data-stu-id="d74a5-112">The following sections provide information about the property sets supported in DirectShow:</span></span>

-   [<span data-ttu-id="d74a5-113">**Набор свойств защиты копирования DVD-дисков**</span><span class="sxs-lookup"><span data-stu-id="d74a5-113">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   [<span data-ttu-id="d74a5-114">**Набор свойств караоке для DVD**</span><span class="sxs-lookup"><span data-stu-id="d74a5-114">**DVD Karaoke Property Set**</span></span>](dvd-karaoke-property-set.md)
-   [<span data-ttu-id="d74a5-115">**Набор свойств подизображения DVD**</span><span class="sxs-lookup"><span data-stu-id="d74a5-115">**DVD Subpicture Property Set**</span></span>](dvd-subpicture-property-set.md)
-   [<span data-ttu-id="d74a5-116">Набор свойств транспорта внешнего устройства</span><span class="sxs-lookup"><span data-stu-id="d74a5-116">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
-   [<span data-ttu-id="d74a5-117">Набор свойств пошагового выполнения кадра</span><span class="sxs-lookup"><span data-stu-id="d74a5-117">Frame Stepping Property Set</span></span>](frame-stepping-property-set.md)
-   [<span data-ttu-id="d74a5-118">Закрепить набор свойств</span><span class="sxs-lookup"><span data-stu-id="d74a5-118">Pin Property Set</span></span>](pin-property-set.md)
-   [<span data-ttu-id="d74a5-119">**Набор свойств изменения скорости**</span><span class="sxs-lookup"><span data-stu-id="d74a5-119">**Rate Change Property Set**</span></span>](rate-change-property-set.md)

 

 



