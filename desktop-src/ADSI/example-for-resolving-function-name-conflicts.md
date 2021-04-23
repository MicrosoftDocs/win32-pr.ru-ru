---
title: Пример разрешения конфликтов имен функций
description: В этом разделе описывается, как разрешать конфликты имен функций при создании расширения для ADSI.
ms.assetid: 8121f037-3845-44ba-a2cd-8d7f15e0beb2
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, пример кода Visual Basic, разрешение конфликтов имен функций
- разрешение конфликтов имен функций ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049f9ce6447bf6d6ead783db3e34f74374333f10
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339249"
---
# <a name="example-for-resolving-function-name-conflicts"></a><span data-ttu-id="0bc1d-105">Пример разрешения конфликтов имен функций</span><span class="sxs-lookup"><span data-stu-id="0bc1d-105">Example for Resolving Function Name Conflicts</span></span>

<span data-ttu-id="0bc1d-106">Рассмотрим следующий пример.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-106">Consider the following:</span></span>

-   <span data-ttu-id="0bc1d-107">IADs0 не поддерживает Func0.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-107">IADs0 does not support Func0.</span></span>
-   <span data-ttu-id="0bc1d-108">IADs1 поддерживает func1 и Func0.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-108">IADs1 supports Func1 and Func0.</span></span>
-   <span data-ttu-id="0bc1d-109">IADs2 поддерживает Func2 и Func0.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-109">IADs2 supports Func2 and Func0.</span></span>

<span data-ttu-id="0bc1d-110">Все три интерфейса являются сдвоенными интерфейсами.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-110">All three interfaces are dual interfaces.</span></span>


```C++
IADs0 : IDispatch
{
    OtherFunc();
}

IADs1 : IDispatch
{
    Func0() 
    Func1();
}

IADs2 : IDispatch
{
    Func0()
    Func2();
}
```




```VB
Dim myInf1 as IADs1
 
myInf1.Func1  ' IADs1::Func1 is invoked using direct vtable access 
 
myInf1.Func2  ' IADs2::Func2 is invoked using GetIDsOfNames/Invoke
```



<span data-ttu-id="0bc1d-111">Имейте в виду, что несмотря на то, что IADs1 не поддерживает Func2, клиент ADSI распознает один интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , поддерживающий все сдвоенные и диспетчеризации интерфейсы в модели.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-111">Be aware that even though IADs1 does not support Func2, an ADSI client recognizes one [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that supports all the dual and dispatch interfaces in the model.</span></span> <span data-ttu-id="0bc1d-112">Таким же клиент ADSI может напрямую вызвать Func2 с помощью myInf1. Func2, не разрешая интерфейс, поддерживающий Func2.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-112">Thus, the ADSI client can directly call Func2 using myInf1.Func2 without resolving which interface supports Func2.</span></span>


```VB
myInf1.Func2
```



<span data-ttu-id="0bc1d-113">Как IADs1, так и IADs2 имеют функцию с именем Func0, но IADs1:: Func0 вызывается напрямую с помощью доступа к таблице vtable, так как оба следующих условия применимы к клиенту:</span><span class="sxs-lookup"><span data-stu-id="0bc1d-113">Both IADs1 and IADs2 have a function called Func0, but IADs1::Func0 is invoked directly using vtable access, because both of following apply to the client:</span></span>

-   <span data-ttu-id="0bc1d-114">Клиент имеет указатель на объект IADs1 с двойным интерфейсом, который имеет функцию с именем Func0.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-114">The client has a pointer to dual interface IADs1 object, which has a function called Func0.</span></span>
-   <span data-ttu-id="0bc1d-115">Visual Basic поддерживает прямой доступ к vtable, предполагая, что тип данных доступен через библиотеку типов.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-115">Visual Basic supports direct vtable access, assuming that type of data is available through the type library.</span></span>

<span data-ttu-id="0bc1d-116">В следующем примере кода клиент имеет сдвоенный указатель на IADs2 вместо IADs1.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-116">In the next code example, the client has a dual interface pointer to IADs2 instead of IADs1.</span></span> <span data-ttu-id="0bc1d-117">Таким образом, IADs2:: Func0 вызывается с помощью прямого доступа vtable.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-117">Therefore, IADs2::Func0 is invoked using direct vtable access.</span></span>


```VB
Dim myInf2 as IADs2
Set myInf2 = myInf1 ' Query for pointer to IADs2 
myInf2.Func0
```



<span data-ttu-id="0bc1d-118">Опять же, в следующем примере кода и IADs1, и IADs2 имеют функцию с именем Func0, но здесь клиент имеет указатель на сдвоенный интерфейс IADs0, который не имеет функции с именем Func0.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-118">Again, in the next code example, both IADs1 and IADs2 have a function called Func0, but, here, the client has a pointer to a dual interface, IADs0, which does not have a function called Func0.</span></span> <span data-ttu-id="0bc1d-119">Таким образом, прямой доступ к vtable не может быть выполнен.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-119">Therefore, no direct vtable access can be performed.</span></span> <span data-ttu-id="0bc1d-120">Вместо этого вызываются [**IDispatch:: GetIdsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) и [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) для вызова Func0.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-120">Instead, [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) are called to invoke Func0.</span></span>


