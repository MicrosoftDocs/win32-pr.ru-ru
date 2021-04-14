---
title: Метод типа Ибасикдевице
description: Возвращает значение перечисления, указывающее тип устройства DLNA.
ms.assetid: D9FB3A02-7796-4ACB-B7D3-D171D1D9B77F
keywords:
- Метод типа потоковая передача мультимедиа API
- Метод Type потоковая передача мультимедиа API, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод Type
topic_type:
- apiref
api_name:
- IBasicDevice.Type
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a69f0671c82363ff61179c0120b3db8f6e755de9
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2020
ms.locfileid: "104414100"
---
# <a name="ibasicdevicetype-method"></a><span data-ttu-id="a998c-106">Метод Ибасикдевице:: Type</span><span class="sxs-lookup"><span data-stu-id="a998c-106">IBasicDevice::Type method</span></span>

<span data-ttu-id="a998c-107">Возвращает значение перечисления, указывающее тип устройства DLNA.</span><span class="sxs-lookup"><span data-stu-id="a998c-107">Retrieves an enumeration value indicating the device type of the DLNA device.</span></span>

## <a name="syntax"></a><span data-ttu-id="a998c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a998c-108">Syntax</span></span>


```C++
HRESULT Type(
  [out] DeviceTypes *value
);
```



## <a name="parameters"></a><span data-ttu-id="a998c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a998c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a998c-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a998c-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a998c-111">Получает указатель на значение [**девицетипес**](devicetypes.md) .</span><span class="sxs-lookup"><span data-stu-id="a998c-111">Receives a pointer to a [**DeviceTypes**](devicetypes.md) value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a998c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a998c-112">Return value</span></span>

<span data-ttu-id="a998c-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a998c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a998c-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a998c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a998c-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a998c-115">Return code</span></span>                                                                          | <span data-ttu-id="a998c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a998c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a998c-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a998c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a998c-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="a998c-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="a998c-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a998c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a998c-120">**ибасикдевице**</span><span class="sxs-lookup"><span data-stu-id="a998c-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





