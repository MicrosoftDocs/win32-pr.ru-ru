---
title: Код уведомления TBN_GETINFOTIP (Коммктрл. h)
description: Извлекает сведения о всплывающей подсказке для элемента панели инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 877de60c-f6e1-440a-81f0-d66ab443c985
keywords:
- TBN_GETINFOTIP кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_GETINFOTIP
- TBN_GETINFOTIPA
- TBN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda2c1b181ebea1840b153b8b2df8328b3f2cc8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071369"
---
# <a name="tbn_getinfotip-notification-code"></a><span data-ttu-id="192ff-105">\_Код уведомления ТБН жетинфотип</span><span class="sxs-lookup"><span data-stu-id="192ff-105">TBN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="192ff-106">Извлекает сведения о всплывающей подсказке для элемента панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="192ff-106">Retrieves infotip information for a toolbar item.</span></span> <span data-ttu-id="192ff-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="192ff-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETINFOTIP

    lptbgit = (LPNMTBGETINFOTIP) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="192ff-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="192ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="192ff-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="192ff-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="192ff-110">Указатель на структуру [**нмтбжетинфотип**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) , содержащую сведения об элементе и получающую сведения о всплывающих подсказках.</span><span class="sxs-lookup"><span data-stu-id="192ff-110">Pointer to an [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) structure that contains item information and receives infotip information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="192ff-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="192ff-111">Return value</span></span>

<span data-ttu-id="192ff-112">Возвращаемое значение игнорируется элементом управления.</span><span class="sxs-lookup"><span data-stu-id="192ff-112">The return value is ignored by the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="192ff-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="192ff-113">Remarks</span></span>

<span data-ttu-id="192ff-114">Поддержка подсказки на панели инструментов позволяет отображать подсказки для элементов, имеющих размер ИНФОТИПСИЗЕ символов.</span><span class="sxs-lookup"><span data-stu-id="192ff-114">The infotip support in the toolbar allows the toolbar to display tooltips for items that are as large as INFOTIPSIZE characters.</span></span> <span data-ttu-id="192ff-115">Если этот код уведомления не обрабатывается, панель инструментов будет использовать текст элемента для подсказки.</span><span class="sxs-lookup"><span data-stu-id="192ff-115">If this notification code is not processed, the toolbar will use the item's text for the infotip.</span></span>

## <a name="requirements"></a><span data-ttu-id="192ff-116">Требования</span><span class="sxs-lookup"><span data-stu-id="192ff-116">Requirements</span></span>



| <span data-ttu-id="192ff-117">Требование</span><span class="sxs-lookup"><span data-stu-id="192ff-117">Requirement</span></span> | <span data-ttu-id="192ff-118">Значение</span><span class="sxs-lookup"><span data-stu-id="192ff-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="192ff-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="192ff-119">Minimum supported client</span></span><br/> | <span data-ttu-id="192ff-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="192ff-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="192ff-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="192ff-121">Minimum supported server</span></span><br/> | <span data-ttu-id="192ff-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="192ff-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="192ff-123">Header</span><span class="sxs-lookup"><span data-stu-id="192ff-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="192ff-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="192ff-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="192ff-125">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="192ff-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="192ff-126">**ТБН \_ ЖЕТИНФОТИПВ** (Юникод) и **ТБН \_ жетинфотипа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="192ff-126">**TBN\_GETINFOTIPW** (Unicode) and **TBN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 





