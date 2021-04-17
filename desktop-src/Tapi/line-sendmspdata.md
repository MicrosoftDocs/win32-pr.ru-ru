---
description: Сообщение ТСПИ LINE \_ сендмспдата отправляется, когда поставщику услуг телефонии (TSP) требуется передать сведения поставщику службы мультимедиа (MSP).
ms.assetid: 982f40b3-7758-493c-9d04-6480e3c9e86d
title: Сообщение LINE_SENDMSPDATA (Тспи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce46664be0bc7f312af8b45cc5e06e13a7d91488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685341"
---
# <a name="line_sendmspdata-message"></a><span data-ttu-id="2c41f-103">Строка \_ сообщения сендмспдата</span><span class="sxs-lookup"><span data-stu-id="2c41f-103">LINE\_SENDMSPDATA message</span></span>

<span data-ttu-id="2c41f-104">Сообщение ТСПИ **Line \_ сендмспдата** отправляется, когда поставщику услуг телефонии (TSP) требуется передать сведения поставщику службы мультимедиа (MSP).</span><span class="sxs-lookup"><span data-stu-id="2c41f-104">The TSPI **LINE\_SENDMSPDATA** message is sent when the telephony service provider (TSP) wants to pass information to the media service provider (MSP).</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="2c41f-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c41f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c41f-106">*хтлине*</span><span class="sxs-lookup"><span data-stu-id="2c41f-106">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="2c41f-107">Маркер TAPI для линии.</span><span class="sxs-lookup"><span data-stu-id="2c41f-107">The TAPI handle for the line.</span></span>

</dd> <dt>

<span data-ttu-id="2c41f-108">*хткалл*</span><span class="sxs-lookup"><span data-stu-id="2c41f-108">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="2c41f-109">Маркер TAPI для вызова.</span><span class="sxs-lookup"><span data-stu-id="2c41f-109">The TAPI handle for the call.</span></span>

</dd> <dt>

<span data-ttu-id="2c41f-110">*двмсг*</span><span class="sxs-lookup"><span data-stu-id="2c41f-110">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="2c41f-111">Строка значения \_ сендмспдата.</span><span class="sxs-lookup"><span data-stu-id="2c41f-111">The value LINE\_SENDMSPDATA.</span></span>

</dd> <dt>

<span data-ttu-id="2c41f-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="2c41f-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="2c41f-113">Указывает MSP, который должен получить сообщение.</span><span class="sxs-lookup"><span data-stu-id="2c41f-113">Identifies the MSP that should receive the message.</span></span> <span data-ttu-id="2c41f-114">Если значение равно 0, сообщение будет отправлено всем MSP.</span><span class="sxs-lookup"><span data-stu-id="2c41f-114">If 0, the message will be sent to all MSPs.</span></span> <span data-ttu-id="2c41f-115">Это обработчик, который передается функции [**тспи \_ линекреатемспинстанце**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) .</span><span class="sxs-lookup"><span data-stu-id="2c41f-115">This is the handle that is passed to the [**TSPI\_LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) function.</span></span>

</dd> <dt>

<span data-ttu-id="2c41f-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="2c41f-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="2c41f-117">Буфер для передачи в MSP.</span><span class="sxs-lookup"><span data-stu-id="2c41f-117">The buffer to pass to the MSP.</span></span> <span data-ttu-id="2c41f-118">Этот буфер не интерпретируется интерфейсом TAPI.</span><span class="sxs-lookup"><span data-stu-id="2c41f-118">The buffer is not interpreted by TAPI.</span></span>

</dd> <dt>

<span data-ttu-id="2c41f-119">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="2c41f-119">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="2c41f-120">Размер (в байтах) буфера в *dwParam2*.</span><span class="sxs-lookup"><span data-stu-id="2c41f-120">The size, in bytes, of the buffer in *dwParam2*.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c41f-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c41f-121">Remarks</span></span>

<span data-ttu-id="2c41f-122">Чтобы это сообщение работало, поставщик услуг должен согласовать TAPI версии 3,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="2c41f-122">The service provider must negotiate a TAPI version 3.0 or later for this message to operate.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c41f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="2c41f-123">Requirements</span></span>



| <span data-ttu-id="2c41f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="2c41f-124">Requirement</span></span> | <span data-ttu-id="2c41f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="2c41f-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2c41f-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="2c41f-126">TAPI version</span></span><br/> | <span data-ttu-id="2c41f-127">Требуется TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="2c41f-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="2c41f-128">Header</span><span class="sxs-lookup"><span data-stu-id="2c41f-128">Header</span></span><br/>       | <dl> <span data-ttu-id="2c41f-129"><dt>Тспи. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c41f-129"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c41f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c41f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c41f-131">Сведения о поставщике службы мультимедиа (MSP)</span><span class="sxs-lookup"><span data-stu-id="2c41f-131">About The Media Service Provider (MSP)</span></span>](./about-the-media-service-provider-msp-.md)
</dt> <dt>

[<span data-ttu-id="2c41f-132">**ТСПИ \_ линемспидентифи**</span><span class="sxs-lookup"><span data-stu-id="2c41f-132">**TSPI\_lineMSPIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
</dt> <dt>

[<span data-ttu-id="2c41f-133">**ТСПИ \_ линекреатемспинстанце**</span><span class="sxs-lookup"><span data-stu-id="2c41f-133">**TSPI\_LineCreateMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
</dt> <dt>

[<span data-ttu-id="2c41f-134">**ТСПИ \_ линеклосемспинстанце**</span><span class="sxs-lookup"><span data-stu-id="2c41f-134">**TSPI\_lineCloseMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
</dt> <dt>

[<span data-ttu-id="2c41f-135">**ТСПИ \_ линереЦиевемспдата**</span><span class="sxs-lookup"><span data-stu-id="2c41f-135">**TSPI\_lineRecieveMSPData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
</dt> <dt>

[<span data-ttu-id="2c41f-136">**линедевкапс**</span><span class="sxs-lookup"><span data-stu-id="2c41f-136">**LINEDEVCAPS**</span></span>](/windows/win32/api/tapi/ns-tapi-linedevcaps)
</dt> </dl>

 

