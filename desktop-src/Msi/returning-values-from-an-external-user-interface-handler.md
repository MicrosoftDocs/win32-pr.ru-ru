---
description: Внешний обработчик пользовательского интерфейса может возвращать любое количество значений, чтобы установщик Windows в зависимости от типа кнопки, предоставленной в параметре типа сообщения, который установщик передает в обработчик.
ms.assetid: a918082d-709d-4b4f-ae3b-5f16ed0ca910
title: Возвращение значений из внешнего обработчика пользовательского интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b466f6bc3cc034551a01bd2b87caa7292824e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811801"
---
# <a name="returning-values-from-an-external-user-interface-handler"></a><span data-ttu-id="d592a-103">Возвращение значений из внешнего обработчика пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="d592a-103">Returning Values from an External User Interface Handler</span></span>

<span data-ttu-id="d592a-104">Внешний обработчик пользовательского интерфейса может возвращать любое количество значений, чтобы установщик Windows в зависимости от типа кнопки, предоставленной в параметре типа сообщения, который установщик передает в обработчик.</span><span class="sxs-lookup"><span data-stu-id="d592a-104">An external user interface (UI) handler can return any number of values to Windows Installer depending on the button type provided in the message type parameter the installer passes to the handler.</span></span>

<span data-ttu-id="d592a-105">Внешний обработчик пользовательского интерфейса может возвращать значения – 1 и 0 в любое время, так как они не связаны с типами кнопок.</span><span class="sxs-lookup"><span data-stu-id="d592a-105">The external UI handler can return the values –1 and 0 at any time because these are not related to the button types.</span></span> <span data-ttu-id="d592a-106">Возвращаемое значение – 1 указывает, что во внешнем обработчике пользовательского интерфейса произошла внутренняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="d592a-106">A return value of –1 indicates that an internal error occurred in the external UI handler.</span></span> <span data-ttu-id="d592a-107">Возвращаемое значение 0 указывает, что внешний обработчик пользовательского интерфейса не обработал сообщение установщика, и установщик должен обработать сообщение.</span><span class="sxs-lookup"><span data-stu-id="d592a-107">A return value of 0 indicates that the external UI handler has not handled the installer message and the installer must handle the message instead.</span></span>

<span data-ttu-id="d592a-108">Для сообщений, не содержащих тип кнопки, например ИНСТАЛЛМЕССАЖЕ \_ актиондата и инсталлмессаже \_ , возврат идканцел отменяет установку.</span><span class="sxs-lookup"><span data-stu-id="d592a-108">For messages that do not include a button type, such as INSTALLMESSAGE\_ACTIONDATA and INSTALLMESSAGE\_PROGRESS, returning IDCANCEL cancels the installation.</span></span> <span data-ttu-id="d592a-109">Возврат ИДОК уведомляет установщик о том, что сообщение было обработано внешним обработчиком пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d592a-109">Returning IDOK notifies the installer that the message was handled by the external UI handler.</span></span>

<span data-ttu-id="d592a-110">Оставшиеся возвращаемые значения, как описано ниже, непосредственно связаны с типами кнопок, которые включены в тип сообщений.</span><span class="sxs-lookup"><span data-stu-id="d592a-110">The remaining return values, as described below, are directly related to the button types that are included with the message type.</span></span>



