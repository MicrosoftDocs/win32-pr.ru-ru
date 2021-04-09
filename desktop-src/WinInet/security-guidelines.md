---
title: Рекомендации по безопасности
description: Важно, чтобы пользователь уведомил о возможных проблемах безопасности.
ms.assetid: f0c041fd-3cc5-491e-b088-6c93fcd61def
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3d4214ba4582394ed555bafd58551e8b047493
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134343"
---
# <a name="security-guideline"></a><span data-ttu-id="28de3-103">Рекомендации по безопасности</span><span class="sxs-lookup"><span data-stu-id="28de3-103">Security Guideline</span></span>

<span data-ttu-id="28de3-104">Важно, чтобы пользователь уведомил о возможных проблемах безопасности.</span><span class="sxs-lookup"><span data-stu-id="28de3-104">It is important to keep the user informed about possible security issues.</span></span>

## <a name="notify-the-user-of-security-related-events"></a><span data-ttu-id="28de3-105">Уведомлять пользователя о событиях Security-Related</span><span class="sxs-lookup"><span data-stu-id="28de3-105">Notify the User of Security-Related Events</span></span>

<span data-ttu-id="28de3-106">Всегда уведомлять пользователя о каких-либо изменениях в безопасности, будь то ошибка безопасности, например сбой сертификата, или изменение безопасности базового протокола, например изменение с HTTPS-сайта на сайт HTTP.</span><span class="sxs-lookup"><span data-stu-id="28de3-106">Always notify the user of any change in security, whether it is a security-related error such as a certificate failure, or a change in the security of the underlying protocol, such as change from an HTTPS site to an HTTP site.</span></span>

## <a name="notify-the-user-of-security-related-errors"></a><span data-ttu-id="28de3-107">Уведомлять пользователя об ошибках Security-Related</span><span class="sxs-lookup"><span data-stu-id="28de3-107">Notify the User of Security-Related Errors</span></span>

<span data-ttu-id="28de3-108">Когда приложение получает сообщение об ошибке, которое может указывать на проблему безопасности, функция **интернетеррордлг** предоставляет стандартный, привычный интерфейс для уведомления пользователя в большинстве случаев.</span><span class="sxs-lookup"><span data-stu-id="28de3-108">When your application receives an error message that may indicate a security problem, the **InternetErrorDlg** function provides a standard, familiar interface for notifying the user in most cases.</span></span>

<span data-ttu-id="28de3-109">Ниже перечислены ошибки, которые относятся к этой категории.</span><span class="sxs-lookup"><span data-stu-id="28de3-109">Among the errors that fall in this category are:</span></span>

<span data-ttu-id="28de3-110">**Ошибка \_ Интернет \_ -HTTP \_ для \_ HTTPS \_ в \_ редир**</span><span class="sxs-lookup"><span data-stu-id="28de3-110">**ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR**</span></span>

<span data-ttu-id="28de3-111">**Ошибка в \_ Интернете, \_ Недопустимый \_ ЦС**</span><span class="sxs-lookup"><span data-stu-id="28de3-111">**ERROR\_INTERNET\_INVALID\_CA**</span></span>

<span data-ttu-id="28de3-112">**сообщение об ошибке " \_ Интернет \_ -Публикация не \_ \_ \_ защищена"**</span><span class="sxs-lookup"><span data-stu-id="28de3-112">**ERROR\_INTERNET\_POST\_IS\_NON\_SECURE**</span></span>

<span data-ttu-id="28de3-113">**ошибки при ошибках \_ сертификатов Интернета ( \_ сек) \_ \_**</span><span class="sxs-lookup"><span data-stu-id="28de3-113">**ERROR\_INTERNET\_SEC\_CERT\_ERRORS**</span></span>

<span data-ttu-id="28de3-114">**Ошибка \_ \_ \_ \_ недопустимое общее имя сертификата Internet sec \_**</span><span class="sxs-lookup"><span data-stu-id="28de3-114">**ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID**</span></span>

<span data-ttu-id="28de3-115">**Ошибка \_ при \_ обращении к Интернету с \_ \_ \_ недопустимым сертификатом**</span><span class="sxs-lookup"><span data-stu-id="28de3-115">**ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID**</span></span>

<span data-ttu-id="28de3-116">Невозможность уведомить пользователя об ошибках, например, может предоставить пользователю различные виды нарушений безопасности, включая атаки с подменой или недобровольную раскрытие информации.</span><span class="sxs-lookup"><span data-stu-id="28de3-116">A failure to notify the user of errors such as these can expose the user to various sorts of security breaches, including spoofing attacks or involuntary information disclosure.</span></span>

## <a name="notify-the-user-when-connection-security-changes"></a><span data-ttu-id="28de3-117">Уведомлять пользователя при изменении параметров безопасности подключения</span><span class="sxs-lookup"><span data-stu-id="28de3-117">Notify the User When Connection Security Changes</span></span>

<span data-ttu-id="28de3-118">Всегда уведомлять пользователя при изменении безопасности соединения, например, с HTTPS на HTTP.</span><span class="sxs-lookup"><span data-stu-id="28de3-118">Always notify the user when the security of the connection changes, for example from HTTPS to HTTP.</span></span> <span data-ttu-id="28de3-119">В противном случае, если пользователь явно не выбрал, чтобы получать уведомления об этих изменениях, вы скрываете риски недобровольного раскрытия информации.</span><span class="sxs-lookup"><span data-stu-id="28de3-119">Otherwise, unless the user has explicitly chosen not to be notified of such changes, you are concealing the risks of involuntary information disclosure.</span></span>

<span data-ttu-id="28de3-120">Между функциями, которые сообщают об изменении безопасности соединения, относятся функция обратного вызова **интернетстатускаллбакк** и функция **интернетконфирмзонекроссинг** .</span><span class="sxs-lookup"><span data-stu-id="28de3-120">Among the functions that report such a change in connection security are the **InternetStatusCallback** callback function and the **InternetConfirmZoneCrossing** function.</span></span>

> [!Note]  
> <span data-ttu-id="28de3-121">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="28de3-121">WinINet does not support server implementations.</span></span> <span data-ttu-id="28de3-122">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="28de3-122">In addition, it should not be used from a service.</span></span> <span data-ttu-id="28de3-123">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="28de3-123">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 