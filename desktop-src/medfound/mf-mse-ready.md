---
description: Определяет различные состояния готовности расширения источника мультимедиа.
ms.assetid: 7455B92F-CC2D-4743-935D-F5EBFD834397
title: Перечисление MF_MSE_READY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_READY
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: bff2155a2cb2cb21d4c25d868f95472f47f15b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910203"
---
# <a name="mf_mse_ready-enumeration"></a><span data-ttu-id="cdac8-103">\_ \_ Перечисление ГОТОВности MF для MSE</span><span class="sxs-lookup"><span data-stu-id="cdac8-103">MF\_MSE\_READY enumeration</span></span>

<span data-ttu-id="cdac8-104">Определяет различные состояния готовности расширения источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cdac8-104">Defines the different ready states of the Media Source Extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdac8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cdac8-105">Syntax</span></span>


```C++
typedef enum _MF_MSE_READY { 
  MF_MSE_READY_CLOSED  = 1,
  MF_MSE_READY_OPEN    = 2,
  MF_MSE_READY_ENDED   = 3
} MF_MSE_READY;
```



## <a name="constants"></a><span data-ttu-id="cdac8-106">Константы</span><span class="sxs-lookup"><span data-stu-id="cdac8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cdac8-107"><span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**\_ \_ Готово к закрытию с поддержкой MSE \_**</span><span class="sxs-lookup"><span data-stu-id="cdac8-107"><span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**MF\_MSE\_READY\_CLOSED**</span></span>
</dt> <dd>

<span data-ttu-id="cdac8-108">Источник мультимедиа закрыт.</span><span class="sxs-lookup"><span data-stu-id="cdac8-108">The media source is closed.</span></span>

</dd> <dt>

<span data-ttu-id="cdac8-109"><span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**\_ \_ ОТКРЫТа MF с поддержкой MSE \_**</span><span class="sxs-lookup"><span data-stu-id="cdac8-109"><span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**MF\_MSE\_READY\_OPEN**</span></span>
</dt> <dd>

<span data-ttu-id="cdac8-110">Источник мультимедиа открыт.</span><span class="sxs-lookup"><span data-stu-id="cdac8-110">The media source is open.</span></span>

</dd> <dt>

<span data-ttu-id="cdac8-111"><span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**\_ \_ закончено, готово к работе с MSE \_**</span><span class="sxs-lookup"><span data-stu-id="cdac8-111"><span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**MF\_MSE\_READY\_ENDED**</span></span>
</dt> <dd>

<span data-ttu-id="cdac8-112">Источник мультимедиа завершен.</span><span class="sxs-lookup"><span data-stu-id="cdac8-112">The media source is ended.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cdac8-113">Требования</span><span class="sxs-lookup"><span data-stu-id="cdac8-113">Requirements</span></span>



| <span data-ttu-id="cdac8-114">Требование</span><span class="sxs-lookup"><span data-stu-id="cdac8-114">Requirement</span></span> | <span data-ttu-id="cdac8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="cdac8-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdac8-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cdac8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cdac8-117">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cdac8-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cdac8-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cdac8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cdac8-119">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cdac8-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="cdac8-120">IDL</span><span class="sxs-lookup"><span data-stu-id="cdac8-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cdac8-121"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cdac8-121"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdac8-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cdac8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdac8-123">Перечисления Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cdac8-123">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