| <span data-ttu-id="d592a-111">Возвращаемое значение внешнего пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="d592a-111">External UI return value</span></span> | <span data-ttu-id="d592a-112">Значение</span><span class="sxs-lookup"><span data-stu-id="d592a-112">Meaning</span></span>                                                                                                |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d592a-113">IDOK</span><span class="sxs-lookup"><span data-stu-id="d592a-113">IDOK</span></span>                     | <span data-ttu-id="d592a-114">Пользователь нажал кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="d592a-114">The **OK** button was pressed by the user.</span></span> <span data-ttu-id="d592a-115">Сведения о сообщении были понятны.</span><span class="sxs-lookup"><span data-stu-id="d592a-115">The message information was understood.</span></span>                     |
| <span data-ttu-id="d592a-116">IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="d592a-116">IDCANCEL</span></span>                 | <span data-ttu-id="d592a-117">Была нажата кнопка **"Отмена"** .</span><span class="sxs-lookup"><span data-stu-id="d592a-117">The **CANCEL** button was pressed.</span></span> <span data-ttu-id="d592a-118">Отмените установку.</span><span class="sxs-lookup"><span data-stu-id="d592a-118">Cancel the installation.</span></span>                                            |
| <span data-ttu-id="d592a-119">IDABORT</span><span class="sxs-lookup"><span data-stu-id="d592a-119">IDABORT</span></span>                  | <span data-ttu-id="d592a-120">Была нажата кнопка **прервать** .</span><span class="sxs-lookup"><span data-stu-id="d592a-120">The **ABORT** button was pressed.</span></span> <span data-ttu-id="d592a-121">Прервать установку.</span><span class="sxs-lookup"><span data-stu-id="d592a-121">Abort the installation.</span></span>                                              |
| <span data-ttu-id="d592a-122">IDRETRY</span><span class="sxs-lookup"><span data-stu-id="d592a-122">IDRETRY</span></span>                  | <span data-ttu-id="d592a-123">Была нажата кнопка **"повторить** ".</span><span class="sxs-lookup"><span data-stu-id="d592a-123">The **RETRY** button was pressed.</span></span> <span data-ttu-id="d592a-124">Повторите действие.</span><span class="sxs-lookup"><span data-stu-id="d592a-124">Try the action again.</span></span>                                                |
| <span data-ttu-id="d592a-125">IDIGNORE</span><span class="sxs-lookup"><span data-stu-id="d592a-125">IDIGNORE</span></span>                 | <span data-ttu-id="d592a-126">Нажата кнопка " **пропустить** ".</span><span class="sxs-lookup"><span data-stu-id="d592a-126">The **IGNORE** button was pressed.</span></span> <span data-ttu-id="d592a-127">Игнорировать ошибку и продолжить.</span><span class="sxs-lookup"><span data-stu-id="d592a-127">Ignore the error and continue.</span></span>                                      |
| <span data-ttu-id="d592a-128">IDYES</span><span class="sxs-lookup"><span data-stu-id="d592a-128">IDYES</span></span>                    | <span data-ttu-id="d592a-129">Нажата кнопка **Да** .</span><span class="sxs-lookup"><span data-stu-id="d592a-129">The **YES** button was pressed.</span></span> <span data-ttu-id="d592a-130">Ответ голосами подтверждающими, продолжение текущей последовательности событий..</span><span class="sxs-lookup"><span data-stu-id="d592a-130">The affirmative response, continue with current sequence of events..</span></span>   |
| <span data-ttu-id="d592a-131">IDNO</span><span class="sxs-lookup"><span data-stu-id="d592a-131">IDNO</span></span>                     | <span data-ttu-id="d592a-132">Была нажата кнопка " **нет** ".</span><span class="sxs-lookup"><span data-stu-id="d592a-132">The **NO** button was pressed.</span></span> <span data-ttu-id="d592a-133">Отрицательный ответ — не продолжать текущую последовательность событий.</span><span class="sxs-lookup"><span data-stu-id="d592a-133">The negative response, do not continue with current sequence of events.</span></span> |



 

<span data-ttu-id="d592a-134">Например, если внешний обработчик пользовательского интерфейса отправляет сообщение с \_ флагом "МБ абортретригноре сообщений", внешний обработчик пользовательского интерфейса может возвращать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="d592a-134">For example, if the external UI handler is sent a message with the MB\_ABORTRETRYIGNORE message box styles flag, the external UI handler can return one of the following values:</span></span>

-   <span data-ttu-id="d592a-135">– 1 (ошибка во внешнем обработчике пользовательского интерфейса)</span><span class="sxs-lookup"><span data-stu-id="d592a-135">–1 (error in external UI handler)</span></span>
-   <span data-ttu-id="d592a-136">0 (не предпринимать никаких действий во внешнем обработчике пользовательского интерфейса, разрешить установщик Windows его обработку)</span><span class="sxs-lookup"><span data-stu-id="d592a-136">0 (no action taken in external UI handler, let Windows Installer handle it)</span></span>
-   <span data-ttu-id="d592a-137">ИДАБОРТ (нажата кнопка **прерывания** )</span><span class="sxs-lookup"><span data-stu-id="d592a-137">IDABORT (**ABORT** button pressed)</span></span>
-   <span data-ttu-id="d592a-138">ИДРЕТРИ (нажата кнопка **"повторить** ")</span><span class="sxs-lookup"><span data-stu-id="d592a-138">IDRETRY (**RETRY** button pressed)</span></span>
-   <span data-ttu-id="d592a-139">ИДИГНОРЕ (нажата кнопка "**пропустить** ")</span><span class="sxs-lookup"><span data-stu-id="d592a-139">IDIGNORE (**IGNORE** button pressed)</span></span>

 

 



