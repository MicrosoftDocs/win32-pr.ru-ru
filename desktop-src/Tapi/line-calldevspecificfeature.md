---
description: Сообщение ТСПИ LINE \_ каллдевспеЦификфеатуре отправляется в функцию обратного вызова линивент, чтобы УВЕДОМЛЯТЬ TAPI о событиях конкретного устройства, происходящих в строке или адресе.
ms.assetid: bf470f5b-f7e5-4f98-9b60-12da599ebf26
title: Сообщение LINE_CALLDEVSPECIFICFEATURE (Тспи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2891f019035f53be4dbc0a40de429e5c0d9dc567
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689282"
---
# <a name="line_calldevspecificfeature-message"></a><span data-ttu-id="75f40-103">Строка \_ сообщения каллдевспеЦификфеатуре</span><span class="sxs-lookup"><span data-stu-id="75f40-103">LINE\_CALLDEVSPECIFICFEATURE message</span></span>

<span data-ttu-id="75f40-104">Сообщение ТСПИ **Line \_ каллдевспеЦификфеатуре** отправляется в функцию обратного вызова [**ЛИНИВЕНТ**](/windows/win32/api/tspi/nc-tspi-lineevent) , чтобы уведомлять TAPI о событиях конкретного устройства, происходящих в строке или адресе.</span><span class="sxs-lookup"><span data-stu-id="75f40-104">The TSPI **LINE\_CALLDEVSPECIFICFEATURE** message is sent to the [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) callback function to notify TAPI about device-specific events occurring on a line or address.</span></span> <span data-ttu-id="75f40-105">Значение сообщения и интерпретация параметров *dwParam1* через *dwParam3* зависят от устройства.</span><span class="sxs-lookup"><span data-stu-id="75f40-105">The meaning of the message and the interpretation of the *dwParam1* through *dwParam3* parameters is device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="75f40-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="75f40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75f40-107">*хтлине*</span><span class="sxs-lookup"><span data-stu-id="75f40-107">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="75f40-108">Обработчик непрозрачного объекта TAPI для устройства линии.</span><span class="sxs-lookup"><span data-stu-id="75f40-108">The TAPI opaque object handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="75f40-109">*хткалл*</span><span class="sxs-lookup"><span data-stu-id="75f40-109">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="75f40-110">Непрозрачный объект TAPI для устройства вызова.</span><span class="sxs-lookup"><span data-stu-id="75f40-110">The TAPI opaque object handle to the call device.</span></span>

</dd> <dt>

<span data-ttu-id="75f40-111">*двмсг*</span><span class="sxs-lookup"><span data-stu-id="75f40-111">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="75f40-112">Строка значения \_ каллдевспеЦификфеатуре.</span><span class="sxs-lookup"><span data-stu-id="75f40-112">The value LINE\_CALLDEVSPECIFICFEATURE.</span></span>

</dd> <dt>

<span data-ttu-id="75f40-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="75f40-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="75f40-114">Зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="75f40-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="75f40-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="75f40-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="75f40-116">Зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="75f40-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="75f40-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="75f40-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="75f40-118">Зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="75f40-118">Device specific.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75f40-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="75f40-119">Remarks</span></span>

<span data-ttu-id="75f40-120">Сообщение **Line \_ каллдевспеЦификфеатуре** используется поставщиком услуг совместно с функцией [**тспи \_ линедевспеЦификфеатуре**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) .</span><span class="sxs-lookup"><span data-stu-id="75f40-120">The **LINE\_CALLDEVSPECIFICFEATURE** message is used by a service provider in conjunction with the [**TSPI\_lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) function.</span></span> <span data-ttu-id="75f40-121">Его значение зависит от конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="75f40-121">Its meaning is device specific.</span></span>

<span data-ttu-id="75f40-122">TAPI отправляет в приложения сообщение [**Line \_ девспеЦификфеатуре**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) в ответ на получение этого сообщения от поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="75f40-122">TAPI sends the [**LINE\_DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) message to applications in response to receiving this message from a service provider.</span></span> <span data-ttu-id="75f40-123">Параметры *хтлине* и *хткалл* преобразуются в соответствующий *хкалл* в качестве параметра *хдевице* на уровне TAPI.</span><span class="sxs-lookup"><span data-stu-id="75f40-123">The *htLine* and *htCall* parameters are translated to the appropriate *hCall* as the *hDevice* parameter at the TAPI level.</span></span> <span data-ttu-id="75f40-124">Параметры *dwParam1*, *dwParam2* и *dwParam3* передаются в неизмененном виде.</span><span class="sxs-lookup"><span data-stu-id="75f40-124">The *dwParam1*, *dwParam2*, and *dwParam3* parameters are passed through unmodified.</span></span>

<span data-ttu-id="75f40-125">Непосредственно соответствующего сообщения на уровне TAPI нет, хотя это сообщение очень похоже на LINE \_ девспеЦификфеатуре.</span><span class="sxs-lookup"><span data-stu-id="75f40-125">There is no directly corresponding message at the TAPI level, although this message is very similar to LINE\_DEVSPECIFICFEATURE.</span></span> <span data-ttu-id="75f40-126">На уровне ТСПИ сообщения компонента, относящиеся к конкретному устройству, разбиваются между этими событиями в строках и адресах, а также событиями отчетов при вызовах.</span><span class="sxs-lookup"><span data-stu-id="75f40-126">At the TSPI level, the device-specific feature messages are split between those reporting events on lines and addresses, and those reporting events on calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="75f40-127">Требования</span><span class="sxs-lookup"><span data-stu-id="75f40-127">Requirements</span></span>



| <span data-ttu-id="75f40-128">Требование</span><span class="sxs-lookup"><span data-stu-id="75f40-128">Requirement</span></span> | <span data-ttu-id="75f40-129">Значение</span><span class="sxs-lookup"><span data-stu-id="75f40-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="75f40-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="75f40-130">TAPI version</span></span><br/> | <span data-ttu-id="75f40-131">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="75f40-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="75f40-132">Header</span><span class="sxs-lookup"><span data-stu-id="75f40-132">Header</span></span><br/>       | <dl> <span data-ttu-id="75f40-133"><dt>Тспи. h</dt></span><span class="sxs-lookup"><span data-stu-id="75f40-133"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75f40-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75f40-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="75f40-135">[**Строка \_ девспеЦификфеатуре**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="75f40-135">[**LINE\_DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="75f40-136">**ТСПИ \_ линедевспеЦификфеатуре**</span><span class="sxs-lookup"><span data-stu-id="75f40-136">**TSPI\_lineDevSpecificFeature**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
</dt> </dl>

 

