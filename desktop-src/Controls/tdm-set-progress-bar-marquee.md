---
title: Сообщение TDM_SET_PROGRESS_BAR_MARQUEE (Коммктрл. h)
description: Запускает и останавливает отображение индикатора выполнения в диалоговом окне задачи и задает скорость бегущей строки.
ms.assetid: df947171-a916-4db9-abe0-57a3bf11037f
keywords:
- Элементы управления Windows для TDM_SET_PROGRESS_BAR_MARQUEE сообщений
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_MARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f73d3d4308d2e3f963c015b6e36f385902bea6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071960"
---
# <a name="tdm_set_progress_bar_marquee-message"></a><span data-ttu-id="2522d-104">TDM \_ задать \_ \_ \_ сообщение области индикатора выполнения</span><span class="sxs-lookup"><span data-stu-id="2522d-104">TDM\_SET\_PROGRESS\_BAR\_MARQUEE message</span></span>

<span data-ttu-id="2522d-105">Запускает и останавливает отображение индикатора выполнения в диалоговом окне задачи и задает скорость бегущей строки.</span><span class="sxs-lookup"><span data-stu-id="2522d-105">Starts and stops the marquee display of the progress bar in a task dialog, and sets the speed of the marquee.</span></span>

## <a name="parameters"></a><span data-ttu-id="2522d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2522d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2522d-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2522d-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2522d-108">**Логическое** значение, указывающее, следует ли включать или отключать отображение бегущей строки.</span><span class="sxs-lookup"><span data-stu-id="2522d-108">A **BOOL** that indicates whether to turn the marquee display on or off.</span></span> <span data-ttu-id="2522d-109">Используйте **значение true** , чтобы включить отображение бегущей строки, или **значение false** , чтобы отключить его.</span><span class="sxs-lookup"><span data-stu-id="2522d-109">Use **TRUE** to turn on the marquee display, or **FALSE** to turn it off.</span></span>

</dd> <dt>

<span data-ttu-id="2522d-110">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2522d-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2522d-111">Значение **uint** , указывающее время (в миллисекундах) между обновлениями анимации области.</span><span class="sxs-lookup"><span data-stu-id="2522d-111">A **UINT** that specifies the time, in milliseconds, between marquee animation updates.</span></span> <span data-ttu-id="2522d-112">Если этот параметр равен нулю, то анимация бегущей строки обновляется каждые 30 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="2522d-112">If this parameter is zero, the marquee animation is updated every 30 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2522d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2522d-113">Return value</span></span>

<span data-ttu-id="2522d-114">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="2522d-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="2522d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2522d-115">Remarks</span></span>

<span data-ttu-id="2522d-116">Сведения о режиме бегущей строки см. в разделе [элемент управления](progress-bar-control.md)"индикатор выполнения".</span><span class="sxs-lookup"><span data-stu-id="2522d-116">For information on marquee mode, see [Progress Bar Control](progress-bar-control.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2522d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2522d-117">Requirements</span></span>



| <span data-ttu-id="2522d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2522d-118">Requirement</span></span> | <span data-ttu-id="2522d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2522d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2522d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2522d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2522d-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2522d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2522d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2522d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2522d-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2522d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2522d-124">Header</span><span class="sxs-lookup"><span data-stu-id="2522d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2522d-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2522d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





