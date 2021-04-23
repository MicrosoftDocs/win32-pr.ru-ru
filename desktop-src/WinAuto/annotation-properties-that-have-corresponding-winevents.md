---
title: Свойства аннотации, имеющие соответствующие Виневентс
description: Будьте внимательны при переопределении свойств, которые часто изменяются, особенно при проверке клиентами в результате WinEvent (состояние, значение и, для некоторых элементов управления, свойств имени).
ms.assetid: 2505d015-9381-4e1c-a10f-6db3fbb25ca3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a8849c66cb0067b63be1c846e9e140ae06f4b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413210"
---
# <a name="annotation-properties-that-have-corresponding-winevents"></a><span data-ttu-id="8b702-103">Свойства аннотации, имеющие соответствующие Виневентс</span><span class="sxs-lookup"><span data-stu-id="8b702-103">Annotation Properties That Have Corresponding WinEvents</span></span>

<span data-ttu-id="8b702-104">Будьте внимательны при переопределении свойств, которые часто изменяются, особенно при проверке клиентами в результате WinEvent ( [**состояние**](state-property.md), [**значение**](value-property.md)и, для некоторых элементов управления, свойств [**имени**](name-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="8b702-104">Be careful when overriding properties that change frequently, particularly those that are examined by clients as a result of a WinEvent (such as [**State**](state-property.md), [**Value**](value-property.md), and, for some controls, the [**Name**](name-property.md) properties).</span></span>

<span data-ttu-id="8b702-105">Во многих случаях, особенно для элементов управления USER и Комктл, WinEvent сообщает об изменении свойства перед уведомлением владельца элемента управления (обычно через [WM \_ Notify](../controls/wm-notify.md)).</span><span class="sxs-lookup"><span data-stu-id="8b702-105">In many cases, especially for USER and ComCtl controls, the WinEvent signaling a property change is sent before the owner of the control is notified (typically via [WM\_NOTIFY](../controls/wm-notify.md)).</span></span> <span data-ttu-id="8b702-106">Обновление свойства с помощью [**сетпропвалуе**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) в \_ обработчике уведомлений WM будет слишком поздно; клиенты, использующие обработчики в контексте, уже будут иметь доступ к старому значению.</span><span class="sxs-lookup"><span data-stu-id="8b702-106">Updating the property using [**SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) in the WM\_NOTIFY handler will be too late; clients using in-context hooking will already have accessed the old value.</span></span>

<span data-ttu-id="8b702-107">Управлять этими типами свойств можно с помощью объектов сервера обратного вызова (с помощью [**сетпропсервер**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)). Однако сервер не может использовать состояние, которое обновляется \_ обработчиком уведомлений WM, так как этот обработчик еще не был вызван.</span><span class="sxs-lookup"><span data-stu-id="8b702-107">You can handle these types of properties by using callback server objects (using [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)); however, the server cannot use any state that is updated in the WM\_NOTIFY handler because that handler will not yet have been called.</span></span> <span data-ttu-id="8b702-108">Например, вместо использования кэшированной переменной текущего значения, которая обновлена в \_ обработчике уведомлений WM и будет устаревшей, объект обратного вызова [**иаккпропсервер:: жетпропвалуе**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) должен отправить сообщение непосредственно в элемент управления, чтобы получить истинное текущее значение для создания требуемого свойства.</span><span class="sxs-lookup"><span data-stu-id="8b702-108">For example, instead of using a cached current value variable that is updated in the WM\_NOTIFY handler and will be out-of-date, the [**IAccPropServer::GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) callback object should send a message directly to the control to get its true current value to generate the required property.</span></span>

 

 