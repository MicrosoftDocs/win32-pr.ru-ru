---
title: Сообщение WM_DDE_REQUEST (DDE. h)
description: Клиентское приложение платформа динамических данных Exchange (DDE) отправляет \_ \_ сообщение запроса WM DDE в приложение сервера DDE для запроса значения элемента данных. Чтобы опубликовать это сообщение, вызовите функцию почтовых сообщений со следующими параметрами.
ms.assetid: 922452d2-455c-43e1-a8a8-e3c52b0fab51
keywords:
- Обмен данными с сообщениями WM_DDE_REQUEST
topic_type:
- apiref
api_name:
- WM_DDE_REQUEST
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7d5eab75d3b7298d78547b17fccfb164a47ae4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801966"
---
# <a name="wm_dde_request-message"></a><span data-ttu-id="6b7bd-105">\_ \_ Сообщение запроса DDE WM</span><span class="sxs-lookup"><span data-stu-id="6b7bd-105">WM\_DDE\_REQUEST message</span></span>

<span data-ttu-id="6b7bd-106">Клиентское приложение платформа динамических данных Exchange (DDE) отправляет сообщение **\_ \_ запроса WM DDE** в приложение сервера DDE для запроса значения элемента данных.</span><span class="sxs-lookup"><span data-stu-id="6b7bd-106">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_REQUEST** message to a DDE server application to request the value of a data item.</span></span>

<span data-ttu-id="6b7bd-107">Чтобы опубликовать это сообщение, вызовите функцию почтовых [**сообщений**](/windows/desktop/api/winuser/nf-winuser-postmessagea) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="6b7bd-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_REQUEST     0x03E6
```



## <a name="parameters"></a><span data-ttu-id="6b7bd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b7bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b7bd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b7bd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b7bd-110">Маркер клиентского окна, отправляющего сообщение.</span><span class="sxs-lookup"><span data-stu-id="6b7bd-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="6b7bd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b7bd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b7bd-112">Слово нижнего порядка указывает формат стандартного или зарегистрированного буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="6b7bd-112">The low-order word specifies a standard or registered clipboard format.</span></span>

<span data-ttu-id="6b7bd-113">Слово высокого порядка содержит объект Atom, который определяет элемент данных, запрошенный с сервера.</span><span class="sxs-lookup"><span data-stu-id="6b7bd-113">The high-order word contains an atom that identifies the data item requested from the server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b7bd-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b7bd-114">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="6b7bd-115">Товаров</span><span class="sxs-lookup"><span data-stu-id="6b7bd-115">Posting</span></span>

<span data-ttu-id="6b7bd-116">Клиентское приложение выделяет Atom, вызывая функцию [**глобаладдатом**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="6b7bd-116">The client application allocates the atom by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

### <a name="receiving"></a><span data-ttu-id="6b7bd-117">Получение</span><span class="sxs-lookup"><span data-stu-id="6b7bd-117">Receiving</span></span>

<span data-ttu-id="6b7bd-118">Если принимающее (серверное) приложение может удовлетворить запрос, оно реагирует на сообщение [**данных WM \_ DDE \_**](wm-dde-data.md) , содержащее запрошенные данные.</span><span class="sxs-lookup"><span data-stu-id="6b7bd-118">If the receiving (server) application can satisfy the request, it responds with a [**WM\_DDE\_DATA**](wm-dde-data.md) message containing the requested data.</span></span> <span data-ttu-id="6b7bd-119">В противном случае он реагирует на отрицательное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) .</span><span class="sxs-lookup"><span data-stu-id="6b7bd-119">Otherwise, it responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="6b7bd-120">При ответе с помощью [**\_ \_ данных в формате WM DDE**](wm-dde-data.md) или сообщения [**WM \_ DDE \_ ACK**](wm-dde-ack.md) серверное приложение может либо повторно использовать Atom, либо удалить Atom и создать новый.</span><span class="sxs-lookup"><span data-stu-id="6b7bd-120">When responding with either a [**WM\_DDE\_DATA**](wm-dde-data.md) or [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the server application can either reuse the atom or it can delete the atom and create a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b7bd-121">Требования</span><span class="sxs-lookup"><span data-stu-id="6b7bd-121">Requirements</span></span>



| <span data-ttu-id="6b7bd-122">Требование</span><span class="sxs-lookup"><span data-stu-id="6b7bd-122">Requirement</span></span> | <span data-ttu-id="6b7bd-123">Значение</span><span class="sxs-lookup"><span data-stu-id="6b7bd-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b7bd-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b7bd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6b7bd-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6b7bd-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6b7bd-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b7bd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6b7bd-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6b7bd-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6b7bd-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6b7bd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b7bd-129"><dt>DDE. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b7bd-129"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b7bd-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b7bd-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="6b7bd-131">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="6b7bd-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6b7bd-132">**глобаладдатом**</span><span class="sxs-lookup"><span data-stu-id="6b7bd-132">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="6b7bd-133">**паккдделпарам**</span><span class="sxs-lookup"><span data-stu-id="6b7bd-133">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="6b7bd-134">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="6b7bd-134">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="6b7bd-135">**реуседделпарам**</span><span class="sxs-lookup"><span data-stu-id="6b7bd-135">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="6b7bd-136">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="6b7bd-136">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="6b7bd-137">**унпаккдделпарам**</span><span class="sxs-lookup"><span data-stu-id="6b7bd-137">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="6b7bd-138">**WM \_ DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="6b7bd-138">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="6b7bd-139">**\_данные DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="6b7bd-139">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

<span data-ttu-id="6b7bd-140">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="6b7bd-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6b7bd-141">Сведения о платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="6b7bd-141">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

