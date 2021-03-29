---
title: Автоматизация воспроизведения
description: Автоматизация воспроизведения
ms.assetid: 3aa05a54-58d7-4d14-93ee-459aa860b20e
keywords:
- Макрос МЦивндкреате
- Макрос МЦивндплай
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6097d38b3d468b6de68ee7e11f98f530aff00d2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779610"
---
# <a name="automating-playback"></a><span data-ttu-id="06f4c-105">Автоматизация воспроизведения</span><span class="sxs-lookup"><span data-stu-id="06f4c-105">Automating Playback</span></span>

<span data-ttu-id="06f4c-106">Вы можете автоматизировать воспроизведение в приложении с помощью [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) и макроса [**мЦивндплай**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) , а также [**мЦивнддестрой**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) или макроса [**мЦивндклосе**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) .</span><span class="sxs-lookup"><span data-stu-id="06f4c-106">You can automate playback in your application by using [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) and the [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) macro, along with either the [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) or the [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) macro.</span></span> <span data-ttu-id="06f4c-107">Чтобы автоматизировать воспроизведение, укажите стили МЦИВНДФ \_ ноплайбар и мЦивндф \_ нотифимоде в параметре \**мЦивндкреате \* \* \* двстиле* .</span><span class="sxs-lookup"><span data-stu-id="06f4c-107">To automate playback, specify the MCIWNDF\_NOPLAYBAR and MCIWNDF\_NOTIFYMODE styles in the \**MCIWndCreate\*\*\*dwStyle* parameter.</span></span> <span data-ttu-id="06f4c-108">Укажите стиль МЦИВНДФ \_ ноплайбар, чтобы скрыть панель инструментов, и стиль мЦивндф \_ нотифимоде, чтобы выдать соответствующее сообщение уведомления при прекращении воспроизведения устройства.</span><span class="sxs-lookup"><span data-stu-id="06f4c-108">Specify the MCIWNDF\_NOPLAYBAR style to hide the toolbar, and the MCIWNDF\_NOTIFYMODE style to issue an appropriate notification message when the device stops playing.</span></span>

<span data-ttu-id="06f4c-109">Устройство или файл, указанный в **мЦивндкреате** , можно воспроизвести с помощью **мЦивндплай**.</span><span class="sxs-lookup"><span data-stu-id="06f4c-109">You can play the device or file specified in **MCIWndCreate** by using **MCIWndPlay**.</span></span> <span data-ttu-id="06f4c-110">Макрос МЦивндплай начинает воспроизводить содержимое из текущего расположения воспроизведения и переходит к его концу.</span><span class="sxs-lookup"><span data-stu-id="06f4c-110">The MCIWndPlay macro starts playing the content from its current playback position and continues to its end.</span></span>

<span data-ttu-id="06f4c-111">Можно уничтожить или закрыть окно МЦивнд с помощью макроса [**мЦивнддестрой**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) или [**мЦивндклосе**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) .</span><span class="sxs-lookup"><span data-stu-id="06f4c-111">You can destroy or close an MCIWnd window by using the [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) or [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) macro.</span></span> <span data-ttu-id="06f4c-112">Макрос **мЦивнддестрой** закрывает устройство или файл и уничтожает окно мЦивнд путем аннулирования его обработчика.</span><span class="sxs-lookup"><span data-stu-id="06f4c-112">The **MCIWndDestroy** macro closes the device or file and destroys the MCIWnd window by invalidating its handle.</span></span> <span data-ttu-id="06f4c-113">Если приложение может повторно использовать окно МЦивнд, используйте **мЦивндклосе** , чтобы закрыть устройство, не уничтожая окно.</span><span class="sxs-lookup"><span data-stu-id="06f4c-113">If your application can reuse the MCIWnd window, use **MCIWndClose** to close the device without destroying the window.</span></span>

<span data-ttu-id="06f4c-114">Приложение может определить, когда устройство перестает воспроизводиться, и автоматически закрывать окно.</span><span class="sxs-lookup"><span data-stu-id="06f4c-114">Your application can detect when the device stops playing and automatically close the window.</span></span> <span data-ttu-id="06f4c-115">Для этого укажите \_ стиль мЦивндф нотифимоде для параметра *двстиле* [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span><span class="sxs-lookup"><span data-stu-id="06f4c-115">To do this, specify the MCIWNDF\_NOTIFYMODE style for the *dwStyle* parameter of [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span></span> <span data-ttu-id="06f4c-116">Это приводит к тому, что устройство отправляет сообщение [**мЦивндм \_ нотифимоде**](mciwndm-notifymode.md) при каждом изменении режима.</span><span class="sxs-lookup"><span data-stu-id="06f4c-116">This causes the device to send a [**MCIWNDM\_NOTIFYMODE**](mciwndm-notifymode.md) message whenever it changes modes.</span></span> <span data-ttu-id="06f4c-117">Приложение может перехватить это сообщение, чтобы определить, завершилось ли воспроизведение устройства.</span><span class="sxs-lookup"><span data-stu-id="06f4c-117">Your application can trap this message to determine whether the device has stopped playing.</span></span> <span data-ttu-id="06f4c-118">Когда устройство перестает воспроизводиться, приложение закрывает окно.</span><span class="sxs-lookup"><span data-stu-id="06f4c-118">When the device stops playing, the application closes the window.</span></span>

 

 




