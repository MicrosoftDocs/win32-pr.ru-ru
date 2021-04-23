---
title: Структура MPTHREAT_LOCALIZED_INFO (Мпклиент. h)
description: Локализованные сведения для угрозы.
ms.assetid: 99DC9737-9A61-4407-B544-A7A979C5B556
keywords:
- MPTHREAT_LOCALIZED_INFO структуры устаревшие функции среды Windows
- Функции PMPTHREAT_LOCALIZED_INFO указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPTHREAT_LOCALIZED_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87ea0bee7c8cae15389b40b64038aad92a56dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415476"
---
# <a name="mpthreat_localized_info-structure"></a><span data-ttu-id="f5f91-105">\_Локализованная \_ информационная структура мпсреат</span><span class="sxs-lookup"><span data-stu-id="f5f91-105">MPTHREAT\_LOCALIZED\_INFO structure</span></span>

<span data-ttu-id="f5f91-106">Локализованные сведения для угрозы.</span><span class="sxs-lookup"><span data-stu-id="f5f91-106">Localized information for a threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5f91-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5f91-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_LOCALIZED_INFO {
  MPTHREAT_ID           ThreatID;
  MP_MIDL_STRING LPWSTR CategoryName;
  MP_MIDL_STRING LPWSTR CategoryDescription;
  MP_MIDL_STRING LPWSTR SeverityName;
  MP_MIDL_STRING LPWSTR SeverityDescription;
  MP_MIDL_STRING LPWSTR ShortDescription;
  MP_MIDL_STRING LPWSTR DefaultActionName;;
  MP_MIDL_STRING LPWSTR Advice;
  MP_MIDL_STRING LPWSTR ThreatUrl;
} MPTHREAT_LOCALIZED_INFO, *PMPTHREAT_LOCALIZED_INFO;
```



## <a name="members"></a><span data-ttu-id="f5f91-108">Члены</span><span class="sxs-lookup"><span data-stu-id="f5f91-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f5f91-109">**среатид**</span><span class="sxs-lookup"><span data-stu-id="f5f91-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="f5f91-110">Тип: **мпсреат \_ ID**</span><span class="sxs-lookup"><span data-stu-id="f5f91-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="f5f91-111">Идентификатор угрозы.</span><span class="sxs-lookup"><span data-stu-id="f5f91-111">Threat identifier.</span></span> <span data-ttu-id="f5f91-112">Верхний бит задан для выявления угроз, связанных с антивирусной программой.</span><span class="sxs-lookup"><span data-stu-id="f5f91-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="f5f91-113">**CategoryName**</span><span class="sxs-lookup"><span data-stu-id="f5f91-113">**CategoryName**</span></span>
</dt> <dd>

<span data-ttu-id="f5f91-114">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="f5f91-114">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f5f91-115">Классификация угроз, например Троян или троянская Keylogger.</span><span class="sxs-lookup"><span data-stu-id="f5f91-115">Threat classification, such as a trojan or a keylogger.</span></span>

</dd> <dt>

<span data-ttu-id="f5f91-116">**категоридескриптион**</span><span class="sxs-lookup"><span data-stu-id="f5f91-116">**CategoryDescription**</span></span>
</dt> <dd>

<span data-ttu-id="f5f91-117">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="f5f91-117">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f5f91-118">Описание категории угроз.</span><span class="sxs-lookup"><span data-stu-id="f5f91-118">Description of threat category.</span></span>

</dd> <dt>

<span data-ttu-id="f5f91-119">**северитинаме**</span><span class="sxs-lookup"><span data-stu-id="f5f91-119">**SeverityName**</span></span>
</dt> <dd>

<span data-ttu-id="f5f91-120">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="f5f91-120">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f5f91-121">Степень серьезности угрозы, например серьезная или умеренная.</span><span class="sxs-lookup"><span data-stu-id="f5f91-121">Threat severity level, such as severe or moderate.</span></span>

</dd> <dt>

<span data-ttu-id="f5f91-122">**северитидескриптион**</span><span class="sxs-lookup"><span data-stu-id="f5f91-122">**SeverityDescription**</span></span>
</dt> <dd>

<span data-ttu-id="f5f91-123">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="f5f91-123">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f5f91-124">Описание уровня серьезности угрозы.</span><span class="sxs-lookup"><span data-stu-id="f5f91-124">Description of threat severity level.</span></span>

</dd> <dt>

<span data-ttu-id="f5f91-125">**шортдескриптион**</span><span class="sxs-lookup"><span data-stu-id="f5f91-125">**ShortDescription**</span></span>
</dt> <dd>

<span data-ttu-id="f5f91-126">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="f5f91-126">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f5f91-127">Краткое описание угрозы.</span><span class="sxs-lookup"><span data-stu-id="f5f91-127">Short description of threat.</span></span>

</dd> <dt>

<span data-ttu-id="f5f91-128">**Дефаултактионнаме;**</span><span class="sxs-lookup"><span data-stu-id="f5f91-128">**DefaultActionName;**</span></span>
</dt> <dd>

<span data-ttu-id="f5f91-129">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="f5f91-129">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f5f91-130">Имя действия по умолчанию, например Remove или карантин, предлагаемое ядром.</span><span class="sxs-lookup"><span data-stu-id="f5f91-130">Name of default action, such as remove or quarantine, suggested by engine.</span></span>

</dd> <dt>

<span data-ttu-id="f5f91-131">**Advice**</span><span class="sxs-lookup"><span data-stu-id="f5f91-131">**Advice**</span></span>
</dt> <dd>

<span data-ttu-id="f5f91-132">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="f5f91-132">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f5f91-133">Советы по конкретной угрозе.</span><span class="sxs-lookup"><span data-stu-id="f5f91-133">Advice for the particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="f5f91-134">**среатурл**</span><span class="sxs-lookup"><span data-stu-id="f5f91-134">**ThreatUrl**</span></span>
</dt> <dd>

<span data-ttu-id="f5f91-135">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="f5f91-135">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f5f91-136">URL-адрес веб-страницы, содержащей сведения об угрозе.</span><span class="sxs-lookup"><span data-stu-id="f5f91-136">A URL to a webpage containing information about the threat.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5f91-137">Требования</span><span class="sxs-lookup"><span data-stu-id="f5f91-137">Requirements</span></span>



| <span data-ttu-id="f5f91-138">Требование</span><span class="sxs-lookup"><span data-stu-id="f5f91-138">Requirement</span></span> | <span data-ttu-id="f5f91-139">Значение</span><span class="sxs-lookup"><span data-stu-id="f5f91-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f91-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5f91-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f5f91-141">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f5f91-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f5f91-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5f91-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f5f91-143">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f5f91-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5f91-144">Header</span><span class="sxs-lookup"><span data-stu-id="f5f91-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5f91-145"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5f91-145"><dt>MpClient.h</dt></span></span> </dl> |



 

 





