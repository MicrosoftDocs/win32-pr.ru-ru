---
title: Структура MPTHREAT_INFOEX_NIS (Мпклиент. h)
description: Содержит сведения, относящиеся к NIS.
ms.assetid: 3887C5BF-B1F6-4420-B40A-9585E44BE7A9
keywords:
- MPTHREAT_INFOEX_NIS структуры устаревшие функции среды Windows
- Функции PMPTHREAT_INFOEX_NIS указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_NIS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4ed68432a2d0ebe78535a139fcc7b0882b9ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071572"
---
# <a name="mpthreat_infoex_nis-structure"></a><span data-ttu-id="02d02-105">\_ \_ Структура NIS мпсреат инфоекс</span><span class="sxs-lookup"><span data-stu-id="02d02-105">MPTHREAT\_INFOEX\_NIS structure</span></span>

<span data-ttu-id="02d02-106">Содержит сведения, относящиеся к NIS.</span><span class="sxs-lookup"><span data-stu-id="02d02-106">Contains NIS-specific information.</span></span>

## <a name="syntax"></a><span data-ttu-id="02d02-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02d02-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_NIS {
  MP_MIDL_STRING LPWSTR SourceIP;
  MP_MIDL_STRING LPWSTR DestinationIP;
  DWORD                 dwSourceport;
  DWORD                 dwDestinationport;
  MP_MIDL_STRING LPWSTR Protocol;
  MP_MIDL_STRING LPWSTR Link;
} MPTHREAT_INFOEX_NIS, *PMPTHREAT_INFOEX_NIS;
```



## <a name="members"></a><span data-ttu-id="02d02-108">Члены</span><span class="sxs-lookup"><span data-stu-id="02d02-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="02d02-109">**SourceIP**</span><span class="sxs-lookup"><span data-stu-id="02d02-109">**SourceIP**</span></span>
</dt> <dd>

<span data-ttu-id="02d02-110">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="02d02-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="02d02-111">**дестинатионип**</span><span class="sxs-lookup"><span data-stu-id="02d02-111">**DestinationIP**</span></span>
</dt> <dd>

<span data-ttu-id="02d02-112">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="02d02-112">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="02d02-113">**двсаурцепорт**</span><span class="sxs-lookup"><span data-stu-id="02d02-113">**dwSourceport**</span></span>
</dt> <dd>

<span data-ttu-id="02d02-114">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="02d02-114">Type: **DWORD**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="02d02-115">**двдестинатионпорт**</span><span class="sxs-lookup"><span data-stu-id="02d02-115">**dwDestinationport**</span></span>
</dt> <dd>

<span data-ttu-id="02d02-116">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="02d02-116">Type: **DWORD**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="02d02-117">**Протокол**</span><span class="sxs-lookup"><span data-stu-id="02d02-117">**Protocol**</span></span>
</dt> <dd>

<span data-ttu-id="02d02-118">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="02d02-118">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="02d02-119">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="02d02-119">**Link**</span></span>
</dt> <dd>

<span data-ttu-id="02d02-120">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="02d02-120">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

<span data-ttu-id="02d02-121"></dd> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="02d02-121"></dd> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="02d02-122">Требования</span><span class="sxs-lookup"><span data-stu-id="02d02-122">Requirements</span></span>



| <span data-ttu-id="02d02-123">Требование</span><span class="sxs-lookup"><span data-stu-id="02d02-123">Requirement</span></span> | <span data-ttu-id="02d02-124">Значение</span><span class="sxs-lookup"><span data-stu-id="02d02-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02d02-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02d02-125">Minimum supported client</span></span><br/> | <span data-ttu-id="02d02-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="02d02-126">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="02d02-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02d02-127">Minimum supported server</span></span><br/> | <span data-ttu-id="02d02-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="02d02-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="02d02-129">Header</span><span class="sxs-lookup"><span data-stu-id="02d02-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="02d02-130"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="02d02-130"><dt>MpClient.h</dt></span></span> </dl> |



 

 





