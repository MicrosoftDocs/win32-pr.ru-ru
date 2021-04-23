---
description: TAPI отправляет в \_ приложение сообщение Phone девспеЦифик, чтобы уведомить приложение о событиях конкретного устройства, происходящих на телефоне. Значение сообщения и интерпретация параметров определяются реализацией.
ms.assetid: e3e803dd-b041-48b7-9acf-a89989370204
title: Сообщение PHONE_DEVSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c817f273a49fdcda36995cec335811fb06c8a917
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674812"
---
# <a name="phone_devspecific-message"></a><span data-ttu-id="2d819-104">\_Сообщение ДЕВСПЕЦИФИК телефона</span><span class="sxs-lookup"><span data-stu-id="2d819-104">PHONE\_DEVSPECIFIC message</span></span>

<span data-ttu-id="2d819-105">TAPI отправляет в приложение сообщение **Phone \_ девспеЦифик** , чтобы уведомить приложение о событиях конкретного устройства, происходящих на телефоне.</span><span class="sxs-lookup"><span data-stu-id="2d819-105">TAPI sends the **PHONE\_DEVSPECIFIC** message to an application to notify the application about device-specific events occurring at the phone.</span></span> <span data-ttu-id="2d819-106">Значение сообщения и интерпретация параметров определяются реализацией.</span><span class="sxs-lookup"><span data-stu-id="2d819-106">The meaning of the message and the interpretation of the parameters is implementation-defined.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="2d819-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d819-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d819-108">*хфоне*</span><span class="sxs-lookup"><span data-stu-id="2d819-108">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="2d819-109">Маркер телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="2d819-109">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="2d819-110">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="2d819-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="2d819-111">Экземпляр обратного вызова приложения, предоставленный при открытии телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="2d819-111">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="2d819-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="2d819-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="2d819-113">Зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="2d819-113">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="2d819-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="2d819-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="2d819-115">Зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="2d819-115">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="2d819-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="2d819-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="2d819-117">Зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="2d819-117">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d819-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d819-118">Return value</span></span>

<span data-ttu-id="2d819-119">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="2d819-119">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d819-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2d819-120">Requirements</span></span>



| <span data-ttu-id="2d819-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2d819-121">Requirement</span></span> | <span data-ttu-id="2d819-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2d819-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2d819-123">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="2d819-123">TAPI version</span></span><br/> | <span data-ttu-id="2d819-124">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2d819-124">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="2d819-125">Header</span><span class="sxs-lookup"><span data-stu-id="2d819-125">Header</span></span><br/>       | <dl> <span data-ttu-id="2d819-126"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d819-126"><dt>Tapi.h</dt></span></span> </dl> |



 

 




