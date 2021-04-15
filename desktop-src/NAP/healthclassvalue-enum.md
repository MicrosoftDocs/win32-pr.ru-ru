---
title: Перечисление Хеалсклассвалуе (Наппротокол. h)
description: Указывает значение TLV класса работоспособности.
ms.assetid: af80c27a-a686-494b-8795-73eb366deaa0
keywords:
- Хеалсклассвалуе перечисление NAP
topic_type:
- apiref
api_name:
- HealthClassValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ade44b74d03a69d6ccf410a042adf3819b8cc782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488961"
---
# <a name="healthclassvalue-enumeration"></a><span data-ttu-id="66403-104">Перечисление Хеалсклассвалуе</span><span class="sxs-lookup"><span data-stu-id="66403-104">HealthClassValue enumeration</span></span>

> [!Note]  
> <span data-ttu-id="66403-105">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="66403-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="66403-106">Тип перечисления **хеалсклассвалуе** указывает значение TLV класса работоспособности.</span><span class="sxs-lookup"><span data-stu-id="66403-106">The **HealthClassValue** enumeration type indicates the value of the health class TLV.</span></span>

## <a name="syntax"></a><span data-ttu-id="66403-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66403-107">Syntax</span></span>


```C++
typedef enum tagHealthClassValue { 
  healthClassFirewall        = 0,
  healthClassPatchLevel      = 1,
  healthClassAntiVirus       = 2,
  healthClassCriticalUpdate  = 3,
  healthClassReserved        = 128
} HealthClassValue;
```



## <a name="constants"></a><span data-ttu-id="66403-108">Константы</span><span class="sxs-lookup"><span data-stu-id="66403-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="66403-109"><span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**хеалсклассфиревалл**</span><span class="sxs-lookup"><span data-stu-id="66403-109"><span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**healthClassFirewall**</span></span>
</dt> <dd>

<span data-ttu-id="66403-110">TLV класса работоспособности — брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="66403-110">The health class TLV is firewall.</span></span>

</dd> <dt>

<span data-ttu-id="66403-111"><span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**хеалскласспатчлевел**</span><span class="sxs-lookup"><span data-stu-id="66403-111"><span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**healthClassPatchLevel**</span></span>
</dt> <dd>

<span data-ttu-id="66403-112">В TLV класса работоспособности находится уровень обновления.</span><span class="sxs-lookup"><span data-stu-id="66403-112">The health class TLV is patch level.</span></span>

</dd> <dt>

<span data-ttu-id="66403-113"><span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**хеалсклассантивирус**</span><span class="sxs-lookup"><span data-stu-id="66403-113"><span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**healthClassAntiVirus**</span></span>
</dt> <dd>

<span data-ttu-id="66403-114">TLV класса работоспособности — это антивирусная программа.</span><span class="sxs-lookup"><span data-stu-id="66403-114">The health class TLV is antivirus.</span></span>

</dd> <dt>

<span data-ttu-id="66403-115"><span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**хеалскласскритикалупдате**</span><span class="sxs-lookup"><span data-stu-id="66403-115"><span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**healthClassCriticalUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="66403-116">TLV класса работоспособности является критическим обновлением.</span><span class="sxs-lookup"><span data-stu-id="66403-116">The health class TLV is critical update.</span></span>

</dd> <dt>

<span data-ttu-id="66403-117"><span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**хеалсклассресервед**</span><span class="sxs-lookup"><span data-stu-id="66403-117"><span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**healthClassReserved**</span></span>
</dt> <dd>

<span data-ttu-id="66403-118">Зарезервировано только для системного использования.</span><span class="sxs-lookup"><span data-stu-id="66403-118">Reserved for system use only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66403-119">Требования</span><span class="sxs-lookup"><span data-stu-id="66403-119">Requirements</span></span>



| <span data-ttu-id="66403-120">Требование</span><span class="sxs-lookup"><span data-stu-id="66403-120">Requirement</span></span> | <span data-ttu-id="66403-121">Значение</span><span class="sxs-lookup"><span data-stu-id="66403-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="66403-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66403-122">Minimum supported client</span></span><br/> | <span data-ttu-id="66403-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66403-123">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="66403-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66403-124">Minimum supported server</span></span><br/> | <span data-ttu-id="66403-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="66403-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="66403-126">Header</span><span class="sxs-lookup"><span data-stu-id="66403-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="66403-127"><dt>Наппротокол. h</dt></span><span class="sxs-lookup"><span data-stu-id="66403-127"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="66403-128">IDL</span><span class="sxs-lookup"><span data-stu-id="66403-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="66403-129"><dt>Наппротокол. idl</dt></span><span class="sxs-lookup"><span data-stu-id="66403-129"><dt>NapProtocol.idl</dt></span></span> </dl> |



 

 





