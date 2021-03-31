---
title: Сообщение SBM_GETSCROLLBARINFO (Winuser. h)
description: Отправляется приложением для получения сведений об указанной полосе прокрутки.
ms.assetid: db6f704f-99ee-448c-ae7a-dd5a23399fb6
keywords:
- Элементы управления Windows для SBM_GETSCROLLBARINFO сообщений
topic_type:
- apiref
api_name:
- SBM_GETSCROLLBARINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8bdd78eb665bd069d854538bb2bdfae1a946765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802182"
---
# <a name="sbm_getscrollbarinfo-message"></a><span data-ttu-id="1c714-104">\_Сообщение СБМ жетскроллбаринфо</span><span class="sxs-lookup"><span data-stu-id="1c714-104">SBM\_GETSCROLLBARINFO message</span></span>

<span data-ttu-id="1c714-105">Отправляется приложением для получения сведений об указанной полосе прокрутки.</span><span class="sxs-lookup"><span data-stu-id="1c714-105">Sent by an application to retrieve information about the specified scroll bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="1c714-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c714-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c714-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1c714-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c714-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="1c714-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1c714-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c714-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c714-110">Указатель на структуру [**скроллбаринфо**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) , которая получает сведения.</span><span class="sxs-lookup"><span data-stu-id="1c714-110">Pointer to a [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) structure that receives the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c714-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c714-111">Return value</span></span>

<span data-ttu-id="1c714-112">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1c714-112">Returns nonzero if successful or zero otherwise.</span></span>

<span data-ttu-id="1c714-113">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="1c714-113">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c714-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1c714-114">Requirements</span></span>



| <span data-ttu-id="1c714-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1c714-115">Requirement</span></span> | <span data-ttu-id="1c714-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1c714-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c714-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c714-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1c714-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1c714-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1c714-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c714-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1c714-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1c714-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1c714-121">Header</span><span class="sxs-lookup"><span data-stu-id="1c714-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c714-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c714-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c714-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c714-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="1c714-124">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1c714-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1c714-125">**жетскроллбаринфо**</span><span class="sxs-lookup"><span data-stu-id="1c714-125">**GetScrollBarInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo)
</dt> <dt>

[<span data-ttu-id="1c714-126">**скроллбаринфо**</span><span class="sxs-lookup"><span data-stu-id="1c714-126">**SCROLLBARINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollbarinfo)
</dt> </dl>

 

