---
title: Сообщение TB_PRESSBUTTON (Коммктрл. h)
description: Нажимает или освобождает указанную кнопку на панели инструментов.
ms.assetid: 03f6c3c2-d679-4e3a-a07b-c7e46c97972a
keywords:
- Элементы управления Windows для TB_PRESSBUTTON сообщений
topic_type:
- apiref
api_name:
- TB_PRESSBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0e86092951b242cee7388fc0d5d1bbdbca835e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136807"
---
# <a name="tb_pressbutton-message"></a><span data-ttu-id="06fdc-104">\_Сообщение ПРЕССБУТТОН ТБ</span><span class="sxs-lookup"><span data-stu-id="06fdc-104">TB\_PRESSBUTTON message</span></span>

<span data-ttu-id="06fdc-105">Нажимает или освобождает указанную кнопку на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="06fdc-105">Presses or releases the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="06fdc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="06fdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06fdc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06fdc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06fdc-108">Идентификатор команды для нажатия или выпуска.</span><span class="sxs-lookup"><span data-stu-id="06fdc-108">Command identifier of the button to press or release.</span></span>

</dd> <dt>

<span data-ttu-id="06fdc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06fdc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06fdc-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это **логическое** значение, указывающее, следует ли нажать или отпустить указанную кнопку.</span><span class="sxs-lookup"><span data-stu-id="06fdc-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to press or release the specified button.</span></span> <span data-ttu-id="06fdc-111">Если **значение равно true**, кнопка нажата.</span><span class="sxs-lookup"><span data-stu-id="06fdc-111">If **TRUE**, the button is pressed.</span></span> <span data-ttu-id="06fdc-112">Если **значение равно false**, кнопка отпущена.</span><span class="sxs-lookup"><span data-stu-id="06fdc-112">If **FALSE**, the button is released.</span></span>

<span data-ttu-id="06fdc-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="06fdc-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06fdc-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06fdc-114">Return value</span></span>

<span data-ttu-id="06fdc-115">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="06fdc-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="06fdc-116">Требования</span><span class="sxs-lookup"><span data-stu-id="06fdc-116">Requirements</span></span>



| <span data-ttu-id="06fdc-117">Требование</span><span class="sxs-lookup"><span data-stu-id="06fdc-117">Requirement</span></span> | <span data-ttu-id="06fdc-118">Значение</span><span class="sxs-lookup"><span data-stu-id="06fdc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06fdc-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06fdc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="06fdc-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06fdc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06fdc-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06fdc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="06fdc-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="06fdc-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06fdc-123">Header</span><span class="sxs-lookup"><span data-stu-id="06fdc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="06fdc-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="06fdc-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

