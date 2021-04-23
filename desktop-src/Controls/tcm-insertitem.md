---
title: Сообщение TCM_INSERTITEM (Коммктрл. h)
description: Вставляет новую вкладку в элемент управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл InsertItem.
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- Элементы управления Windows для TCM_INSERTITEM сообщений
topic_type:
- apiref
api_name:
- TCM_INSERTITEM
- TCM_INSERTITEMA
- TCM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58002006944a221571e37c37d25259d0aaa74fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654665"
---
# <a name="tcm_insertitem-message"></a><span data-ttu-id="9286f-105">\_Сообщение INSERTITEM TCM</span><span class="sxs-lookup"><span data-stu-id="9286f-105">TCM\_INSERTITEM message</span></span>

<span data-ttu-id="9286f-106">Вставляет новую вкладку в элемент управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="9286f-106">Inserts a new tab in a tab control.</span></span> <span data-ttu-id="9286f-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="9286f-107">You can send this message explicitly or by using the [**TabCtrl\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9286f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9286f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9286f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9286f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9286f-110">Индекс новой вкладки.</span><span class="sxs-lookup"><span data-stu-id="9286f-110">Index of the new tab.</span></span>

</dd> <dt>

<span data-ttu-id="9286f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9286f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9286f-112">Указатель на структуру [**тЦитем**](/windows/win32/api/commctrl/ns-commctrl-tcitema) , указывающую атрибуты вкладки. Члены этой структуры, **двстате** и **двстатемаск** , игнорируются этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="9286f-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that specifies the attributes of the tab. The **dwState** and **dwStateMask** members of this structure are ignored by this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9286f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9286f-113">Return value</span></span>

<span data-ttu-id="9286f-114">Возвращает индекс новой вкладки, если она выполнена успешно, или значение-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9286f-114">Returns the index of the new tab if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9286f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9286f-115">Requirements</span></span>



| <span data-ttu-id="9286f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9286f-116">Requirement</span></span> | <span data-ttu-id="9286f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9286f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9286f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9286f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9286f-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9286f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9286f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9286f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9286f-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9286f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9286f-122">Header</span><span class="sxs-lookup"><span data-stu-id="9286f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9286f-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9286f-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="9286f-124">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="9286f-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9286f-125">**TCM \_ ИНСЕРТИТЕМВ** (Юникод) и **TCM \_ инсертитема** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9286f-125">**TCM\_INSERTITEMW** (Unicode) and **TCM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





