---
title: Перечисление MP_FASTPATH_TYPE (Мпклиент. h)
description: Тип Фастпас.
ms.assetid: BD72228F-DCC0-435E-A408-BD7FB02E55E1
keywords:
- MP_FASTPATH_TYPE перечисления устаревшие функции среды Windows
- PMP_FASTPATH_TYPE указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MP_FASTPATH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e89db79c54b166a833369ff52e47473463e0a2b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137298"
---
# <a name="mp_fastpath_type-enumeration"></a><span data-ttu-id="4f84e-105">\_ \_ Перечисление типов фастпас MP</span><span class="sxs-lookup"><span data-stu-id="4f84e-105">MP\_FASTPATH\_TYPE enumeration</span></span>

<span data-ttu-id="4f84e-106">Тип Фастпас.</span><span class="sxs-lookup"><span data-stu-id="4f84e-106">FastPath type.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f84e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f84e-107">Syntax</span></span>


```C++
typedef enum tagMP_FASTPATH_TYPE { 
  MP_FASTPATH_UNKNOWN   = 0,
  MP_FASTPATH_VDM       = 1,
  MP_FASTPATH_DISABLED  = 2
} MP_FASTPATH_TYPE, *PMP_FASTPATH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="4f84e-108">Константы</span><span class="sxs-lookup"><span data-stu-id="4f84e-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4f84e-109"><span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**фастпас пакета управления \_ \_ неизвестен**</span><span class="sxs-lookup"><span data-stu-id="4f84e-109"><span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**MP\_FASTPATH\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="4f84e-110">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="4f84e-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="4f84e-111"><span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**пакет управления \_ фастпас \_ VDM**</span><span class="sxs-lookup"><span data-stu-id="4f84e-111"><span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**MP\_FASTPATH\_VDM**</span></span>
</dt> <dd>

<span data-ttu-id="4f84e-112">Обновление VDM.</span><span class="sxs-lookup"><span data-stu-id="4f84e-112">VDM update.</span></span>

</dd> <dt>

<span data-ttu-id="4f84e-113"><span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**\_ФАСТПАС MP \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="4f84e-113"><span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**MP\_FASTPATH\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="4f84e-114">Уведомление об отключении подписи.</span><span class="sxs-lookup"><span data-stu-id="4f84e-114">Signature disable notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f84e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4f84e-115">Requirements</span></span>



| <span data-ttu-id="4f84e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4f84e-116">Requirement</span></span> | <span data-ttu-id="4f84e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4f84e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f84e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f84e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4f84e-119">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4f84e-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4f84e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f84e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4f84e-121">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4f84e-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4f84e-122">Header</span><span class="sxs-lookup"><span data-stu-id="4f84e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f84e-123"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f84e-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





