---
title: Предоставление дополнительных сведений, не охваченных интерфейсом IAccessible
description: В зависимости от своих продуктов разработчикам серверов может потребоваться предоставить сведения или функции в дополнение к поддержке Microsoft Active Accessibility.
ms.assetid: c45009ca-6be3-4645-9097-36671a41dfce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3834c60de8f18fd5ec0719919a1cd79e22f451e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338665"
---
# <a name="exposing-additional-information-not-covered-by-iaccessible-interface"></a><span data-ttu-id="c097a-103">Предоставление дополнительных сведений, не охваченных интерфейсом IAccessible</span><span class="sxs-lookup"><span data-stu-id="c097a-103">Exposing Additional Information Not Covered by IAccessible Interface</span></span>

<span data-ttu-id="c097a-104">В зависимости от своих продуктов разработчикам серверов может потребоваться предоставить сведения или функции в дополнение к поддержке Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="c097a-104">Depending on their products, server developers might need to expose information or functionality in addition to Microsoft Active Accessibility support.</span></span> <span data-ttu-id="c097a-105">Если это так, обратитесь к разработчикам вспомогательных технологий (клиенты), чтобы убедиться, что они добавляют поддержку функций.</span><span class="sxs-lookup"><span data-stu-id="c097a-105">If this is the case, work with assistive technology vendors (clients) to ensure that they add support for the features.</span></span>

<span data-ttu-id="c097a-106">Не пытайтесь расширить интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="c097a-106">Do not attempt to extend the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="c097a-107">После публикации интерфейсы не могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="c097a-107">Interfaces cannot be changed once they are published.</span></span> <span data-ttu-id="c097a-108">Чтобы предоставить дополнительные сведения, используйте пользовательский интерфейс и предоставьте его с помощью одного из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="c097a-108">To expose additional information, use a custom interface and expose it by using one of the following techniques:</span></span>

-   [<span data-ttu-id="c097a-109">Использование OBJID \_ нативеом для предоставления собственного интерфейса объектной модели для окна</span><span class="sxs-lookup"><span data-stu-id="c097a-109">Using OBJID\_NATIVEOM to expose a native object model interface for a window</span></span>](using-objid-nativeom-to-expose-a-native-object-model-interface-for-a-window.md)
-   [<span data-ttu-id="c097a-110">Использование QueryService для предоставления собственного интерфейса объектной модели для объекта IAccessible</span><span class="sxs-lookup"><span data-stu-id="c097a-110">Using QueryService to expose a native object model interface for an IAccessible object</span></span>](using-queryservice-to-expose-a-native-object-model-interface-for-an-iaccessible-object.md)

<span data-ttu-id="c097a-111">Обратите внимание, что целью интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) является наличие четко определенного интерфейса, используемого серверами и клиентами.</span><span class="sxs-lookup"><span data-stu-id="c097a-111">Note that the goal of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is to have a well-defined interface that is used by servers and clients.</span></span> <span data-ttu-id="c097a-112">Прежде чем предоставлять доступ к пользовательским интерфейсам, не забудьте предоставить как можно больше информации через **IAccessible**.</span><span class="sxs-lookup"><span data-stu-id="c097a-112">Before exposing custom interfaces, be sure to expose as much information as possible through **IAccessible**.</span></span>

<span data-ttu-id="c097a-113">Нельзя использовать [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для предоставления настраиваемых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="c097a-113">You cannot use [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to expose custom interfaces.</span></span> <span data-ttu-id="c097a-114">Используйте **IServiceProvider:: QueryService** , как описано в следующих процедурах.</span><span class="sxs-lookup"><span data-stu-id="c097a-114">Use **IServiceProvider::QueryService** as outlined in the following procedures.</span></span>

 

 