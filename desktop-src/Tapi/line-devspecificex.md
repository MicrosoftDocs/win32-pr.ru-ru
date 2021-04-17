---
description: Сообщение TAPI LINE \_ девспеЦифицекс отправляется для уведомления приложения о событиях конкретного устройства, происходящих в строке, адресе или вызове. Значение сообщения и интерпретация параметров зависят от устройства.
ms.assetid: 137e91fd-a09e-430c-9d46-8e5be65f03d1
title: Сообщение LINE_DEVSPECIFICEX (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba25047858c641ea4c6cec7d15ba06df24e8ee39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675939"
---
# <a name="line_devspecificex-message"></a><span data-ttu-id="1d866-104">Строка \_ сообщения девспеЦифицекс</span><span class="sxs-lookup"><span data-stu-id="1d866-104">LINE\_DEVSPECIFICEX message</span></span>

<span data-ttu-id="1d866-105">Сообщение TAPI **Line \_ девспеЦифицекс** отправляется для уведомления приложения о событиях конкретного устройства, происходящих в строке, адресе или вызове.</span><span class="sxs-lookup"><span data-stu-id="1d866-105">The TAPI **LINE\_DEVSPECIFICEX** message is sent to notify the application about device-specific events occurring on a line, address, or call.</span></span> <span data-ttu-id="1d866-106">Значение сообщения и интерпретация параметров зависят от устройства.</span><span class="sxs-lookup"><span data-stu-id="1d866-106">The meaning of the message and the interpretation of the parameters are device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="1d866-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d866-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d866-108">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="1d866-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="1d866-109">Обработчик для линейного устройства или вызова.</span><span class="sxs-lookup"><span data-stu-id="1d866-109">A handle to either a line device or call.</span></span> <span data-ttu-id="1d866-110">Этот параметр относится к конкретному устройству.</span><span class="sxs-lookup"><span data-stu-id="1d866-110">This parameter is device specific.</span></span>

</dd> <dt>

<span data-ttu-id="1d866-111">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="1d866-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="1d866-112">Экземпляр обратного вызова, указанный при открытии строки.</span><span class="sxs-lookup"><span data-stu-id="1d866-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="1d866-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="1d866-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="1d866-114">Зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="1d866-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="1d866-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="1d866-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="1d866-116">Зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="1d866-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="1d866-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="1d866-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="1d866-118">Зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="1d866-118">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d866-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d866-119">Return value</span></span>

<span data-ttu-id="1d866-120">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="1d866-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d866-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d866-121">Remarks</span></span>

<span data-ttu-id="1d866-122">Сообщение **Line \_ девспеЦифицекс** используется поставщиком услуг в сочетании с функцией [**линедевспеЦифик**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) .</span><span class="sxs-lookup"><span data-stu-id="1d866-122">The **LINE\_DEVSPECIFICEX** message is used by a service provider in conjunction with the [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) function.</span></span> <span data-ttu-id="1d866-123">Его значение зависит от конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="1d866-123">Its meaning is device specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d866-124">Требования</span><span class="sxs-lookup"><span data-stu-id="1d866-124">Requirements</span></span>



| <span data-ttu-id="1d866-125">Требование</span><span class="sxs-lookup"><span data-stu-id="1d866-125">Requirement</span></span> | <span data-ttu-id="1d866-126">Значение</span><span class="sxs-lookup"><span data-stu-id="1d866-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1d866-127">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="1d866-127">TAPI version</span></span><br/> | <span data-ttu-id="1d866-128">Требуется TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="1d866-128">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="1d866-129">Header</span><span class="sxs-lookup"><span data-stu-id="1d866-129">Header</span></span><br/>       | <dl> <span data-ttu-id="1d866-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d866-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




