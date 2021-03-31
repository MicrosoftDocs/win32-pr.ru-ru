---
title: Структура MPTHREAT_INFOEX_BEHAVIOR (Мпклиент. h)
description: Содержит сведения, относящиеся к изменению поведения.
ms.assetid: 762E755F-5BA1-476D-B395-6617093309C5
keywords:
- MPTHREAT_INFOEX_BEHAVIOR структуры устаревшие функции среды Windows
- Функции PMPTHREAT_INFOEX_BEHAVIOR указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_BEHAVIOR
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0bc00aeb56aec38b88f2590211c705079834f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803532"
---
# <a name="mpthreat_infoex_behavior-structure"></a><span data-ttu-id="5c264-105">\_ \_ Структура поведения инфоекс мпсреат</span><span class="sxs-lookup"><span data-stu-id="5c264-105">MPTHREAT\_INFOEX\_BEHAVIOR structure</span></span>

<span data-ttu-id="5c264-106">Содержит сведения, относящиеся к изменению поведения.</span><span class="sxs-lookup"><span data-stu-id="5c264-106">Contains behavior modification-specific information.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c264-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c264-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_BEHAVIOR {
  ULARGE_INTEGER         SignatureID;
  ULONGLONG              EngineVersion;
  ULONGLONG              ASDeltaSignatureVersion;
  ULONGLONG              AVDeltaSignatureVersion;
  MP_HASH_TYPE           HashType;
  DWORD                  FidelityValue;
  MP_MIDL_STRING  LPWSTR HashValue;
  MP_MIDL_STRING  LPWSTR TargetFileName;
  MP_MIDL_STRING  LPWSTR TargetFileHash;
} MPTHREAT_INFOEX_BEHAVIOR, *PMPTHREAT_INFOEX_BEHAVIOR;
```



## <a name="members"></a><span data-ttu-id="5c264-108">Члены</span><span class="sxs-lookup"><span data-stu-id="5c264-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5c264-109">**сигнатуреид**</span><span class="sxs-lookup"><span data-stu-id="5c264-109">**SignatureID**</span></span>
</dt> <dd>

<span data-ttu-id="5c264-110">Тип: **уларже \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="5c264-110">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="5c264-111">Идентификатор подписи изменения поведения, заданный ядром во время обнаружения.</span><span class="sxs-lookup"><span data-stu-id="5c264-111">Behavior modification signature ID given by the engine at the time of detection.</span></span>

</dd> <dt>

<span data-ttu-id="5c264-112">**EngineVersion**</span><span class="sxs-lookup"><span data-stu-id="5c264-112">**EngineVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5c264-113">Тип: **улонглонг**</span><span class="sxs-lookup"><span data-stu-id="5c264-113">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="5c264-114">Версия модуля подсистемы.</span><span class="sxs-lookup"><span data-stu-id="5c264-114">Engine module version.</span></span>

</dd> <dt>

<span data-ttu-id="5c264-115">**асделтасигнатуреверсион**</span><span class="sxs-lookup"><span data-stu-id="5c264-115">**ASDeltaSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5c264-116">Тип: **улонглонг**</span><span class="sxs-lookup"><span data-stu-id="5c264-116">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="5c264-117">Версия сигнатуры антишпионского по.</span><span class="sxs-lookup"><span data-stu-id="5c264-117">Antispyware signature version.</span></span>

</dd> <dt>

<span data-ttu-id="5c264-118">**авделтасигнатуреверсион**</span><span class="sxs-lookup"><span data-stu-id="5c264-118">**AVDeltaSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5c264-119">Тип: **улонглонг**</span><span class="sxs-lookup"><span data-stu-id="5c264-119">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="5c264-120">Версия сигнатуры Антивируса</span><span class="sxs-lookup"><span data-stu-id="5c264-120">Antivirus signature version</span></span>

</dd> <dt>

<span data-ttu-id="5c264-121">**хаштипе**</span><span class="sxs-lookup"><span data-stu-id="5c264-121">**HashType**</span></span>
</dt> <dd>

<span data-ttu-id="5c264-122">Тип: **[ **\_ \_ тип хэша MP**](mp-hash-type.md)**</span><span class="sxs-lookup"><span data-stu-id="5c264-122">Type: **[**MP\_HASH\_TYPE**](mp-hash-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5c264-123">Используемый тип хэша.</span><span class="sxs-lookup"><span data-stu-id="5c264-123">Hash type used.</span></span> <span data-ttu-id="5c264-124">См. раздел [**\_ \_ тип хэша MP**](mp-hash-type.md).</span><span class="sxs-lookup"><span data-stu-id="5c264-124">See [**MP\_HASH\_TYPE**](mp-hash-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c264-125">**фиделитивалуе**</span><span class="sxs-lookup"><span data-stu-id="5c264-125">**FidelityValue**</span></span>
</dt> <dd>

<span data-ttu-id="5c264-126">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="5c264-126">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="5c264-127">Значение точности.</span><span class="sxs-lookup"><span data-stu-id="5c264-127">Fidelity value.</span></span>

</dd> <dt>

<span data-ttu-id="5c264-128">**хашвалуе**</span><span class="sxs-lookup"><span data-stu-id="5c264-128">**HashValue**</span></span>
</dt> <dd>

<span data-ttu-id="5c264-129">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="5c264-129">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="5c264-130">Хэш файла.</span><span class="sxs-lookup"><span data-stu-id="5c264-130">The hash of the file.</span></span>

</dd> <dt>

<span data-ttu-id="5c264-131">**таржетфиленаме**</span><span class="sxs-lookup"><span data-stu-id="5c264-131">**TargetFileName**</span></span>
</dt> <dd>

<span data-ttu-id="5c264-132">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="5c264-132">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="5c264-133">Путь и имя целевого файла.</span><span class="sxs-lookup"><span data-stu-id="5c264-133">The path and name of the targeted file.</span></span>

</dd> <dt>

<span data-ttu-id="5c264-134">**таржетфилехаш**</span><span class="sxs-lookup"><span data-stu-id="5c264-134">**TargetFileHash**</span></span>
</dt> <dd>

<span data-ttu-id="5c264-135">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="5c264-135">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="5c264-136">Хэш целевого файла.</span><span class="sxs-lookup"><span data-stu-id="5c264-136">The hash of the targeted file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c264-137">Требования</span><span class="sxs-lookup"><span data-stu-id="5c264-137">Requirements</span></span>



| <span data-ttu-id="5c264-138">Требование</span><span class="sxs-lookup"><span data-stu-id="5c264-138">Requirement</span></span> | <span data-ttu-id="5c264-139">Значение</span><span class="sxs-lookup"><span data-stu-id="5c264-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c264-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5c264-140">Minimum supported client</span></span><br/> | <span data-ttu-id="5c264-141">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5c264-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5c264-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5c264-142">Minimum supported server</span></span><br/> | <span data-ttu-id="5c264-143">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5c264-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5c264-144">Header</span><span class="sxs-lookup"><span data-stu-id="5c264-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c264-145"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c264-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c264-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c264-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c264-147">**\_тип ХЭША \_ MP**</span><span class="sxs-lookup"><span data-stu-id="5c264-147">**MP\_HASH\_TYPE**</span></span>](mp-hash-type.md)
</dt> </dl>

 

 





