---
description: Пропускает указанное число устройств в последовательности перечисления.
ms.assetid: 38b72b80-93f5-433e-977c-e3ee503daae5
title: 'Метод Иенумпортабледевицеконнекторс:: Skip (Девпкэй. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Skip
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: c00daecccd12beee8e9e741c2906e47484fa6da3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081146"
---
# <a name="ienumportabledeviceconnectorsskip-method"></a><span data-ttu-id="fdb91-103">Метод Иенумпортабледевицеконнекторс:: Skip</span><span class="sxs-lookup"><span data-stu-id="fdb91-103">IEnumPortableDeviceConnectors::Skip method</span></span>

<span data-ttu-id="fdb91-104">Метод **Skip** пропускает указанное число устройств в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="fdb91-104">The **Skip** method skips the specified number of devices in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdb91-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fdb91-105">Syntax</span></span>


```C++
HRESULT Skip(
  [in] UINT32 cConnectors
);
```



## <a name="parameters"></a><span data-ttu-id="fdb91-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fdb91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdb91-107">*кконнекторс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fdb91-107">*cConnectors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb91-108">Число пропускаемых устройств.</span><span class="sxs-lookup"><span data-stu-id="fdb91-108">The number of devices to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdb91-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fdb91-109">Return value</span></span>

<span data-ttu-id="fdb91-110">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fdb91-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fdb91-111">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="fdb91-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fdb91-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fdb91-112">Return code</span></span>                                                                             | <span data-ttu-id="fdb91-113">Описание</span><span class="sxs-lookup"><span data-stu-id="fdb91-113">Description</span></span>                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fdb91-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fdb91-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="fdb91-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="fdb91-115">The method succeeded.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="fdb91-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="fdb91-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="fdb91-117">Не удалось пропускать указанное число устройств.</span><span class="sxs-lookup"><span data-stu-id="fdb91-117">The specified number of devices could not be skipped.</span></span> <span data-ttu-id="fdb91-118">Одна из возможных причин: параметр *кконнекторс* указывает больше устройств, чем фактически остается в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="fdb91-118">One possible cause: The *cConnectors* parameter specifies more devices than actually remain in the enumeration sequence.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fdb91-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fdb91-119">Requirements</span></span>



| <span data-ttu-id="fdb91-120">Требование</span><span class="sxs-lookup"><span data-stu-id="fdb91-120">Requirement</span></span> | <span data-ttu-id="fdb91-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fdb91-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdb91-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fdb91-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fdb91-123">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fdb91-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="fdb91-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fdb91-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fdb91-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fdb91-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                   |
| <span data-ttu-id="fdb91-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fdb91-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdb91-127"><dt>Девпкэй. h; </dt> <dt>Портабледевицеконнектапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdb91-127"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="fdb91-128">IDL</span><span class="sxs-lookup"><span data-stu-id="fdb91-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fdb91-129"><dt>Портабледевицеконнектапи. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fdb91-129"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="fdb91-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fdb91-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="fdb91-131"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdb91-131"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="fdb91-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fdb91-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdb91-133">**иенумпортабледевицеконнекторс**</span><span class="sxs-lookup"><span data-stu-id="fdb91-133">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




