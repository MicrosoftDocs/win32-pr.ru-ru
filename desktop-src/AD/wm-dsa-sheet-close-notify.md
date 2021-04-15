---
title: Сообщение WM_DSA_SHEET_CLOSE_NOTIFY
description: Отправляется в оснастку консоли управления Active Directory MMC при удалении дополнительной страницы свойств.
ms.assetid: 74271550-e1f7-4576-a04f-52d5b7c619cb
ms.tgt_platform: multiple
keywords:
- Сообщение WM_DSA_SHEET_CLOSE_NOTIFY Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CLOSE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36f03cdb6224ae5f55bc995897d766ce61e67693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654531"
---
# <a name="wm_dsa_sheet_close_notify-message"></a><span data-ttu-id="6ae6d-104">\_ \_ \_ Сообщение о закрытии страницы WM DSA \_</span><span class="sxs-lookup"><span data-stu-id="6ae6d-104">WM\_DSA\_SHEET\_CLOSE\_NOTIFY message</span></span>

<span data-ttu-id="6ae6d-105">При удалении дополнительной страницы свойств в оснастке консоли управления Active Directory MMC отправляется сообщение об ошибке **\_ Close (закрыть) \_ листа \_ \_ WM DSA** .</span><span class="sxs-lookup"><span data-stu-id="6ae6d-105">The **WM\_DSA\_SHEET\_CLOSE\_NOTIFY** message is posted to the Active Directory MMC snap-in when a secondary property sheet is destroyed.</span></span>

> [!Note]  
> <span data-ttu-id="6ae6d-106">Это значение сообщения не определено в опубликованном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="6ae6d-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="6ae6d-107">Чтобы использовать это значение сообщения, необходимо определить его самостоятельно в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="6ae6d-107">To use this message value, you must define it yourself in the exact format shown.</span></span>

 


```C++
#define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5)
```




```C++
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_DSA_SHEET_CLOSE_NOTIFY,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="6ae6d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ae6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ae6d-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="6ae6d-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6ae6d-110">Обработчик окна оснастки, который будет обрабатывать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="6ae6d-110">The window handle of the snap-in window that will process this message.</span></span> <span data-ttu-id="6ae6d-111">Этот маркер получается из элемента **хвндхидден** структуры [**пропшиткфг**](propsheetcfg.md) .</span><span class="sxs-lookup"><span data-stu-id="6ae6d-111">This handle is obtained from the **hwndHidden** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6ae6d-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ae6d-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ae6d-113">Содержит определяемое приложением 32-разрядное значение.</span><span class="sxs-lookup"><span data-stu-id="6ae6d-113">Contains an application-defined 32-bit value.</span></span> <span data-ttu-id="6ae6d-114">Это значение берется из элемента **впарамшитклосе** структуры [**пропшиткфг**](propsheetcfg.md) .</span><span class="sxs-lookup"><span data-stu-id="6ae6d-114">This is obtained from the **wParamSheetClose** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6ae6d-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ae6d-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ae6d-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="6ae6d-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ae6d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ae6d-117">Return value</span></span>

<span data-ttu-id="6ae6d-118">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="6ae6d-118">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ae6d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="6ae6d-119">Requirements</span></span>



| <span data-ttu-id="6ae6d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="6ae6d-120">Requirement</span></span> | <span data-ttu-id="6ae6d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6ae6d-121">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6ae6d-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ae6d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6ae6d-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ae6d-123">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6ae6d-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ae6d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6ae6d-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ae6d-125">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ae6d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ae6d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ae6d-127">**пропшиткфг**</span><span class="sxs-lookup"><span data-stu-id="6ae6d-127">**PROPSHEETCFG**</span></span>](propsheetcfg.md)
</dt> </dl>

 

 





