---
title: Структура MPEXPIRATION_DATA (Мпклиент. h)
description: Уведомление о состоянии истечения срока действия продукта.
ms.assetid: BF464FFD-16AE-4F46-83CD-E0355478180C
keywords:
- MPEXPIRATION_DATA структуры устаревшие функции среды Windows
- Функции PMPEXPIRATION_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPEXPIRATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df5e417b1ce6b1d1f4c15d646b44b0ea6c1fade2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650364"
---
# <a name="mpexpiration_data-structure"></a><span data-ttu-id="9d823-105">\_Структура данных мпекспиратион</span><span class="sxs-lookup"><span data-stu-id="9d823-105">MPEXPIRATION\_DATA structure</span></span>

<span data-ttu-id="9d823-106">Уведомление о состоянии истечения срока действия продукта.</span><span class="sxs-lookup"><span data-stu-id="9d823-106">Product expiration status notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d823-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d823-107">Syntax</span></span>


```C++
typedef struct tagMPEXPIRATION_DATA {
  MP_EXPIRE_REASON       Reason;
  MP_EXPIRE_STATE_REPORT State;
} MPEXPIRATION_DATA, *PMPEXPIRATION_DATA;
```



## <a name="members"></a><span data-ttu-id="9d823-108">Члены</span><span class="sxs-lookup"><span data-stu-id="9d823-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9d823-109">**Причина**</span><span class="sxs-lookup"><span data-stu-id="9d823-109">**Reason**</span></span>
</dt> <dd>

<span data-ttu-id="9d823-110">Тип: **\_ \_ Причина истечения срока действия MP**</span><span class="sxs-lookup"><span data-stu-id="9d823-110">Type: **MP\_EXPIRE\_REASON**</span></span>

</dd> <dd>

<span data-ttu-id="9d823-111">Причина истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="9d823-111">Expiration reason.</span></span> <span data-ttu-id="9d823-112">Это одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="9d823-112">This is one of the following possible values:</span></span>



| <span data-ttu-id="9d823-113">Значение</span><span class="sxs-lookup"><span data-stu-id="9d823-113">Value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="9d823-114">Значение</span><span class="sxs-lookup"><span data-stu-id="9d823-114">Meaning</span></span>                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| <span id="MP_EXPIRED_UNKNOWN"></span><span id="mp_expired_unknown"></span><dl> <span data-ttu-id="9d823-115"><dt>**Пакет управления \_ Истек срок действия \_ неизвестного**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9d823-115"><dt>**MP\_EXPIRED\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="9d823-116">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="9d823-116">Unknown.</span></span><br/>    |
| <span id="MP_EXPIRED_EVAL"></span><span id="mp_expired_eval"></span><dl> <span data-ttu-id="9d823-117"><dt>**Пакет управления \_ Срок действия \_ пробной оценки**</dt> <dt>1</dt> истек</span><span class="sxs-lookup"><span data-stu-id="9d823-117"><dt>**MP\_EXPIRED\_EVAL**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="9d823-118">Аттестаци.</span><span class="sxs-lookup"><span data-stu-id="9d823-118">Evaluation.</span></span><br/> |
| <span id="MP_EXPIRED_WAT"></span><span id="mp_expired_wat"></span><dl> <span data-ttu-id="9d823-119"><dt>**Пакет управления \_ Истек срок действия \_ западноафриканскому**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9d823-119"><dt>**MP\_EXPIRED\_WAT**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="9d823-120">Западноафриканскому.</span><span class="sxs-lookup"><span data-stu-id="9d823-120">WAT.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="9d823-121">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="9d823-121">**State**</span></span>
</dt> <dd>

<span data-ttu-id="9d823-122">Тип: **\_ \_ \_ отчет о состоянии истечения срока действия пакета управления**</span><span class="sxs-lookup"><span data-stu-id="9d823-122">Type: **MP\_EXPIRE\_STATE\_REPORT**</span></span>

</dd> <dd>

<span data-ttu-id="9d823-123">Состояние истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="9d823-123">Expiration state.</span></span> <span data-ttu-id="9d823-124">Это одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="9d823-124">This is one of the following possible values:</span></span>



| <span data-ttu-id="9d823-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9d823-125">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="9d823-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9d823-126">Meaning</span></span>                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| <span id="MP_EXPIRE_STATE_REPORT_UNKNOWN"></span><span id="mp_expire_state_report_unknown"></span><dl> <span data-ttu-id="9d823-127"><dt>**Пакет управления \_ Отчет о состоянии истечения срока действия \_ \_ \_ неизвестен**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9d823-127"><dt>**MP\_EXPIRE\_STATE\_REPORT\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="9d823-128">Состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="9d823-128">State unknown.</span></span><br/> |
| <span id="MP_EXPIRE_STATE_REPORT_VALID"></span><span id="mp_expire_state_report_valid"></span><dl> <span data-ttu-id="9d823-129"><dt>**Пакет управления \_ \_ \_ \_ Допустимый отчет о состоянии истечения срока действия**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9d823-129"><dt>**MP\_EXPIRE\_STATE\_REPORT\_VALID**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="9d823-130">Без истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="9d823-130">No expiration.</span></span><br/> |
| <span id="MP_EXPIRE_STATE_REPORT_WARNING"></span><span id="mp_expire_state_report_warning"></span><dl> <span data-ttu-id="9d823-131"><dt>**Пакет управления \_ \_ \_ \_ Предупреждение о состоянии истечения срока действия**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9d823-131"><dt>**MP\_EXPIRE\_STATE\_REPORT\_WARNING**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="9d823-132">Приближается срок действия.</span><span class="sxs-lookup"><span data-stu-id="9d823-132">Near expired.</span></span><br/>  |
| <span id="MP_EXPIRE_STATE_REPORT_EXPIRED"></span><span id="mp_expire_state_report_expired"></span><dl> <span data-ttu-id="9d823-133"><dt>**Пакет управления \_ \_ \_ \_ Срок действия отчета об ИСтечении срока действия истек**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9d823-133"><dt>**MP\_EXPIRE\_STATE\_REPORT\_EXPIRED**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="9d823-134">Истек.</span><span class="sxs-lookup"><span data-stu-id="9d823-134">Expired.</span></span><br/>       |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d823-135">Требования</span><span class="sxs-lookup"><span data-stu-id="9d823-135">Requirements</span></span>



| <span data-ttu-id="9d823-136">Требование</span><span class="sxs-lookup"><span data-stu-id="9d823-136">Requirement</span></span> | <span data-ttu-id="9d823-137">Значение</span><span class="sxs-lookup"><span data-stu-id="9d823-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d823-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d823-138">Minimum supported client</span></span><br/> | <span data-ttu-id="9d823-139">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9d823-139">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9d823-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d823-140">Minimum supported server</span></span><br/> | <span data-ttu-id="9d823-141">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9d823-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d823-142">Header</span><span class="sxs-lookup"><span data-stu-id="9d823-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d823-143"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d823-143"><dt>MpClient.h</dt></span></span> </dl> |



 

 





