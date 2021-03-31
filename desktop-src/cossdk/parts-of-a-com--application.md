---
description: Приложения COM+ состоят из одного или нескольких COM-компонентов.
ms.assetid: e7ed2844-276e-4726-952d-e4d3be2eb6e8
title: Части приложения COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f75aba454689e25e8706d4a7e3f059d498891f9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496026"
---
# <a name="parts-of-a-com-application"></a><span data-ttu-id="8d5ae-103">Части приложения COM+</span><span class="sxs-lookup"><span data-stu-id="8d5ae-103">Parts of a COM+ Application</span></span>

<span data-ttu-id="8d5ae-104">Приложения COM+ состоят из одного или нескольких COM-компонентов.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-104">COM+ applications consist of one or more COM components.</span></span>

<span data-ttu-id="8d5ae-105">В документации по COM+ используются следующие термины:</span><span class="sxs-lookup"><span data-stu-id="8d5ae-105">The following terms are used throughout the COM+ documentation:</span></span>

<dl> <dt>

<span data-ttu-id="8d5ae-106"><span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*COM-компонент*</span><span class="sxs-lookup"><span data-stu-id="8d5ae-106"><span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*COM component*</span></span>
</dt> <dd>

<span data-ttu-id="8d5ae-107">Двоичная единица кода, которая создает COM-объекты (включает в себя код упаковки и регистрации).</span><span class="sxs-lookup"><span data-stu-id="8d5ae-107">A binary unit of code that creates COM objects (includes packaging and registration code).</span></span>

</dd> <dt>

<span data-ttu-id="8d5ae-108"><span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*COM-объект*</span><span class="sxs-lookup"><span data-stu-id="8d5ae-108"><span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*COM object*</span></span>
</dt> <dd>

<span data-ttu-id="8d5ae-109">Экземпляр класса COM.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-109">An instance of a COM class.</span></span>

</dd> <dt>

<span data-ttu-id="8d5ae-110"><span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*COM-класс*</span><span class="sxs-lookup"><span data-stu-id="8d5ae-110"><span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*COM class*</span></span>
</dt> <dd>

<span data-ttu-id="8d5ae-111">Именованная конкретная реализация одного или нескольких интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-111">A named, concrete implementation of one or more interfaces.</span></span> <span data-ttu-id="8d5ae-112">Класс COM определяется идентификатором CLSID (иногда идентификатором ProgID также).</span><span class="sxs-lookup"><span data-stu-id="8d5ae-112">A COM class is identified by a CLSID (sometimes by a ProgID also).</span></span>

</dd> <dt>

<span data-ttu-id="8d5ae-113"><span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*COM-интерфейс*</span><span class="sxs-lookup"><span data-stu-id="8d5ae-113"><span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*COM interface*</span></span>
</dt> <dd>

<span data-ttu-id="8d5ae-114">Группа связанных функций методов, предоставляемых классом COM, задающих контракт.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-114">A group of related method functions exposed by a COM class that specify a contract.</span></span> <span data-ttu-id="8d5ae-115">Сюда входят имя, сигнатура интерфейса, семантика интерфейса и формат буфера маршалирования.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-115">This includes the name, interface signature, interface semantics, and marshaling buffer format.</span></span> <span data-ttu-id="8d5ae-116">Интерфейс определяется по идентификатору IID.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-116">An interface is identified by an IID.</span></span> <span data-ttu-id="8d5ae-117">Синтаксис интерфейса определяется в библиотеках типов IDL и (или).</span><span class="sxs-lookup"><span data-stu-id="8d5ae-117">The interface syntax is defined in IDL and/or type libraries.</span></span> <span data-ttu-id="8d5ae-118">Интерфейсы класса COM должны быть разделены на управляемые, Объединенные наборы методов.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-118">The interfaces of a COM class should be divided into manageable, cohesive sets of methods.</span></span>

<span data-ttu-id="8d5ae-119">COM-интерфейсы являются неизменяемыми; COM-контракт указывает, что их нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-119">COM interfaces are immutable; the COM contract states that they cannot be modified.</span></span> <span data-ttu-id="8d5ae-120">Любое изменение (например, добавление методов) требует определения нового интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-120">Any modification (such as adding methods) requires defining a new interface.</span></span>

</dd> <dt>

<span data-ttu-id="8d5ae-121"><span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*COM-метод*</span><span class="sxs-lookup"><span data-stu-id="8d5ae-121"><span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*COM method*</span></span>
</dt> <dd>

<span data-ttu-id="8d5ae-122">Один из набора связанных функций, предоставляемых COM-интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-122">One of a set of related functions provided by a COM interface.</span></span>

</dd> </dl>

## <a name="configured-and-unconfigured-components"></a><span data-ttu-id="8d5ae-123">Настроенные и ненастроенные компоненты</span><span class="sxs-lookup"><span data-stu-id="8d5ae-123">Configured and Unconfigured Components</span></span>

<span data-ttu-id="8d5ae-124">Чтобы воспользоваться преимуществами служб, поддерживаемых приложениями COM+, среда COM+ накладывает определенные требования к COM-компонентам, созданным для приложений COM+.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-124">To take advantage of the services that COM+ applications support, the COM+ environment imposes specific requirements on COM components built for COM+ applications.</span></span> <span data-ttu-id="8d5ae-125">При добавлении в приложение COM+ компонент COM называется *настроенным компонентом*.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-125">When added to a COM+ application, a COM component is known as a *configured component*.</span></span>

<span data-ttu-id="8d5ae-126">COM-компоненты, созданные для приложений COM+, являются компонентами внутрипроцессного сервера.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-126">COM components built for COM+ applications are in-process server components.</span></span> <span data-ttu-id="8d5ae-127">Компонент должен содержать библиотеку типов (TLB-файл) для описания всех классов, реализованных в компоненте, и объявления интерфейсов для всех классов в компоненте.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-127">The component must contain a type library (.tlb file) to describe all classes implemented in the component and declare the interfaces on all classes in the component.</span></span> <span data-ttu-id="8d5ae-128">Эти компоненты можно создавать и реализовывать с помощью Microsoft Visual Basic, Microsoft Visual C++ или любого совместимого с COM средства разработки.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-128">You can create and implement these components with Microsoft Visual Basic, Microsoft Visual C++, or any COM-compatible development tool.</span></span>

<span data-ttu-id="8d5ae-129">*Ненастроенный компонент* — это компонент, который не устанавливается в приложении COM+.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-129">An *unconfigured component* is a component that isn't installed in a COM+ application.</span></span> <span data-ttu-id="8d5ae-130">Большинство ненастроенных компонентов можно преобразовать в настроенные компоненты, просто интегрируя их в приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-130">You can transform most unconfigured components into configured components simply by integrating them into a COM+ application.</span></span>

> [!Note]  
> <span data-ttu-id="8d5ae-131">Не используйте один и тот же AppID для приложения COM+ и в реестре для ненастроенного компонента.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-131">Do not use the same AppID for both a COM+ application and in the registry for an unconfigured component.</span></span> <span data-ttu-id="8d5ae-132">При активации ненастроенного компонента, поскольку Активация может получить сведения о приложении COM+ из реестра, не содержащего сведения, необходимые для активации COM.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-132">When the unconfigured component is activated , as activation may retrieve the COM+ application information from the registry that does not contain the information required for COM activation.</span></span> <span data-ttu-id="8d5ae-133">Аналогичные проблемы могут возникнуть при вызове [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) из Dllhost, где размещается серверное приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-133">Similar problems could arise if a call is made to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) from DllHost that hosts COM+ Server application.</span></span>

 

 

 
