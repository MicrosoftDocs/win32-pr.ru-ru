---
description: TAPI моделирует кнопки телефонов и лампы в виде пар «кнопка-лампа».
ms.assetid: e4c50bd6-a256-407f-af3b-b24383a30ea0
title: Кнопки телефона
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3e65c34096c0cf043b85d80c9c726c6bef982d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812484"
---
# <a name="phone-buttons"></a><span data-ttu-id="7b84f-103">Кнопки телефона</span><span class="sxs-lookup"><span data-stu-id="7b84f-103">Phone Buttons</span></span>

<span data-ttu-id="7b84f-104">TAPI моделирует кнопки и лампы телефона как пары "кнопка-лампа".</span><span class="sxs-lookup"><span data-stu-id="7b84f-104">TAPI models a phone's buttons and lamps as button-lamp pairs.</span></span> <span data-ttu-id="7b84f-105">Кнопка без лампы рядом с ней или лампа без кнопки задается с помощью "фиктивного" индикатора для отсутствующей лампы или кнопки.</span><span class="sxs-lookup"><span data-stu-id="7b84f-105">A button with no lamp next to it or a lamp with no button is specified using a "dummy" indicator for the missing lamp or button.</span></span> <span data-ttu-id="7b84f-106">Кнопка с несколькими лампами моделируется с помощью нескольких пар «кнопка-лампа».</span><span class="sxs-lookup"><span data-stu-id="7b84f-106">A button with multiple lamps is modeled by using multiple button-lamp pairs.</span></span>

<span data-ttu-id="7b84f-107">Можно задать и получить сведения, связанные с кнопкой телефона.</span><span class="sxs-lookup"><span data-stu-id="7b84f-107">Information associated with a phone button can be set and retrieved.</span></span> <span data-ttu-id="7b84f-108">При нажатии кнопки в функцию приложения отправляется сообщение [**\_ кнопки телефона**](phone-button.md) .</span><span class="sxs-lookup"><span data-stu-id="7b84f-108">When a button is pressed, a [**PHONE\_BUTTON**](phone-button.md) message is sent to the application function.</span></span> <span data-ttu-id="7b84f-109">Параметры этого сообщения являются маркером телефонного устройства и идентификатором лампы кнопки, которая была нажата.</span><span class="sxs-lookup"><span data-stu-id="7b84f-109">The parameters of this message are a handle to the phone device and the button-lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="7b84f-110">Кнопкам с "0" до "9", " \* " и " \# " назначаются кнопки с идентификатором лампы от 0 до 11.</span><span class="sxs-lookup"><span data-stu-id="7b84f-110">The keypad buttons '0' through '9', '\*', and '\#' are assigned the fixed button-lamp identifiers 0 through 11.</span></span>

<span data-ttu-id="7b84f-111">К функциям, связанным с кнопками, относятся [**фонесетбуттонинфо**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), которые задают информацию, связанную с кнопкой на телефонном устройстве, и [**фонежетбуттонинфо**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), которая возвращает сведения, связанные с кнопкой на телефонном устройстве.</span><span class="sxs-lookup"><span data-stu-id="7b84f-111">The functions associated with buttons are [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), which sets the information associated with a button on a phone device, and [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), which returns information associated with a button on a phone device.</span></span> <span data-ttu-id="7b84f-112">\_При нажатии кнопки на телефоне в приложение отправляется сообщение кнопки телефона.</span><span class="sxs-lookup"><span data-stu-id="7b84f-112">The PHONE\_BUTTON message is sent to an application when a button on the phone is pressed.</span></span>

<span data-ttu-id="7b84f-113">Информация, связанная с кнопкой, не имеет никаких семантических значений, чем касается TAPI.</span><span class="sxs-lookup"><span data-stu-id="7b84f-113">The information associated with a button does not carry any semantic meaning as far as TAPI is concerned.</span></span> <span data-ttu-id="7b84f-114">Он полезен для приложений для конкретных устройств, которые понимают смысл этой информации для конкретного телефонного устройства или для пользователя, например интерактивной справки.</span><span class="sxs-lookup"><span data-stu-id="7b84f-114">It is useful for device-specific applications that understand the meaning of this information for a given phone device, or for display to the user, such as online help.</span></span>

 

 



