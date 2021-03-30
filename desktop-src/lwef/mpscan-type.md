---
title: Перечисление MPSCAN_TYPE (Мпклиент. h)
description: Тип выполняемого сканирования.
ms.assetid: 980A80FD-FF02-4338-B7FB-DAA141F65E89
keywords:
- MPSCAN_TYPE перечисления устаревшие функции среды Windows
- PMPSCAN_TYPE указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MPSCAN_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb89137dc9cfe5b8a4ff1f44a7a101239aa3a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801252"
---
# <a name="mpscan_type-enumeration"></a><span data-ttu-id="6efc2-105">\_Перечисление типов мпскан</span><span class="sxs-lookup"><span data-stu-id="6efc2-105">MPSCAN\_TYPE enumeration</span></span>

<span data-ttu-id="6efc2-106">Тип выполняемого сканирования.</span><span class="sxs-lookup"><span data-stu-id="6efc2-106">Type of scan performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6efc2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6efc2-107">Syntax</span></span>


```C++
typedef enum tagMPSCAN_TYPE { 
  MPSCAN_TYPE_UNKNOWN   = 0,
  MPSCAN_TYPE_QUICK     = 1,
  MPSCAN_TYPE_FULL      = 2,
  MPSCAN_TYPE_RESOURCE  = 3,
  MPSCAN_TYPE_MAXVALUE  = 3
} MPSCAN_TYPE, *PMPSCAN_TYPE;
```



## <a name="constants"></a><span data-ttu-id="6efc2-108">Константы</span><span class="sxs-lookup"><span data-stu-id="6efc2-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6efc2-109"><span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**\_неизвестный тип мпскан \_**</span><span class="sxs-lookup"><span data-stu-id="6efc2-109"><span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**MPSCAN\_TYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="6efc2-110">Только для внутреннего применения.</span><span class="sxs-lookup"><span data-stu-id="6efc2-110">Internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="6efc2-111"><span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**\_Быстрый ввод типа мпскан \_**</span><span class="sxs-lookup"><span data-stu-id="6efc2-111"><span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**MPSCAN\_TYPE\_QUICK**</span></span>
</dt> <dd>

<span data-ttu-id="6efc2-112">Сканирует выполняющиеся процессы и различные точки АВТОЗАПУСКА в системе, где обычно скрываются вредоносные программы.</span><span class="sxs-lookup"><span data-stu-id="6efc2-112">Scans running processes and various ASEP points in the system where malware typically hides.</span></span>

</dd> <dt>

<span data-ttu-id="6efc2-113"><span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**\_тип мпскан \_ Full**</span><span class="sxs-lookup"><span data-stu-id="6efc2-113"><span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**MPSCAN\_TYPE\_FULL**</span></span>
</dt> <dd>

<span data-ttu-id="6efc2-114">Выполняет быструю проверку, а затем проверяет все фиксированные диски системы.</span><span class="sxs-lookup"><span data-stu-id="6efc2-114">Performs a quick scan followed by scan of all fixed drives of the system.</span></span>

</dd> <dt>

<span data-ttu-id="6efc2-115"><span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**\_ресурс типа \_ мпскан**</span><span class="sxs-lookup"><span data-stu-id="6efc2-115"><span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**MPSCAN\_TYPE\_RESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="6efc2-116">Сканирует определенные ресурсы, например файлы или папки.</span><span class="sxs-lookup"><span data-stu-id="6efc2-116">Scans specific resources, such as files or folders.</span></span>

</dd> <dt>

<span data-ttu-id="6efc2-117"><span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**МПСКАН \_ тип \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="6efc2-117"><span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**MPSCAN\_TYPE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="6efc2-118">Максимально возможное значение.</span><span class="sxs-lookup"><span data-stu-id="6efc2-118">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6efc2-119">Требования</span><span class="sxs-lookup"><span data-stu-id="6efc2-119">Requirements</span></span>



| <span data-ttu-id="6efc2-120">Требование</span><span class="sxs-lookup"><span data-stu-id="6efc2-120">Requirement</span></span> | <span data-ttu-id="6efc2-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6efc2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6efc2-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6efc2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6efc2-123">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6efc2-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6efc2-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6efc2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6efc2-125">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6efc2-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6efc2-126">Header</span><span class="sxs-lookup"><span data-stu-id="6efc2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6efc2-127"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="6efc2-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





