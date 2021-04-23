---
description: Возвращает тип физического соединителя для выходного видео.
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: OPM_GET_CONNECTOR_TYPE (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a95ca88b079aa93b4c2665fe7aa954eb58cfc1a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263506"
---
# <a name="opm_get_connector_type"></a><span data-ttu-id="0b1e3-103">ОПМ \_ получить \_ \_ Тип соединителя</span><span class="sxs-lookup"><span data-stu-id="0b1e3-103">OPM\_GET\_CONNECTOR\_TYPE</span></span>

<span data-ttu-id="0b1e3-104">Возвращает тип физического соединителя для выходного видео.</span><span class="sxs-lookup"><span data-stu-id="0b1e3-104">Returns the physical connector type of the video output.</span></span>



| <span data-ttu-id="0b1e3-105">Требование</span><span class="sxs-lookup"><span data-stu-id="0b1e3-105">Requirement</span></span> | <span data-ttu-id="0b1e3-106">Значение</span><span class="sxs-lookup"><span data-stu-id="0b1e3-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="0b1e3-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="0b1e3-107">Request GUID</span></span> | <span data-ttu-id="0b1e3-108">ОПМ \_ получить \_ \_ Тип соединителя</span><span class="sxs-lookup"><span data-stu-id="0b1e3-108">OPM\_GET\_CONNECTOR\_TYPE</span></span>                                                   |
| <span data-ttu-id="0b1e3-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0b1e3-109">Input data</span></span>   | <span data-ttu-id="0b1e3-110">Нет</span><span class="sxs-lookup"><span data-stu-id="0b1e3-110">None</span></span>                                                                        |
| <span data-ttu-id="0b1e3-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="0b1e3-111">Return data</span></span>  | <span data-ttu-id="0b1e3-112">[**\_ Стандартная \_ информационная структура ОПМ**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="0b1e3-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0b1e3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b1e3-113">Remarks</span></span>

<span data-ttu-id="0b1e3-114">Тип соединителя возвращается в элементе **улинформатион** [**\_ \_ информационной структуры ОПМ Standard**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="0b1e3-114">The connector type is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="0b1e3-115">Значение **улинформатион** равно одному из типов соединителей, перечисленных в списке [**флагов типа соединителя ОПМ**](opm-connector-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0b1e3-115">The value of **ulInformation** is equal to one of the connector types listed in [**OPM Connector Type Flags**](opm-connector-type-flags.md).</span></span>

<span data-ttu-id="0b1e3-116">В режиме эмуляции Копп тип соединителя может сочетаться с **\_ \_ \_ \_ \_ внутренним флагом типа соединителя ОПМ Копп Compatible** .</span><span class="sxs-lookup"><span data-stu-id="0b1e3-116">In COPP emulation mode, the connector type might be combined with the **OPM\_COPP\_COMPATIBLE\_CONNECTOR\_TYPE\_INTERNAL** flag.</span></span> <span data-ttu-id="0b1e3-117">Используйте побитовое **и** для извлечения типа соединителя:</span><span class="sxs-lookup"><span data-stu-id="0b1e3-117">Use a bitwise **AND** to extract the connector type:</span></span>

`ulInformation & ~OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL`

<span data-ttu-id="0b1e3-118">Приложения должны игнорировать **внутренний флаг \_ \_ \_ \_ типа \_ соединителя ОПМ Копп Compatible** .</span><span class="sxs-lookup"><span data-stu-id="0b1e3-118">Applications should ignore the **OPM\_COPP\_COMPATIBLE\_CONNECTOR\_TYPE\_INTERNAL** flag.</span></span> <span data-ttu-id="0b1e3-119">Дополнительные сведения см. в подразделе "Примечания" [**флагов типа соединителя ОПМ**](opm-connector-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0b1e3-119">For more information, see the Remarks section of [**OPM Connector Type Flags**](opm-connector-type-flags.md).</span></span>

<span data-ttu-id="0b1e3-120">Этот запрос эквивалентен \_ запросу дксва коппкуериконнектортипе, используемому в сертифицированном протоколе защиты выходных данных (Копп).</span><span class="sxs-lookup"><span data-stu-id="0b1e3-120">This query is equivalent to the DXVA\_COPPQueryConnectorType query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b1e3-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0b1e3-121">Requirements</span></span>



| <span data-ttu-id="0b1e3-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0b1e3-122">Requirement</span></span> | <span data-ttu-id="0b1e3-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0b1e3-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0b1e3-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0b1e3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0b1e3-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b1e3-125">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0b1e3-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0b1e3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0b1e3-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0b1e3-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0b1e3-128">Header</span><span class="sxs-lookup"><span data-stu-id="0b1e3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b1e3-129"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b1e3-129"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b1e3-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b1e3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b1e3-131">**Иопмвидеуутпут:: Коппкомпатиблежетинформатион**</span><span class="sxs-lookup"><span data-stu-id="0b1e3-131">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="0b1e3-132">**Иопмвидеуутпут:: о.**</span><span class="sxs-lookup"><span data-stu-id="0b1e3-132">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="0b1e3-133">Запросы состояния ОПМ</span><span class="sxs-lookup"><span data-stu-id="0b1e3-133">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




