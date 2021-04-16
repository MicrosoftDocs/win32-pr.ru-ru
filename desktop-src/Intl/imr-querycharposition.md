---
description: Уведомляет приложение, когда выбранному РЕДАКТОРу требуется информация о координатах символа в строке композиции. Приложение получает эту команду через \_ сообщение запроса WM IME \_ с параметрами параметров, как показано ниже.
ms.assetid: cae7e5b3-8aaf-452d-80df-fb0ae04a342c
title: Код уведомления IMR_QUERYCHARPOSITION (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947eec9b3dd1f678d9266bb795214cf392629193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683361"
---
# <a name="imr_querycharposition-notification-code"></a><span data-ttu-id="3b854-104">\_Код уведомления КУЕРИЧАРПОСИТИОН IMR</span><span class="sxs-lookup"><span data-stu-id="3b854-104">IMR\_QUERYCHARPOSITION notification code</span></span>

<span data-ttu-id="3b854-105">Уведомляет приложение, когда выбранному РЕДАКТОРу требуется информация о координатах символа в строке композиции.</span><span class="sxs-lookup"><span data-stu-id="3b854-105">Notifies an application when the selected IME needs information about the coordinates of a character in the composition string.</span></span> <span data-ttu-id="3b854-106">Приложение получает эту команду через сообщение [**запроса WM \_ IME \_**](wm-ime-request.md) с параметрами параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="3b854-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_QUERYCHARPOSITION
```



## <a name="parameters"></a><span data-ttu-id="3b854-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b854-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b854-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="3b854-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="3b854-109">Задайте значение IMR \_ куеричарпоситион.</span><span class="sxs-lookup"><span data-stu-id="3b854-109">Set to IMR\_QUERYCHARPOSITION.</span></span>

</dd> <dt>

<span data-ttu-id="3b854-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b854-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="3b854-111">Указатель на структуру [**имечарпоситион**](/windows/win32/api/imm/ns-imm-imecharposition) , содержащую позиции символа в окне композиции.</span><span class="sxs-lookup"><span data-stu-id="3b854-111">Pointer to an [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure that contains the position of the character in the composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b854-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b854-112">Return Value</span></span>

<span data-ttu-id="3b854-113">Функция возвращает ненулевое значение, если приложение заполняет структуру [**имечарпоситион**](/windows/win32/api/imm/ns-imm-imecharposition) .</span><span class="sxs-lookup"><span data-stu-id="3b854-113">Returns a nonzero value if the application fills the [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure.</span></span> <span data-ttu-id="3b854-114">В противном случае команда возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="3b854-114">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b854-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b854-115">Remarks</span></span>

<span data-ttu-id="3b854-116">Приложение, которое рисует строку композиции, а не полагается на IME, отвечает за заполнение всех элементов структуры [**имечарпоситион**](/windows/win32/api/imm/ns-imm-imecharposition) .</span><span class="sxs-lookup"><span data-stu-id="3b854-116">An application that draws the composition string itself, instead of relying on the IME, is responsible for filling in all the members of the [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure.</span></span> <span data-ttu-id="3b854-117">В противном случае приложение должно передать команду в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) или [**иммисуимессаже**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) , если она имеет собственное окно пользовательского интерфейса IME.</span><span class="sxs-lookup"><span data-stu-id="3b854-117">Otherwise, the application should pass the command to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) if it has its own IME user interface window.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b854-118">Требования</span><span class="sxs-lookup"><span data-stu-id="3b854-118">Requirements</span></span>



| <span data-ttu-id="3b854-119">Требование</span><span class="sxs-lookup"><span data-stu-id="3b854-119">Requirement</span></span> | <span data-ttu-id="3b854-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3b854-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b854-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b854-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3b854-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3b854-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3b854-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b854-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3b854-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3b854-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3b854-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3b854-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b854-126"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b854-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b854-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b854-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b854-128">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="3b854-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="3b854-129">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="3b854-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="3b854-130">**имечарпоситион**</span><span class="sxs-lookup"><span data-stu-id="3b854-130">**IMECHARPOSITION**</span></span>](/windows/win32/api/imm/ns-imm-imecharposition)
</dt> <dt>

[<span data-ttu-id="3b854-131">**иммисуимессаже**</span><span class="sxs-lookup"><span data-stu-id="3b854-131">**ImmIsUIMessage**</span></span>](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> <dt>

[<span data-ttu-id="3b854-132">**\_запрос IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="3b854-132">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 
