---
description: Поставщик свойств использует методы Ивбемпропертипровидер в качестве основного интерфейса для WMI. С помощью Ивбемпропертипровидер можно реализовать код для извлечения и изменения свойств класса и экземпляра.
ms.assetid: d08c2ca4-9f8a-4a27-80fc-688d7c56f5eb
ms.tgt_platform: multiple
title: Реализация основного интерфейса для поставщика свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942117547380000e0da7d22a5e933cba4b3ffced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712462"
---
# <a name="implementing-the-primary-interface-for-a-property-provider"></a><span data-ttu-id="441c8-104">Реализация основного интерфейса для поставщика свойств</span><span class="sxs-lookup"><span data-stu-id="441c8-104">Implementing the Primary Interface for a Property Provider</span></span>

<span data-ttu-id="441c8-105">Поставщик свойств использует методы [**ивбемпропертипровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) в качестве основного интерфейса для WMI.</span><span class="sxs-lookup"><span data-stu-id="441c8-105">A property provider uses the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) methods as the primary interface to WMI.</span></span> <span data-ttu-id="441c8-106">С помощью **ивбемпропертипровидер** можно реализовать код для извлечения и изменения свойств класса и экземпляра.</span><span class="sxs-lookup"><span data-stu-id="441c8-106">With **IWbemPropertyProvider**, you can implement the code to retrieve and modify class and instance properties.</span></span>

<span data-ttu-id="441c8-107">В следующей таблице перечислены методы [**ивбемпропертипровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) , которые можно реализовать для поставщика свойств.</span><span class="sxs-lookup"><span data-stu-id="441c8-107">The following table lists the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) methods that you can implement for a property provider.</span></span>



| <span data-ttu-id="441c8-108">Метод</span><span class="sxs-lookup"><span data-stu-id="441c8-108">Method</span></span>                                                   | <span data-ttu-id="441c8-109">Функция</span><span class="sxs-lookup"><span data-stu-id="441c8-109">Feature</span></span>      |
|----------------------------------------------------------|--------------|
| [<span data-ttu-id="441c8-110">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="441c8-110">**GetProperty**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) | <span data-ttu-id="441c8-111">Получения</span><span class="sxs-lookup"><span data-stu-id="441c8-111">Retrieval</span></span>    |
| [<span data-ttu-id="441c8-112">**Putproperty изменил**</span><span class="sxs-lookup"><span data-stu-id="441c8-112">**PutProperty**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) | <span data-ttu-id="441c8-113">Изменение</span><span class="sxs-lookup"><span data-stu-id="441c8-113">Modification</span></span> |



 

> [!Note]  
> <span data-ttu-id="441c8-114">Поставщик свойств необходимо реализовать как внутрипроцессный поставщик.</span><span class="sxs-lookup"><span data-stu-id="441c8-114">You must implement a property provider as an in-process provider.</span></span> <span data-ttu-id="441c8-115">Инструментарий WMI инициализирует поставщики свойств, написанные как службы или исполняемые файлы, но никогда не будет [**вызывать их методы**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) [**putproperty изменил**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) и.</span><span class="sxs-lookup"><span data-stu-id="441c8-115">WMI will initialize property providers written as services or executable files but will never call their [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) and [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) methods.</span></span>

 

<span data-ttu-id="441c8-116">Если вы решили не поддерживать один из этих методов, поставщик может предоставить реализацию заглушки, которая возвращает **поставщик WBEM \_ E \_ \_ не \_** поддерживает.</span><span class="sxs-lookup"><span data-stu-id="441c8-116">If you choose not to support one of these methods, your provider can supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE**.</span></span>

<span data-ttu-id="441c8-117">Поставщик свойств определяет управляемый класс или экземпляр с помощью набора из трех квалификаторов: **пропертиконтекст**, **InstanceContext** и **классконтекст**.</span><span class="sxs-lookup"><span data-stu-id="441c8-117">A property provider identifies a managed class or instance by a set of three qualifiers: **PropertyContext**, **InstanceContext**, and **ClassContext**.</span></span> <span data-ttu-id="441c8-118">Инструментарий WMI передает строковые константы, описывающие эти три квалификатора поставщику свойств.</span><span class="sxs-lookup"><span data-stu-id="441c8-118">WMI will pass in string constants describing these three qualifiers to your property provider.</span></span>

