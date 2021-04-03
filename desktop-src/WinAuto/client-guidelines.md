---
title: Рекомендации для клиентов
description: Разработчики клиентов должны использовать следующие функциональные возможности для получения сведений об элементах пользовательского интерфейса.
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ced411c24ed0b7aa3ab97cbe1ce2511d4e6b05
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "103987143"
---
# <a name="client-guidelines"></a><span data-ttu-id="0e5e7-103">Рекомендации для клиентов</span><span class="sxs-lookup"><span data-stu-id="0e5e7-103">Client Guidelines</span></span>

<span data-ttu-id="0e5e7-104">Разработчики клиентов должны использовать следующие функциональные возможности для получения сведений о элементах пользовательского интерфейса:</span><span class="sxs-lookup"><span data-stu-id="0e5e7-104">Client developers should use the following functionality to get information about the user interface elements:</span></span>

-   <span data-ttu-id="0e5e7-105">Чтобы получить интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для объектов, вызовите [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)или [**акцессиблеобжектфромевент**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span><span class="sxs-lookup"><span data-stu-id="0e5e7-105">To get an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface to objects, call [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), or [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span></span>
-   <span data-ttu-id="0e5e7-106">Для проверки доступных объектов и управления ими используйте свойства и методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="0e5e7-106">To examine and manipulate accessible objects, use the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods.</span></span>
-   <span data-ttu-id="0e5e7-107">Чтобы получить [виневентс](winevents-overview.md), вызовите [**сетвиневенсук**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) , чтобы зарегистрировать функцию обратного вызова WinEvent для событий, относящихся к клиентскому приложению.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-107">To receive [WinEvents](winevents-overview.md), call [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) to register a WinEvent callback function for those events that are relevant to the client application.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0e5e7-108">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="0e5e7-108">In this section</span></span>

-   [<span data-ttu-id="0e5e7-109">Получение идентификаторов дочерних объектов клиентами</span><span class="sxs-lookup"><span data-stu-id="0e5e7-109">How Clients Obtain Child IDs</span></span>](how-clients-obtain-child-ids.md)

 

 




