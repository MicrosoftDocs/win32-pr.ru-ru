---
title: Перечисление MPDETECTION_ORIGIN (Мпклиент. h)
description: Источник обнаружения.
ms.assetid: 9FEE2FAD-3E44-4134-B968-53E971F6B092
keywords:
- MPDETECTION_ORIGIN перечисления устаревшие функции среды Windows
- PMPDETECTION_ORIGIN указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MPDETECTION_ORIGIN
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4224aafef2c72db2a8d3b27f338ca83feaf64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654473"
---
# <a name="mpdetection_origin-enumeration"></a><span data-ttu-id="b961d-105">\_Перечисление источника мпдетектион</span><span class="sxs-lookup"><span data-stu-id="b961d-105">MPDETECTION\_ORIGIN enumeration</span></span>

<span data-ttu-id="b961d-106">Источник обнаружения.</span><span class="sxs-lookup"><span data-stu-id="b961d-106">Detection origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="b961d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b961d-107">Syntax</span></span>


```C++
typedef enum tagMPDETECTION_ORIGIN { 
  MPDETECTION_ORIGIN_UNKNOWN        = 0,
  MPDETECTION_ORIGIN_LOCAL_MACHINE  = 1 << 0,
  MPDETECTION_ORIGIN_NETWORKSHARE   = 1 << 1,
  MPDETECTION_ORIGIN_INTERNET       = 1 << 2,
  MPDETECTION_ORIGIN_OUTBOUND       = 1 << 3,
  MPDETECTION_ORIGIN_INBOUND        = 1 << 4
} MPDETECTION_ORIGIN, *PMPDETECTION_ORIGIN;
```



## <a name="constants"></a><span data-ttu-id="b961d-108">Константы</span><span class="sxs-lookup"><span data-stu-id="b961d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b961d-109"><span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**\_неизвестный источник мпдетектион \_**</span><span class="sxs-lookup"><span data-stu-id="b961d-109"><span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**MPDETECTION\_ORIGIN\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="b961d-110">Обнаруженная угрозой причина неизвестна.</span><span class="sxs-lookup"><span data-stu-id="b961d-110">Threat detected origin unknown.</span></span>

</dd> <dt>

<span data-ttu-id="b961d-111"><span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**МПДЕТЕКТИОН \_ исходный \_ локальный \_ компьютер**</span><span class="sxs-lookup"><span data-stu-id="b961d-111"><span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**MPDETECTION\_ORIGIN\_LOCAL\_MACHINE**</span></span>
</dt> <dd>

<span data-ttu-id="b961d-112">Обнаружена угроза на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="b961d-112">Threat detected on local machine.</span></span>

</dd> <dt>

<span data-ttu-id="b961d-113"><span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**МПДЕТЕКТИОН \_ происхождение \_ нетворкшаре**</span><span class="sxs-lookup"><span data-stu-id="b961d-113"><span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION\_ORIGIN\_NETWORKSHARE**</span></span>
</dt> <dd>

<span data-ttu-id="b961d-114">Обнаружена угроза на сетевом ресурсе.</span><span class="sxs-lookup"><span data-stu-id="b961d-114">Threat detected on network share.</span></span>

</dd> <dt>

<span data-ttu-id="b961d-115"><span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**МПДЕТЕКТИОН \_ Источник \_ Интернет**</span><span class="sxs-lookup"><span data-stu-id="b961d-115"><span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**MPDETECTION\_ORIGIN\_INTERNET**</span></span>
</dt> <dd>

<span data-ttu-id="b961d-116">Обнаружена угроза в Интернете.</span><span class="sxs-lookup"><span data-stu-id="b961d-116">Threat detected on internet.</span></span>

</dd> <dt>

<span data-ttu-id="b961d-117"><span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**\_исходящий \_ трафик источника мпдетектион**</span><span class="sxs-lookup"><span data-stu-id="b961d-117"><span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**MPDETECTION\_ORIGIN\_OUTBOUND**</span></span>
</dt> <dd>

<span data-ttu-id="b961d-118">Обнаружена угроза исходящего подключения.</span><span class="sxs-lookup"><span data-stu-id="b961d-118">Threat detected on an outbound connection.</span></span>

</dd> <dt>

<span data-ttu-id="b961d-119"><span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**\_входящий источник \_ мпдетектион**</span><span class="sxs-lookup"><span data-stu-id="b961d-119"><span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**MPDETECTION\_ORIGIN\_INBOUND**</span></span>
</dt> <dd>

<span data-ttu-id="b961d-120">Обнаружена угроза во входящем соединении.</span><span class="sxs-lookup"><span data-stu-id="b961d-120">Threat detected on an inbound connection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b961d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b961d-121">Requirements</span></span>



| <span data-ttu-id="b961d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b961d-122">Requirement</span></span> | <span data-ttu-id="b961d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b961d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b961d-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b961d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b961d-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b961d-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b961d-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b961d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b961d-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b961d-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b961d-128">Header</span><span class="sxs-lookup"><span data-stu-id="b961d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b961d-129"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="b961d-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





