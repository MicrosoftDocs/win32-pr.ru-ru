---
description: Обработка Юникода в приложении IME-Aware
ms.assetid: fa202c1e-d0af-441f-b878-ed98205a880c
title: Обработка Юникода в приложении IME-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78174776eb608c3e494fd5967acba41609e436a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684618"
---
# <a name="handling-unicode-in-an-ime-aware-application"></a><span data-ttu-id="27cf8-103">Обработка Юникода в приложении IME-Aware</span><span class="sxs-lookup"><span data-stu-id="27cf8-103">Handling Unicode in an IME-Aware Application</span></span>

<span data-ttu-id="27cf8-104">С помощью IMM вовлечены две проблемы и его обработка в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="27cf8-104">Two issues are involved with the IMM and its handling of Unicode.</span></span> <span data-ttu-id="27cf8-105">Первая причина заключается в том, что версии Юникода функций IMM извлекают размер буфера в байтах вместо 16-разрядных символов Юникода.</span><span class="sxs-lookup"><span data-stu-id="27cf8-105">The first issue is that the Unicode versions of IMM functions retrieve the size of a buffer in bytes instead of 16-bit Unicode characters.</span></span> <span data-ttu-id="27cf8-106">Вторая ошибка состоит в том, что модуль IMM обычно извлекает символы Юникода (а не символы DBCS) в сообщениях [**\_ \_ char**](wm-ime-char.md) [**WM \_ char**](../inputdev/wm-char.md) и WM IME.</span><span class="sxs-lookup"><span data-stu-id="27cf8-106">The second issue is that the IMM normally retrieves Unicode characters (instead of DBCS characters) in the [**WM\_CHAR**](../inputdev/wm-char.md) and [**WM\_IME\_CHAR**](wm-ime-char.md) messages.</span></span>

<span data-ttu-id="27cf8-107">Windows поддерживает интерфейс Юникод для IMM, а также изначально поддерживаемый интерфейс ANSI.</span><span class="sxs-lookup"><span data-stu-id="27cf8-107">Windows supports a Unicode interface for the IMM, in addition to the ANSI interface originally supported.</span></span>

<span data-ttu-id="27cf8-108">Приложения должны использовать [**регистерклассв**](/windows/win32/api/winuser/nf-winuser-registerclassa) , чтобы заставить сообщения [**WM \_ char**](../inputdev/wm-char.md) и [**WM \_ IME \_**](wm-ime-char.md) получали символы Юникода вместо символов DBCS в параметре *wParam* .</span><span class="sxs-lookup"><span data-stu-id="27cf8-108">Your applications should use [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) to cause the [**WM\_CHAR**](../inputdev/wm-char.md) and [**WM\_IME\_CHAR**](wm-ime-char.md) messages to retrieve Unicode characters instead of DBCS characters in the *wParam* parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27cf8-109">См. также</span><span class="sxs-lookup"><span data-stu-id="27cf8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27cf8-110">Использование диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="27cf8-110">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 
