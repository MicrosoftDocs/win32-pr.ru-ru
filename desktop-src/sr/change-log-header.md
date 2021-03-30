---
title: Структура CHANGE_LOG_HEADER
description: Заголовок журнала изменений.
ms.assetid: 24fee9a5-b073-474f-afd5-d81f66399936
keywords:
- Восстановление системы структуры CHANGE_LOG_HEADER
- Восстановление системы указателей на структуру PCHANGE_LOG_HEADER
topic_type:
- apiref
api_name:
- CHANGE_LOG_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5512ff9c9e708095f38e3ae1dcf80ce2e0e4443b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414869"
---
# <a name="change_log_header-structure"></a><span data-ttu-id="d4f6b-105">\_ \_ Структура заголовка журнала изменений</span><span class="sxs-lookup"><span data-stu-id="d4f6b-105">CHANGE\_LOG\_HEADER structure</span></span>

<span data-ttu-id="d4f6b-106">\[Эти сведения относятся только к Windows XP с пакетом обновления 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="d4f6b-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="d4f6b-107">Заголовок журнала изменений.</span><span class="sxs-lookup"><span data-stu-id="d4f6b-107">The change log header.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4f6b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4f6b-108">Syntax</span></span>


```C++
typedef struct _CHANGE_LOG_HEADER {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwLogVersion;
  RECORD_HEADER DataHeader;
  BYTE          byteData[1];
} CHANGE_LOG_HEADER, *PCHANGE_LOG_HEADER;
```



## <a name="members"></a><span data-ttu-id="d4f6b-109">Члены</span><span class="sxs-lookup"><span data-stu-id="d4f6b-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="d4f6b-110">**рекордхеадер**</span><span class="sxs-lookup"><span data-stu-id="d4f6b-110">**RecordHeader**</span></span>
</dt> <dd>

<span data-ttu-id="d4f6b-111">Структура [**\_ заголовка записи**](record-header.md) .</span><span class="sxs-lookup"><span data-stu-id="d4f6b-111">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="d4f6b-112">Элемент **дврекордтипе** должен иметь значение рекордтипелогхеадер (0).</span><span class="sxs-lookup"><span data-stu-id="d4f6b-112">The **dwRecordType** member should be set to RecordTypeLogHeader (0).</span></span> <span data-ttu-id="d4f6b-113">Элемент **дврекордсизе** должен учитывать все элементы, а также дополнительный параметр **DWORD** , следующий за этим заголовком.</span><span class="sxs-lookup"><span data-stu-id="d4f6b-113">The **dwRecordSize** member should account for all the members, plus the extra **DWORD** value that follows this header.</span></span> <span data-ttu-id="d4f6b-114">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="d4f6b-114">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d4f6b-115">**двмагикнум**</span><span class="sxs-lookup"><span data-stu-id="d4f6b-115">**dwMagicNum**</span></span>
</dt> <dd>

<span data-ttu-id="d4f6b-116">Этот элемент должен иметь значение 0xabcdef12.</span><span class="sxs-lookup"><span data-stu-id="d4f6b-116">This member should be set to 0xabcdef12.</span></span>

</dd> <dt>

<span data-ttu-id="d4f6b-117">**двлогверсион**</span><span class="sxs-lookup"><span data-stu-id="d4f6b-117">**dwLogVersion**</span></span>
</dt> <dd>

<span data-ttu-id="d4f6b-118">Этот элемент должен иметь значение 2.</span><span class="sxs-lookup"><span data-stu-id="d4f6b-118">This member should be set to 2.</span></span>

</dd> <dt>

<span data-ttu-id="d4f6b-119">**"Заголовок"**</span><span class="sxs-lookup"><span data-stu-id="d4f6b-119">**DataHeader**</span></span>
</dt> <dd>

<span data-ttu-id="d4f6b-120">Структура [**\_ заголовка записи**](record-header.md) .</span><span class="sxs-lookup"><span data-stu-id="d4f6b-120">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="d4f6b-121">Элемент **дврекордтипе** должен иметь значение **рекордтипеволумепас** (2).</span><span class="sxs-lookup"><span data-stu-id="d4f6b-121">The **dwRecordType** member should be set to **RecordTypeVolumePath** (2).</span></span>

</dd> <dt>

<span data-ttu-id="d4f6b-122">**битедата**</span><span class="sxs-lookup"><span data-stu-id="d4f6b-122">**byteData**</span></span>
</dt> <dd>

<span data-ttu-id="d4f6b-123">Начало строки, завершающейся нулем, которая указывает путь к тому.</span><span class="sxs-lookup"><span data-stu-id="d4f6b-123">The start of a null-terminated string that specifies the volume path.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4f6b-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4f6b-124">Remarks</span></span>

<span data-ttu-id="d4f6b-125">За этим заголовком следует значение **DWORD** , которое должно быть идентично значению элемента **дврекордсизе** в **рекордхеадер**.</span><span class="sxs-lookup"><span data-stu-id="d4f6b-125">This header is followed by a **DWORD** value that should be identical to the value of the **dwRecordSize** member of **RecordHeader**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4f6b-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d4f6b-126">Requirements</span></span>



| <span data-ttu-id="d4f6b-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d4f6b-127">Requirement</span></span> | <span data-ttu-id="d4f6b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d4f6b-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d4f6b-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4f6b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d4f6b-130">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d4f6b-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d4f6b-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4f6b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d4f6b-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d4f6b-132">None supported</span></span><br/>                            |
| <span data-ttu-id="d4f6b-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d4f6b-133">End of client support</span></span><br/>    | <span data-ttu-id="d4f6b-134">Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="d4f6b-134">Windows XP with SP2</span></span><br/>                       |



 

 





