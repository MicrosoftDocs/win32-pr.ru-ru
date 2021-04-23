---
title: Сдвоенные интерфейсы (ADSI)
description: Используйте COM-интерфейсы для доступа к свойствам и методам любых объектов поставщика ADSI.
ms.assetid: 6f3fd725-d660-4cc3-8de2-8ed7800b1141
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34c858275098dd82362d229bc9e1cc35b544c55
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793789"
---
# <a name="dual-interfaces-adsi"></a><span data-ttu-id="2cc9e-103">Сдвоенные интерфейсы (ADSI)</span><span class="sxs-lookup"><span data-stu-id="2cc9e-103">Dual Interfaces (ADSI)</span></span>

<span data-ttu-id="2cc9e-104">Используйте COM-интерфейсы для доступа к свойствам и методам любых объектов поставщика ADSI.</span><span class="sxs-lookup"><span data-stu-id="2cc9e-104">Use COM interfaces to access the properties and methods on any provider ADSI objects.</span></span> <span data-ttu-id="2cc9e-105">Свойство только для чтения сопоставляется с записью интерфейса в форме **Get \_ <PropertyName>**.</span><span class="sxs-lookup"><span data-stu-id="2cc9e-105">A read-only property maps to an interface entry of the form **get\_<PropertyName>**.</span></span> <span data-ttu-id="2cc9e-106">Свойство, доступное для чтения и записи, сопоставляется с двумя записями интерфейса в форме **Get \_ <PropertyName>** и **помещается \_ <PropertyName>**.</span><span class="sxs-lookup"><span data-stu-id="2cc9e-106">A read/write property maps to two interface entries of the form **get\_<PropertyName>** and **put\_<PropertyName>**.</span></span>

<span data-ttu-id="2cc9e-107">Все методы в интерфейсе COM должны:</span><span class="sxs-lookup"><span data-stu-id="2cc9e-107">All methods on a COM interface must:</span></span>

-   <span data-ttu-id="2cc9e-108">Возвращает значение HRESULT для обозначения успешного или неуспешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="2cc9e-108">Return an HRESULT value to indicate success or failure.</span></span> <span data-ttu-id="2cc9e-109">Тип **HRESULT** обсуждается в спецификации COM.</span><span class="sxs-lookup"><span data-stu-id="2cc9e-109">The **HRESULT** type is discussed in the COM specification.</span></span>
-   <span data-ttu-id="2cc9e-110">При вызове **QueryInterface** возвращается **\_ интерфейс E** для нереализованных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="2cc9e-110">On calls to **QueryInterface**, return **E\_NOINTERFACE** for unimplemented interfaces.</span></span>
-   <span data-ttu-id="2cc9e-111">Возвращает **E \_ нотимпл** для нереализованных методов в интерфейсах, которые в противном случае реализованы.</span><span class="sxs-lookup"><span data-stu-id="2cc9e-111">Return **E\_NOTIMPL** for unimplemented methods on interfaces that are otherwise implemented.</span></span>
-   <span data-ttu-id="2cc9e-112">Возвращаемое **\_ свойство E ADS \_ \_ не \_ поддерживается** для свойств интерфейса, которые не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="2cc9e-112">Return **E\_ADS\_PROPERTY\_NOT\_SUPPORTED** for interface properties that are not supported.</span></span>

<span data-ttu-id="2cc9e-113">Чтобы обеспечить совместимость с контроллерами автоматизации, все параметры и возвращаемые типы должны находиться в подмножестве, определенном типом данных Automation VARIANT.</span><span class="sxs-lookup"><span data-stu-id="2cc9e-113">To retain compatibility with Automation controllers, all parameters and return types should be within the subset defined by the Automation VARIANT data type.</span></span> <span data-ttu-id="2cc9e-114">Дополнительные сведения см. в разделе **варианты** и **VARIANTARG** в пакете SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="2cc9e-114">For more information, see **VARIANT** and **VARIANTARG** in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="2cc9e-115">Объект Active Directory поставщика может предоставлять интерфейсы, которые используют типы данных, отличные от тех, которые находятся в подмножестве **вариантов** .</span><span class="sxs-lookup"><span data-stu-id="2cc9e-115">A provider Active Directory object can expose interfaces that use data types other than those in the **VARIANT** subset.</span></span> <span data-ttu-id="2cc9e-116">Однако контроллеры автоматизации, такие как Visual Basic, не могут вызывать эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="2cc9e-116">However, Automation controllers such as Visual Basic are not able to call those interfaces.</span></span> <span data-ttu-id="2cc9e-117">Большинство интерфейсов поставщика ADSI являются производными от [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) и могут использоваться как указатели интерфейса **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="2cc9e-117">Most ADSI provider interfaces are derived from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) and can be used as **IDispatch** interface pointers.</span></span> <span data-ttu-id="2cc9e-118">Однако интерфейсы ADSI [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)и [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension) не являются производными от **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="2cc9e-118">However, the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), and [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) ADSI interfaces are not derived from **IDispatch**.</span></span>

 

 