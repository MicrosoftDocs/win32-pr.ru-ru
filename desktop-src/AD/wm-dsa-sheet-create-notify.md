---
title: Сообщение WM_DSA_SHEET_CREATE_NOTIFY
description: Опубликовано в оснастке консоли управления Active Directory MMC для создания дополнительной страницы свойств.
ms.assetid: 878878bf-fb78-4669-b282-1dd3349f35d5
ms.tgt_platform: multiple
keywords:
- Сообщение WM_DSA_SHEET_CREATE_NOTIFY Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CREATE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f08424e7b39449861ec654f1ff7891c6e9c60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988733"
---
# <a name="wm_dsa_sheet_create_notify-message"></a><span data-ttu-id="92925-104">\_ \_ \_ \_ Сообщение об ошибке создания уведомления для листа WM DSA</span><span class="sxs-lookup"><span data-stu-id="92925-104">WM\_DSA\_SHEET\_CREATE\_NOTIFY message</span></span>

<span data-ttu-id="92925-105">В оснастке консоли управления Active Directory MMC для создания дополнительной страницы свойств отправляется сообщение **\_ \_ \_ \_ уведомления о создании сообщения об ошибке WM DSA** .</span><span class="sxs-lookup"><span data-stu-id="92925-105">The **WM\_DSA\_SHEET\_CREATE\_NOTIFY** message is posted to the Active Directory MMC snap-in to create a secondary property sheet.</span></span>

> [!Note]  
> <span data-ttu-id="92925-106">Это значение сообщения не определено в опубликованном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="92925-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="92925-107">Чтобы использовать это значение сообщения, определите его в точно указанном формате.</span><span class="sxs-lookup"><span data-stu-id="92925-107">To use this message value, define it in the exact format shown.</span></span>

 


```C++
#define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
LRESULT SendMessage(
    (HWND) hwnd, 
    WM_DSA_SHEET_CREATE_NOTIFY,
    (WPARAM) wParam, 
    (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="92925-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="92925-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92925-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="92925-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="92925-110">Обработчик окна оснастки, который будет обрабатывать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="92925-110">The window handle of the snap-in window that will process this message.</span></span> <span data-ttu-id="92925-111">Этот маркер получается из элемента **хвндхидден** структуры [**пропшиткфг**](propsheetcfg.md) .</span><span class="sxs-lookup"><span data-stu-id="92925-111">This handle is obtained from the **hwndHidden** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="92925-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="92925-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92925-113">Содержит указатель на структуру [**\_ \_ \_ сведений о странице DSA sec**](dsa-sec-page-info.md) , которая определяет создаваемую дополнительную страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="92925-113">Contains a pointer to a [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure that defines the secondary property sheet to create.</span></span> <span data-ttu-id="92925-114">Получатель сообщений должен освободить эту память с помощью функции [**функции LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) , если она больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="92925-114">The message receiver must free this memory with the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function when it is no longer required.</span></span>

</dd> <dt>

<span data-ttu-id="92925-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92925-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92925-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="92925-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92925-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92925-117">Return value</span></span>

<span data-ttu-id="92925-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="92925-118">Not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="92925-119">Требования</span><span class="sxs-lookup"><span data-stu-id="92925-119">Requirements</span></span>



| <span data-ttu-id="92925-120">Требование</span><span class="sxs-lookup"><span data-stu-id="92925-120">Requirement</span></span> | <span data-ttu-id="92925-121">Значение</span><span class="sxs-lookup"><span data-stu-id="92925-121">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="92925-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92925-122">Minimum supported client</span></span><br/> | <span data-ttu-id="92925-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92925-123">Windows Vista</span></span><br/>       |
| <span data-ttu-id="92925-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92925-124">Minimum supported server</span></span><br/> | <span data-ttu-id="92925-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92925-125">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92925-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92925-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92925-127">**пропшиткфг**</span><span class="sxs-lookup"><span data-stu-id="92925-127">**PROPSHEETCFG**</span></span>](propsheetcfg.md)
</dt> <dt>

[<span data-ttu-id="92925-128">**\_ \_ сведения о странице DSA sec \_**</span><span class="sxs-lookup"><span data-stu-id="92925-128">**DSA\_SEC\_PAGE\_INFO**</span></span>](dsa-sec-page-info.md)
</dt> <dt>

[<span data-ttu-id="92925-129">**Функции LocalFree**</span><span class="sxs-lookup"><span data-stu-id="92925-129">**LocalFree**</span></span>](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

