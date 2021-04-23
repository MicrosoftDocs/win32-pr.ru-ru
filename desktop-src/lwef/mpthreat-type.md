---
title: Перечисление MPTHREAT_TYPE (Мпклиент. h)
description: Возможные типы угроз.
ms.assetid: 56061F12-AA89-4203-BED4-99613E24002A
keywords:
- MPTHREAT_TYPE перечисления устаревшие функции среды Windows
- PMPTHREAT_TYPE указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MPTHREAT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed823b100c91f259252d7cad71e554099caf6a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415281"
---
# <a name="mpthreat_type-enumeration"></a><span data-ttu-id="2ccba-105">\_Перечисление типов мпсреат</span><span class="sxs-lookup"><span data-stu-id="2ccba-105">MPTHREAT\_TYPE enumeration</span></span>

<span data-ttu-id="2ccba-106">Возможные типы угроз.</span><span class="sxs-lookup"><span data-stu-id="2ccba-106">Possible threat types.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ccba-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ccba-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_TYPE { 
  MPTHREAT_TYPE_KNOWNBAD   = 0,
  MPTHREAT_TYPE_BEHAVIOR   = 1,
  MPTHREAT_TYPE_UNKNOWN    = 2,
  MPTHREAT_TYPE_KNOWNGOOD  = 3,
  MPTHREAT_TYPE_NIS        = 4,
  MPTHREAT_TYPE_MAXVALUE   = 4
} MPTHREAT_TYPE, *PMPTHREAT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="2ccba-108">Константы</span><span class="sxs-lookup"><span data-stu-id="2ccba-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2ccba-109"><span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**\_тип мпсреат \_ кновнбад**</span><span class="sxs-lookup"><span data-stu-id="2ccba-109"><span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**MPTHREAT\_TYPE\_KNOWNBAD**</span></span>
</dt> <dd>

<span data-ttu-id="2ccba-110">Обнаружена известная неплохая угроза с помощью сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="2ccba-110">Known bad threat detected via signature.</span></span>

</dd> <dt>

<span data-ttu-id="2ccba-111"><span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**\_поведение типа \_ мпсреат**</span><span class="sxs-lookup"><span data-stu-id="2ccba-111"><span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**MPTHREAT\_TYPE\_BEHAVIOR**</span></span>
</dt> <dd>

<span data-ttu-id="2ccba-112">Обнаружена подозрительная угроза с помощью мониторинга поведения.</span><span class="sxs-lookup"><span data-stu-id="2ccba-112">Suspicious threat detected via behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="2ccba-113"><span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**\_неизвестный тип мпсреат \_**</span><span class="sxs-lookup"><span data-stu-id="2ccba-113"><span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**MPTHREAT\_TYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="2ccba-114">Неизвестные угрозы (Неклассифицированные).</span><span class="sxs-lookup"><span data-stu-id="2ccba-114">Unknown threats (unclassified).</span></span>

</dd> <dt>

<span data-ttu-id="2ccba-115"><span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**\_тип мпсреат \_ кновнгуд**</span><span class="sxs-lookup"><span data-stu-id="2ccba-115"><span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**MPTHREAT\_TYPE\_KNOWNGOOD**</span></span>
</dt> <dd>

<span data-ttu-id="2ccba-116">Известная хорошая угроза.</span><span class="sxs-lookup"><span data-stu-id="2ccba-116">Known good threat.</span></span>

</dd> <dt>

<span data-ttu-id="2ccba-117"><span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**МПСРЕАТ \_ тип \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="2ccba-117"><span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**MPTHREAT\_TYPE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="2ccba-118">Обнаружение угроз NIS.</span><span class="sxs-lookup"><span data-stu-id="2ccba-118">NIS threat detection.</span></span>

</dd> <dt>

<span data-ttu-id="2ccba-119"><span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**МПСРЕАТ \_ тип \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="2ccba-119"><span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**MPTHREAT\_TYPE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="2ccba-120">Максимально возможное значение.</span><span class="sxs-lookup"><span data-stu-id="2ccba-120">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ccba-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2ccba-121">Requirements</span></span>



| <span data-ttu-id="2ccba-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2ccba-122">Requirement</span></span> | <span data-ttu-id="2ccba-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2ccba-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ccba-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2ccba-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2ccba-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2ccba-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2ccba-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2ccba-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2ccba-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2ccba-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ccba-128">Header</span><span class="sxs-lookup"><span data-stu-id="2ccba-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ccba-129"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ccba-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





