---
title: Сообщение TB_CHECKBUTTON (Коммктрл. h)
description: Проверяет или снимает заданную кнопку на панели инструментов.
ms.assetid: e67734a9-851c-41ab-8ad7-15d434f58e5a
keywords:
- Элементы управления Windows для TB_CHECKBUTTON сообщений
topic_type:
- apiref
api_name:
- TB_CHECKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7734b37da44db38d9ca09b34ad9e666cc90eb5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072030"
---
# <a name="tb_checkbutton-message"></a><span data-ttu-id="7a6a4-104">\_Сообщение ЧЕККБУТТОН ТБ</span><span class="sxs-lookup"><span data-stu-id="7a6a4-104">TB\_CHECKBUTTON message</span></span>

<span data-ttu-id="7a6a4-105">Проверяет или снимает заданную кнопку на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-105">Checks or unchecks a given button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="7a6a4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a6a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a6a4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a6a4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a6a4-108">Идентификатор команды для проверки.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-108">Command identifier of the button to check.</span></span>

</dd> <dt>

<span data-ttu-id="7a6a4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a6a4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a6a4-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это **логическое** значение, указывающее, следует ли установить или снять указанную кнопку.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to check or uncheck the specified button.</span></span> <span data-ttu-id="7a6a4-111">Если **значение — true**, добавляется проверка.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-111">If **TRUE**, the check is added.</span></span> <span data-ttu-id="7a6a4-112">Если **значение равно false**, то проверка будет удалена.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-112">If **FALSE**, the check is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a6a4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a6a4-113">Return value</span></span>

<span data-ttu-id="7a6a4-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a6a4-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a6a4-115">Remarks</span></span>

<span data-ttu-id="7a6a4-116">Если кнопка отмечена, она отображается в нажатом состоянии.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-116">When a button is checked, it is displayed in the pressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a6a4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="7a6a4-117">Requirements</span></span>



| <span data-ttu-id="7a6a4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="7a6a4-118">Requirement</span></span> | <span data-ttu-id="7a6a4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="7a6a4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a6a4-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a6a4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7a6a4-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a6a4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7a6a4-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a6a4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7a6a4-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7a6a4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7a6a4-124">Header</span><span class="sxs-lookup"><span data-stu-id="7a6a4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a6a4-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a6a4-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

