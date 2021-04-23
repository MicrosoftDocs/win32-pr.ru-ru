---
description: Сообщение TAPI LINE \_ девспеЦификфеатуре отправляется для уведомления приложения о событиях конкретного устройства, происходящих в строке, адресе или вызове. Значение сообщения и интерпретация параметров зависят от устройства.
ms.assetid: 5f1a4da2-1a2a-4a18-8a69-82d27ddca9cf
title: Сообщение LINE_DEVSPECIFICFEATURE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d45f91f4b3d45b52a345827e6535b054e9cf2c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689491"
---
# <a name="line_devspecificfeature-message"></a><span data-ttu-id="43424-104">Строка \_ сообщения девспеЦификфеатуре</span><span class="sxs-lookup"><span data-stu-id="43424-104">LINE\_DEVSPECIFICFEATURE message</span></span>

<span data-ttu-id="43424-105">Сообщение TAPI **Line \_ девспеЦификфеатуре** отправляется для уведомления приложения о событиях конкретного устройства, происходящих в строке, адресе или вызове.</span><span class="sxs-lookup"><span data-stu-id="43424-105">The TAPI **LINE\_DEVSPECIFICFEATURE** message is sent to notify the application about device-specific events occurring on a line, address, or call.</span></span> <span data-ttu-id="43424-106">Значение сообщения и интерпретация параметров зависят от устройства.</span><span class="sxs-lookup"><span data-stu-id="43424-106">The meaning of the message and the interpretation of the parameters are device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="43424-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="43424-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43424-108">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="43424-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="43424-109">Обработчик для линейного устройства или вызова.</span><span class="sxs-lookup"><span data-stu-id="43424-109">A handle to either a line device or call.</span></span> <span data-ttu-id="43424-110">Это зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="43424-110">This is device specific.</span></span>

</dd> <dt>

<span data-ttu-id="43424-111">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="43424-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="43424-112">Экземпляр обратного вызова, указанный при открытии строки.</span><span class="sxs-lookup"><span data-stu-id="43424-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="43424-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="43424-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="43424-114">Зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="43424-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="43424-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="43424-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="43424-116">Зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="43424-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="43424-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="43424-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="43424-118">Зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="43424-118">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43424-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43424-119">Return value</span></span>

<span data-ttu-id="43424-120">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="43424-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="43424-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43424-121">Remarks</span></span>

<span data-ttu-id="43424-122">Сообщение **Line \_ девспеЦификфеатуре** используется поставщиком услуг в сочетании с функцией [**линедевспеЦификфеатуре**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) .</span><span class="sxs-lookup"><span data-stu-id="43424-122">The **LINE\_DEVSPECIFICFEATURE** message is used by a service provider in conjunction with the [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) function.</span></span> <span data-ttu-id="43424-123">Его значение зависит от конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="43424-123">Its meaning is device specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="43424-124">Требования</span><span class="sxs-lookup"><span data-stu-id="43424-124">Requirements</span></span>



| <span data-ttu-id="43424-125">Требование</span><span class="sxs-lookup"><span data-stu-id="43424-125">Requirement</span></span> | <span data-ttu-id="43424-126">Значение</span><span class="sxs-lookup"><span data-stu-id="43424-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="43424-127">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="43424-127">TAPI version</span></span><br/> | <span data-ttu-id="43424-128">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="43424-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="43424-129">Header</span><span class="sxs-lookup"><span data-stu-id="43424-129">Header</span></span><br/>       | <dl> <span data-ttu-id="43424-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="43424-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




