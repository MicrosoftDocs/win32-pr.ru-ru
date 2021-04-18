---
description: В фильтре записи звука произошла ошибка устройства.
ms.assetid: 13f8641b-7881-4f1c-816c-77c140e48ed4
title: EC_SNDDEV_IN_ERROR (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f9b95055483b1bda812179f1a1bf132d12de7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652153"
---
# <a name="ec_snddev_in_error"></a><span data-ttu-id="84b05-103">\_Ошибка EC \_ снддев \_</span><span class="sxs-lookup"><span data-stu-id="84b05-103">EC\_SNDDEV\_IN\_ERROR</span></span>

<span data-ttu-id="84b05-104">В фильтре записи звука произошла ошибка устройства.</span><span class="sxs-lookup"><span data-stu-id="84b05-104">A device error has occurred in an audio capture filter.</span></span>

## <a name="parameters"></a><span data-ttu-id="84b05-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="84b05-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84b05-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="84b05-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="84b05-107">Значение типа DWORD из перечислимого типа [**снддев \_ Err**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) , указывающее, как осуществлялся доступ к устройству в момент возникновения сбоя.</span><span class="sxs-lookup"><span data-stu-id="84b05-107">DWORD value from the [**SNDDEV\_ERR**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) enumerated type, indicating how the device was being accessed when the failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="84b05-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="84b05-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="84b05-109">Значение типа DWORD, указывающее на ошибку, возвращенную при вызове звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="84b05-109">DWORD value indicating the error returned from the sound device call.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="84b05-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="84b05-110">Default Action</span></span>

<span data-ttu-id="84b05-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="84b05-111">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="84b05-112">Требования</span><span class="sxs-lookup"><span data-stu-id="84b05-112">Requirements</span></span>



| <span data-ttu-id="84b05-113">Требование</span><span class="sxs-lookup"><span data-stu-id="84b05-113">Requirement</span></span> | <span data-ttu-id="84b05-114">Значение</span><span class="sxs-lookup"><span data-stu-id="84b05-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="84b05-115">Header</span><span class="sxs-lookup"><span data-stu-id="84b05-115">Header</span></span><br/> | <dl> <span data-ttu-id="84b05-116"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="84b05-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84b05-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84b05-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84b05-118">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="84b05-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="84b05-119">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="84b05-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




