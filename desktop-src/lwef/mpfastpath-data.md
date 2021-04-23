---
title: Структура MPFASTPATH_DATA (Мпклиент. h)
description: Уведомление об обновлении Фастпас.
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- MPFASTPATH_DATA структуры устаревшие функции среды Windows
- Функции PMPFASTPATH_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPFASTPATH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2850a48074fee6984564550683c7fe595d0779ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710470"
---
# <a name="mpfastpath_data-structure"></a><span data-ttu-id="bb9ab-105">\_Структура данных мпфастпас</span><span class="sxs-lookup"><span data-stu-id="bb9ab-105">MPFASTPATH\_DATA structure</span></span>

<span data-ttu-id="bb9ab-106">Уведомление об обновлении Фастпас.</span><span class="sxs-lookup"><span data-stu-id="bb9ab-106">FastPath update notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb9ab-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb9ab-107">Syntax</span></span>


```C++
typedef struct tagMPFASTPATH_DATA {
  MP_SIGNATURE_TYPE         SignatureType;
  MP_FASTPATH_TYPE          FastPathSignatureType;
  MP_MIDL_STRING LPWSTR     FastPathSignatureVersion;
  ULARGE_INTEGER            CompilationTimestamp;
  MP_PERSISTENCE_LIMIT_TYPE PersistenceType;
  MP_MIDL_STRING LPWSTR     PersistenceValue;
  MP_MIDL_STRING LPWSTR     PersistencePath;
  MP_REMOVAL_REASON         Reason;
} MPFASTPATH_DATA, *PMPFASTPATH_DATA;
```



## <a name="members"></a><span data-ttu-id="bb9ab-108">Члены</span><span class="sxs-lookup"><span data-stu-id="bb9ab-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="bb9ab-109">**сигнатуретипе**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-109">**SignatureType**</span></span>
</dt> <dd>

<span data-ttu-id="bb9ab-110">Тип: **[ **\_ \_ тип подписи пакета управления**](mp-signature-type.md)**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-110">Type: **[**MP\_SIGNATURE\_TYPE**](mp-signature-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb9ab-111">Тип подписи.</span><span class="sxs-lookup"><span data-stu-id="bb9ab-111">Signature type.</span></span>

</dd> <dt>

<span data-ttu-id="bb9ab-112">**фастпассигнатуретипе**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-112">**FastPathSignatureType**</span></span>
</dt> <dd>

<span data-ttu-id="bb9ab-113">Тип: **[ **\_ \_ тип MP фастпас**](mp-fastpath-type.md)**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-113">Type: **[**MP\_FASTPATH\_TYPE**](mp-fastpath-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb9ab-114">Тип подписи Фастпас.</span><span class="sxs-lookup"><span data-stu-id="bb9ab-114">FastPath signature type.</span></span>

</dd> <dt>

<span data-ttu-id="bb9ab-115">**фастпассигнатуреверсион**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-115">**FastPathSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="bb9ab-116">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-116">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="bb9ab-117">Версия сигнатуры Фастпас (необязательно).</span><span class="sxs-lookup"><span data-stu-id="bb9ab-117">FastPath signature version (optional).</span></span>

</dd> <dt>

<span data-ttu-id="bb9ab-118">**компилатионтиместамп**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-118">**CompilationTimestamp**</span></span>
</dt> <dd>

<span data-ttu-id="bb9ab-119">Тип: **уларже \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-119">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="bb9ab-120">Отметка времени компиляции (UTC).</span><span class="sxs-lookup"><span data-stu-id="bb9ab-120">Compilation timestamp (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="bb9ab-121">**PersistenceType**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-121">**PersistenceType**</span></span>
</dt> <dd>

<span data-ttu-id="bb9ab-122">Тип: **[ **\_ \_ \_ тип ограничения сохраняемости MP**](mp-persistence-limit-type.md)**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-122">Type: **[**MP\_PERSISTENCE\_LIMIT\_TYPE**](mp-persistence-limit-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb9ab-123">Тип сохраняемости (необязательный).</span><span class="sxs-lookup"><span data-stu-id="bb9ab-123">Persistence type (optional).</span></span>

</dd> <dt>

<span data-ttu-id="bb9ab-124">**персистенцевалуе**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-124">**PersistenceValue**</span></span>
</dt> <dd>

<span data-ttu-id="bb9ab-125">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-125">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="bb9ab-126">Значение сохраняемости (необязательно).</span><span class="sxs-lookup"><span data-stu-id="bb9ab-126">Persistence value (optional).</span></span>

</dd> <dt>

<span data-ttu-id="bb9ab-127">**персистенцепас**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-127">**PersistencePath**</span></span>
</dt> <dd>

<span data-ttu-id="bb9ab-128">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-128">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="bb9ab-129">Путь сохраняемости (необязательно).</span><span class="sxs-lookup"><span data-stu-id="bb9ab-129">Persistence path (optional).</span></span>

</dd> <dt>

<span data-ttu-id="bb9ab-130">**Причина**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-130">**Reason**</span></span>
</dt> <dd>

<span data-ttu-id="bb9ab-131">Тип: **[ **\_ \_ Причина удаления пакета управления**](mp-removal-reason.md)**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-131">Type: **[**MP\_REMOVAL\_REASON**](mp-removal-reason.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb9ab-132">Причина удаления подписи.</span><span class="sxs-lookup"><span data-stu-id="bb9ab-132">Reason for signature removal.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb9ab-133">Требования</span><span class="sxs-lookup"><span data-stu-id="bb9ab-133">Requirements</span></span>



| <span data-ttu-id="bb9ab-134">Требование</span><span class="sxs-lookup"><span data-stu-id="bb9ab-134">Requirement</span></span> | <span data-ttu-id="bb9ab-135">Значение</span><span class="sxs-lookup"><span data-stu-id="bb9ab-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb9ab-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb9ab-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bb9ab-137">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bb9ab-137">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bb9ab-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb9ab-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bb9ab-139">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bb9ab-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb9ab-140">Header</span><span class="sxs-lookup"><span data-stu-id="bb9ab-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb9ab-141"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb9ab-141"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb9ab-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb9ab-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb9ab-143">**\_тип фастпас пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-143">**MP\_FASTPATH\_TYPE**</span></span>](mp-fastpath-type.md)
</dt> <dt>

[<span data-ttu-id="bb9ab-144">**\_тип ограничения сохраняемости пакета управления \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-144">**MP\_PERSISTENCE\_LIMIT\_TYPE**</span></span>](mp-persistence-limit-type.md)
</dt> <dt>

[<span data-ttu-id="bb9ab-145">**\_тип подписи пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="bb9ab-145">**MP\_SIGNATURE\_TYPE**</span></span>](mp-signature-type.md)
</dt> </dl>

 

 





