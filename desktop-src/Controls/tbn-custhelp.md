---
title: Код уведомления TBN_CUSTHELP (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, что пользователь выбрал кнопку «Справка» в диалоговом окне Настройка панели инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: e889764b-abbd-42a6-8c13-ace6ee052039
keywords:
- TBN_CUSTHELP кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_CUSTHELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89754deaef2ec4ceb020bd1572c5a419315299e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891645"
---
# <a name="tbn_custhelp-notification-code"></a><span data-ttu-id="6b335-105">\_Код уведомления ТБН кусселп</span><span class="sxs-lookup"><span data-stu-id="6b335-105">TBN\_CUSTHELP notification code</span></span>

<span data-ttu-id="6b335-106">Сообщает родительскому окну панели инструментов, что пользователь выбрал кнопку «Справка» в диалоговом окне Настройка панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="6b335-106">Notifies a toolbar's parent window that the user has chosen the Help button in the Customize Toolbar dialog box.</span></span> <span data-ttu-id="6b335-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6b335-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_CUSTHELP 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6b335-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b335-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b335-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b335-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b335-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="6b335-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b335-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b335-111">Return value</span></span>

<span data-ttu-id="6b335-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="6b335-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b335-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6b335-113">Requirements</span></span>



| <span data-ttu-id="6b335-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6b335-114">Requirement</span></span> | <span data-ttu-id="6b335-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6b335-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b335-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b335-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6b335-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6b335-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b335-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b335-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6b335-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6b335-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b335-120">Header</span><span class="sxs-lookup"><span data-stu-id="6b335-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b335-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b335-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





