---
description: Возвращает тип шины ввода-вывода, используемой выходными данными видео.
ms.assetid: 1aff4c81-ffa0-4116-b7ea-60b1b83042df
title: OPM_GET_ADAPTER_BUS_TYPE (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde3611eb00977670c59c4326f793c1cb9037fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711434"
---
# <a name="opm_get_adapter_bus_type"></a><span data-ttu-id="a4fef-103">ОПМ \_ получить \_ \_ Тип шины \_ адаптера</span><span class="sxs-lookup"><span data-stu-id="a4fef-103">OPM\_GET\_ADAPTER\_BUS\_TYPE</span></span>

<span data-ttu-id="a4fef-104">Возвращает тип шины ввода-вывода, используемой выходными данными видео.</span><span class="sxs-lookup"><span data-stu-id="a4fef-104">Returns the type of I/O bus used by the video output.</span></span>



| <span data-ttu-id="a4fef-105">Требование</span><span class="sxs-lookup"><span data-stu-id="a4fef-105">Requirement</span></span> | <span data-ttu-id="a4fef-106">Значение</span><span class="sxs-lookup"><span data-stu-id="a4fef-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="a4fef-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="a4fef-107">Request GUID</span></span> | <span data-ttu-id="a4fef-108">ОПМ \_ получить \_ \_ Тип шины \_ адаптера</span><span class="sxs-lookup"><span data-stu-id="a4fef-108">OPM\_GET\_ADAPTER\_BUS\_TYPE</span></span>                                                |
| <span data-ttu-id="a4fef-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a4fef-109">Input data</span></span>   | <span data-ttu-id="a4fef-110">Нет</span><span class="sxs-lookup"><span data-stu-id="a4fef-110">None</span></span>                                                                        |
| <span data-ttu-id="a4fef-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="a4fef-111">Return data</span></span>  | <span data-ttu-id="a4fef-112">[**\_ Стандартная \_ информационная структура ОПМ**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="a4fef-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a4fef-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4fef-113">Remarks</span></span>

<span data-ttu-id="a4fef-114">Тип шины возвращается в элементе **улинформатион** [**\_ \_ информационной структуры ОПМ Standard**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="a4fef-114">The bus type is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="a4fef-115">Значение представляет собой побитовое **или** для [**флагов типа шины ОПМ**](opm-bus-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a4fef-115">The value is a bitwise **OR** of [**OPM Bus Type Flags**](opm-bus-type-flags.md).</span></span>

<span data-ttu-id="a4fef-116">Этот запрос эквивалентен \_ запросу дксва коппкуерибусдата, используемому в сертифицированном протоколе защиты выходных данных (Копп).</span><span class="sxs-lookup"><span data-stu-id="a4fef-116">This query is equivalent to the DXVA\_COPPQueryBusData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4fef-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a4fef-117">Requirements</span></span>



| <span data-ttu-id="a4fef-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a4fef-118">Requirement</span></span> | <span data-ttu-id="a4fef-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a4fef-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a4fef-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4fef-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a4fef-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4fef-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a4fef-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4fef-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a4fef-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a4fef-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a4fef-124">Header</span><span class="sxs-lookup"><span data-stu-id="a4fef-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4fef-125"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4fef-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4fef-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4fef-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4fef-127">**Иопмвидеуутпут:: Коппкомпатиблежетинформатион**</span><span class="sxs-lookup"><span data-stu-id="a4fef-127">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="a4fef-128">**Иопмвидеуутпут:: о.**</span><span class="sxs-lookup"><span data-stu-id="a4fef-128">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="a4fef-129">Запросы состояния ОПМ</span><span class="sxs-lookup"><span data-stu-id="a4fef-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




