---
description: Возвращает позицию в векторе, где произошло изменение.
ms.assetid: 00756d77-aae0-45f0-8bd4-cf68af9bdc7c
title: 'Метод Ивекторчанжедевентаргс:: get_Index (Ивекторчанжедевентаргс. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_Index
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: 5c131567ec7fc2861ce11db9e5d7ec581f6f663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072752"
---
# <a name="ivectorchangedeventargsget_index-method"></a><span data-ttu-id="69954-103">Метод индекса Ивекторчанжедевентаргс:: Get \_</span><span class="sxs-lookup"><span data-stu-id="69954-103">IVectorChangedEventArgs::get\_Index method</span></span>

<span data-ttu-id="69954-104">Возвращает позицию в векторе, где произошло изменение.</span><span class="sxs-lookup"><span data-stu-id="69954-104">Gets the position in the vector where the change occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="69954-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69954-105">Syntax</span></span>


```C++
HRESULT get_Index(
  [out, retval] unsigned *value
);
```



## <a name="parameters"></a><span data-ttu-id="69954-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="69954-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69954-107">*значение* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="69954-107">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="69954-108">Тип: \**без знака \** _</span><span class="sxs-lookup"><span data-stu-id="69954-108">Type: \**unsigned\** _</span></span>

<span data-ttu-id="69954-109">Отсчитываемая от нуля координата в векторе, где произошло изменение, если применимо.</span><span class="sxs-lookup"><span data-stu-id="69954-109">The zero-based position in the vector where the change occurred, if applicable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69954-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69954-110">Return value</span></span>

<span data-ttu-id="69954-111">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="69954-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="69954-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="69954-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="69954-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="69954-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="69954-114">Требования</span><span class="sxs-lookup"><span data-stu-id="69954-114">Requirements</span></span>



| <span data-ttu-id="69954-115">Требование</span><span class="sxs-lookup"><span data-stu-id="69954-115">Requirement</span></span> | <span data-ttu-id="69954-116">Значение</span><span class="sxs-lookup"><span data-stu-id="69954-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69954-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="69954-117">Minimum supported client</span></span><br/> | <span data-ttu-id="69954-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="69954-118">Windows 8</span></span><br/>                                                                                 |
| <span data-ttu-id="69954-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="69954-119">Minimum supported server</span></span><br/> | <span data-ttu-id="69954-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="69954-120">Windows Server 2012</span></span><br/>                                                                       |
| <span data-ttu-id="69954-121">Header</span><span class="sxs-lookup"><span data-stu-id="69954-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="69954-122"><dt>Ивекторчанжедевентаргс. h</dt></span><span class="sxs-lookup"><span data-stu-id="69954-122"><dt>IVectorChangedEventArgs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69954-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69954-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69954-124">**ивекторчанжедевентаргс**</span><span class="sxs-lookup"><span data-stu-id="69954-124">**IVectorChangedEventArgs**</span></span>](ivectorchangedeventargs.md)
</dt> </dl>

 

 




