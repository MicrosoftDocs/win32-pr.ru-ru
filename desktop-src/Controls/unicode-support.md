---
title: Поддержка Юникода для стандартных элементов управления
description: В этом разделе описывается поддержка Юникода для общих управляющих уведомлений.
ms.assetid: 5020F638-261D-4D32-ACC4-F9572EDBE875
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb029d6e1c018f1793c749aefb2f88104559cae
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103988007"
---
# <a name="unicode-support-for-common-controls"></a><span data-ttu-id="8f313-103">Поддержка Юникода для стандартных элементов управления</span><span class="sxs-lookup"><span data-stu-id="8f313-103">Unicode Support for Common Controls</span></span>

<span data-ttu-id="8f313-104">В этом разделе описывается поддержка Юникода для общих управляющих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8f313-104">This topic describes how to support Unicode for common control notifications.</span></span>


<span data-ttu-id="8f313-105">Для версий 5,80 и более поздних comctl32.dll уведомления общих элементов управления поддерживают формат ANSI и Юникод в системах Windows 95 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="8f313-105">For versions 5.80 and later of comctl32.dll, common controls notifications support both ANSI and Unicode formats on Windows 95 systems or later.</span></span> <span data-ttu-id="8f313-106">Система определяет, какой формат следует использовать, отправляя окно сообщение [**\_ нотифиформат WM**](wm-notifyformat.md) .</span><span class="sxs-lookup"><span data-stu-id="8f313-106">The system determines which format to use by sending your window a [**WM\_NOTIFYFORMAT**](wm-notifyformat.md) message.</span></span> <span data-ttu-id="8f313-107">Чтобы указать формат, вернитесь в \_ ANSI для уведомлений ANSI или NFR \_ Unicode для уведомлений в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="8f313-107">To specify a format, return NFR\_ANSI for ANSI notifications or NFR\_UNICODE for Unicode notifications.</span></span> <span data-ttu-id="8f313-108">Если это сообщение не обрабатывается, система вызывает [**исвиндовуникоде**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) для определения формата.</span><span class="sxs-lookup"><span data-stu-id="8f313-108">If you do not handle this message, the system calls [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) to determine the format.</span></span> <span data-ttu-id="8f313-109">Поскольку Windows 95 и Windows 98 всегда возвращают **значение false** для вызова этой функции, они по умолчанию используют Уведомления ANSI.</span><span class="sxs-lookup"><span data-stu-id="8f313-109">Since Windows 95 and Windows 98 always return **FALSE** to this function call, they use ANSI notifications by default.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f313-110">См. также</span><span class="sxs-lookup"><span data-stu-id="8f313-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f313-111">Общие сведения об элементах управления</span><span class="sxs-lookup"><span data-stu-id="8f313-111">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 