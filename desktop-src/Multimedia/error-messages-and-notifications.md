---
title: Сообщения об ошибках и уведомления
description: Сообщения об ошибках и уведомления
ms.assetid: 7f804364-d8be-4e52-ab0e-fba05bcf76ce
keywords:
- Макрос МЦивнджетеррор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e40e78c72dc378baa37b56dbb2d5718ae2d85b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069900"
---
# <a name="error-messages-and-notifications"></a><span data-ttu-id="d740b-104">Сообщения об ошибках и уведомления</span><span class="sxs-lookup"><span data-stu-id="d740b-104">Error Messages and Notifications</span></span>

<span data-ttu-id="d740b-105">МЦивнд использует MCI для управления устройствами, которые воспроизводят и записывают данные мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d740b-105">MCIWnd uses MCI to control the devices that play and record multimedia data.</span></span> <span data-ttu-id="d740b-106">В общем случае МЦивнд отображает ошибки MCI в диалоговом окне ошибки.</span><span class="sxs-lookup"><span data-stu-id="d740b-106">In general, MCIWnd displays MCI errors in an error dialog box.</span></span> <span data-ttu-id="d740b-107">Ошибка MCI возникает при сбое команды MCI.</span><span class="sxs-lookup"><span data-stu-id="d740b-107">An MCI error is generated whenever an MCI command fails.</span></span> <span data-ttu-id="d740b-108">Например, если приложение попытается возобновить приостановленное воспроизведение с помощью макроса [**мЦивндресуме**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) , а текущее устройство не поддерживает Resume, пользователю будет сообщено об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d740b-108">For example, if your application tries to resume paused playback by using the [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) macro and the current device does not support resume, an error is reported to the user.</span></span>

<span data-ttu-id="d740b-109">МЦивнд предоставляет два способа обработки сообщений об ошибках:</span><span class="sxs-lookup"><span data-stu-id="d740b-109">MCIWnd allows you two choices for handling error messages:</span></span>

-   <span data-ttu-id="d740b-110">Можно предотвратить достижение пользователями сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="d740b-110">You can prevent error messages from reaching the user.</span></span> <span data-ttu-id="d740b-111">Чтобы предотвратить отображение сообщений об ошибках MCI, укажите \_ стиль окна мЦивндф ноеррордлг при создании экземпляра окна мЦивнд с помощью функции [**МЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) или [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="d740b-111">To prevent the display of MCI error messages, specify the MCIWNDF\_NOERRORDLG window style when you create an instance of an MCIWnd window by using the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) or [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span>
-   <span data-ttu-id="d740b-112">Их можно перенаправить в приложение для показа.</span><span class="sxs-lookup"><span data-stu-id="d740b-112">You can redirect them to your application for display.</span></span> <span data-ttu-id="d740b-113">Чтобы перенаправить сообщения об ошибках MCI в приложение, укажите \_ стиль окна мЦивндф нотиферрор при создании экземпляра окна мЦивнд с помощью **МЦивндкреате** или **CreateWindowEx**.</span><span class="sxs-lookup"><span data-stu-id="d740b-113">To redirect MCI error messages to your application, specify the MCIWNDF\_NOTIFYERROR window style when you create an instance of an MCIWnd window by using **MCIWndCreate** or **CreateWindowEx**.</span></span>

<span data-ttu-id="d740b-114">Если уведомление об ошибке включено, МЦивнд отправляет каждое сообщение уведомления ([**мЦивндм \_ нотиферрор**](mciwndm-notifyerror.md)) в основной обработчик сообщений родительского окна мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="d740b-114">When error notification is enabled, MCIWnd sends each notification message ([**MCIWNDM\_NOTIFYERROR**](mciwndm-notifyerror.md)) to the main message handler of the parent of the MCIWnd window.</span></span> <span data-ttu-id="d740b-115">Приложение должно иметь обработчик сообщений для обработки получаемых им сообщений уведомления.</span><span class="sxs-lookup"><span data-stu-id="d740b-115">Your application must have a message handler to process the notification messages it receives.</span></span>

<span data-ttu-id="d740b-116">Текстовое описание последнего сообщения об ошибке MCI можно получить с помощью макроса [**мЦивнджетеррор**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) .</span><span class="sxs-lookup"><span data-stu-id="d740b-116">You can obtain a textual description of the most recent MCI error message by using the [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) macro.</span></span> <span data-ttu-id="d740b-117">Этот макрос возвращает текст в определяемом приложением буфере.</span><span class="sxs-lookup"><span data-stu-id="d740b-117">This macro returns the text in an application-defined buffer.</span></span> <span data-ttu-id="d740b-118">Если строка ошибки длиннее, чем буфер, МЦивнд усекает строку.</span><span class="sxs-lookup"><span data-stu-id="d740b-118">If the error string is longer than the buffer, MCIWnd truncates the string.</span></span>

<span data-ttu-id="d740b-119">Вы можете направить все уведомления в другое окно с помощью макроса [**мЦивндсетовнер**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) .</span><span class="sxs-lookup"><span data-stu-id="d740b-119">You can route all notifications to another window by using the [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) macro.</span></span>

 

 