---
description: Произошла ошибка устройства в фильтре модуля подготовки звука.
ms.assetid: 60e36476-f553-468d-a28d-351fdf4a02f1
title: EC_SNDDEV_OUT_ERROR (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1182aaba7bb30ad27511b47ba8e4432d8fd33da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652152"
---
# <a name="ec_snddev_out_error"></a><span data-ttu-id="fc03a-103">\_Ошибка EC снддев \_ out \_</span><span class="sxs-lookup"><span data-stu-id="fc03a-103">EC\_SNDDEV\_OUT\_ERROR</span></span>

<span data-ttu-id="fc03a-104">Произошла ошибка устройства в фильтре модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="fc03a-104">A device error has occurred in an audio renderer filter.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc03a-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc03a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc03a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="fc03a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="fc03a-107">Значение типа DWORD из перечислимого типа [**снддев \_ Err**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) , указывающее, как осуществлялся доступ к устройству в момент возникновения сбоя.</span><span class="sxs-lookup"><span data-stu-id="fc03a-107">DWORD value from the [**SNDDEV\_ERR**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) enumerated type, indicating how the device was being accessed when the failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="fc03a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="fc03a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="fc03a-109">Значение типа DWORD, указывающее на ошибку, возвращенную при вызове звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="fc03a-109">DWORD value indicating the error returned from the sound device call.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="fc03a-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="fc03a-110">Default Action</span></span>

<span data-ttu-id="fc03a-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="fc03a-111">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc03a-112">Требования</span><span class="sxs-lookup"><span data-stu-id="fc03a-112">Requirements</span></span>



| <span data-ttu-id="fc03a-113">Требование</span><span class="sxs-lookup"><span data-stu-id="fc03a-113">Requirement</span></span> | <span data-ttu-id="fc03a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="fc03a-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc03a-115">Header</span><span class="sxs-lookup"><span data-stu-id="fc03a-115">Header</span></span><br/> | <dl> <span data-ttu-id="fc03a-116"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc03a-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc03a-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc03a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc03a-118">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="fc03a-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="fc03a-119">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="fc03a-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




