---
title: Повторное использование объектов
description: Повторное использование объектов
ms.assetid: 07055fea-bdfe-4c7a-be07-2edcbf609dd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a830eb539823b0350c9ce41a096cda821bb0cb
ms.sourcegitcommit: 917c90b6ed4af323fedada331211b40396876424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/08/2020
ms.locfileid: "104533080"
---
# <a name="reusing-objects"></a><span data-ttu-id="b00c5-103">Повторное использование объектов</span><span class="sxs-lookup"><span data-stu-id="b00c5-103">Reusing Objects</span></span>

<span data-ttu-id="b00c5-104">Важной целью любой объектной модели является предоставление авторам объектов возможности повторного использования и расширения объектов, предоставляемых другими пользователями, в виде частей собственных реализаций.</span><span class="sxs-lookup"><span data-stu-id="b00c5-104">An important goal of any object model is to enable object authors to reuse and extend objects provided by others as pieces of their own implementations.</span></span> <span data-ttu-id="b00c5-105">Одним из способов сделать это в Microsoft Visual C++ и других языках является использование *наследования реализации*, которое позволяет объекту наследовать (подкласс) некоторые из его функций из другого объекта при переопределении других функций.</span><span class="sxs-lookup"><span data-stu-id="b00c5-105">One way to do this in Microsoft Visual C++ and other languages is by using *implementation inheritance*, which allows an object to inherit ("subclass") some of its functions from another object while overriding other functions.</span></span>

<span data-ttu-id="b00c5-106">Проблема для взаимодействия с объектом в масштабе всей системы с помощью традиционной наследования реализации заключается в том, что контракт (интерфейс) между объектами в иерархии реализации не определен явным образом.</span><span class="sxs-lookup"><span data-stu-id="b00c5-106">The problem for systemwide object interaction using traditional implementation inheritance is that the contract (the interface) between objects in an implementation hierarchy is not clearly defined.</span></span> <span data-ttu-id="b00c5-107">Фактически он является неявным и неоднозначным.</span><span class="sxs-lookup"><span data-stu-id="b00c5-107">In fact, it is implicit and ambiguous.</span></span> <span data-ttu-id="b00c5-108">Когда родительский или дочерний объект изменяет свою реализацию, поведение связанных компонентов может стать неопределенным или унстабли реализованным.</span><span class="sxs-lookup"><span data-stu-id="b00c5-108">When the parent or child object changes its implementation, the behavior of related components might become undefined or unstably implemented.</span></span> <span data-ttu-id="b00c5-109">В любом приложении, где реализация может управляться одной группой инженеров, которая обновляет все компоненты одновременно, это не всегда является серьезной проблемой.</span><span class="sxs-lookup"><span data-stu-id="b00c5-109">In any single application, where the implementation can be managed by a single engineering team that updates all of the components at the same time, this is not always a major concern.</span></span> <span data-ttu-id="b00c5-110">В среде, в которой компоненты одной команды созданы с использованием черного ящика и других компонентов, созданных другими группами, этот тип нестабильной работы будет неустойчивым.</span><span class="sxs-lookup"><span data-stu-id="b00c5-110">In an environment where the components of one team are built through black-box reuse of other components built by other teams, this type of instability jeopardizes reuse.</span></span> <span data-ttu-id="b00c5-111">Кроме того, наследование реализации обычно работает только внутри границ процесса.</span><span class="sxs-lookup"><span data-stu-id="b00c5-111">Additionally, implementation inheritance usually works only within process boundaries.</span></span> <span data-ttu-id="b00c5-112">Это делает традиционную реализацию наследования непрактичной для крупных, развивающихся систем, состоящих из программных компонентов, созданных многими инженерными группами.</span><span class="sxs-lookup"><span data-stu-id="b00c5-112">This makes traditional implementation inheritance impractical for large, evolving systems composed of software components built by many engineering teams.</span></span>

<span data-ttu-id="b00c5-113">Ключом к созданию повторно используемых компонентов является возможность интерпретировать объект как непрозрачную рамку.</span><span class="sxs-lookup"><span data-stu-id="b00c5-113">The key to building reusable components is to be able to treat the object as an opaque box.</span></span> <span data-ttu-id="b00c5-114">Это означает, что фрагмент кода, пытающийся повторно использовать другой объект, не знает ничего и должен знать ничего, о внутренней структуре или реализации используемого компонента.</span><span class="sxs-lookup"><span data-stu-id="b00c5-114">This means that the piece of code attempting to reuse another object knows nothing, and needs to know nothing, about the internal structure or implementation of the component being used.</span></span> <span data-ttu-id="b00c5-115">Иными словами, код, пытающийся повторно использовать компонент, зависит от поведения объекта, а не от его точной реализации.</span><span class="sxs-lookup"><span data-stu-id="b00c5-115">In other words, the code attempting to reuse a component depends on the behavior of the object and not its exact implementation.</span></span>

<span data-ttu-id="b00c5-116">Чтобы обеспечить возможность повторного использования черного ящика, COM использует другие установленные механизмы повторного использования, такие как *Включение, делегирование* и *агрегирование*.</span><span class="sxs-lookup"><span data-stu-id="b00c5-116">To achieve black-box reusability, COM adopts other established reusability mechanisms such as *containment/delegation* and *aggregation*.</span></span>

> [!NOTE]  
> <span data-ttu-id="b00c5-117">Для удобства используемый объект называется *внутренним объектом* , и объект, выполняющий использование этого внутреннего объекта, является *внешним объектом*.</span><span class="sxs-lookup"><span data-stu-id="b00c5-117">For convenience, the object being reused is called the *inner object* and the object making use of that inner object is the *outer object*.</span></span>

 

<span data-ttu-id="b00c5-118">Важно помнить оба этих механизма того, как внешний объект отображается для его клиентов.</span><span class="sxs-lookup"><span data-stu-id="b00c5-118">It is important to remember in both these mechanisms how the outer object appears to its clients.</span></span> <span data-ttu-id="b00c5-119">С точки зрения клиентов, оба объекта реализуют интерфейсы, к которым клиент может получить указатель.</span><span class="sxs-lookup"><span data-stu-id="b00c5-119">As far as the clients are concerned, both objects implement any interfaces to which the client can get a pointer.</span></span> <span data-ttu-id="b00c5-120">Клиент рассматривает внешний объект как непрозрачное поле и, следовательно, не заботится о внутренней структуре внешней обжектâ € ", а также о том, что клиент заботится только о поведении.</span><span class="sxs-lookup"><span data-stu-id="b00c5-120">The client treats the outer object as an opaque box and therefore does not care, nor does it need to care, about the internal structure of the outer objectâ€”the client cares only about behavior.</span></span>

<span data-ttu-id="b00c5-121">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="b00c5-121">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="b00c5-122">Включение и делегирование</span><span class="sxs-lookup"><span data-stu-id="b00c5-122">Containment/Delegation</span></span>](containment-delegation.md)
-   [<span data-ttu-id="b00c5-123">Статистической обработки</span><span class="sxs-lookup"><span data-stu-id="b00c5-123">Aggregation</span></span>](aggregation.md)

 

 




