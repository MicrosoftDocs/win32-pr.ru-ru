---
title: Включение и делегирование
description: Наиболее распространенным механизмом повторного использования объектов в COM является включение или делегирование.
ms.assetid: 56396c11-889a-4f28-8fa7-9e48c805c501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d26e0c1d1e48596cb9acef740405c797f6f0f46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332355"
---
# <a name="containmentdelegation"></a><span data-ttu-id="0d738-103">Включение и делегирование</span><span class="sxs-lookup"><span data-stu-id="0d738-103">Containment/Delegation</span></span>

<span data-ttu-id="0d738-104">Наиболее распространенным механизмом повторного использования объектов в COM является *Включение или делегирование*.</span><span class="sxs-lookup"><span data-stu-id="0d738-104">The most common mechanism for object reuse in COM is *containment/delegation*.</span></span> <span data-ttu-id="0d738-105">Этот тип повторного использования является знакомым понятием в большинстве объектно-ориентированных языков и систем.</span><span class="sxs-lookup"><span data-stu-id="0d738-105">This type of reuse is a familiar concept found in most object-oriented languages and systems.</span></span> <span data-ttu-id="0d738-106">Внешний объект, который должен использовать внутренний объект, выступает в качестве клиента объекта для внутреннего объекта.</span><span class="sxs-lookup"><span data-stu-id="0d738-106">The outer object, which needs to make use of the inner object, acts as an object client to the inner object.</span></span> <span data-ttu-id="0d738-107">Внешний объект "содержит" внутренний объект, а если внешний объект требует службы внутреннего объекта, внешний объект явно делегирует реализацию методам внутреннего объекта.</span><span class="sxs-lookup"><span data-stu-id="0d738-107">The outer object "contains" the inner object, and when the outer object requires the services of the inner object, the outer object explicitly delegates implementation to the inner object's methods.</span></span> <span data-ttu-id="0d738-108">То есть внешний объект использует службы внутреннего объекта для реализации самого себя.</span><span class="sxs-lookup"><span data-stu-id="0d738-108">That is, the outer object uses the inner object's services to implement itself.</span></span>

<span data-ttu-id="0d738-109">Внешние и внутренние объекты не обязательно должны поддерживать одни и те же интерфейсы, хотя, безусловно, разумно содержать объект, реализующий интерфейс, который не реализует внешний объект, и реализовывать методы внешнего объекта просто как вызовы соответствующих методов во внутреннем объекте.</span><span class="sxs-lookup"><span data-stu-id="0d738-109">It is not necessary for the outer and inner objects to support the same interfaces, although it certainly is reasonable to contain an object that implements an interface that the outer object does not and implement the methods of the outer object simply as calls to the corresponding methods in the inner object.</span></span> <span data-ttu-id="0d738-110">Однако если сложность внешнего и внутреннего объектов сильно отличается, внешний объект может реализовать некоторые методы его интерфейсов, делегируя вызовы к методам интерфейса, реализованным во внутреннем объекте.</span><span class="sxs-lookup"><span data-stu-id="0d738-110">When the complexity of the outer and inner objects differs greatly, however, the outer object may implement some of the methods of its interfaces by delegating calls to interface methods implemented in the inner object.</span></span>

<span data-ttu-id="0d738-111">Реализовать вложение для внешнего объекта очень просто.</span><span class="sxs-lookup"><span data-stu-id="0d738-111">It is simple to implement containment for an outer object.</span></span> <span data-ttu-id="0d738-112">Внешний объект создает внутренние объекты, которые он должен использовать как любой другой клиент.</span><span class="sxs-lookup"><span data-stu-id="0d738-112">The outer object creates the inner objects it needs to use as any other client would.</span></span> <span data-ttu-id="0d738-113">Ничего нового — этот процесс похож на объект C++, который сам содержит строковый объект C++, используемый для выполнения определенных строковых функций, даже если внешний объект не считается строковым объектом в его собственном правом.</span><span class="sxs-lookup"><span data-stu-id="0d738-113">This is nothing new—the process is like a C++ object that itself contains a C++ string object that it uses to perform certain string functions, even if the outer object is not considered a string object in its own right.</span></span> <span data-ttu-id="0d738-114">Затем, используя указатель на внутренний объект, вызов метода во внешнем объекте создает вызов метода внутреннего объекта.</span><span class="sxs-lookup"><span data-stu-id="0d738-114">Then, using its pointer to the inner object, a call to a method in the outer object generates a call to an inner object method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d738-115">См. также</span><span class="sxs-lookup"><span data-stu-id="0d738-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d738-116">Статистической обработки</span><span class="sxs-lookup"><span data-stu-id="0d738-116">Aggregation</span></span>](aggregation.md)
</dt> </dl>

 

 




