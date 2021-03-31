---
title: Перечисление MP_SIGNATURE_TYPE (Мпклиент. h)
description: Возможные типы сигнатур.
ms.assetid: 44B195A8-866D-4B87-9576-54E00658F9B3
keywords:
- MP_SIGNATURE_TYPE перечисления устаревшие функции среды Windows
- PMP_SIGNATURE_TYPE указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MP_SIGNATURE_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b99f7140706e9a6d3fa32e7eb346ef6478f3f26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490395"
---
# <a name="mp_signature_type-enumeration"></a><span data-ttu-id="4b4d2-105">\_ \_ Перечисление типов сигнатур MP</span><span class="sxs-lookup"><span data-stu-id="4b4d2-105">MP\_SIGNATURE\_TYPE enumeration</span></span>

<span data-ttu-id="4b4d2-106">Возможные типы сигнатур.</span><span class="sxs-lookup"><span data-stu-id="4b4d2-106">Possible signature types.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b4d2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b4d2-107">Syntax</span></span>


```C++
typedef enum tagMP_SIGNATURE_TYPE { 
  MP_SIGNATURE_ANTIMALWARE     = 0,
  MP_SIGNATURE_ANTIVIRUS       = 1,
  MP_SIGNATURE_ANTISPYWARE     = 2,
  MP_SIGNATURE_NIS             = 3,
  MP_SIGNATURE_TYPES_MAXVALUE  = 3
} MP_SIGNATURE_TYPE, *PMP_SIGNATURE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="4b4d2-108">Константы</span><span class="sxs-lookup"><span data-stu-id="4b4d2-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4b4d2-109"><span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**\_АНТИвредоносная программа с подписью пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="4b4d2-109"><span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**MP\_SIGNATURE\_ANTIMALWARE**</span></span>
</dt> <dd>

<span data-ttu-id="4b4d2-110">Антивирусные и антишпионские подписи.</span><span class="sxs-lookup"><span data-stu-id="4b4d2-110">Both antivirus and antispyware signatures.</span></span>

</dd> <dt>

<span data-ttu-id="4b4d2-111"><span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**\_антивирусная подпись MP \_**</span><span class="sxs-lookup"><span data-stu-id="4b4d2-111"><span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**MP\_SIGNATURE\_ANTIVIRUS**</span></span>
</dt> <dd>

<span data-ttu-id="4b4d2-112">Только антивирусные подписи.</span><span class="sxs-lookup"><span data-stu-id="4b4d2-112">Only antivirus signatures.</span></span>

</dd> <dt>

<span data-ttu-id="4b4d2-113"><span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**Антишпионская программа с \_ подписью пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="4b4d2-113"><span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**MP\_SIGNATURE\_ANTISPYWARE**</span></span>
</dt> <dd>

<span data-ttu-id="4b4d2-114">Только сигнатуры для защиты от шпионского по.</span><span class="sxs-lookup"><span data-stu-id="4b4d2-114">Only antispyware signatures.</span></span>

</dd> <dt>

<span data-ttu-id="4b4d2-115"><span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**\_NIS-подпись пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="4b4d2-115"><span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**MP\_SIGNATURE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="4b4d2-116">Подписи NIS.</span><span class="sxs-lookup"><span data-stu-id="4b4d2-116">NIS signatures.</span></span>

</dd> <dt>

<span data-ttu-id="4b4d2-117"><span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**\_типы сигнатур \_ MP \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="4b4d2-117"><span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**MP\_SIGNATURE\_TYPES\_MAXVALUE**</span></span>
<span data-ttu-id="4b4d2-118"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4b4d2-118"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="4b4d2-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4b4d2-119">Requirements</span></span>



| <span data-ttu-id="4b4d2-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4b4d2-120">Requirement</span></span> | <span data-ttu-id="4b4d2-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4b4d2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b4d2-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b4d2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4b4d2-123">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4b4d2-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4b4d2-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b4d2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4b4d2-125">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4b4d2-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4b4d2-126">Header</span><span class="sxs-lookup"><span data-stu-id="4b4d2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b4d2-127"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b4d2-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





