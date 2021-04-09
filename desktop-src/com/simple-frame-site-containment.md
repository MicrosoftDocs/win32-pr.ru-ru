---
title: Включение веб-узла простого фрейма
description: Включение веб-узла простого фрейма
ms.assetid: 85c3565f-f557-43af-8d36-58414d0790cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0106bc88d9f69f380590e808741e0b1a0bdc2f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986329"
---
# <a name="simple-frame-site-containment"></a><span data-ttu-id="12d7a-103">Включение веб-узла простого фрейма</span><span class="sxs-lookup"><span data-stu-id="12d7a-103">Simple Frame Site Containment</span></span>

<span data-ttu-id="12d7a-104">Контейнерный элемент управления — это элемент управления ActiveX, который может содержать другие элементы управления.</span><span class="sxs-lookup"><span data-stu-id="12d7a-104">A container control is an ActiveX control that is capable of containing other controls.</span></span> <span data-ttu-id="12d7a-105">Примером элемента управления контейнера является поле группы, содержащее коллекцию переключателей.</span><span class="sxs-lookup"><span data-stu-id="12d7a-105">A group box that contains a collection of radio buttons is an example of a container control.</span></span> <span data-ttu-id="12d7a-106">Элементы управления "контейнер" должны установить \_ бит состояния СИМПЛЕФРАМЕ олемиск и вызывать его реализацию [**исимплефрамесите**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) контейнера.</span><span class="sxs-lookup"><span data-stu-id="12d7a-106">Container controls should set the OLEMISC\_SIMPLEFRAME status bit, and should call its container's [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) implementation.</span></span> <span data-ttu-id="12d7a-107">Контейнер элементов управления ActiveX, поддерживающий элементы управления контейнера, должен реализовывать **исимплефрамесите**.</span><span class="sxs-lookup"><span data-stu-id="12d7a-107">An ActiveX control container that supports container controls must implement **ISimpleFrameSite**.</span></span>

<span data-ttu-id="12d7a-108">CATID-{157083E0-2368-11cf-87B9-00AA006C8166} \_ СИМПЛЕФРАМЕКОНТРОЛ CATID</span><span class="sxs-lookup"><span data-stu-id="12d7a-108">CATID - {157083E0-2368-11cf-87B9-00AA006C8166} CATID\_SimpleFrameControl</span></span>

## <a name="related-topics"></a><span data-ttu-id="12d7a-109">См. также</span><span class="sxs-lookup"><span data-stu-id="12d7a-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12d7a-110">Категории компонентов</span><span class="sxs-lookup"><span data-stu-id="12d7a-110">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