```VB
Dim myInfNone as IADs0
Set myInfNone = myInf1    ' The aggregated object that 
   ' supports IADs1 and IADs2.
myInfNone.Func0
```



<span data-ttu-id="0bc1d-121">Рассмотрим следующие два варианта:</span><span class="sxs-lookup"><span data-stu-id="0bc1d-121">Consider these two cases:</span></span>

-   <span data-ttu-id="0bc1d-122">IADs1 и IADs2 реализуются двумя COM-компонентами, Ext1 и ext2 соответственно.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-122">IADs1 and IADs2 are implemented by two COM components, Ext1 and Ext2, respectively.</span></span> <span data-ttu-id="0bc1d-123">Если Ext1 находится перед ext2 в реестре, вызывается IADs1:: Func0.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-123">If Ext1 comes before Ext2 in the registry, IADs1::Func0 is invoked.</span></span> <span data-ttu-id="0bc1d-124">Однако если ext2 находится в реестре первыми, вызывается IADs2:: Func0.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-124">However, if Ext2 comes first in the registry, IADs2::Func0 is invoked.</span></span>
-   <span data-ttu-id="0bc1d-125">Если IADs1 и ADs2 реализуются одним и тем же объектом расширения, Func0 всегда вызывается методами [**иадсекстенсион::P риватежетидсофнамес**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) и [**приватеинвоке**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) расширения.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-125">If IADs1 and ADs2 are implemented by the same extension object, Func0 is always invoked by the extension's [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) and [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) methods.</span></span>

<span data-ttu-id="0bc1d-126">Разработчик расширений должен определить, как разрешать конфликты функций или свойств различных сдвоенных интерфейсов [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с одинаковым именем в расширении.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-126">The extension developer must determine how to resolve conflicts of functions, or properties, of different dual [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces that have the same name in an extension.</span></span> <span data-ttu-id="0bc1d-127">Реализация методов [**иадсекстенсион::P риватежетидсофнамес**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) и [**приватеинвоке**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) должна устранить этот конфликт.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-127">The implementation of [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) and [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) methods should resolve this conflict.</span></span> <span data-ttu-id="0bc1d-128">Например, если используются IMyInterface1:: Func1 и IMyInterface2:: Func1, где IMyInterface1 и IMyInterface2 — сдвоенные интерфейсы **IDispatch** , поддерживаемые одним и тем же объектом расширения.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-128">For example, if you use IMyInterface1::Func1 and IMyInterface2::Func1, where IMyInterface1 and IMyInterface2 are dual **IDispatch** interfaces supported by the same extension object.</span></span> <span data-ttu-id="0bc1d-129">Методы **приватежетидсофнамес** и **приватеинвоке** должны определять, какой func1 следует вызывать всегда.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-129">The **PrivateGetIDsOfNames** and **PrivateInvoke** methods must determine which Func1 should always be called.</span></span>

<span data-ttu-id="0bc1d-130">То же относится и к конфликтующим идентификаторам DISPID в разных интерфейсах Dual или [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="0bc1d-130">The same applies to conflicting DISPIDs in different dual or [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces.</span></span>

<span data-ttu-id="0bc1d-131">Например, DISPID IMyInterface1:: Y имеет значение 2 в файле IMyInterface1. odl или IMyInterface1. idl.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-131">For example, the DISPID of IMyInterface1::Y is 2 in the file imyinterface1.odl, or imyinterface1.idl.</span></span> <span data-ttu-id="0bc1d-132">Идентификатор DISPID IMyInterface2:: X также равен 2 в iMyInterface2. ODL.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-132">The DISPID of IMyInterface2::X is also 2 in iMyInterface2.odl.</span></span> <span data-ttu-id="0bc1d-133">[**Иадсекстенсион::P риватежетидсофнамес**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) должен возвращать уникальный идентификатор DISPID в самом расширении для каждого, вместо того чтобы возвращать один и тот же DISPID для обоих.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-133">[**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) must return a unique DISPID, within the extension itself, for each, instead of returning the same DISPID for both.</span></span>

<span data-ttu-id="0bc1d-134">ADSI разрешает первую проблему, не поддерживая несколько интерфейсов с конфликтующими именами функций или свойств.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-134">ADSI resolves the first problem by not supporting multiple interfaces with conflicting function or property names.</span></span> <span data-ttu-id="0bc1d-135">Она разрешает вторую проблему, добавляя уникальный объект, который находится в том же объекте расширения, но не в неиспользуемые биты DISPID.</span><span class="sxs-lookup"><span data-stu-id="0bc1d-135">It resolves the second problem by adding a unique, that is within the same extension object, interface number to the unused bits of the DISPID.</span></span>

 

 