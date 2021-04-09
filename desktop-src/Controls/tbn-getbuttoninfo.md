---
title: Код уведомления TBN_GETBUTTONINFO (Коммктрл. h)
description: Извлекает сведения о настройке панели инструментов и уведомляет родительское окно панели инструментов о любых изменениях, внесенных в панель инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 088527fe-5a38-4c35-ba68-d0cbfdee410c
keywords:
- TBN_GETBUTTONINFO кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_GETBUTTONINFO
- TBN_GETBUTTONINFOA
- TBN_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409297306901980fa8b831e5c1129a13c596ef0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989060"
---
# <a name="tbn_getbuttoninfo-notification-code"></a><span data-ttu-id="0e3e4-105">\_Код уведомления ТБН жетбуттонинфо</span><span class="sxs-lookup"><span data-stu-id="0e3e4-105">TBN\_GETBUTTONINFO notification code</span></span>

<span data-ttu-id="0e3e4-106">Извлекает сведения о настройке панели инструментов и уведомляет родительское окно панели инструментов о любых изменениях, внесенных в панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="0e3e4-106">Retrieves toolbar customization information and notifies the toolbar's parent window of any changes being made to the toolbar.</span></span> <span data-ttu-id="0e3e4-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0e3e4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETBUTTONINFO 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0e3e4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e3e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e3e4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e3e4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e3e4-110">Указатель на структуру [**нмтулбар**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="0e3e4-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="0e3e4-111">Элемент **Член iItem** Указывает отсчитываемый от нуля индекс, который предоставляет количество кнопок, отображаемых в диалоговом окне Настройка панели инструментов, как доступные и представленные на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="0e3e4-111">The **iItem** member specifies a zero-based index that provides a count of the buttons the Customize Toolbar dialog box displays as both available and present on the toolbar.</span></span> <span data-ttu-id="0e3e4-112">Элемент **псзтекст** указывает адрес текущего текста кнопки, а **кчтекст** указывает ее длину в символах.</span><span class="sxs-lookup"><span data-stu-id="0e3e4-112">The **pszText** member specifies the address of the current button text, and **cchText** specifies its length in characters.</span></span> <span data-ttu-id="0e3e4-113">Приложение должно заполнить структуру сведениями о кнопке.</span><span class="sxs-lookup"><span data-stu-id="0e3e4-113">The application should fill the structure with information about the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e3e4-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e3e4-114">Return value</span></span>

<span data-ttu-id="0e3e4-115">Возвращает **значение true** , если сведения о кнопке скопированы в указанную структуру, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0e3e4-115">Returns **TRUE** if button information was copied to the specified structure, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e3e4-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e3e4-116">Remarks</span></span>

<span data-ttu-id="0e3e4-117">Элемент управления ToolBar выделяет буфер, и получатель (родительское окно) должен скопировать текст в этот буфер.</span><span class="sxs-lookup"><span data-stu-id="0e3e4-117">The toolbar control allocates a buffer, and the receiver (parent window) must copy the text into that buffer.</span></span> <span data-ttu-id="0e3e4-118">Элемент **кчтекст** содержит длину буфера, выделенного панелью инструментов при \_ отправке ТБН жетбуттонинфо в родительское окно.</span><span class="sxs-lookup"><span data-stu-id="0e3e4-118">The **cchText** member contains the length of the buffer allocated by the toolbar when TBN\_GETBUTTONINFO is sent to the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e3e4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0e3e4-119">Requirements</span></span>



| <span data-ttu-id="0e3e4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0e3e4-120">Requirement</span></span> | <span data-ttu-id="0e3e4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0e3e4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e3e4-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e3e4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0e3e4-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e3e4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0e3e4-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e3e4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0e3e4-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0e3e4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e3e4-126">Header</span><span class="sxs-lookup"><span data-stu-id="0e3e4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e3e4-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e3e4-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0e3e4-128">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="0e3e4-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0e3e4-129">**ТБН \_ ЖЕТБУТТОНИНФОВ** (Юникод) и **ТБН \_ жетбуттонинфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0e3e4-129">**TBN\_GETBUTTONINFOW** (Unicode) and **TBN\_GETBUTTONINFOA** (ANSI)</span></span><br/>       |



 

 





