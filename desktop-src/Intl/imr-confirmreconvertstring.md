---
description: Уведомляет приложение, когда редактору IME требуется изменить структуру РЕКОНВЕРТСТРИНГ. Приложение получает эту команду через \_ сообщение запроса WM IME \_ с параметрами параметров, как показано ниже.
ms.assetid: 035a7072-d292-4883-bc3e-d1e9ed64d9ec
title: Код уведомления IMR_CONFIRMRECONVERTSTRING (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c500a155be14f447bb07ad506e12d5bece66e225
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813681"
---
# <a name="imr_confirmreconvertstring-notification-code"></a><span data-ttu-id="ece7a-104">\_Код уведомления КОНФИРМРЕКОНВЕРТСТРИНГ IMR</span><span class="sxs-lookup"><span data-stu-id="ece7a-104">IMR\_CONFIRMRECONVERTSTRING notification code</span></span>

<span data-ttu-id="ece7a-105">Уведомляет приложение, когда редактору IME требуется изменить структуру [**реконвертстринг**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="ece7a-105">Notifies an application when the IME needs to change the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="ece7a-106">Приложение получает эту команду через сообщение [**запроса WM \_ IME \_**](wm-ime-request.md) с параметрами параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="ece7a-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_CONFIRMRECONVERTSTRING
```



## <a name="parameters"></a><span data-ttu-id="ece7a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ece7a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ece7a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="ece7a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="ece7a-109">Задайте значение IMR \_ конфирмреконвертстринг.</span><span class="sxs-lookup"><span data-stu-id="ece7a-109">Set to IMR\_CONFIRMRECONVERTSTRING.</span></span>

</dd> <dt>

<span data-ttu-id="ece7a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="ece7a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="ece7a-111">Указатель на структуру [**реконвертстринг**](/windows/win32/api/imm/ns-imm-reconvertstring) из редактора IME.</span><span class="sxs-lookup"><span data-stu-id="ece7a-111">Pointer to a [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure from the IME.</span></span> <span data-ttu-id="ece7a-112">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="ece7a-112">For more information, see the Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ece7a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ece7a-113">Return Value</span></span>

<span data-ttu-id="ece7a-114">Возвращает ненулевое значение, если приложение принимает измененную структуру [**реконвертстринг**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="ece7a-114">Returns a nonzero value if the application accepts the changed [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="ece7a-115">В противном случае команда возвращает 0, а редактор IME использует исходную структуру **реконвертстринг** .</span><span class="sxs-lookup"><span data-stu-id="ece7a-115">Otherwise, the command returns 0 and the IME uses the original **RECONVERTSTRING** structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="ece7a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ece7a-116">Remarks</span></span>

<span data-ttu-id="ece7a-117">Приложение заполняет структуру [**реконвертстринг**](/windows/win32/api/imm/ns-imm-reconvertstring) при получении команды [IMR \_ реконвертстринг](imr-reconvertstring.md) .</span><span class="sxs-lookup"><span data-stu-id="ece7a-117">The application fills in the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure upon receiving the [IMR\_RECONVERTSTRING](imr-reconvertstring.md) command.</span></span>

<span data-ttu-id="ece7a-118">После того как приложение обработало [ \_ реконвертстринг IMR](imr-reconvertstring.md), редактор IME может изменить структуру [**реконвертстринг**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="ece7a-118">After the application has handled [IMR\_RECONVERTSTRING](imr-reconvertstring.md), the IME might or might not adjust the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="ece7a-119">Редактор IME отправляет \_ запрос WM IME \_ с помощью **IMR \_ конфирмреконвертстринг** для подтверждения изменений в структуре **реконвертстринг** .</span><span class="sxs-lookup"><span data-stu-id="ece7a-119">The IME sends WM\_IME\_REQUEST with **IMR\_CONFIRMRECONVERTSTRING** to confirm the changes to the **RECONVERTSTRING** structure.</span></span> <span data-ttu-id="ece7a-120">Если приложение возвращает **true** для **IMR \_ конфирмреконвертстринг**, редактор IME создает новую строку композиции на основе структуры **реконвертстринг** для команды **IMR \_ конфирмреконвертстринг** .</span><span class="sxs-lookup"><span data-stu-id="ece7a-120">If the application returns **TRUE** for **IMR\_CONFIRMRECONVERTSTRING**, the IME generates a new composition string based on the **RECONVERTSTRING** structure for the **IMR\_CONFIRMRECONVERTSTRING** command.</span></span> <span data-ttu-id="ece7a-121">Если приложение возвращает **значение false** для **\_ КОНФИРМРЕКОНВЕРТСТРИНГА IMR**, редактор IME создает новую строку композиции на основе исходной структуры **реконвертстринг** , заданной приложением в \_ команде IMR реконвертстринг.</span><span class="sxs-lookup"><span data-stu-id="ece7a-121">If the application returns **FALSE** for **IMR\_CONFIRMRECONVERTSTRING**, the IME generates a new composition string based on the original **RECONVERTSTRING** structure specified by the application in the IMR\_RECONVERTSTRING command.</span></span>

## <a name="requirements"></a><span data-ttu-id="ece7a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ece7a-122">Requirements</span></span>



| <span data-ttu-id="ece7a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ece7a-123">Requirement</span></span> | <span data-ttu-id="ece7a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ece7a-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece7a-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ece7a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ece7a-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ece7a-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ece7a-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ece7a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ece7a-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ece7a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ece7a-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ece7a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ece7a-130"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ece7a-130"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ece7a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ece7a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ece7a-132">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="ece7a-132">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="ece7a-133">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="ece7a-133">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="ece7a-134">\_РЕКОНВЕРТСТРИНГ IMR</span><span class="sxs-lookup"><span data-stu-id="ece7a-134">IMR\_RECONVERTSTRING</span></span>](imr-reconvertstring.md)
</dt> <dt>

[<span data-ttu-id="ece7a-135">**реконвертстринг**</span><span class="sxs-lookup"><span data-stu-id="ece7a-135">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="ece7a-136">**\_запрос IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="ece7a-136">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




