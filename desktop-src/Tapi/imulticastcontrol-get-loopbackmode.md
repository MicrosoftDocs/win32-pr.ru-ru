---
description: Метод Get \_ лупбаккмоде получает режим многоадресного замыкания на себя.
ms.assetid: 2499c108-f70b-4afe-aa2b-2376c95b84bd
title: 'Метод Имултикастконтрол:: get_LoopbackMode (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 203d68f5b620ddf5e5ce7a36e4f8b85820deab2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685432"
---
# <a name="imulticastcontrolget_loopbackmode-method"></a><span data-ttu-id="d2ef8-103">Метод Имултикастконтрол:: Get \_ лупбаккмоде</span><span class="sxs-lookup"><span data-stu-id="d2ef8-103">IMulticastControl::get\_LoopbackMode method</span></span>

<span data-ttu-id="d2ef8-104">\[**получить \_ Лупбаккмоде** недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d2ef8-104">\[**get\_LoopbackMode** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d2ef8-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="d2ef8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d2ef8-106">Метод **Get \_ лупбаккмоде** получает режим многоадресного замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="d2ef8-106">The **get\_LoopbackMode** method gets the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ef8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2ef8-107">Syntax</span></span>


```C++
HRESULT get_LoopbackMode(
  [out] MULTICAST_LOOPBACK_MODE *pMode
);
```



## <a name="parameters"></a><span data-ttu-id="d2ef8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2ef8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2ef8-109">*пмоде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d2ef8-109">*pMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ef8-110">Указатель на дескриптор [**\_ \_ режима многоадресной рассылки**](multicast-loopback-mode.md) в текущем режиме замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="d2ef8-110">Pointer to the [**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md) descriptor of the current loopback mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2ef8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2ef8-111">Return value</span></span>

<span data-ttu-id="d2ef8-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="d2ef8-112">This method can return one of these values.</span></span>



| <span data-ttu-id="d2ef8-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d2ef8-113">Value</span></span>                                                                                        | <span data-ttu-id="d2ef8-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d2ef8-114">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="d2ef8-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d2ef8-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d2ef8-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="d2ef8-116">Method succeeded.</span></span><br/>                   |
| <dl> <span data-ttu-id="d2ef8-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d2ef8-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d2ef8-118">Недопустимый параметр *пмоде* .</span><span class="sxs-lookup"><span data-stu-id="d2ef8-118">The *pMode* parameter is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d2ef8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d2ef8-119">Requirements</span></span>



| <span data-ttu-id="d2ef8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d2ef8-120">Requirement</span></span> | <span data-ttu-id="d2ef8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d2ef8-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ef8-122">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="d2ef8-122">TAPI version</span></span><br/> | <span data-ttu-id="d2ef8-123">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d2ef8-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d2ef8-124">Header</span><span class="sxs-lookup"><span data-stu-id="d2ef8-124">Header</span></span><br/>       | <dl> <span data-ttu-id="d2ef8-125"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2ef8-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="d2ef8-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d2ef8-126">Library</span></span><br/>      | <dl> <span data-ttu-id="d2ef8-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2ef8-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d2ef8-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d2ef8-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="d2ef8-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2ef8-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d2ef8-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2ef8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2ef8-131">**имултикастконтрол**</span><span class="sxs-lookup"><span data-stu-id="d2ef8-131">**IMulticastControl**</span></span>](imulticastcontrol.md)
</dt> </dl>

 

 




