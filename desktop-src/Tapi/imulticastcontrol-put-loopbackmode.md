---
description: Лупбаккмоде размещения \_ задает режим многоадресного замыкания на себя.
ms.assetid: 38b28529-224f-4624-bb5e-22fee500e8e6
title: 'Имултикастконтрол: метод ut_LoopbackMode:p (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5b5e51b3814b380cc06d9c960db1a4e4b9ecb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679730"
---
# <a name="imulticastcontrolput_loopbackmode-method"></a><span data-ttu-id="96a40-103">Имултикастконтрол::p UT \_ лупбаккмоде метод</span><span class="sxs-lookup"><span data-stu-id="96a40-103">IMulticastControl::put\_LoopbackMode method</span></span>

<span data-ttu-id="96a40-104">\[**Размещение \_ Лупбаккмоде** недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="96a40-104">\[**put\_LoopbackMode** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="96a40-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="96a40-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="96a40-106">**\_ Лупбаккмоде размещения** задает режим многоадресного замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="96a40-106">The **put\_LoopbackMode** sets the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="96a40-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96a40-107">Syntax</span></span>


```C++
HRESULT put_LoopbackMode(
  [in] MULTICAST_LOOPBACK_MODE mode
);
```



## <a name="parameters"></a><span data-ttu-id="96a40-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="96a40-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96a40-109">*режим* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="96a40-109">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96a40-110">[**Многоадресная рассылка \_ Дескриптор \_ режима замыкания**](multicast-loopback-mode.md) на себя нового режима замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="96a40-110">[**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md) descriptor of the new loopback mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96a40-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96a40-111">Return value</span></span>

<span data-ttu-id="96a40-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="96a40-112">This method can return one of these values.</span></span>



| <span data-ttu-id="96a40-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="96a40-113">Return code</span></span>                                                                                  | <span data-ttu-id="96a40-114">Описание</span><span class="sxs-lookup"><span data-stu-id="96a40-114">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="96a40-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="96a40-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="96a40-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="96a40-116">Method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="96a40-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="96a40-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="96a40-118">Недопустимый параметр *mode* .</span><span class="sxs-lookup"><span data-stu-id="96a40-118">The *mode* parameter is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="96a40-119">Требования</span><span class="sxs-lookup"><span data-stu-id="96a40-119">Requirements</span></span>



| <span data-ttu-id="96a40-120">Требование</span><span class="sxs-lookup"><span data-stu-id="96a40-120">Requirement</span></span> | <span data-ttu-id="96a40-121">Значение</span><span class="sxs-lookup"><span data-stu-id="96a40-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96a40-122">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="96a40-122">TAPI version</span></span><br/> | <span data-ttu-id="96a40-123">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="96a40-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="96a40-124">Header</span><span class="sxs-lookup"><span data-stu-id="96a40-124">Header</span></span><br/>       | <dl> <span data-ttu-id="96a40-125"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="96a40-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="96a40-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="96a40-126">Library</span></span><br/>      | <dl> <span data-ttu-id="96a40-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96a40-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="96a40-128">DLL</span><span class="sxs-lookup"><span data-stu-id="96a40-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="96a40-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96a40-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="96a40-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96a40-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96a40-131">**имултикастконтрол**</span><span class="sxs-lookup"><span data-stu-id="96a40-131">**IMulticastControl**</span></span>](imulticastcontrol.md)
</dt> </dl>

 

 




