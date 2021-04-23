---
title: Сообщение MCM_SIZERECTTOMIN (Коммктрл. h)
description: Вычисляет, сколько календарей помещается в данном прямоугольнике, а затем возвращает минимальный размер, который прямоугольник должен соответствовать этому количеству календарей. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сизеректтомин.
ms.assetid: d52a7f68-e0c9-4646-a4aa-97129dffeb5d
keywords:
- Элементы управления Windows для MCM_SIZERECTTOMIN сообщений
topic_type:
- apiref
api_name:
- MCM_SIZERECTTOMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f525f4cca9280b92fab0b9b86aa1d950ed990ef4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137434"
---
# <a name="mcm_sizerecttomin-message"></a><span data-ttu-id="10661-105">\_Сообщение MCM сизеректтомин</span><span class="sxs-lookup"><span data-stu-id="10661-105">MCM\_SIZERECTTOMIN message</span></span>

<span data-ttu-id="10661-106">Вычисляет, сколько календарей помещается в данном прямоугольнике, а затем возвращает минимальный размер, который прямоугольник должен соответствовать этому количеству календарей.</span><span class="sxs-lookup"><span data-stu-id="10661-106">Calculates how many calendars will fit in the given rectangle, and then returns the minimum size that a rectangle needs to be to fit that number of calendars.</span></span> <span data-ttu-id="10661-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ сизеректтомин**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) .</span><span class="sxs-lookup"><span data-stu-id="10661-107">You can send this message explicitly or by using the [**MonthCal\_SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="10661-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="10661-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10661-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10661-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10661-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="10661-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="10661-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10661-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10661-112">В записи содержит указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , описывающую область, которая больше или равна размеру, необходимой для размещения требуемого количества календарей.</span><span class="sxs-lookup"><span data-stu-id="10661-112">On entry, contains a pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that describes a region that is greater than or equal to the size necessary to fit the desired number of calendars.</span></span> <span data-ttu-id="10661-113">При возврате этой функции содержит структуру минимального значения **Rect** , которая соответствует этому числу календарей.</span><span class="sxs-lookup"><span data-stu-id="10661-113">When this function returns, contains the minimum **RECT** structure that fits this number of calendars.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10661-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10661-114">Return value</span></span>

<span data-ttu-id="10661-115">Не используется.</span><span class="sxs-lookup"><span data-stu-id="10661-115">Unused.</span></span>

## <a name="requirements"></a><span data-ttu-id="10661-116">Требования</span><span class="sxs-lookup"><span data-stu-id="10661-116">Requirements</span></span>



| <span data-ttu-id="10661-117">Требование</span><span class="sxs-lookup"><span data-stu-id="10661-117">Requirement</span></span> | <span data-ttu-id="10661-118">Значение</span><span class="sxs-lookup"><span data-stu-id="10661-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10661-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10661-119">Minimum supported client</span></span><br/> | <span data-ttu-id="10661-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10661-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10661-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10661-121">Minimum supported server</span></span><br/> | <span data-ttu-id="10661-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="10661-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10661-123">Header</span><span class="sxs-lookup"><span data-stu-id="10661-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="10661-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="10661-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

