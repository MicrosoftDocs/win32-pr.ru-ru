---
title: Рекомендации по серверам
description: Чтобы обеспечить работу Microsoft Active Accessibility, серверы должны предоставить клиентам сведения о специальных возможностях.
ms.assetid: 88be4bae-fdeb-467c-b5b1-19f2adc0575d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344721428c94e2ea3d9e9ff78e194851ba9304db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410713"
---
# <a name="server-guidelines"></a><span data-ttu-id="81a86-103">Рекомендации по серверам</span><span class="sxs-lookup"><span data-stu-id="81a86-103">Server Guidelines</span></span>

<span data-ttu-id="81a86-104">Чтобы обеспечить работу Microsoft Active Accessibility, серверы должны предоставить клиентам сведения о специальных возможностях.</span><span class="sxs-lookup"><span data-stu-id="81a86-104">For Microsoft Active Accessibility to work as designed, servers must provide accessibility information to clients.</span></span>

<span data-ttu-id="81a86-105">Для реализации [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)разработчики сервера должны следовать этому базовому процессу.</span><span class="sxs-lookup"><span data-stu-id="81a86-105">To implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), server developers must follow this basic process.</span></span>

1.  <span data-ttu-id="81a86-106">Создайте объекты со специальными возможностями, реализовав свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и методы для пользовательских элементов пользовательского интерфейса и для клиента приложения.</span><span class="sxs-lookup"><span data-stu-id="81a86-106">Create accessible objects by implementing the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods for your custom user interface elements and for your application's client.</span></span> <span data-ttu-id="81a86-107">Не забудьте предоставить сдвоенный интерфейс, поддерживающий и **IAccessible** , и [**IDispatch**](idispatch-interface.md) , чтобы клиенты, написанные на Visual Basic Майкрософт и различные языки сценариев, могли получить сведения об этих объектах.</span><span class="sxs-lookup"><span data-stu-id="81a86-107">Be sure to provide a dual interface that supports both **IAccessible** and [**IDispatch**](idispatch-interface.md) so that clients written in Microsoft Visual Basic and various scripting languages can get information about the objects.</span></span>
2.  <span data-ttu-id="81a86-108">Вызовите [**нотифивиневент**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) , чтобы уведомить клиентов об изменениях в пользовательских элементах пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="81a86-108">Call [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) to notify clients of changes to your custom user interface elements.</span></span>
3.  <span data-ttu-id="81a86-109">Обработайте [**WM \_ GetObject**](wm-getobject.md) для предоставления доступа к доступным объектам.</span><span class="sxs-lookup"><span data-stu-id="81a86-109">Handle [**WM\_GETOBJECT**](wm-getobject.md) to provide access to your accessible objects.</span></span>

<span data-ttu-id="81a86-110">Рекомендации и рекомендации по проектированию объектов со специальными возможностями см. в [Руководстве разработчика для Active Accessibility серверов](developer-s-guide-for-active-accessibility-servers.md).</span><span class="sxs-lookup"><span data-stu-id="81a86-110">For suggestions and guidelines for designing accessible objects, see [Developer's Guide for Active Accessibility Servers](developer-s-guide-for-active-accessibility-servers.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="81a86-111">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="81a86-111">In this section</span></span>

-   [<span data-ttu-id="81a86-112">Как серверы реализуют дочерние идентификаторы</span><span class="sxs-lookup"><span data-stu-id="81a86-112">How Servers Implement Child IDs</span></span>](how-servers-implement-child-ids.md)

 

 




