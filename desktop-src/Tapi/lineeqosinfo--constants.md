---
description: Эти константы используются TSP для обнаружения результатов запроса QoS (качество обслуживания).
ms.assetid: 617ddbf4-212f-4990-93c2-f38f04b035ab
title: Константы LINEEQOSINFO_ (Тспи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423cc6172a1c6c87c1f3bb38929f727a15dad5c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679726"
---
# <a name="lineeqosinfo_-constants"></a><span data-ttu-id="0a5bf-103">\_Константы линикосинфо</span><span class="sxs-lookup"><span data-stu-id="0a5bf-103">LINEEQOSINFO\_ Constants</span></span>

<span data-ttu-id="0a5bf-104">Эти константы используются TSP для обнаружения результатов запроса QoS (качество обслуживания).</span><span class="sxs-lookup"><span data-stu-id="0a5bf-104">These constants are used by a TSP to identify the result of a QoS (Quality of Service) request.</span></span>

<dl> <dt>

<span data-ttu-id="0a5bf-105"><span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**ЛИНИКОСИНФО \_ нокос**</span><span class="sxs-lookup"><span data-stu-id="0a5bf-105"><span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**LINEEQOSINFO\_NOQOS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="0a5bf-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0a5bf-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="0a5bf-107">Качество обслуживания недоступно.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-107">QoS is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a5bf-108"><span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**ЛИНИКОСИНФО \_ адмиссионфаилуре**</span><span class="sxs-lookup"><span data-stu-id="0a5bf-108"><span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**LINEEQOSINFO\_ADMISSIONFAILURE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="0a5bf-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="0a5bf-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="0a5bf-110">Не удалось выполнить запрос QoS.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-110">The QoS request could not be met.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a5bf-111"><span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**ЛИНИКОСИНФО \_ POLICYFAILURE**</span><span class="sxs-lookup"><span data-stu-id="0a5bf-111"><span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**LINEEQOSINFO\_POLICYFAILURE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="0a5bf-112">0x00000003</span><span class="sxs-lookup"><span data-stu-id="0a5bf-112">0x00000003</span></span>
</dt> <dt>



<span data-ttu-id="0a5bf-113">Тип запрошенного качества обслуживания не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-113">The type of QoS requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a5bf-114"><span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**ЛИНИКОСИНФО \_ Общая ошибка**</span><span class="sxs-lookup"><span data-stu-id="0a5bf-114"><span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**LINEEQOSINFO\_GENERICERROR**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="0a5bf-115">0x00000004</span><span class="sxs-lookup"><span data-stu-id="0a5bf-115">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="0a5bf-116">Неуказанная ошибка QoS.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-116">Unspecified QoS error.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a5bf-117">Требования</span><span class="sxs-lookup"><span data-stu-id="0a5bf-117">Requirements</span></span>



| <span data-ttu-id="0a5bf-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0a5bf-118">Requirement</span></span> | <span data-ttu-id="0a5bf-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0a5bf-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0a5bf-120">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="0a5bf-120">TAPI version</span></span><br/> | <span data-ttu-id="0a5bf-121">Требуется TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="0a5bf-121">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="0a5bf-122">Header</span><span class="sxs-lookup"><span data-stu-id="0a5bf-122">Header</span></span><br/>       | <dl> <span data-ttu-id="0a5bf-123"><dt>Тспи. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a5bf-123"><dt>Tspi.h</dt></span></span> </dl> |



 

 




