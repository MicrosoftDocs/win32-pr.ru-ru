---
title: Код уведомления TBN_RESET (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, что пользователь выполнил Сброс содержимого диалогового окна "Настройка панели инструментов". Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 55efba85-b453-48b9-83df-76820249e7a8
keywords:
- TBN_RESET кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_RESET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 117ee2a50445ffe4dd8cd23d952fde7836bcf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071965"
---
# <a name="tbn_reset-notification-code"></a><span data-ttu-id="817e1-105">\_Код уведомления о сбросе ТБН</span><span class="sxs-lookup"><span data-stu-id="817e1-105">TBN\_RESET notification code</span></span>

<span data-ttu-id="817e1-106">Сообщает родительскому окну панели инструментов, что пользователь выполнил Сброс содержимого диалогового окна "Настройка панели инструментов".</span><span class="sxs-lookup"><span data-stu-id="817e1-106">Notifies the toolbar's parent window that the user has reset the content of the Customize Toolbar dialog box.</span></span> <span data-ttu-id="817e1-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="817e1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_RESET 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="817e1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="817e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="817e1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="817e1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="817e1-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="817e1-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="817e1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="817e1-111">Return value</span></span>

<span data-ttu-id="817e1-112">Возвратите ТБНРФ \_ ендкустомизе, чтобы закрыть диалоговое окно Настройка панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="817e1-112">Return TBNRF\_ENDCUSTOMIZE to close the Customize Toolbar dialog box.</span></span> <span data-ttu-id="817e1-113">Все остальные возвращаемые значения игнорируются.</span><span class="sxs-lookup"><span data-stu-id="817e1-113">All other return values are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="817e1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="817e1-114">Requirements</span></span>



| <span data-ttu-id="817e1-115">Требование</span><span class="sxs-lookup"><span data-stu-id="817e1-115">Requirement</span></span> | <span data-ttu-id="817e1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="817e1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="817e1-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="817e1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="817e1-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="817e1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="817e1-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="817e1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="817e1-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="817e1-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="817e1-121">Header</span><span class="sxs-lookup"><span data-stu-id="817e1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="817e1-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="817e1-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





