---
title: Метод Ивмдрминдивидуализатионстатус-Status (Вмдрмсдк. h)
description: Метод WebMethod извлекает подробные сведения о ходе процесса индивидуализации.
ms.assetid: 8985f3cc-006d-4fd5-b218-d3af3473b8e3
keywords:
- Метод WebMethod формат Windows Media Format
- Метод WebMethod формат Windows Media Format, интерфейс Ивмдрминдивидуализатионстатус
- Интерфейс Ивмдрминдивидуализатионстатус интерфейса Windows Media Format, методического состояния
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus.GetStatus
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f144f188de46d17702dd22aa12e2245156b59a21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704478"
---
# <a name="iwmdrmindividualizationstatusgetstatus-method"></a><span data-ttu-id="df15d-106">Метод Ивмдрминдивидуализатионстатус:: with Status</span><span class="sxs-lookup"><span data-stu-id="df15d-106">IWMDRMIndividualizationStatus::GetStatus method</span></span>

<span data-ttu-id="df15d-107">Метод **WebMethod извлекает** подробные сведения о ходе процесса индивидуализации.</span><span class="sxs-lookup"><span data-stu-id="df15d-107">The **GetStatus** method retrieves detailed information about individualization progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="df15d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df15d-108">Syntax</span></span>


```C++
HRESULT GetStatus(
  [out] WM_INDIVIDUALIZE_STATUS *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="df15d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="df15d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df15d-110">*пстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="df15d-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df15d-111">Получает структуру [**\_ \_ состояния WM индивидуализируйте**](drmwm-individualize-status.md) , содержащую подробные сведения о состоянии попытки индивидуализации.</span><span class="sxs-lookup"><span data-stu-id="df15d-111">Receives a [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure containing detailed information about the status of the individualization attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df15d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df15d-112">Return value</span></span>

<span data-ttu-id="df15d-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="df15d-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="df15d-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="df15d-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="df15d-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="df15d-115">Return code</span></span>                                                                          | <span data-ttu-id="df15d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="df15d-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="df15d-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="df15d-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="df15d-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="df15d-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="df15d-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df15d-119">Remarks</span></span>

<span data-ttu-id="df15d-120">Нет.</span><span class="sxs-lookup"><span data-stu-id="df15d-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="df15d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="df15d-121">Requirements</span></span>



| <span data-ttu-id="df15d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="df15d-122">Requirement</span></span> | <span data-ttu-id="df15d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="df15d-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df15d-124">Header</span><span class="sxs-lookup"><span data-stu-id="df15d-124">Header</span></span><br/> | <dl> <span data-ttu-id="df15d-125"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="df15d-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df15d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df15d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df15d-127">**Интерфейс Ивмдрминдивидуализатионстатус**</span><span class="sxs-lookup"><span data-stu-id="df15d-127">**IWMDRMIndividualizationStatus Interface**</span></span>](iwmdrmindividualizationstatus.md)
</dt> </dl>

 

 





