---
description: Уведомляет приложение, когда выбранному редактору IME требуется преобразованная строка из приложения. Приложение получает эту команду через \_ сообщение запроса WM IME \_ с набором параметров, как показано ниже.
ms.assetid: 1a007bed-15e5-4400-9d2f-32e37e1765d2
title: Код уведомления IMR_DOCUMENTFEED (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4fe46f95b7ad17ba7bb7850ec3fb9ca980519f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264401"
---
# <a name="imr_documentfeed-notification-code"></a><span data-ttu-id="6ef65-104">\_Код уведомления ДОКУМЕНТФИД IMR</span><span class="sxs-lookup"><span data-stu-id="6ef65-104">IMR\_DOCUMENTFEED notification code</span></span>

<span data-ttu-id="6ef65-105">Уведомляет приложение, когда выбранному редактору IME требуется преобразованная строка из приложения.</span><span class="sxs-lookup"><span data-stu-id="6ef65-105">Notifies an application when the selected IME needs the converted string from the application.</span></span> <span data-ttu-id="6ef65-106">Приложение получает эту команду через сообщение [**запроса WM \_ IME \_**](wm-ime-request.md) с набором параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="6ef65-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters set as shown below.</span></span>


```C++
LRESULT IMR_DOCUMENTFEED
```



## <a name="parameters"></a><span data-ttu-id="6ef65-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ef65-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ef65-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ef65-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="6ef65-109">Задайте значение IMR \_ документфид.</span><span class="sxs-lookup"><span data-stu-id="6ef65-109">Set to IMR\_DOCUMENTFEED.</span></span>

</dd> <dt>

<span data-ttu-id="6ef65-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ef65-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="6ef65-111">Указатель на буфер, в котором будет содержаться структура [**реконвертстринг**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="6ef65-111">Pointer to a buffer to contain the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ef65-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ef65-112">Return Value</span></span>

<span data-ttu-id="6ef65-113">Возвращает текущую структуру строки повторного преобразования.</span><span class="sxs-lookup"><span data-stu-id="6ef65-113">Returns the current reconversion string structure.</span></span> <span data-ttu-id="6ef65-114">Если параметр *lParam* имеет значение **null**, приложение возвращает необходимый размер буфера для хранения структуры.</span><span class="sxs-lookup"><span data-stu-id="6ef65-114">If *lParam* is set to **NULL**, the application returns the required size for the buffer to hold the structure.</span></span> <span data-ttu-id="6ef65-115">Команда возвращает 0, если она не выполнена.</span><span class="sxs-lookup"><span data-stu-id="6ef65-115">The command returns 0 if it does not succeed.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ef65-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ef65-116">Remarks</span></span>

<span data-ttu-id="6ef65-117">Редактор IME кэширует преобразованные строки для повышения точности преобразования.</span><span class="sxs-lookup"><span data-stu-id="6ef65-117">The IME caches converted strings for higher conversion accuracy.</span></span> <span data-ttu-id="6ef65-118">Одним из ограничений на кэширование IME является то, что оно теряет преобразованную строку в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="6ef65-118">One caching limitation of the IME is that it loses the converted string under the following circumstances:</span></span>

-   <span data-ttu-id="6ef65-119">Позицию курсора для приложения перемещается по ключу, например к клавише курсора.</span><span class="sxs-lookup"><span data-stu-id="6ef65-119">The caret position for the application is moved by a key, for example, a cursor key.</span></span>
-   <span data-ttu-id="6ef65-120">Позиции курсора для приложения перемещаются мышью.</span><span class="sxs-lookup"><span data-stu-id="6ef65-120">The caret position for the application is moved by the mouse.</span></span>
-   <span data-ttu-id="6ef65-121">Откроется новый документ.</span><span class="sxs-lookup"><span data-stu-id="6ef65-121">A new document is opened.</span></span>

<span data-ttu-id="6ef65-122">С помощью команды **IMR \_ документфид** редактор IME может обновлять кэшированные строки в любое время.</span><span class="sxs-lookup"><span data-stu-id="6ef65-122">With the **IMR\_DOCUMENTFEED** command, the IME can refresh its cached strings any time.</span></span> <span data-ttu-id="6ef65-123">Использование этой команды повышает точность преобразования.</span><span class="sxs-lookup"><span data-stu-id="6ef65-123">Use of this command improves conversion accuracy.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ef65-124">Требования</span><span class="sxs-lookup"><span data-stu-id="6ef65-124">Requirements</span></span>



| <span data-ttu-id="6ef65-125">Требование</span><span class="sxs-lookup"><span data-stu-id="6ef65-125">Requirement</span></span> | <span data-ttu-id="6ef65-126">Значение</span><span class="sxs-lookup"><span data-stu-id="6ef65-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ef65-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ef65-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6ef65-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6ef65-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6ef65-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ef65-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6ef65-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6ef65-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6ef65-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6ef65-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ef65-132"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ef65-132"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ef65-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ef65-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ef65-134">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="6ef65-134">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="6ef65-135">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="6ef65-135">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="6ef65-136">**реконвертстринг**</span><span class="sxs-lookup"><span data-stu-id="6ef65-136">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="6ef65-137">**\_запрос IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="6ef65-137">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




