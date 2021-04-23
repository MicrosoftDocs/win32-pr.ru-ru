---
description: Телефонная связь Майкрософт моделирует кнопки телефонов и лампы в виде пар «кнопка-лампа».
ms.assetid: 6ac912bb-8d2b-4aa3-a6e8-af86fbaabd58
title: Кнопки (API телефонии)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd1fc18e02331f98f4dbb98cfea7d9df2ca7f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673527"
---
# <a name="buttons-telephony-api"></a><span data-ttu-id="047e6-103">Кнопки (API телефонии)</span><span class="sxs-lookup"><span data-stu-id="047e6-103">Buttons (Telephony API)</span></span>

<span data-ttu-id="047e6-104">Телефонная связь Майкрософт моделирует кнопки и лампы телефона в виде пар "кнопка-лампа".</span><span class="sxs-lookup"><span data-stu-id="047e6-104">Microsoft Telephony models a phone's buttons and lamps as button-lamp pairs.</span></span> <span data-ttu-id="047e6-105">Кнопка с индикатором "нет лампы" или лампа без кнопки задается с помощью фиктивного индикатора для отсутствующей лампы или кнопки.</span><span class="sxs-lookup"><span data-stu-id="047e6-105">A button with no lamp next to it, or a lamp with no button is specified using a dummy indicator for the missing lamp or button.</span></span> <span data-ttu-id="047e6-106">Кнопка с несколькими лампами моделируется с помощью нескольких пар «кнопка-лампа».</span><span class="sxs-lookup"><span data-stu-id="047e6-106">A button with multiple lamps is modeled by using multiple button-lamp pairs.</span></span>

<span data-ttu-id="047e6-107">Можно задать и получить сведения, связанные с кнопкой телефона.</span><span class="sxs-lookup"><span data-stu-id="047e6-107">Information associated with a phone button can be set and retrieved.</span></span> <span data-ttu-id="047e6-108">При нажатии кнопки поставщик услуг отправляет сообщение [**\_ кнопки телефона**](/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)) функции обратного вызова TAPI.</span><span class="sxs-lookup"><span data-stu-id="047e6-108">When a button is pressed, the service provider sends a [**PHONE\_BUTTON**](/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)) message to the TAPI callback function.</span></span> <span data-ttu-id="047e6-109">Параметры этого сообщения являются маркером телефонного устройства и идентификатором кнопки или лампы нажатой кнопки.</span><span class="sxs-lookup"><span data-stu-id="047e6-109">Parameters of this message are a handle to the phone device and the button/lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="047e6-110">Кнопкам "0" с "9", " \* " и " \# " назначены фиксированные идентификаторы кнопок и лампы от 0 до 11.</span><span class="sxs-lookup"><span data-stu-id="047e6-110">The keypad button '0' through '9', '\*', and '\#' are assigned fixed button/lamp identifiers 0 through 11.</span></span>

<span data-ttu-id="047e6-111">Функция [**тспи \_ фонесетбуттонинфо**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo) задает сведения, связанные с кнопкой на телефонном устройстве.</span><span class="sxs-lookup"><span data-stu-id="047e6-111">The function [**TSPI\_phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo) sets the information associated with a button on a phone device.</span></span> <span data-ttu-id="047e6-112">[**Тспи \_ фонежетбуттонинфо**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetbuttoninfo) возвращает сведения, связанные с кнопкой на телефонном устройстве.</span><span class="sxs-lookup"><span data-stu-id="047e6-112">[**TSPI\_phoneGetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetbuttoninfo) returns information associated with a button on a phone device.</span></span> <span data-ttu-id="047e6-113">Поставщик услуг отправляет \_ сообщение кнопки телефона функции обратного вызова TAPI при нажатии кнопки на телефоне.</span><span class="sxs-lookup"><span data-stu-id="047e6-113">The service provider sends a PHONE\_BUTTON message to the TAPI callback function when a button on the phone is pressed.</span></span>

<span data-ttu-id="047e6-114">Сведения, связанные с кнопкой, не имеют семантического смысла, чем ТСПИ.</span><span class="sxs-lookup"><span data-stu-id="047e6-114">The information associated with a button does not carry any semantic meaning as far as TSPI is concerned.</span></span> <span data-ttu-id="047e6-115">Он полезен для приложений для конкретных устройств, которые преобразуют эту информацию для конкретного телефонного устройства или для пользователя, например, в справочной системе приложения.</span><span class="sxs-lookup"><span data-stu-id="047e6-115">It is useful for device-specific applications that interpret this information for a given phone device, or for display to the user, such as in an application's help system.</span></span>

 

 
