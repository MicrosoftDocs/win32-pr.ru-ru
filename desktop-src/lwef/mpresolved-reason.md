---
title: Перечисление MPRESOLVED_REASON (Мпклиент. h)
description: Возможные причины сбоя исправления.
ms.assetid: 29E875D7-97DA-4129-AB71-B261CD0E682A
keywords:
- MPRESOLVED_REASON перечисления устаревшие функции среды Windows
- PMPRESOLVED_REASON указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MPRESOLVED_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab31fc8b734852ccdf15278f535d916228b43976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071789"
---
# <a name="mpresolved_reason-enumeration"></a><span data-ttu-id="b0420-105">\_Перечисление причин мпресолвед</span><span class="sxs-lookup"><span data-stu-id="b0420-105">MPRESOLVED\_REASON enumeration</span></span>

<span data-ttu-id="b0420-106">Возможные причины сбоя исправления.</span><span class="sxs-lookup"><span data-stu-id="b0420-106">Possible reasons for a remediation failure being resolved.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0420-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0420-107">Syntax</span></span>


```C++
typedef enum tagMPRESOLVED_REASON { 
  MPRESOLVED_REASON_UNKNOWN    = 0,
  MPRESOLVED_REASON_FULL_SCAN  = 1,
  MPRESOLVED_REASON_TIMED_OUT  = 2
} MPRESOLVED_REASON, *PMPRESOLVED_REASON;
```



## <a name="constants"></a><span data-ttu-id="b0420-108">Константы</span><span class="sxs-lookup"><span data-stu-id="b0420-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b0420-109"><span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**\_Причина мпресолвед \_ неизвестна**</span><span class="sxs-lookup"><span data-stu-id="b0420-109"><span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**MPRESOLVED\_REASON\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="b0420-110">В состоянии ошибки.</span><span class="sxs-lookup"><span data-stu-id="b0420-110">In an error state.</span></span>

</dd> <dt>

<span data-ttu-id="b0420-111"><span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**МПРЕСОЛВЕД \_ Причина \_ полной \_ проверки**</span><span class="sxs-lookup"><span data-stu-id="b0420-111"><span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**MPRESOLVED\_REASON\_FULL\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="b0420-112">Выполнена полная проверка.</span><span class="sxs-lookup"><span data-stu-id="b0420-112">A full scan was performed.</span></span>

</dd> <dt>

<span data-ttu-id="b0420-113"><span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**Причина истечения \_ \_ времени \_ ожидания мпресолвед**</span><span class="sxs-lookup"><span data-stu-id="b0420-113"><span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**MPRESOLVED\_REASON\_TIMED\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="b0420-114">Прошло достаточно времени.</span><span class="sxs-lookup"><span data-stu-id="b0420-114">Enough time has passed.</span></span> <span data-ttu-id="b0420-115">Значение по умолчанию — одна неделя.</span><span class="sxs-lookup"><span data-stu-id="b0420-115">The default is one week.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0420-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b0420-116">Requirements</span></span>



| <span data-ttu-id="b0420-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b0420-117">Requirement</span></span> | <span data-ttu-id="b0420-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b0420-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0420-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0420-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b0420-120">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b0420-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b0420-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0420-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b0420-122">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b0420-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0420-123">Header</span><span class="sxs-lookup"><span data-stu-id="b0420-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0420-124"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0420-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