<span data-ttu-id="441c8-119">Поставщик свойств должен быть готов к обработке следующих типов квалификаторов контекста:</span><span class="sxs-lookup"><span data-stu-id="441c8-119">Your property provider must be prepared to handle the following types of context qualifiers:</span></span>

-   <span data-ttu-id="441c8-120">Квалификатор **InstanceContext** присоединяется к экземпляру и содержит сведения, которые применяются к каждому свойству в экземпляре.</span><span class="sxs-lookup"><span data-stu-id="441c8-120">The **InstanceContext** qualifier is attached to an instance and contains information that applies to every property in the instance.</span></span>
-   <span data-ttu-id="441c8-121">Квалификатор **классконтекст** присоединяется к классу и содержит сведения, которые применяются к каждому экземпляру в классе.</span><span class="sxs-lookup"><span data-stu-id="441c8-121">The **ClassContext** qualifier is attached to a class and contains information that applies to every instance in the class.</span></span> <span data-ttu-id="441c8-122">Например, в классе, используемом для хранения данных, предоставляемых поставщиком реестра, **классконтекст** может быть путем к разделу реестра, который содержит свойства, которые необходимо сообщить.</span><span class="sxs-lookup"><span data-stu-id="441c8-122">For example, in a class used to store data supplied by the Registry provider, **ClassContext** can be the path to the registry key that contains the properties to be reported.</span></span>
-   <span data-ttu-id="441c8-123">Квалификатор **пропертиконтекст** указывает зависящую от контекста информацию, относящуюся к свойству.</span><span class="sxs-lookup"><span data-stu-id="441c8-123">The **PropertyContext** qualifier specifies context-specific information that pertains to the property.</span></span> <span data-ttu-id="441c8-124">Например, в классе, используемом для хранения данных, предоставляемых поставщиком реестра, **пропертиконтекст** указывает имя значения реестра, которое будет храниться в свойстве.</span><span class="sxs-lookup"><span data-stu-id="441c8-124">For example, in a class used to store data supplied by the Registry provider, **PropertyContext** specifies the name of the registry value to be stored by the property.</span></span>

<span data-ttu-id="441c8-125">Эти квалификаторы могут работать вместе.</span><span class="sxs-lookup"><span data-stu-id="441c8-125">These qualifiers can work together.</span></span> <span data-ttu-id="441c8-126">Можно назначить значение **InstanceContext** и **пропертиконтекст** , чтобы сообщить поставщику о том, как обрабатывать определенные типы экземпляров.</span><span class="sxs-lookup"><span data-stu-id="441c8-126">You can designate both an **InstanceContext** and **PropertyContext** value to tell the provider how to treat particular types of instances.</span></span> <span data-ttu-id="441c8-127">Например, можно пометить экземпляры, которые поставщик будет распознать как доступный для чтения, но получив только одно записываемое свойство.</span><span class="sxs-lookup"><span data-stu-id="441c8-127">For example, you might want to mark instances the provider will recognize as readable but having only one writeable property.</span></span>

<span data-ttu-id="441c8-128">Наиболее распространенный квалификатор — **пропертиконтекст**.</span><span class="sxs-lookup"><span data-stu-id="441c8-128">The most common qualifier used is **PropertyContext**.</span></span> <span data-ttu-id="441c8-129">Таким образом, WMI предоставляет квалификатор **динпропс** в качестве ярлыка.</span><span class="sxs-lookup"><span data-stu-id="441c8-129">Therefore, WMI provides the **DynProps** qualifier as a shortcut.</span></span> <span data-ttu-id="441c8-130">Инструментарий WMI считает, что каждое свойство в экземпляре, помеченном **динпропс** , также имеет квалификаторы **dynamic**, [**provider**](/windows/desktop/api/Provider/nl-provider-provider)и **пропертиконтекст** .</span><span class="sxs-lookup"><span data-stu-id="441c8-130">WMI considers each property in an instance marked with **DynProps** to also have the **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **PropertyContext** qualifiers.</span></span>

 

 



