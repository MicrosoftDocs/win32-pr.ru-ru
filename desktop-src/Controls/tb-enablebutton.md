---
title: Сообщение TB_ENABLEBUTTON (Коммктрл. h)
description: Включает или отключает указанную кнопку на панели инструментов.
ms.assetid: d73851ee-f909-4b70-9514-c45cd3a7e999
keywords:
- Элементы управления Windows для TB_ENABLEBUTTON сообщений
topic_type:
- apiref
api_name:
- TB_ENABLEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caf2fe865d49f9c89e31b1701abfcbf7991ae72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654717"
---
# <a name="tb_enablebutton-message"></a><span data-ttu-id="4fc9c-104">\_Сообщение ЕНАБЛЕБУТТОН ТБ</span><span class="sxs-lookup"><span data-stu-id="4fc9c-104">TB\_ENABLEBUTTON message</span></span>

<span data-ttu-id="4fc9c-105">Включает или отключает указанную кнопку на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="4fc9c-105">Enables or disables the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="4fc9c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4fc9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fc9c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4fc9c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4fc9c-108">Идентификатор команды для включения или отключения.</span><span class="sxs-lookup"><span data-stu-id="4fc9c-108">Command identifier of the button to enable or disable.</span></span>

</dd> <dt>

<span data-ttu-id="4fc9c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4fc9c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4fc9c-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это **логическое** значение, указывающее, следует ли включать или отключать указанную кнопку.</span><span class="sxs-lookup"><span data-stu-id="4fc9c-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to enable or disable the specified button.</span></span> <span data-ttu-id="4fc9c-111">Если **значение равно true**, кнопка включена.</span><span class="sxs-lookup"><span data-stu-id="4fc9c-111">If **TRUE**, the button is enabled.</span></span> <span data-ttu-id="4fc9c-112">Если задано **значение false**, кнопка отключена.</span><span class="sxs-lookup"><span data-stu-id="4fc9c-112">If **FALSE**, the button is disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fc9c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4fc9c-113">Return value</span></span>

<span data-ttu-id="4fc9c-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4fc9c-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fc9c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4fc9c-115">Remarks</span></span>

<span data-ttu-id="4fc9c-116">Если кнопка включена, ее можно нажать и проверить.</span><span class="sxs-lookup"><span data-stu-id="4fc9c-116">When a button has been enabled, it can be pressed and checked.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fc9c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4fc9c-117">Requirements</span></span>



| <span data-ttu-id="4fc9c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4fc9c-118">Requirement</span></span> | <span data-ttu-id="4fc9c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4fc9c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc9c-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fc9c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4fc9c-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4fc9c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4fc9c-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fc9c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4fc9c-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4fc9c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4fc9c-124">Header</span><span class="sxs-lookup"><span data-stu-id="4fc9c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fc9c-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fc9c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

