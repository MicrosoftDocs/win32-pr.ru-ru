---
title: Сообщение TBM_SETTHUMBLENGTH (Коммктрл. h)
description: Задает длину ползунка в TrackBar. Это сообщение пропускается, если значение TrackBar не имеет \_ стиля TBS FIXEDLENGTH.
ms.assetid: 027fe341-a60a-4dbe-a48a-5ddaadef0b4a
keywords:
- Элементы управления Windows для TBM_SETTHUMBLENGTH сообщений
topic_type:
- apiref
api_name:
- TBM_SETTHUMBLENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d4ac33d2df43a267766e14ab95fb9729692bbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535126"
---
# <a name="tbm_setthumblength-message"></a><span data-ttu-id="4c22a-105">\_Сообщение ТБМ сетсумбленгс</span><span class="sxs-lookup"><span data-stu-id="4c22a-105">TBM\_SETTHUMBLENGTH message</span></span>

<span data-ttu-id="4c22a-106">Задает длину ползунка в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="4c22a-106">Sets the length of the slider in a trackbar.</span></span> <span data-ttu-id="4c22a-107">Это сообщение пропускается, если значение TrackBar не имеет стиля [**TBS \_ FIXEDLENGTH**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="4c22a-107">This message is ignored if the trackbar does not have the [**TBS\_FIXEDLENGTH**](trackbar-control-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="4c22a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c22a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c22a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4c22a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c22a-110">Длина ползунка в пикселях.</span><span class="sxs-lookup"><span data-stu-id="4c22a-110">Length, in pixels, of the slider.</span></span>

</dd> <dt>

<span data-ttu-id="4c22a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4c22a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4c22a-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4c22a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c22a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c22a-113">Return value</span></span>

<span data-ttu-id="4c22a-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="4c22a-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c22a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4c22a-115">Requirements</span></span>



| <span data-ttu-id="4c22a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4c22a-116">Requirement</span></span> | <span data-ttu-id="4c22a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4c22a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c22a-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c22a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4c22a-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c22a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4c22a-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c22a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4c22a-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4c22a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4c22a-122">Header</span><span class="sxs-lookup"><span data-stu-id="4c22a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c22a-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c22a-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c22a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c22a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c22a-125">**ТБМ \_ жетсумбленгс**</span><span class="sxs-lookup"><span data-stu-id="4c22a-125">**TBM\_GETTHUMBLENGTH**</span></span>](tbm-getthumblength.md)
</dt> </dl>

 

 





