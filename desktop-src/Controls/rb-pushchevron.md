---
title: Сообщение RB_PUSHCHEVRON (Коммктрл. h)
description: Посылается элементу управления главной панели для программной отправки шеврона.
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- Элементы управления Windows для RB_PUSHCHEVRON сообщений
topic_type:
- apiref
api_name:
- RB_PUSHCHEVRON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e09e558d5574d4fd28cf01e9794657556dda4ae8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534661"
---
# <a name="rb_pushchevron-message"></a><span data-ttu-id="30fde-104">\_Сообщение ПУШЧЕВРОН RB</span><span class="sxs-lookup"><span data-stu-id="30fde-104">RB\_PUSHCHEVRON message</span></span>

<span data-ttu-id="30fde-105">Посылается элементу управления главной панели для программной отправки шеврона.</span><span class="sxs-lookup"><span data-stu-id="30fde-105">Sent to a rebar control to programmatically push a chevron.</span></span>

## <a name="parameters"></a><span data-ttu-id="30fde-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="30fde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30fde-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30fde-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30fde-108">Отсчитываемый от нуля индекс полосы, Шеврон которого должен быть отправлен.</span><span class="sxs-lookup"><span data-stu-id="30fde-108">Zero-based index of the band whose chevron is to be pushed.</span></span>

</dd> <dt>

<span data-ttu-id="30fde-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30fde-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30fde-110">Определенное приложением 32-разрядное значение.</span><span class="sxs-lookup"><span data-stu-id="30fde-110">An application defined 32-bit value.</span></span> <span data-ttu-id="30fde-111">Он будет передан обратно в приложение в качестве элемента **лпарамнм** структуры [**нмребарчеврон**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) , который передается с уведомлением [РБН \_ чевронпушед](rbn-chevronpushed.md) .</span><span class="sxs-lookup"><span data-stu-id="30fde-111">It will be passed back to the application as the **lParamNM** member of the [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure that is passed with the [RBN\_CHEVRONPUSHED](rbn-chevronpushed.md) notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30fde-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30fde-112">Return value</span></span>

<span data-ttu-id="30fde-113">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="30fde-113">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="30fde-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30fde-114">Remarks</span></span>

<span data-ttu-id="30fde-115">При отправке этого сообщения элемент управления "Главная панель" отправит приложению код уведомления [РБН \_ чевронпушед](rbn-chevronpushed.md) , запросите его, чтобы отобразить угловое меню.</span><span class="sxs-lookup"><span data-stu-id="30fde-115">When this message is sent, the rebar control will send the application an [RBN\_CHEVRONPUSHED](rbn-chevronpushed.md) notification code, prompting it to display the chevron menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="30fde-116">Требования</span><span class="sxs-lookup"><span data-stu-id="30fde-116">Requirements</span></span>



| <span data-ttu-id="30fde-117">Требование</span><span class="sxs-lookup"><span data-stu-id="30fde-117">Requirement</span></span> | <span data-ttu-id="30fde-118">Значение</span><span class="sxs-lookup"><span data-stu-id="30fde-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30fde-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30fde-119">Minimum supported client</span></span><br/> | <span data-ttu-id="30fde-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30fde-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="30fde-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30fde-121">Minimum supported server</span></span><br/> | <span data-ttu-id="30fde-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="30fde-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30fde-123">Header</span><span class="sxs-lookup"><span data-stu-id="30fde-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="30fde-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="30fde-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





