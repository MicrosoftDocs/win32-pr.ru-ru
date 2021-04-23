---
title: Структура MPCONFIGURATION_DATA (Мпклиент. h)
description: Содержит данные об изменениях конфигурации, включая старые и новые значения.
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- MPCONFIGURATION_DATA структуры устаревшие функции среды Windows
- Функции PMPCONFIGURATION_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPCONFIGURATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb54ae4e323f2144dd25c52005d8484b0a207e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071475"
---
# <a name="mpconfiguration_data-structure"></a><span data-ttu-id="ca82f-105">\_Структура данных мпконфигуратион</span><span class="sxs-lookup"><span data-stu-id="ca82f-105">MPCONFIGURATION\_DATA structure</span></span>

<span data-ttu-id="ca82f-106">Содержит данные об изменениях конфигурации, включая старые и новые значения.</span><span class="sxs-lookup"><span data-stu-id="ca82f-106">Contains data about configuration changes, including the old and new values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca82f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca82f-107">Syntax</span></span>


```C++
typedef struct tagMPCONFIGURATION_DATA {
  MP_MIDL_STRING LPWSTR ConfigurationName;
  DWORD                 DataType;
  DWORD                 PreviousDataSize;
  BYTE                  *pPreviousData;
  DWORD                 CurrentDataSize;
  BYTE                  *pCurrentData;
} MPCONFIGURATION_DATA, *PMPCONFIGURATION_DATA;
```



## <a name="members"></a><span data-ttu-id="ca82f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="ca82f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca82f-109">**ConfigurationName**</span><span class="sxs-lookup"><span data-stu-id="ca82f-109">**ConfigurationName**</span></span>
</dt> <dd>

<span data-ttu-id="ca82f-110">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="ca82f-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="ca82f-111">Имя измененной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ca82f-111">Name of the configuration that changed.</span></span>

</dd> <dt>

<span data-ttu-id="ca82f-112">**DataType**</span><span class="sxs-lookup"><span data-stu-id="ca82f-112">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="ca82f-113">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ca82f-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ca82f-114">Тип используемых данных.</span><span class="sxs-lookup"><span data-stu-id="ca82f-114">The type of data used.</span></span>

</dd> <dt>

<span data-ttu-id="ca82f-115">**превиаусдатасизе**</span><span class="sxs-lookup"><span data-stu-id="ca82f-115">**PreviousDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="ca82f-116">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ca82f-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ca82f-117">Размер предыдущих данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="ca82f-117">Size of previous data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ca82f-118">**ппревиаусдата**</span><span class="sxs-lookup"><span data-stu-id="ca82f-118">**pPreviousData**</span></span>
</dt> <dd>

<span data-ttu-id="ca82f-119">Тип: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="ca82f-119">Type: \**BYTE\** _</span></span>

</dd> <dd>

<span data-ttu-id="ca82f-120">Указатель на предыдущие данные.</span><span class="sxs-lookup"><span data-stu-id="ca82f-120">Pointer to previous data.</span></span>

</dd> <dt>

<span data-ttu-id="ca82f-121">_ *Куррентдатасизе*\*</span><span class="sxs-lookup"><span data-stu-id="ca82f-121">_ *CurrentDataSize*\*</span></span>
</dt> <dd>

<span data-ttu-id="ca82f-122">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ca82f-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ca82f-123">Размер новых данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="ca82f-123">Size of new data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ca82f-124">**пкуррентдата**</span><span class="sxs-lookup"><span data-stu-id="ca82f-124">**pCurrentData**</span></span>
</dt> <dd>

<span data-ttu-id="ca82f-125">Тип: **Byte \***</span><span class="sxs-lookup"><span data-stu-id="ca82f-125">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="ca82f-126">Указатель на новые данные.</span><span class="sxs-lookup"><span data-stu-id="ca82f-126">Pointer to new data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca82f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="ca82f-127">Requirements</span></span>



| <span data-ttu-id="ca82f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="ca82f-128">Requirement</span></span> | <span data-ttu-id="ca82f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ca82f-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca82f-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca82f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ca82f-131">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ca82f-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ca82f-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca82f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ca82f-133">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ca82f-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca82f-134">Header</span><span class="sxs-lookup"><span data-stu-id="ca82f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca82f-135"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca82f-135"><dt>MpClient.h</dt></span></span> </dl> |



 

 





