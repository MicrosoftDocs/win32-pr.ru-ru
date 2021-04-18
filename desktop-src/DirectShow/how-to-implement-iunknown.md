---
description: Реализация IUnknown
ms.assetid: 4e363ccb-9725-4be6-bb31-283bf1d658f5
title: Реализация IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27c12e25d56adab1841a375ac6c1ce0857a73b5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536527"
---
# <a name="how-to-implement-iunknown"></a><span data-ttu-id="edace-103">Реализация IUnknown</span><span class="sxs-lookup"><span data-stu-id="edace-103">How to Implement IUnknown</span></span>

<span data-ttu-id="edace-104">Microsoft DirectShow основана на модели COM.</span><span class="sxs-lookup"><span data-stu-id="edace-104">Microsoft DirectShow is based on the Component Object Model (COM).</span></span> <span data-ttu-id="edace-105">При написании собственного фильтра его необходимо реализовать как COM-объект.</span><span class="sxs-lookup"><span data-stu-id="edace-105">If you write your own filter, you must implement it as a COM object.</span></span> <span data-ttu-id="edace-106">Базовые классы DirectShow предоставляют платформу, из которой это можно сделать.</span><span class="sxs-lookup"><span data-stu-id="edace-106">The DirectShow base classes provide a framework from which to do this.</span></span> <span data-ttu-id="edace-107">Использование базовых классов не является обязательным, но может упростить процесс разработки.</span><span class="sxs-lookup"><span data-stu-id="edace-107">Using the base classes is not required, but it can simplify the development process.</span></span> <span data-ttu-id="edace-108">В этой статье описываются некоторые внутренние сведения о COM-объектах и их реализации в базовых классах DirectShow.</span><span class="sxs-lookup"><span data-stu-id="edace-108">This article describes some of the internal details of COM objects and their implementation in the DirectShow base classes.</span></span>

<span data-ttu-id="edace-109">В этой статье предполагается, что вы знаете, как программировать клиентские приложения COM, иными словами, что вы понимаете методы в **IUnknown**, но не предполагается, что он имеет опыт разработки COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="edace-109">This article assumes that you know how to program COM client applications—in other words, that you understand the methods in **IUnknown**—but does not assume any prior experience developing COM objects.</span></span> <span data-ttu-id="edace-110">DirectShow обрабатывает множество деталей разработки COM-объекта.</span><span class="sxs-lookup"><span data-stu-id="edace-110">DirectShow handles many of the details of developing a COM object.</span></span> <span data-ttu-id="edace-111">Если у вас есть опыт разработки COM-объектов, следует прочитать раздел [с помощью кункновн](using-cunknown.md), который описывает базовый класс [**кункновн**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="edace-111">If you have experience developing COM objects, you should read the section [Using CUnknown](using-cunknown.md), which describes the [**CUnknown**](cunknown.md) base class.</span></span>

<span data-ttu-id="edace-112">COM является спецификацией, а не реализацией.</span><span class="sxs-lookup"><span data-stu-id="edace-112">COM is a specification, not an implementation.</span></span> <span data-ttu-id="edace-113">Он определяет правила, которые должен выполнить компонент. перевод этих правил в действие остается разработчиком.</span><span class="sxs-lookup"><span data-stu-id="edace-113">It defines the rules that a component must follow; putting those rules into effect is left to the developer.</span></span> <span data-ttu-id="edace-114">В DirectShow все объекты являются производными от набора базовых классов C++.</span><span class="sxs-lookup"><span data-stu-id="edace-114">In DirectShow, all objects derive from a set of C++ base classes.</span></span> <span data-ttu-id="edace-115">Конструкторы и методы базового класса выполняют большую часть работы по регистрации COM, например поддержание постоянного счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="edace-115">The base class constructors and methods do most of the COM "bookkeeping" work, such as keeping a consistent reference count.</span></span> <span data-ttu-id="edace-116">Производя фильтр от базового класса, вы наследуете функциональность класса.</span><span class="sxs-lookup"><span data-stu-id="edace-116">By deriving your filter from a base class, you inherit the functionality of the class.</span></span> <span data-ttu-id="edace-117">Чтобы эффективно использовать базовые классы, необходимо общее понимание того, как они реализуют спецификацию COM.</span><span class="sxs-lookup"><span data-stu-id="edace-117">To use base classes effectively, you need a general understanding of how they implement the COM specification.</span></span>

<span data-ttu-id="edace-118">Эта статья содержит следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="edace-118">This article contains the following topics.</span></span>

-   [<span data-ttu-id="edace-119">Принцип работы IUnknown</span><span class="sxs-lookup"><span data-stu-id="edace-119">How IUnknown Works</span></span>](how-iunknown-works.md)
-   [<span data-ttu-id="edace-120">Использование Кункновн</span><span class="sxs-lookup"><span data-stu-id="edace-120">Using CUnknown</span></span>](using-cunknown.md)

## <a name="related-topics"></a><span data-ttu-id="edace-121">См. также</span><span class="sxs-lookup"><span data-stu-id="edace-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edace-122">DirectShow и COM</span><span class="sxs-lookup"><span data-stu-id="edace-122">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



