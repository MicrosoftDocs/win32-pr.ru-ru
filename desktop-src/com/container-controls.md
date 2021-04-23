---
title: Контейнерные элементы управления
description: Контейнерные элементы управления
ms.assetid: 4fa59272-54b6-4da9-a7f5-e1b4eab7fa80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69228bcc03017442880d41156f67397ee26bb13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487056"
---
# <a name="container-controls"></a><span data-ttu-id="b930b-103">Контейнерные элементы управления</span><span class="sxs-lookup"><span data-stu-id="b930b-103">Container Controls</span></span>

<span data-ttu-id="b930b-104">Как описано выше, контейнерные элементы управления — это элементы управления ActiveX, которые визуально содержат другие элементы управления.</span><span class="sxs-lookup"><span data-stu-id="b930b-104">As described above, container controls are ActiveX controls that visually contain other controls.</span></span> <span data-ttu-id="b930b-105">Архитектура элементов управления ActiveX определяет интерфейс [**исимплефрамесите**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) для включения элементов управления контейнера.</span><span class="sxs-lookup"><span data-stu-id="b930b-105">The ActiveX controls architecture specifies the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface to enable container controls.</span></span> <span data-ttu-id="b930b-106">Контейнеры также могут поддерживать элементы управления контейнера без поддержки **исимплефрамесите**, хотя поведение не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="b930b-106">Containers may also support container controls without supporting **ISimpleFrameSite**, although the behavior cannot be guaranteed.</span></span> <span data-ttu-id="b930b-107">По этой причине для элементов управления Симплефрамесите существует категория компонента, где требуются все функциональные возможности этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b930b-107">For this reason, a component category exists for SimpleFrameSite controls where the full functionality of this interface is required.</span></span>

<span data-ttu-id="b930b-108">Для поддержки элементов управления контейнера без реализации [**исимплефрамесите**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)контейнер элементов управления ActiveX должен:</span><span class="sxs-lookup"><span data-stu-id="b930b-108">To support container controls without implementing [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), an ActiveX control container must:</span></span>

-   <span data-ttu-id="b930b-109">Активируйте все элементы управления все время.</span><span class="sxs-lookup"><span data-stu-id="b930b-109">Activate all controls at all times.</span></span>
-   <span data-ttu-id="b930b-110">Переподчиненные вложенные элементы управления в hWnd содержащего его элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b930b-110">Reparent the contained controls to the hWnd of the containing control.</span></span>
-   <span data-ttu-id="b930b-111">Оставить родительский элемент контейнерного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b930b-111">Remain the parent of the container control.</span></span>

 

 




