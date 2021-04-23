---
description: Запрашивает, поддерживает ли соединитель цифрового видео DVI версии 1,1 или более поздней.
ms.assetid: b6c450c0-e97f-472d-ae09-fa1e062aeb9e
title: OPM_GET_DVI_CHARACTERISTICS (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6f996b0397db509a45af6e243359c581df333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080429"
---
# <a name="opm_get_dvi_characteristics"></a><span data-ttu-id="31d3a-103">ОПМ \_ Получение \_ \_ характеристик DVI</span><span class="sxs-lookup"><span data-stu-id="31d3a-103">OPM\_GET\_DVI\_CHARACTERISTICS</span></span>

<span data-ttu-id="31d3a-104">Запрашивает, поддерживает ли соединитель цифрового видео DVI версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="31d3a-104">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>



| <span data-ttu-id="31d3a-105">Требование</span><span class="sxs-lookup"><span data-stu-id="31d3a-105">Requirement</span></span> | <span data-ttu-id="31d3a-106">Значение</span><span class="sxs-lookup"><span data-stu-id="31d3a-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="31d3a-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="31d3a-107">Request GUID</span></span> | <span data-ttu-id="31d3a-108">ОПМ \_ Получение \_ \_ характеристик DVI</span><span class="sxs-lookup"><span data-stu-id="31d3a-108">OPM\_GET\_DVI\_CHARACTERISTICS</span></span>                                              |
| <span data-ttu-id="31d3a-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="31d3a-109">Input data</span></span>   | <span data-ttu-id="31d3a-110">Нет</span><span class="sxs-lookup"><span data-stu-id="31d3a-110">None</span></span>                                                                        |
| <span data-ttu-id="31d3a-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="31d3a-111">Return data</span></span>  | <span data-ttu-id="31d3a-112">[**\_ Стандартная \_ информационная структура ОПМ**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="31d3a-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="31d3a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31d3a-113">Remarks</span></span>

<span data-ttu-id="31d3a-114">Если этот запрос выполнен, элемент **улинформатион** в [**информационной структуре ОПМ \_ Standard \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) содержит одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="31d3a-114">If this query succeeds, the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure contains one of the following values.</span></span>



| <span data-ttu-id="31d3a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="31d3a-115">Value</span></span>                                     | <span data-ttu-id="31d3a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="31d3a-116">Description</span></span>               |
|-------------------------------------------|---------------------------|
| <span data-ttu-id="31d3a-117">ОПМ \_ DVI, \_ характеристика \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31d3a-117">OPM\_DVI\_CHARACTERISTIC\_1\_0</span></span>            | <span data-ttu-id="31d3a-118">DVI версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="31d3a-118">DVI version 1.0.</span></span>          |
| <span data-ttu-id="31d3a-119">ОПМ \_ 1 \_ \_ \_ \_ или \_ выше с характеристикой DVI</span><span class="sxs-lookup"><span data-stu-id="31d3a-119">OPM\_DVI\_CHARACTERISTIC\_1\_1\_OR\_ABOVE</span></span> | <span data-ttu-id="31d3a-120">DVI версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="31d3a-120">DVI version 1.1 or later.</span></span> |



 

<span data-ttu-id="31d3a-121">Этот запрос поддерживается только в том случае, если тип физического соединителя — ОПМ, \_ \_ тип \_ DVI.</span><span class="sxs-lookup"><span data-stu-id="31d3a-121">This query is supported only when the physical connector type is OPM\_CONNECTOR\_TYPE\_DVI.</span></span> <span data-ttu-id="31d3a-122">Чтобы получить тип соединителя, отправьте запрос [**\_ \_ \_ типа соединителя ОПМ Get**](opm-get-connector-type.md) .</span><span class="sxs-lookup"><span data-stu-id="31d3a-122">To get the connector type, send the [**OPM\_GET\_CONNECTOR\_TYPE**](opm-get-connector-type.md) query.</span></span>

## <a name="requirements"></a><span data-ttu-id="31d3a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="31d3a-123">Requirements</span></span>



| <span data-ttu-id="31d3a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="31d3a-124">Requirement</span></span> | <span data-ttu-id="31d3a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="31d3a-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="31d3a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31d3a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="31d3a-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="31d3a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="31d3a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31d3a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="31d3a-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="31d3a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="31d3a-130">Header</span><span class="sxs-lookup"><span data-stu-id="31d3a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="31d3a-131"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="31d3a-131"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31d3a-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31d3a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31d3a-133">**Иопмвидеуутпут:: о.**</span><span class="sxs-lookup"><span data-stu-id="31d3a-133">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="31d3a-134">Запросы состояния ОПМ</span><span class="sxs-lookup"><span data-stu-id="31d3a-134">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




