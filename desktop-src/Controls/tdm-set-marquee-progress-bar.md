---
title: Сообщение TDM_SET_MARQUEE_PROGRESS_BAR (Коммктрл. h)
description: Указывает, должен ли размещенный индикатор выполнения диалогового окна задачи отображаться в режиме бегущей строки.
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- Элементы управления Windows для TDM_SET_MARQUEE_PROGRESS_BAR сообщений
topic_type:
- apiref
api_name:
- TDM_SET_MARQUEE_PROGRESS_BAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a9384826b89d07c6564dc511d4909058871ca3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137426"
---
# <a name="tdm_set_marquee_progress_bar-message"></a><span data-ttu-id="e25e7-104">Сообщение с индикатором \_ выполнения TDM Set \_ Marquee \_ \_</span><span class="sxs-lookup"><span data-stu-id="e25e7-104">TDM\_SET\_MARQUEE\_PROGRESS\_BAR message</span></span>

<span data-ttu-id="e25e7-105">Указывает, должен ли размещенный индикатор выполнения диалогового окна задачи отображаться в режиме бегущей строки.</span><span class="sxs-lookup"><span data-stu-id="e25e7-105">Indicates whether the hosted progress bar of a task dialog should be displayed in marquee mode.</span></span>

## <a name="parameters"></a><span data-ttu-id="e25e7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e25e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e25e7-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e25e7-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e25e7-108">**Логическое** значение, указывающее, должен ли индикатор выполнения отображаться в режиме бегущей строки.</span><span class="sxs-lookup"><span data-stu-id="e25e7-108">A **BOOL** that indicates whether the progress bar should be shown in marquee mode.</span></span> <span data-ttu-id="e25e7-109">Значение **true** включает режим бегущей строки, а значение **false** отключает режим бегущей строки.</span><span class="sxs-lookup"><span data-stu-id="e25e7-109">A value of **TRUE** turns on marquee mode, and a value of **FALSE** turns off marquee mode.</span></span>

</dd> <dt>

<span data-ttu-id="e25e7-110">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e25e7-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e25e7-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e25e7-111">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e25e7-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e25e7-112">Return value</span></span>

<span data-ttu-id="e25e7-113">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="e25e7-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="e25e7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e25e7-114">Remarks</span></span>

<span data-ttu-id="e25e7-115">Сведения о режиме бегущей строки см. в разделе [элемент управления](progress-bar-control.md)"индикатор выполнения".</span><span class="sxs-lookup"><span data-stu-id="e25e7-115">For information on marquee mode, see [Progress Bar Control](progress-bar-control.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e25e7-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e25e7-116">Requirements</span></span>



| <span data-ttu-id="e25e7-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e25e7-117">Requirement</span></span> | <span data-ttu-id="e25e7-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e25e7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e25e7-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e25e7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e25e7-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e25e7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e25e7-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e25e7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e25e7-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e25e7-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e25e7-123">Header</span><span class="sxs-lookup"><span data-stu-id="e25e7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e25e7-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e25e7-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





