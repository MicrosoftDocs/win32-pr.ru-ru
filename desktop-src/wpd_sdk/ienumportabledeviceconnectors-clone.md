---
description: Создает копию текущего интерфейса Иенумпортабледевицеконнекторс.
ms.assetid: 64274cb0-1f57-481d-914f-41238cbe2f1b
title: 'Метод Иенумпортабледевицеконнекторс:: Clone (Девпкэй. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Clone
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 0e5273f1c400732c94c7c63918787f5e130a854d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348565"
---
# <a name="ienumportabledeviceconnectorsclone-method"></a><span data-ttu-id="3651a-103">Метод Иенумпортабледевицеконнекторс:: Clone</span><span class="sxs-lookup"><span data-stu-id="3651a-103">IEnumPortableDeviceConnectors::Clone method</span></span>

<span data-ttu-id="3651a-104">Метод **clone** создает копию текущего интерфейса [**иенумпортабледевицеконнекторс**](ienumportabledeviceconnectors.md) .</span><span class="sxs-lookup"><span data-stu-id="3651a-104">The **Clone** method creates a copy of the current [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="3651a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3651a-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPortableDeviceConnectors **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="3651a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3651a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3651a-107">*ппенум* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3651a-107">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3651a-108">Адрес указателя на интерфейс [**иенумпортабледевицеконнекторс**](ienumportabledeviceconnectors.md) .</span><span class="sxs-lookup"><span data-stu-id="3651a-108">The address of a pointer to an [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) interface.</span></span> <span data-ttu-id="3651a-109">Вызывающее приложение должно освободить этот интерфейс, когда он завершит работу с ним.</span><span class="sxs-lookup"><span data-stu-id="3651a-109">The calling application must release this interface when it is done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3651a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3651a-110">Return value</span></span>

<span data-ttu-id="3651a-111">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3651a-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3651a-112">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3651a-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3651a-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3651a-113">Return code</span></span>                                                                          | <span data-ttu-id="3651a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="3651a-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3651a-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3651a-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3651a-116">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="3651a-116">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3651a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3651a-117">Requirements</span></span>



| <span data-ttu-id="3651a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3651a-118">Requirement</span></span> | <span data-ttu-id="3651a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3651a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3651a-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3651a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3651a-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3651a-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="3651a-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3651a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3651a-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3651a-123">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="3651a-124">Header</span><span class="sxs-lookup"><span data-stu-id="3651a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3651a-125"><dt>Девпкэй. h; </dt> <dt>Портабледевицеконнектапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="3651a-125"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="3651a-126">IDL</span><span class="sxs-lookup"><span data-stu-id="3651a-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3651a-127"><dt>Портабледевицеконнектапи. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3651a-127"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="3651a-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3651a-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="3651a-129"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3651a-129"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="3651a-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3651a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3651a-131">**иенумпортабледевицеконнекторс**</span><span class="sxs-lookup"><span data-stu-id="3651a-131">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




