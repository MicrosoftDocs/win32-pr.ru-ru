---
title: SendMessage, сообщение и связанные функции
description: В этом разделе приводятся рекомендации по пересылке сообщений с помощью SendMessage, сообщений и связанных функций с сенсорными сообщениями.
ms.assetid: 9fba2013-17a3-499c-80dc-627e89c0edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fc42e31f3c971c704d18f04a961fb6bd40eb91d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413283"
---
# <a name="sendmessage-postmessage-and-related-functions"></a><span data-ttu-id="e33ae-103">SendMessage, сообщение и связанные функции</span><span class="sxs-lookup"><span data-stu-id="e33ae-103">SendMessage, PostMessage, and Related Functions</span></span>

<span data-ttu-id="e33ae-104">В этом разделе приводятся рекомендации по пересылке сообщений с помощью [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [сообщений](/windows/win32/api/winuser/nf-winuser-postmessagea)и связанных функций с сенсорными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="e33ae-104">This section describes considerations about forwarding messages using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), and related functions with touch messages.</span></span>

<span data-ttu-id="e33ae-105">Если сенсорное сообщение пересылается с помощью [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [сообщения](/windows/win32/api/winuser/nf-winuser-postmessagea)или другой связанной функции, то маркер сенсорного ввода закрывается.</span><span class="sxs-lookup"><span data-stu-id="e33ae-105">If a touch message is forwarded using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), or some other related function, the touch input handle is closed.</span></span> <span data-ttu-id="e33ae-106">Если вы получили сведения, содержащиеся на ссылке сенсорного ввода с помощью вызова [**жеттаучинпутинфо**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo), эти данные останутся действительными до тех пор, пока не освободится память.</span><span class="sxs-lookup"><span data-stu-id="e33ae-106">If you have retrieved the information contained referenced by a touch input handle through a call to [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo), that data will remain valid until you free the memory.</span></span>

<span data-ttu-id="e33ae-107">Приложение, получающее сенсорные сообщения, пересылаемые через один из этих механизмов, владеет сенсорным приемом ввода, который он получает в сообщении *lParam* и отвечает за его закрытие.</span><span class="sxs-lookup"><span data-stu-id="e33ae-107">An application that receives touch messages forwarded through one of these mechanisms owns the touch input handle it receives in the message *LPARAM* and is responsible for closing it.</span></span> <span data-ttu-id="e33ae-108">Если вы не закроете дескриптор с вызовом [**клосетаучинпусандле**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), передайте сообщение в [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca)или перешлите сообщение с помощью [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [сообщения](/windows/win32/api/winuser/nf-winuser-postmessagea)или связанной функции, произойдет утечка памяти.</span><span class="sxs-lookup"><span data-stu-id="e33ae-108">If you don't close the handle with a call to [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), pass the message to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), or forward the message using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), or some related function, you will have a memory leak.</span></span>

> [!Note]  
> <span data-ttu-id="e33ae-109">При переадресации сообщений сенсорного ввода действуют обычные правила изоляции прав пользовательского интерфейса (UIPI).</span><span class="sxs-lookup"><span data-stu-id="e33ae-109">Touch messages are subject to normal User Interface Privilege Isolation (UIPI) rules when they are forwarded.</span></span>

 

## <a name="functions-related-to-sendmessage-and-postmessage"></a><span data-ttu-id="e33ae-110">Функции, относящиеся к SendMessage и почте</span><span class="sxs-lookup"><span data-stu-id="e33ae-110">Functions related to SendMessage and PostMessage</span></span>

<span data-ttu-id="e33ae-111">Следующие функции, которые могут повлиять на состояние сенсорного ввода.</span><span class="sxs-lookup"><span data-stu-id="e33ae-111">The following functions that can affect the state of the touch input handle.</span></span>

-   [<span data-ttu-id="e33ae-112">SendMessage</span><span class="sxs-lookup"><span data-stu-id="e33ae-112">SendMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
-   [<span data-ttu-id="e33ae-113">PostMessage</span><span class="sxs-lookup"><span data-stu-id="e33ae-113">PostMessage</span></span>](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   <span data-ttu-id="e33ae-114">сенднотифимессаже</span><span class="sxs-lookup"><span data-stu-id="e33ae-114">SendNotifyMessage</span></span>
-   <span data-ttu-id="e33ae-115">сендмессажекаллбакк</span><span class="sxs-lookup"><span data-stu-id="e33ae-115">SendMessageCallback</span></span>
-   <span data-ttu-id="e33ae-116">Функции sendmessagetimeout</span><span class="sxs-lookup"><span data-stu-id="e33ae-116">SendMessageTimeout</span></span>
-   <span data-ttu-id="e33ae-117">постсреадмессаже</span><span class="sxs-lookup"><span data-stu-id="e33ae-117">PostThreadMessage</span></span>

## <a name="related-topics"></a><span data-ttu-id="e33ae-118">См. также</span><span class="sxs-lookup"><span data-stu-id="e33ae-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e33ae-119">Функции</span><span class="sxs-lookup"><span data-stu-id="e33ae-119">Functions</span></span>](mtfunctions.md)
</dt> <dt>

[<span data-ttu-id="e33ae-120">дефвиндовпрок</span><span class="sxs-lookup"><span data-stu-id="e33ae-120">DefWindowProc</span></span>](/windows/win32/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

 