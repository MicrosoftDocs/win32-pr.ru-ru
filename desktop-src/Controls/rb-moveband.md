---
title: Сообщение RB_MOVEBAND (Коммктрл. h)
description: Перемещает диапазон из одного индекса в другой.
ms.assetid: bb5b45de-957e-46fb-b59a-18b55b69c395
keywords:
- Элементы управления Windows для RB_MOVEBAND сообщений
topic_type:
- apiref
api_name:
- RB_MOVEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146103c4c3d70fc0514729a00eac152c4847b85c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489234"
---
# <a name="rb_moveband-message"></a><span data-ttu-id="d686c-104">\_Сообщение МОВЕБАНД RB</span><span class="sxs-lookup"><span data-stu-id="d686c-104">RB\_MOVEBAND message</span></span>

<span data-ttu-id="d686c-105">Перемещает диапазон из одного индекса в другой.</span><span class="sxs-lookup"><span data-stu-id="d686c-105">Moves a band from one index to another.</span></span>

## <a name="parameters"></a><span data-ttu-id="d686c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d686c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d686c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d686c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d686c-108">Отсчитываемый от нуля индекс перемещаемого диапазона.</span><span class="sxs-lookup"><span data-stu-id="d686c-108">Zero-based index of the band to be moved.</span></span>

</dd> <dt>

<span data-ttu-id="d686c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d686c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d686c-110">Отсчитываемый от нуля индекс новой позиции полосы.</span><span class="sxs-lookup"><span data-stu-id="d686c-110">Zero-based index of the new band position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d686c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d686c-111">Return value</span></span>

<span data-ttu-id="d686c-112">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d686c-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d686c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d686c-113">Remarks</span></span>

<span data-ttu-id="d686c-114">Скорее всего, это сообщение изменит индекс других полос в элементе управления "Главная панель".</span><span class="sxs-lookup"><span data-stu-id="d686c-114">This message will most likely change the index of other bands in the rebar control.</span></span> <span data-ttu-id="d686c-115">Если полоса перемещена из индекса 6 в индекс 0, то все полосы в между будут иметь индекс, увеличивающийся на единицу.</span><span class="sxs-lookup"><span data-stu-id="d686c-115">If a band is moved from index 6 to index 0, all of the bands in between will have their index incremented by one.</span></span>

<span data-ttu-id="d686c-116">значение *lParam* никогда не должно превышать число полос минус единица.</span><span class="sxs-lookup"><span data-stu-id="d686c-116">*lParam* must never be greater than the number of bands minus one.</span></span> <span data-ttu-id="d686c-117">Количество полос можно получить с помощью сообщения [**RB \_ жетбандкаунт**](rb-getbandcount.md) .</span><span class="sxs-lookup"><span data-stu-id="d686c-117">The number of bands can be obtained with the [**RB\_GETBANDCOUNT**](rb-getbandcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d686c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d686c-118">Requirements</span></span>



| <span data-ttu-id="d686c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d686c-119">Requirement</span></span> | <span data-ttu-id="d686c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d686c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d686c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d686c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d686c-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d686c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d686c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d686c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d686c-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d686c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d686c-125">Header</span><span class="sxs-lookup"><span data-stu-id="d686c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d686c-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d686c-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





