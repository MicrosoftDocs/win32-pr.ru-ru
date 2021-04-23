---
title: Перегрузка Ипропертинотифисинк
description: Перегрузка Ипропертинотифисинк
ms.assetid: c6d52da0-7b7e-4ca8-b903-310bf988d2f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037b27650ae68f355962454ae154d7c332c73518
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411281"
---
# <a name="overloading-ipropertynotifysink"></a><span data-ttu-id="69ba1-103">Перегрузка Ипропертинотифисинк</span><span class="sxs-lookup"><span data-stu-id="69ba1-103">Overloading IPropertyNotifySink</span></span>

<span data-ttu-id="69ba1-104">Многие контейнеры элементов управления ActiveX реализуют немодальное окно обзора свойств.</span><span class="sxs-lookup"><span data-stu-id="69ba1-104">Many ActiveX control containers implement a modeless property browsing window.</span></span> <span data-ttu-id="69ba1-105">Если свойства элемента управления изменяются с помощью страниц свойств элемента управления, то свойства элемента управления могут оказаться несинхронизированными с представлениями этих свойств контейнера (элемент управления всегда является верным).</span><span class="sxs-lookup"><span data-stu-id="69ba1-105">If a control's properties are altered through the control's property pages, then the control's properties can get out of sync with the container's view of those properties (the control is always right, of course).</span></span> <span data-ttu-id="69ba1-106">Чтобы гарантировать, что оно всегда имеет текущие значения для свойств элемента управления, контейнер элемента управления ActiveX может перегрузить интерфейс [**ипропертинотифисинк**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) (привязка данных), а также использовать его для уведомления об изменении свойства элемента управления.</span><span class="sxs-lookup"><span data-stu-id="69ba1-106">To ensure that it always has the current values for a control's properties, an ActiveX control container can overload the [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) interface (data binding) and also use it to be notified that a control property has changed.</span></span> <span data-ttu-id="69ba1-107">Этот метод является необязательным и не является обязательным для контейнеров элементов управления ActiveX или элементов управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="69ba1-107">This technique is optional and is not required of ActiveX control containers or ActiveX controls.</span></span>

<span data-ttu-id="69ba1-108">Обратите внимание, что элемент управления должен использовать [**уведомление OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) только для привязки данных. для обеих целей можно использовать [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) .</span><span class="sxs-lookup"><span data-stu-id="69ba1-108">Note that a control should use [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) only for data binding; it is free to use [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) for either or both purposes.</span></span>

 

 




