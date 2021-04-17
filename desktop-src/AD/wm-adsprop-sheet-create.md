---
title: Сообщение WM_ADSPROP_SHEET_CREATE
description: Отправляется в объект уведомления для создания дополнительной страницы свойств в оснастке консоли управления Active Directory MMC.
ms.assetid: 3efa25f2-cd39-44f8-952e-203f1519ce2c
ms.tgt_platform: multiple
keywords:
- Сообщение WM_ADSPROP_SHEET_CREATE Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_SHEET_CREATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b540ffd87d4350a323577ff5fa317e94f9271f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534223"
---
# <a name="wm_adsprop_sheet_create-message"></a><span data-ttu-id="090da-104">\_Сообщение о \_ создании листа WM адспроп \_</span><span class="sxs-lookup"><span data-stu-id="090da-104">WM\_ADSPROP\_SHEET\_CREATE message</span></span>

<span data-ttu-id="090da-105">Сообщение **о \_ \_ \_ создании адспроп листа WM** отправляется в объект уведомления для создания дополнительной страницы свойств в оснастке консоли управления (MMC) Active Directory.</span><span class="sxs-lookup"><span data-stu-id="090da-105">The **WM\_ADSPROP\_SHEET\_CREATE** message is sent to the notification object to create a secondary property sheet in an Active Directory MMC snap-in.</span></span>

> [!Note]  
> <span data-ttu-id="090da-106">Это значение сообщения не определено в опубликованном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="090da-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="090da-107">Чтобы использовать это значение сообщения, необходимо определить его самостоятельно в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="090da-107">To use this message value, you must define it yourself in the exact format shown.</span></span>

 


```C++
#define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_ADSPROP_SHEET_CREATE,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="090da-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="090da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="090da-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="090da-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="090da-110">Маркер объекта уведомления.</span><span class="sxs-lookup"><span data-stu-id="090da-110">The handle of the notification object.</span></span> <span data-ttu-id="090da-111">Чтобы получить этот маркер, вызовите [**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="090da-111">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="090da-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="090da-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="090da-113">Содержит указатель на структуру [**\_ \_ \_ сведений о странице DSA sec**](dsa-sec-page-info.md) , которая определяет создаваемую вторичную страницу.</span><span class="sxs-lookup"><span data-stu-id="090da-113">Contains a pointer to a [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure that defines the secondary page to create.</span></span> <span data-ttu-id="090da-114">Только одну вторичную страницу свойств можно создать с сообщением **\_ \_ \_ CREATE адспроп листа WM** , поэтому структура [**Дсобжектнамес**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) может содержать только одну структуру [**дсобжект**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .</span><span class="sxs-lookup"><span data-stu-id="090da-114">Only one secondary property sheet can be created with the **WM\_ADSPROP\_SHEET\_CREATE** message, so the [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure can only contain one [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) structure.</span></span>

</dd> <dt>

<span data-ttu-id="090da-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="090da-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="090da-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="090da-116">Not used.</span></span> <span data-ttu-id="090da-117">Должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="090da-117">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="090da-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="090da-118">Return value</span></span>

<span data-ttu-id="090da-119">Возвращаемое значение для этого сообщения всегда равно нулю.</span><span class="sxs-lookup"><span data-stu-id="090da-119">The return value for this message is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="090da-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="090da-120">Remarks</span></span>

<span data-ttu-id="090da-121">Вызывающий объект должен выделить [**структуру \_ \_ \_ сведений о странице DSA sec**](dsa-sec-page-info.md) , строку заголовка и все строки [**Дсобжект**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) , используя один вызов функции [**локалаллок**](/windows/desktop/api/winbase/nf-winbase-localalloc) .</span><span class="sxs-lookup"><span data-stu-id="090da-121">The caller must allocate the [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure, the title string and all [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) strings using a single call to the [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc) function.</span></span> <span data-ttu-id="090da-122">Сообщение **о \_ \_ \_ создании адспроп листа WM** — это асинхронное сообщение, поэтому оно будет возвращаться перед созданием дополнительного листа.</span><span class="sxs-lookup"><span data-stu-id="090da-122">The **WM\_ADSPROP\_SHEET\_CREATE** message is an asynchronous message, so it will return before the secondary sheet is created.</span></span> <span data-ttu-id="090da-123">По этой причине память должна остаться неизменной после возвращения сообщения.</span><span class="sxs-lookup"><span data-stu-id="090da-123">Because of this, the memory must remain intact after the message returns.</span></span> <span data-ttu-id="090da-124">Получатель освободит эту память с помощью одного вызова функции [**функции LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) после создания дополнительного листа.</span><span class="sxs-lookup"><span data-stu-id="090da-124">The receiver will free this memory with a single call to the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function after the secondary sheet is created.</span></span>

## <a name="requirements"></a><span data-ttu-id="090da-125">Требования</span><span class="sxs-lookup"><span data-stu-id="090da-125">Requirements</span></span>



| <span data-ttu-id="090da-126">Требование</span><span class="sxs-lookup"><span data-stu-id="090da-126">Requirement</span></span> | <span data-ttu-id="090da-127">Значение</span><span class="sxs-lookup"><span data-stu-id="090da-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="090da-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="090da-128">Minimum supported client</span></span><br/> | <span data-ttu-id="090da-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="090da-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="090da-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="090da-130">Minimum supported server</span></span><br/> | <span data-ttu-id="090da-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="090da-131">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="090da-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="090da-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="090da-133">**\_ПАРЕНСВНД кфстр DS \_**</span><span class="sxs-lookup"><span data-stu-id="090da-133">**CFSTR\_DS\_PARENTHWND**</span></span>](cfstr-ds-parenthwnd.md)
</dt> <dt>

[<span data-ttu-id="090da-134">**\_ \_ сведения о странице DSA sec \_**</span><span class="sxs-lookup"><span data-stu-id="090da-134">**DSA\_SEC\_PAGE\_INFO**</span></span>](dsa-sec-page-info.md)
</dt> <dt>

[<span data-ttu-id="090da-135">**дсобжектнамес**</span><span class="sxs-lookup"><span data-stu-id="090da-135">**DSOBJECTNAMES**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[<span data-ttu-id="090da-136">**дсобжект**</span><span class="sxs-lookup"><span data-stu-id="090da-136">**DSOBJECT**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> <dt>

[<span data-ttu-id="090da-137">**локалаллок**</span><span class="sxs-lookup"><span data-stu-id="090da-137">**LocalAlloc**</span></span>](/windows/desktop/api/winbase/nf-winbase-localalloc)
</dt> <dt>

[<span data-ttu-id="090da-138">**Функции LocalFree**</span><span class="sxs-lookup"><span data-stu-id="090da-138">**LocalFree**</span></span>](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

