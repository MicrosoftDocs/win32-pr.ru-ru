---
description: Сообщение ТСПИ LINE \_ каллдевспеЦифик отправляется в функцию обратного вызова линивент, чтобы УВЕДОМЛЯТЬ TAPI о событиях конкретного устройства, происходящих при вызове.
ms.assetid: accd753a-3be0-4c7d-bbc7-d294d1381144
title: Сообщение LINE_CALLDEVSPECIFIC (Тспи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a48bf8a54a1f326fe7bb27c82349e5575c8bbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675495"
---
# <a name="line_calldevspecific-message"></a><span data-ttu-id="90db9-103">Строка \_ сообщения каллдевспеЦифик</span><span class="sxs-lookup"><span data-stu-id="90db9-103">LINE\_CALLDEVSPECIFIC message</span></span>

<span data-ttu-id="90db9-104">Сообщение ТСПИ **Line \_ каллдевспеЦифик** отправляется в функцию обратного вызова [**ЛИНИВЕНТ**](/windows/win32/api/tspi/nc-tspi-lineevent) , чтобы уведомлять TAPI о событиях конкретного устройства, происходящих при вызове.</span><span class="sxs-lookup"><span data-stu-id="90db9-104">The TSPI **LINE\_CALLDEVSPECIFIC** message is sent to the [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) callback function to notify TAPI about device-specific events occurring on a call.</span></span> <span data-ttu-id="90db9-105">Значение сообщения и интерпретация параметров *dwParam1* через *dwParam3* зависят от устройства.</span><span class="sxs-lookup"><span data-stu-id="90db9-105">The meaning of the message and the interpretation of the *dwParam1* through *dwParam3* parameters is device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="90db9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="90db9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90db9-107">*хтлине*</span><span class="sxs-lookup"><span data-stu-id="90db9-107">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="90db9-108">Обработчик непрозрачного объекта TAPI для устройства линии.</span><span class="sxs-lookup"><span data-stu-id="90db9-108">The TAPI opaque object handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="90db9-109">*хткалл*</span><span class="sxs-lookup"><span data-stu-id="90db9-109">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="90db9-110">Непрозрачный объект TAPI для устройства вызова.</span><span class="sxs-lookup"><span data-stu-id="90db9-110">The TAPI opaque object handle to the call device.</span></span>

</dd> <dt>

<span data-ttu-id="90db9-111">*двмсг*</span><span class="sxs-lookup"><span data-stu-id="90db9-111">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="90db9-112">Строка значения \_ каллдевспеЦифик.</span><span class="sxs-lookup"><span data-stu-id="90db9-112">The value LINE\_CALLDEVSPECIFIC.</span></span>

</dd> <dt>

<span data-ttu-id="90db9-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="90db9-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="90db9-114">Зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="90db9-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="90db9-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="90db9-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="90db9-116">Зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="90db9-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="90db9-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="90db9-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="90db9-118">Зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="90db9-118">Device specific.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90db9-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90db9-119">Remarks</span></span>

<span data-ttu-id="90db9-120">Сообщение **Line \_ каллдевспеЦифик** используется поставщиком услуг совместно с функцией [**тспи \_ линедевспеЦифик**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) .</span><span class="sxs-lookup"><span data-stu-id="90db9-120">The **LINE\_CALLDEVSPECIFIC** message is used by a service provider in conjunction with the [**TSPI\_lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) function.</span></span> <span data-ttu-id="90db9-121">Его значение зависит от конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="90db9-121">Its meaning is device specific.</span></span>

<span data-ttu-id="90db9-122">TAPI отправляет в приложения сообщение [**Line \_ девспеЦифик**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) в ответ на получение этого сообщения от поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="90db9-122">TAPI sends the [**LINE\_DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) message to applications in response to receiving this message from a service provider.</span></span> <span data-ttu-id="90db9-123">Параметры *хтлине* и *хткалл* преобразуются в соответствующий *хкалл* в качестве параметра *хдевице* на уровне TAPI.</span><span class="sxs-lookup"><span data-stu-id="90db9-123">The *htLine* and *htCall* parameters are translated to the appropriate *hCall* as the *hDevice* parameter at the TAPI level.</span></span> <span data-ttu-id="90db9-124">Параметры *dwParam1*, *dwParam2* и *dwParam3* передаются в неизмененном виде.</span><span class="sxs-lookup"><span data-stu-id="90db9-124">The *dwParam1*, *dwParam2*, and *dwParam3* parameters are passed through unmodified.</span></span>

<span data-ttu-id="90db9-125">Непосредственно соответствующего сообщения на уровне TAPI нет, хотя это сообщение очень похоже на [**Line \_ девспеЦифик**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="90db9-125">There is no directly corresponding message at the TAPI level, although this message is very similar to [**LINE\_DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)).</span></span> <span data-ttu-id="90db9-126">На уровне ТСПИ сообщения, относящиеся к конкретному устройству, разбиваются между этими событиями в строках и адресах, а также событиями отчетов при вызовах.</span><span class="sxs-lookup"><span data-stu-id="90db9-126">At the TSPI level, the device-specific messages are split between those reporting events on lines and addresses, and those reporting events on calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="90db9-127">Требования</span><span class="sxs-lookup"><span data-stu-id="90db9-127">Requirements</span></span>



| <span data-ttu-id="90db9-128">Требование</span><span class="sxs-lookup"><span data-stu-id="90db9-128">Requirement</span></span> | <span data-ttu-id="90db9-129">Значение</span><span class="sxs-lookup"><span data-stu-id="90db9-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="90db9-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="90db9-130">TAPI version</span></span><br/> | <span data-ttu-id="90db9-131">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="90db9-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="90db9-132">Header</span><span class="sxs-lookup"><span data-stu-id="90db9-132">Header</span></span><br/>       | <dl> <span data-ttu-id="90db9-133"><dt>Тспи. h</dt></span><span class="sxs-lookup"><span data-stu-id="90db9-133"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90db9-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90db9-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="90db9-135">[**Строка \_ девспеЦифик**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90db9-135">[**LINE\_DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="90db9-136">**линивент**</span><span class="sxs-lookup"><span data-stu-id="90db9-136">**LINEEVENT**</span></span>](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> <dt>

[<span data-ttu-id="90db9-137">**ТСПИ \_ линедевспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="90db9-137">**TSPI\_lineDevSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
</dt> </dl>

 

