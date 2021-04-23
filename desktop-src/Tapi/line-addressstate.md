---
description: Сообщение TAPI LINE \_ аддрессстате отправляется при изменении состояния адреса в строке, открытой в настоящий момент приложением. Приложение может вызвать Линежетаддрессстатус, чтобы определить текущее состояние адреса.
ms.assetid: af211fa1-79f8-49ac-a1d8-b62981f50519
title: Сообщение LINE_ADDRESSSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d85b42f6957487ff24706485bd09d1d47880fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675273"
---
# <a name="line_addressstate-message"></a><span data-ttu-id="43d0f-104">Строка \_ сообщения аддрессстате</span><span class="sxs-lookup"><span data-stu-id="43d0f-104">LINE\_ADDRESSSTATE message</span></span>

<span data-ttu-id="43d0f-105">Сообщение TAPI **Line \_ аддрессстате** отправляется при изменении состояния адреса в строке, открытой в настоящий момент приложением.</span><span class="sxs-lookup"><span data-stu-id="43d0f-105">The TAPI **LINE\_ADDRESSSTATE** message is sent when the status of an address changes on a line that is currently open by the application.</span></span> <span data-ttu-id="43d0f-106">Приложение может вызвать [**линежетаддрессстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) , чтобы определить текущее состояние адреса.</span><span class="sxs-lookup"><span data-stu-id="43d0f-106">The application can invoke [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) to determine the current status of the address.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="43d0f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="43d0f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43d0f-108">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="43d0f-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="43d0f-109">Маркер устройства линии.</span><span class="sxs-lookup"><span data-stu-id="43d0f-109">A handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="43d0f-110">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="43d0f-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="43d0f-111">Экземпляр обратного вызова, указанный при открытии строки.</span><span class="sxs-lookup"><span data-stu-id="43d0f-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="43d0f-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="43d0f-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="43d0f-113">Идентификатор адреса, который изменил состояние.</span><span class="sxs-lookup"><span data-stu-id="43d0f-113">The address identifier of the address that changed status.</span></span>

</dd> <dt>

<span data-ttu-id="43d0f-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="43d0f-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="43d0f-115">Состояние адреса, которое было изменено.</span><span class="sxs-lookup"><span data-stu-id="43d0f-115">The address state that changed.</span></span> <span data-ttu-id="43d0f-116">Может быть одной или несколькими [**\_ константами линеаддрессстате**](lineaddressstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="43d0f-116">Can be one or more of the [**LINEADDRESSSTATE\_ constants**](lineaddressstate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="43d0f-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="43d0f-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="43d0f-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="43d0f-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43d0f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43d0f-119">Return value</span></span>

<span data-ttu-id="43d0f-120">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="43d0f-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="43d0f-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43d0f-121">Remarks</span></span>

<span data-ttu-id="43d0f-122">Сообщение **Line \_ аддрессстате** отправляется в любое приложение, которое открыло это устройство и включило это сообщение.</span><span class="sxs-lookup"><span data-stu-id="43d0f-122">The **LINE\_ADDRESSSTATE** message is sent to any application that has opened the line device and that has enabled this message.</span></span> <span data-ttu-id="43d0f-123">Отправка этого сообщения для различных элементов состояния может контролироваться и запрашиваться с помощью [**линежетстатусмессажес**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) и [**линесетстатусмессажес**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="43d0f-123">The sending of this message for the various status items can be controlled and queried using [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) and [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span> <span data-ttu-id="43d0f-124">По умолчанию отчеты о состоянии адреса отключены.</span><span class="sxs-lookup"><span data-stu-id="43d0f-124">By default, address status reporting is disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="43d0f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="43d0f-125">Requirements</span></span>



| <span data-ttu-id="43d0f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="43d0f-126">Requirement</span></span> | <span data-ttu-id="43d0f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="43d0f-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="43d0f-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="43d0f-128">TAPI version</span></span><br/> | <span data-ttu-id="43d0f-129">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="43d0f-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="43d0f-130">Header</span><span class="sxs-lookup"><span data-stu-id="43d0f-130">Header</span></span><br/>       | <dl> <span data-ttu-id="43d0f-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="43d0f-131"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43d0f-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43d0f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43d0f-133">**линеаддресскапс**</span><span class="sxs-lookup"><span data-stu-id="43d0f-133">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="43d0f-134">**линежетаддресскапс**</span><span class="sxs-lookup"><span data-stu-id="43d0f-134">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[<span data-ttu-id="43d0f-135">**линежетаддрессстатус**</span><span class="sxs-lookup"><span data-stu-id="43d0f-135">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[<span data-ttu-id="43d0f-136">**линежетстатусмессажес**</span><span class="sxs-lookup"><span data-stu-id="43d0f-136">**lineGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages)
</dt> <dt>

[<span data-ttu-id="43d0f-137">**линесетстатусмессажес**</span><span class="sxs-lookup"><span data-stu-id="43d0f-137">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> </dl>

 

 




