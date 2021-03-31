---
title: Получение ошибок для указателей интерфейса IAccessible
description: В этом разделе описываются ситуации, в которых может возникнуть ошибка для указателя на интерфейс IAccessible.
ms.assetid: 408bfa47-fda0-4a25-89c1-da41d967ad61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d3bd9e39dae9c5de9ad1644e5955bd5fb90d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888783"
---
# <a name="receiving-errors-for-iaccessible-interface-pointers"></a><span data-ttu-id="2fbe4-103">Получение ошибок для указателей интерфейса IAccessible</span><span class="sxs-lookup"><span data-stu-id="2fbe4-103">Receiving Errors for IAccessible Interface Pointers</span></span>

<span data-ttu-id="2fbe4-104">В этом разделе описываются ситуации, в которых может возникнуть ошибка для указателя на интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="2fbe4-104">This topic describes situations in which you might receive an error for an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span> <span data-ttu-id="2fbe4-105">Функции **IAccessible** могут возвращать ошибки для указателей на интерфейсы **IAccessible** , когда пользователь закрывает приложение, которому принадлежит объект, или если пользователь откроет элемент управления через пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2fbe4-105">**IAccessible** functions can return errors for **IAccessible** interface pointers when a user closes an application that the object belongs to, or if a user dismisses a control through the user interface.</span></span>

## <a name="user-closes-an-application"></a><span data-ttu-id="2fbe4-106">Пользователь закрывает приложение</span><span class="sxs-lookup"><span data-stu-id="2fbe4-106">User Closes an Application</span></span>

<span data-ttu-id="2fbe4-107">Если пользователь закрывает приложение, содержащее объект, указывающий на указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , все будущие вызовы этого объекта будут возвращать код ошибки.</span><span class="sxs-lookup"><span data-stu-id="2fbe4-107">If a user closes the application that contains an object to which the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer was pointing, then all future calls to that object will return an error code.</span></span> <span data-ttu-id="2fbe4-108">Ошибка, например **CO \_ E \_ обжнотконнектед**, указывает, что объект больше не существует.</span><span class="sxs-lookup"><span data-stu-id="2fbe4-108">The error, such as **CO\_E\_OBJNOTCONNECTED**, will indicate that the object does not exist anymore.</span></span> <span data-ttu-id="2fbe4-109">Это относится ко всем указателям интерфейса **IAccessible** .</span><span class="sxs-lookup"><span data-stu-id="2fbe4-109">This applies to all **IAccessible** interface pointers.</span></span>

## <a name="user-dismisses-a-control"></a><span data-ttu-id="2fbe4-110">Пользователь закрывает элемент управления</span><span class="sxs-lookup"><span data-stu-id="2fbe4-110">User Dismisses a Control</span></span>

<span data-ttu-id="2fbe4-111">Если пользователь закрывает элемент управления (например, нажав кнопку "Отправить"), клиенты по-прежнему могут вызывать методы и свойства метода [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для этого объекта, так как объект не был освобожден.</span><span class="sxs-lookup"><span data-stu-id="2fbe4-111">If a user dismisses a control (for example, by pressing a push button), clients can still call [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties on this object because the object has not been released.</span></span> <span data-ttu-id="2fbe4-112">Однако будущие вызовы будут поступать с сообщениями об ошибках.</span><span class="sxs-lookup"><span data-stu-id="2fbe4-112">However, future calls will receive error messages.</span></span>

<span data-ttu-id="2fbe4-113">Эта ситуация относится к следующим функциям и методам:</span><span class="sxs-lookup"><span data-stu-id="2fbe4-113">This situation applies to the following functions and methods:</span></span>

-   [<span data-ttu-id="2fbe4-114">**акцессиблеобжектфромевент**</span><span class="sxs-lookup"><span data-stu-id="2fbe4-114">**AccessibleObjectFromEvent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)
-   [<span data-ttu-id="2fbe4-115">**акцессиблеобжектфромпоинт**</span><span class="sxs-lookup"><span data-stu-id="2fbe4-115">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [<span data-ttu-id="2fbe4-116">**акцессиблеобжектфромвиндов**</span><span class="sxs-lookup"><span data-stu-id="2fbe4-116">**AccessibleObjectFromWindow**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [<span data-ttu-id="2fbe4-117">**IAccessible:: Акчиттест**</span><span class="sxs-lookup"><span data-stu-id="2fbe4-117">**IAccessible::accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="2fbe4-118">**IAccessible:: Аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="2fbe4-118">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="2fbe4-119">**IAccessible:: Get \_ аккфокус**</span><span class="sxs-lookup"><span data-stu-id="2fbe4-119">**IAccessible::get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [<span data-ttu-id="2fbe4-120">**IAccessible:: Get \_ аккселектион**</span><span class="sxs-lookup"><span data-stu-id="2fbe4-120">**IAccessible::get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)

 

 




