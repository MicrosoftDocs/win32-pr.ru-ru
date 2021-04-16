---
description: Сообщение TAPI LINE \_ девспеЦифик отправляется для уведомления приложения о событиях конкретного устройства, происходящих в строке, адресе или вызове. Значение сообщения и интерпретация параметров зависят от устройства.
ms.assetid: 6a58e77b-6ee2-4d2d-aca2-71b239f6a1dc
title: Сообщение LINE_DEVSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91907b10c0176258648fa165bbeb922a61a402ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689082"
---
# <a name="line_devspecific-message"></a><span data-ttu-id="d412f-104">Строка \_ сообщения девспеЦифик</span><span class="sxs-lookup"><span data-stu-id="d412f-104">LINE\_DEVSPECIFIC message</span></span>

<span data-ttu-id="d412f-105">Сообщение TAPI **Line \_ девспеЦифик** отправляется для уведомления приложения о событиях конкретного устройства, происходящих в строке, адресе или вызове.</span><span class="sxs-lookup"><span data-stu-id="d412f-105">The TAPI **LINE\_DEVSPECIFIC** message is sent to notify the application about device-specific events occurring on a line, address, or call.</span></span> <span data-ttu-id="d412f-106">Значение сообщения и интерпретация параметров зависят от устройства.</span><span class="sxs-lookup"><span data-stu-id="d412f-106">The meaning of the message and the interpretation of the parameters are device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="d412f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d412f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d412f-108">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="d412f-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="d412f-109">Обработчик для линейного устройства или вызова.</span><span class="sxs-lookup"><span data-stu-id="d412f-109">A handle to either a line device or call.</span></span> <span data-ttu-id="d412f-110">Это зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="d412f-110">This is device specific.</span></span>

</dd> <dt>

<span data-ttu-id="d412f-111">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="d412f-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="d412f-112">Экземпляр обратного вызова, указанный при открытии строки.</span><span class="sxs-lookup"><span data-stu-id="d412f-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="d412f-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="d412f-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="d412f-114">Зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="d412f-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="d412f-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="d412f-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="d412f-116">Зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="d412f-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="d412f-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="d412f-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="d412f-118">Зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="d412f-118">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d412f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d412f-119">Return value</span></span>

<span data-ttu-id="d412f-120">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="d412f-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d412f-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d412f-121">Remarks</span></span>

<span data-ttu-id="d412f-122">Сообщение **Line \_ девспеЦифик** используется поставщиком услуг в сочетании с функцией [**линедевспеЦифик**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) .</span><span class="sxs-lookup"><span data-stu-id="d412f-122">The **LINE\_DEVSPECIFIC** message is used by a service provider in conjunction with the [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) function.</span></span> <span data-ttu-id="d412f-123">Его значение зависит от конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="d412f-123">Its meaning is device specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="d412f-124">Требования</span><span class="sxs-lookup"><span data-stu-id="d412f-124">Requirements</span></span>



| <span data-ttu-id="d412f-125">Требование</span><span class="sxs-lookup"><span data-stu-id="d412f-125">Requirement</span></span> | <span data-ttu-id="d412f-126">Значение</span><span class="sxs-lookup"><span data-stu-id="d412f-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d412f-127">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="d412f-127">TAPI version</span></span><br/> | <span data-ttu-id="d412f-128">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d412f-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d412f-129">Header</span><span class="sxs-lookup"><span data-stu-id="d412f-129">Header</span></span><br/>       | <dl> <span data-ttu-id="d412f-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d412f-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




