---
title: Сообщение TBN_DELETINGBUTTON (Коммктрл. h)
description: Посылается элементом управления ToolBar при удалении кнопки. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 08116071-36d6-456b-88f9-62a22cdb7ed9
keywords:
- Элементы управления Windows для TBN_DELETINGBUTTON сообщений
topic_type:
- apiref
api_name:
- TBN_DELETINGBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26337fd1abc6c67351fe2b38e83ee7d90a11f6e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533896"
---
# <a name="tbn_deletingbutton-message"></a><span data-ttu-id="8add4-105">\_Сообщение ТБН делетингбуттон</span><span class="sxs-lookup"><span data-stu-id="8add4-105">TBN\_DELETINGBUTTON message</span></span>

<span data-ttu-id="8add4-106">Посылается элементом управления ToolBar при удалении кнопки.</span><span class="sxs-lookup"><span data-stu-id="8add4-106">Sent by a toolbar control when a button is about to be deleted.</span></span> <span data-ttu-id="8add4-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8add4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
 TBN_DELETINGBUTTON 

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8add4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8add4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8add4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8add4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8add4-110">Указатель на структуру [**нмтулбар**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) , содержащую сведения об удаляемой кнопке.</span><span class="sxs-lookup"><span data-stu-id="8add4-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about the button being deleted.</span></span> <span data-ttu-id="8add4-111">Для этого кода уведомления допустимы только элементы **HDR** и **Член iItem** этой структуры.</span><span class="sxs-lookup"><span data-stu-id="8add4-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span> <span data-ttu-id="8add4-112">Элемент **Член iItem** этой структуры содержит идентификатор команды удаляемой кнопки.</span><span class="sxs-lookup"><span data-stu-id="8add4-112">The **iItem** member of this structure contains the command identifier of the button being deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8add4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8add4-113">Return value</span></span>

<span data-ttu-id="8add4-114">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8add4-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="8add4-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8add4-115">Requirements</span></span>



| <span data-ttu-id="8add4-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8add4-116">Requirement</span></span> | <span data-ttu-id="8add4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8add4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8add4-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8add4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8add4-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8add4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8add4-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8add4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8add4-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8add4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8add4-122">Header</span><span class="sxs-lookup"><span data-stu-id="8add4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8add4-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8add4-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





