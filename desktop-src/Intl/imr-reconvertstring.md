---
description: Уведомляет приложение, когда для выбранного редактора IME требуется строка для повторного преобразования. Приложение получает эту команду через \_ сообщение запроса WM IME \_ с параметрами параметров, как показано ниже.
ms.assetid: 82ef20b5-bdfa-4bde-abb4-3d14ae35c116
title: Код уведомления IMR_RECONVERTSTRING (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbb1caeedb729b176f116a15e64879d79d519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909500"
---
# <a name="imr_reconvertstring-notification-code"></a><span data-ttu-id="96356-104">\_Код уведомления РЕКОНВЕРТСТРИНГ IMR</span><span class="sxs-lookup"><span data-stu-id="96356-104">IMR\_RECONVERTSTRING notification code</span></span>

<span data-ttu-id="96356-105">Уведомляет приложение, когда для выбранного редактора IME требуется строка для повторного преобразования.</span><span class="sxs-lookup"><span data-stu-id="96356-105">Notifies an application when a selected IME needs a string for reconversion.</span></span> <span data-ttu-id="96356-106">Приложение получает эту команду через сообщение [**запроса WM \_ IME \_**](wm-ime-request.md) с параметрами параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="96356-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_RECONVERTSTRING
```



## <a name="parameters"></a><span data-ttu-id="96356-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="96356-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96356-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="96356-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="96356-109">Задайте значение IMR \_ реконвертстринг.</span><span class="sxs-lookup"><span data-stu-id="96356-109">Set to IMR\_RECONVERTSTRING.</span></span>

</dd> <dt>

<span data-ttu-id="96356-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="96356-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="96356-111">Указатель на буфер, содержащий структуру и строки [**реконвертстринг**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="96356-111">Pointer to a buffer containing the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure and strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96356-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96356-112">Return Value</span></span>

<span data-ttu-id="96356-113">Возвращает текущую структуру строки повторного преобразования.</span><span class="sxs-lookup"><span data-stu-id="96356-113">Returns the current reconversion string structure.</span></span> <span data-ttu-id="96356-114">Если параметр *lParam* имеет значение **null**, приложение возвращает размер буфера, необходимого для хранения структуры.</span><span class="sxs-lookup"><span data-stu-id="96356-114">If *lParam* is set to **NULL**, the application returns the size for the buffer required to hold the structure.</span></span> <span data-ttu-id="96356-115">Команда возвращает 0, если она не выполнена.</span><span class="sxs-lookup"><span data-stu-id="96356-115">The command returns 0 if it does not succeed.</span></span>

## <a name="requirements"></a><span data-ttu-id="96356-116">Требования</span><span class="sxs-lookup"><span data-stu-id="96356-116">Requirements</span></span>



| <span data-ttu-id="96356-117">Требование</span><span class="sxs-lookup"><span data-stu-id="96356-117">Requirement</span></span> | <span data-ttu-id="96356-118">Значение</span><span class="sxs-lookup"><span data-stu-id="96356-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96356-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96356-119">Minimum supported client</span></span><br/> | <span data-ttu-id="96356-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="96356-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="96356-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96356-121">Minimum supported server</span></span><br/> | <span data-ttu-id="96356-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="96356-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="96356-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="96356-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="96356-124"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96356-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96356-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96356-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96356-126">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="96356-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="96356-127">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="96356-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="96356-128">**реконвертстринг**</span><span class="sxs-lookup"><span data-stu-id="96356-128">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="96356-129">**\_запрос IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="96356-129">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




