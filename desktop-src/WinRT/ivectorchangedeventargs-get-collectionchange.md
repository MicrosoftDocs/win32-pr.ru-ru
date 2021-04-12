---
description: Возвращает тип изменения, произошедшего в векторе.
ms.assetid: 213f4794-b972-44e3-a400-8a24b1583ddd
title: 'Метод Ивекторчанжедевентаргс:: get_CollectionChange (Ивекторчанжедевентаргс. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_CollectionChange
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: a843574bcaf93ec524173ba76800cc15012c89fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263083"
---
# <a name="ivectorchangedeventargsget_collectionchange-method"></a><span data-ttu-id="db583-103">Метод Ивекторчанжедевентаргс:: Get \_ коллектиончанже</span><span class="sxs-lookup"><span data-stu-id="db583-103">IVectorChangedEventArgs::get\_CollectionChange method</span></span>

<span data-ttu-id="db583-104">Возвращает тип изменения, произошедшего в векторе.</span><span class="sxs-lookup"><span data-stu-id="db583-104">Gets the type of change that occurred in the vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="db583-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db583-105">Syntax</span></span>


```C++
HRESULT get_CollectionChange(
  [out, retval] CollectionChange *value
);
```



## <a name="parameters"></a><span data-ttu-id="db583-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="db583-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db583-107">*значение* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="db583-107">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="db583-108">Тип: \**коллектиончанже \** _</span><span class="sxs-lookup"><span data-stu-id="db583-108">Type: \**CollectionChange\** _</span></span>

<span data-ttu-id="db583-109">Значение из перечисления [_ *коллектиончанже* \*](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) , описывающее изменение.</span><span class="sxs-lookup"><span data-stu-id="db583-109">A value from the [_ *CollectionChange*\*](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) enumeration that describes the change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db583-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db583-110">Return value</span></span>

<span data-ttu-id="db583-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="db583-111">Type: **HRESULT**</span></span>

<span data-ttu-id="db583-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="db583-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="db583-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="db583-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="db583-114">Требования</span><span class="sxs-lookup"><span data-stu-id="db583-114">Requirements</span></span>



| <span data-ttu-id="db583-115">Требование</span><span class="sxs-lookup"><span data-stu-id="db583-115">Requirement</span></span> | <span data-ttu-id="db583-116">Значение</span><span class="sxs-lookup"><span data-stu-id="db583-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db583-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db583-117">Minimum supported client</span></span><br/> | <span data-ttu-id="db583-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="db583-118">Windows 8</span></span><br/>                                                                                 |
| <span data-ttu-id="db583-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db583-119">Minimum supported server</span></span><br/> | <span data-ttu-id="db583-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="db583-120">Windows Server 2012</span></span><br/>                                                                       |
| <span data-ttu-id="db583-121">Header</span><span class="sxs-lookup"><span data-stu-id="db583-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="db583-122"><dt>Ивекторчанжедевентаргс. h</dt></span><span class="sxs-lookup"><span data-stu-id="db583-122"><dt>IVectorChangedEventArgs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db583-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db583-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db583-124">**ивекторчанжедевентаргс**</span><span class="sxs-lookup"><span data-stu-id="db583-124">**IVectorChangedEventArgs**</span></span>](ivectorchangedeventargs.md)
</dt> </dl>

 

 
