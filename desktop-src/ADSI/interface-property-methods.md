---
title: Методы свойств интерфейса
description: Многие интерфейсы ADSI предназначены для поддержки автоматизации и, таким образом, являются сдвоенными интерфейсами в том, что они поддерживают клиентский доступ через интерфейсы IUnknown и IDispatch.
ms.assetid: b2831fa4-b58d-4b65-8deb-5fb7cd50c724
ms.tgt_platform: multiple
keywords:
- Методы свойств интерфейса
- Описание интерфейсов ADSI ADSI, справочника, методов свойств
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018999d4834859cdb465bba2e6cdb9a05bd38a98
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654369"
---
# <a name="interface-property-methods"></a><span data-ttu-id="94502-105">Методы свойств интерфейса</span><span class="sxs-lookup"><span data-stu-id="94502-105">Interface Property Methods</span></span>

<span data-ttu-id="94502-106">Многие интерфейсы ADSI предназначены для поддержки автоматизации и, таким образом, являются сдвоенными интерфейсами в том, что они поддерживают клиентский доступ через интерфейсы [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) и [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="94502-106">Many ADSI interfaces are designed to support Automation and thus are dual interfaces in that they support client access through both [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces.</span></span> <span data-ttu-id="94502-107">Клиенты, не поддерживающие автоматизацию, такие как написанные на C/C++, устраняют вызов методов напрямую, с помощью метода [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) и вызывают метод напрямую.</span><span class="sxs-lookup"><span data-stu-id="94502-107">Non-Automation clients, such as those written in C/C++, resolve method invocation directly, using the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method, and call the method directly.</span></span> <span data-ttu-id="94502-108">Клиенты автоматизации, также известные как клиенты, привязанные к имени, такие как написанные в Visual Basic или Visual Basic Scripting Edition (VBScript), должны устранять вызов метода косвенно с помощью метода [**DISP**](/previous-versions/windows/desktop/automat/dispinterface) .</span><span class="sxs-lookup"><span data-stu-id="94502-108">Automation clients, also known as name-bound clients, such as those written in Visual Basic, or Visual Basic Scripting Edition (VBScript), must resolve method invocation indirectly using the [**dispinterface**](/previous-versions/windows/desktop/automat/dispinterface) method.</span></span>

<span data-ttu-id="94502-109">Интерфейс ADSI, поддерживающий автоматизацию, определяет методы свойств для получения и изменения свойств объекта, реализующего интерфейс.</span><span class="sxs-lookup"><span data-stu-id="94502-109">An ADSI interface supporting Automation defines property methods for retrieving and modifying properties of an object implementing the interface.</span></span> <span data-ttu-id="94502-110">У методов свойств есть имена, которые  содержат \_ префиксы Get и WHERE в  \_ начале соответствующих имен свойств, например **Get \_ пользователь** и **\_ имя размещения**.</span><span class="sxs-lookup"><span data-stu-id="94502-110">The property methods have names that have **get**\_ and **put**\_ prepended to the appropriate property names, for example, **get\_User** and **put\_Name**.</span></span>

<span data-ttu-id="94502-111">Каждый **метод \_ Get** принимает один параметр в качестве выходных данных.</span><span class="sxs-lookup"><span data-stu-id="94502-111">Each **get\_** method takes a single parameter as output.</span></span> <span data-ttu-id="94502-112">Этот параметр является адресом переменной типа данных свойства, выделенным методом.</span><span class="sxs-lookup"><span data-stu-id="94502-112">This parameter is a method-allocated address of a variable of the property data type.</span></span> <span data-ttu-id="94502-113">При возврате эта переменная предполагает текущее значение запрошенного свойства.</span><span class="sxs-lookup"><span data-stu-id="94502-113">On return, this variable assumes the current value of the requested property.</span></span> <span data-ttu-id="94502-114">Вызывающий объект должен освободить выделенную память переменной, если свойство больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="94502-114">The caller must release the allocated memory of the variable when the property is no longer required.</span></span>

<span data-ttu-id="94502-115">Каждый **метод \_ размещения** принимает один параметр в качестве входного для типа данных соответствующего свойства.</span><span class="sxs-lookup"><span data-stu-id="94502-115">Each **put\_** method takes a single parameter as input for the data type of the corresponding property.</span></span> <span data-ttu-id="94502-116">Параметр содержит новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="94502-116">The parameter holds a new value of the property.</span></span>

<span data-ttu-id="94502-117">В следующем примере кода показан вызов методов свойств, которые следуют обычной процедуре для вызова функции члена объекта.</span><span class="sxs-lookup"><span data-stu-id="94502-117">The following code example shows the invocation of the property methods that follow the usual procedure to call the member function of an object.</span></span>


```C++
IADs *pADs;
BSTR bstrName;
pADs->get_Name(&bstrName);
```



<span data-ttu-id="94502-118">В следующем примере кода показан вызов методов свойств в клиентах автоматизации, которые могут быть несколько разными.</span><span class="sxs-lookup"><span data-stu-id="94502-118">The following code example shows the invocation of the property methods in automation clients, which can be somewhat different.</span></span> <span data-ttu-id="94502-119">Например, Visual Basic использует точечную нотацию.</span><span class="sxs-lookup"><span data-stu-id="94502-119">For example, Visual Basic uses dot notation.</span></span>


```VB
Dim Obj As IADs
Dim objName As String
objName = Obj.Name
```



<span data-ttu-id="94502-120">Все параметры и возвращаемые типы должны иметь тип, определяемый типом данных VARIANT.</span><span class="sxs-lookup"><span data-stu-id="94502-120">All parameters and return types must be of those that the VARIANT data type defines.</span></span> <span data-ttu-id="94502-121">Все методы в сдвоенном интерфейсе возвращают значение HRESULT для обозначения успеха или неудачи.</span><span class="sxs-lookup"><span data-stu-id="94502-121">All methods on a dual interface return an HRESULT value to indicate success or failure.</span></span>

<span data-ttu-id="94502-122">Дополнительные сведения о получении и установке свойств объектов ADSI см. в разделе [кэш свойств](property-cache-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="94502-122">For more information about getting and setting properties on ADSI objects, see [Property Cache](property-cache-interfaces.md).</span></span>

 

 