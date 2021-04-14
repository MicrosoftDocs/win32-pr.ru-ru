---
title: Константы WINBIO_EVENT (Винбио \_ types. h)
description: Укажите типы уведомлений о событиях поставщика услуг для отслеживания.
ms.assetid: 73805413-a8d9-4682-aa21-7032451d750a
topic_type:
- apiref
api_name:
- WINBIO_EVENT_FP_UNCLAIMED
- WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 182a4ffe254e946f1b8deca2c5034e665a58f7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533860"
---
# <a name="winbio_event-constants"></a><span data-ttu-id="e80c9-103">\_Константы событий винбио</span><span class="sxs-lookup"><span data-stu-id="e80c9-103">WINBIO\_EVENT Constants</span></span>

<span data-ttu-id="e80c9-104">Следующие константы можно использовать в функции [**винбиорегистеревентмонитор**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) для указания типов уведомлений о событиях поставщика услуг для отслеживания.</span><span class="sxs-lookup"><span data-stu-id="e80c9-104">The following constants can be used in the [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function to specify the types of service provider event notifications to monitor.</span></span>



| <span data-ttu-id="e80c9-105">Константа</span><span class="sxs-lookup"><span data-stu-id="e80c9-105">Constant</span></span>                                                                                                                                                                                                                        | <span data-ttu-id="e80c9-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e80c9-106">Description</span></span>                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span><dl> <span data-ttu-id="e80c9-107"><dt>**\_НЕутвержденное событие винбио \_ FP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e80c9-107"><dt>**WINBIO\_EVENT\_FP\_UNCLAIMED**</dt></span></span> </dl>                             | <span data-ttu-id="e80c9-108">Датчик обнаружил пальца, который не запрашивался приложением или окном, которое в данный момент находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="e80c9-108">The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="e80c9-109">Биометрическая платформа Windows вызывает функцию обратного вызова для указания на то, что произошел палец, но не пытается определить отпечаток.</span><span class="sxs-lookup"><span data-stu-id="e80c9-109">The Windows Biometric Framework calls into your callback function to indicate that a finger swipe has occurred but does not try to identify the fingerprint.</span></span><br/> |
| <span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span><dl> <span data-ttu-id="e80c9-110"><dt>**неутвержденная ВИНБИО для \_ события \_ FP \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e80c9-110"><dt>**WINBIO\_EVENT\_FP\_UNCLAIMED\_IDENTIFY**</dt></span></span> </dl> | <span data-ttu-id="e80c9-111">Датчик обнаружил пальца, который не запрашивался приложением или окном, которое в данный момент находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="e80c9-111">The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="e80c9-112">Биометрическая платформа Windows пытается опознать отпечаток и передает результат этого процесса функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="e80c9-112">The Windows Biometric Framework attempts to identify the fingerprint and passes the result of that process to your callback function.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="e80c9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e80c9-113">Requirements</span></span>



| <span data-ttu-id="e80c9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e80c9-114">Requirement</span></span> | <span data-ttu-id="e80c9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e80c9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e80c9-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e80c9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e80c9-117">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e80c9-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="e80c9-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e80c9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e80c9-119">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e80c9-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e80c9-120">Header</span><span class="sxs-lookup"><span data-stu-id="e80c9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e80c9-121"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e80c9-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e80c9-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e80c9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e80c9-123">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="e80c9-123">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





