---
title: Функции (сенсорный ввод Windows)
description: Этот раздел содержит функции для сенсорного ввода Windows.
ms.assetid: 6c64ed75-37ac-47ae-b39e-bdf10d2b5211
keywords:
- Касание Windows, функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a18ba246ab8b1d228d257d32982e9afc2c418eb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104071034"
---
# <a name="functions-windows-touch-input"></a><span data-ttu-id="ab63c-104">Функции (сенсорный ввод Windows)</span><span class="sxs-lookup"><span data-stu-id="ab63c-104">Functions (Windows Touch Input)</span></span>

<span data-ttu-id="ab63c-105">Этот раздел содержит функции для сенсорного ввода Windows.</span><span class="sxs-lookup"><span data-stu-id="ab63c-105">This section contains functions for Windows Touch input.</span></span>

<span data-ttu-id="ab63c-106">Для сенсорного ввода Windows используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="ab63c-106">The following functions are used for Windows Touch input.</span></span>



| <span data-ttu-id="ab63c-107">Функция</span><span class="sxs-lookup"><span data-stu-id="ab63c-107">Function</span></span>                                                                                               | <span data-ttu-id="ab63c-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ab63c-108">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab63c-109">**клосетаучинпусандле**</span><span class="sxs-lookup"><span data-stu-id="ab63c-109">**CloseTouchInputHandle**</span></span>](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle)                                                 | <span data-ttu-id="ab63c-110">Закрывает входной маркер касания, освобождает память процесса, связанную с ним, и делает этот маркер недействительным.</span><span class="sxs-lookup"><span data-stu-id="ab63c-110">Closes a touch input handle, frees process memory associated with it, and invalidates the handle.</span></span>                                       |
| [<span data-ttu-id="ab63c-111">**жеттаучинпутинфо**</span><span class="sxs-lookup"><span data-stu-id="ab63c-111">**GetTouchInputInfo**</span></span>](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo)                                                         | <span data-ttu-id="ab63c-112">Получает подробные сведения о сенсорных вводах, связанных с конкретным сенсорным входом.</span><span class="sxs-lookup"><span data-stu-id="ab63c-112">Retrieves detailed information about touch inputs associated with a specific touch input handle.</span></span>                                        |
| [<span data-ttu-id="ab63c-113">**истаучвиндов**</span><span class="sxs-lookup"><span data-stu-id="ab63c-113">**IsTouchWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-istouchwindow)                                                                 | <span data-ttu-id="ab63c-114">Проверяет, поддерживает ли указанное окно сенсорное касание, и, при необходимости, получает флаги модификаторов, заданные для функции касания окна.</span><span class="sxs-lookup"><span data-stu-id="ab63c-114">Checks whether a specified window is touch-capable and, optionally, retrieves the modifier flags set for the window's touch capability.</span></span> |
| [<span data-ttu-id="ab63c-115">**регистертаучвиндов**</span><span class="sxs-lookup"><span data-stu-id="ab63c-115">**RegisterTouchWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)                                                     | <span data-ttu-id="ab63c-116">Регистрирует окно с поддержкой сенсорного ввода.</span><span class="sxs-lookup"><span data-stu-id="ab63c-116">Registers a window as being touch-capable.</span></span>                                                                                              |
| [<span data-ttu-id="ab63c-117">**унрегистертаучвиндов**</span><span class="sxs-lookup"><span data-stu-id="ab63c-117">**UnregisterTouchWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-unregistertouchwindow)                                                 | <span data-ttu-id="ab63c-118">Регистрирует окно, так как оно больше не поддерживает сенсорный ввод.</span><span class="sxs-lookup"><span data-stu-id="ab63c-118">Registers a window as no longer being touch-capable.</span></span>                                                                                    |
| [<span data-ttu-id="ab63c-119">SendMessage, сообщение и связанные функции</span><span class="sxs-lookup"><span data-stu-id="ab63c-119">SendMessage, PostMessage, and Related Functions</span></span>](sendmessage--postmessage--and-related-functions.md) | <span data-ttu-id="ab63c-120">Содержит рекомендации по пересылке сообщений.</span><span class="sxs-lookup"><span data-stu-id="ab63c-120">Contains considerations about forwarding messages.</span></span>                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="ab63c-121">См. также</span><span class="sxs-lookup"><span data-stu-id="ab63c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab63c-122">Сенсорный ввод Windows</span><span class="sxs-lookup"><span data-stu-id="ab63c-122">Windows Touch Input</span></span>](multi-touch-input.md)
</dt> <dt>

[<span data-ttu-id="ab63c-123">Справочное руководством по программированию ввода Windows Touch</span><span class="sxs-lookup"><span data-stu-id="ab63c-123">Windows Touch Input Programming Guide</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 




