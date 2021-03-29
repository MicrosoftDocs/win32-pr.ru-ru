---
description: Возвращает список механизмов защиты, поддерживаемых соединителем.
ms.assetid: dd4cdd3c-6bb5-4427-827d-f3e909e752e5
title: OPM_GET_SUPPORTED_PROTECTION_TYPES (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc79b33673e34d00914b84165d915baa0d8f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991420"
---
# <a name="opm_get_supported_protection_types"></a><span data-ttu-id="422c7-103">ОПМ \_ получить \_ поддерживаемые \_ \_ типы защиты</span><span class="sxs-lookup"><span data-stu-id="422c7-103">OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES</span></span>

<span data-ttu-id="422c7-104">Возвращает список механизмов защиты, поддерживаемых соединителем.</span><span class="sxs-lookup"><span data-stu-id="422c7-104">Returns the list of protection mechanisms that are supported by the connector.</span></span>



| <span data-ttu-id="422c7-105">Требование</span><span class="sxs-lookup"><span data-stu-id="422c7-105">Requirement</span></span> | <span data-ttu-id="422c7-106">Значение</span><span class="sxs-lookup"><span data-stu-id="422c7-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="422c7-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="422c7-107">Request GUID</span></span> | <span data-ttu-id="422c7-108">ОПМ \_ получить \_ поддерживаемые \_ \_ типы защиты</span><span class="sxs-lookup"><span data-stu-id="422c7-108">OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES</span></span>                                      |
| <span data-ttu-id="422c7-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="422c7-109">Input data</span></span>   | <span data-ttu-id="422c7-110">Нет</span><span class="sxs-lookup"><span data-stu-id="422c7-110">None</span></span>                                                                        |
| <span data-ttu-id="422c7-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="422c7-111">Return data</span></span>  | <span data-ttu-id="422c7-112">[**\_ Стандартная \_ информационная структура ОПМ**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="422c7-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="422c7-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="422c7-113">Remarks</span></span>

<span data-ttu-id="422c7-114">Механизмы защиты возвращаются в элементе **улинформатион** [**\_ \_ информационной структуры ОПМ Standard**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="422c7-114">The protection mechanisms are returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="422c7-115">Значение представляет собой побитовое **или** для [флагов типа защиты ОПМ](opm-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="422c7-115">The value is a bitwise **OR** of [OPM Protection Type Flags](opm-protection-type-flags.md).</span></span>

<span data-ttu-id="422c7-116">Этот запрос эквивалентен \_ запросу дксва коппкуерипротектионтипе, используемому в сертифицированном протоколе защиты выходных данных (Копп).</span><span class="sxs-lookup"><span data-stu-id="422c7-116">This query is equivalent to the DXVA\_COPPQueryProtectionType query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="422c7-117">Требования</span><span class="sxs-lookup"><span data-stu-id="422c7-117">Requirements</span></span>



| <span data-ttu-id="422c7-118">Требование</span><span class="sxs-lookup"><span data-stu-id="422c7-118">Requirement</span></span> | <span data-ttu-id="422c7-119">Значение</span><span class="sxs-lookup"><span data-stu-id="422c7-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="422c7-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="422c7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="422c7-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="422c7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="422c7-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="422c7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="422c7-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="422c7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="422c7-124">Header</span><span class="sxs-lookup"><span data-stu-id="422c7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="422c7-125"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="422c7-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="422c7-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="422c7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="422c7-127">**Иопмвидеуутпут:: Коппкомпатиблежетинформатион**</span><span class="sxs-lookup"><span data-stu-id="422c7-127">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="422c7-128">**Иопмвидеуутпут:: о.**</span><span class="sxs-lookup"><span data-stu-id="422c7-128">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="422c7-129">Запросы состояния ОПМ</span><span class="sxs-lookup"><span data-stu-id="422c7-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




