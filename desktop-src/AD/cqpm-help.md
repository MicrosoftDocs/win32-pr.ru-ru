---
title: Сообщение CQPM_HELP (Кмнкуери. h)
description: Отправляется в функцию обратного вызова Ккпажепрок страницы расширения формы запроса, чтобы разрешить расширению страницы отображать контекстную справку для страницы.
ms.assetid: 07f5bd24-bca2-4d87-8e1e-acce552a3bf2
ms.tgt_platform: multiple
keywords:
- Сообщение CQPM_HELP Active Directory
topic_type:
- apiref
api_name:
- CQPM_HELP
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7635b87a0ba489c63f87fb32742c37a9f7044860
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135299"
---
# <a name="cqpm_help-message"></a><span data-ttu-id="93cc1-104">\_Справочное сообщение ККПМ</span><span class="sxs-lookup"><span data-stu-id="93cc1-104">CQPM\_HELP message</span></span>

<span data-ttu-id="93cc1-105">Сообщение **\_ справки ККПМ** отправляется в функцию обратного вызова [**ккпажепрок**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) на странице расширения формы запроса, чтобы разрешить расширению страницы отображать контекстную справку для этой страницы.</span><span class="sxs-lookup"><span data-stu-id="93cc1-105">The **CQPM\_HELP** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to allow the page extension to display context-sensitive help for the page.</span></span> <span data-ttu-id="93cc1-106">По возможности расширение страницы запроса должно отображать контекстную справку в ответ на это событие.</span><span class="sxs-lookup"><span data-stu-id="93cc1-106">If possible, the query page extension should display context-sensitive help in response to this event.</span></span>

## <a name="parameters"></a><span data-ttu-id="93cc1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="93cc1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93cc1-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93cc1-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93cc1-109">Не используется.</span><span class="sxs-lookup"><span data-stu-id="93cc1-109">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="93cc1-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93cc1-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93cc1-111">Указатель на структуру [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) , которая содержит дополнительные данные о пункте меню, элементе управления, диалоговом окне или окне, для которого запрашивается контекстная справка.</span><span class="sxs-lookup"><span data-stu-id="93cc1-111">Pointer to a [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure that contains additional data about the menu item, control, dialog box, or window for which context-sensitive help is requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93cc1-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93cc1-112">Return value</span></span>

<span data-ttu-id="93cc1-113">Возвращаемое значение для этого сообщения игнорируется.</span><span class="sxs-lookup"><span data-stu-id="93cc1-113">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="93cc1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="93cc1-114">Requirements</span></span>



| <span data-ttu-id="93cc1-115">Требование</span><span class="sxs-lookup"><span data-stu-id="93cc1-115">Requirement</span></span> | <span data-ttu-id="93cc1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="93cc1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93cc1-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93cc1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="93cc1-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93cc1-118">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="93cc1-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93cc1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="93cc1-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93cc1-120">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="93cc1-121">Header</span><span class="sxs-lookup"><span data-stu-id="93cc1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="93cc1-122"><dt>Кмнкуери. h</dt></span><span class="sxs-lookup"><span data-stu-id="93cc1-122"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93cc1-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93cc1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93cc1-124">**ккпажепрок**</span><span class="sxs-lookup"><span data-stu-id="93cc1-124">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="93cc1-125">**HELPINFO**</span><span class="sxs-lookup"><span data-stu-id="93cc1-125">**HELPINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-helpinfo)
</dt> </dl>

 

