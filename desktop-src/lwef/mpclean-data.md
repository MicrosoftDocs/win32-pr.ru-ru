---
title: Структура MPCLEAN_DATA (Мпклиент. h)
description: Данные уведомления передаются в функцию чистого обратного вызова.
ms.assetid: 475A6525-5BD8-4B29-A684-53EE2758C790
keywords:
- MPCLEAN_DATA структуры устаревшие функции среды Windows
- Функции PMPCLEAN_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPCLEAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f0c7e867918b6567279be7c41ce72e7e396576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801919"
---
# <a name="mpclean_data-structure"></a><span data-ttu-id="971be-105">\_Структура данных мпклеан</span><span class="sxs-lookup"><span data-stu-id="971be-105">MPCLEAN\_DATA structure</span></span>

<span data-ttu-id="971be-106">Данные уведомления передаются в функцию чистого обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="971be-106">Notification data passed to clean callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="971be-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="971be-107">Syntax</span></span>


```C++
typedef struct tagMPCLEAN_DATA {
  MPTHREAT_ID      ThreatID;
  MPTHREAT_ACTION  ThreatAction;
  DWORD            dwStatus;
  PMPRESOURCE_INFO ResourceInfo;
} MPCLEAN_DATA, *PMPCLEAN_DATA;
```



## <a name="members"></a><span data-ttu-id="971be-108">Члены</span><span class="sxs-lookup"><span data-stu-id="971be-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="971be-109">**среатид**</span><span class="sxs-lookup"><span data-stu-id="971be-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="971be-110">Тип: **мпсреат \_ ID**</span><span class="sxs-lookup"><span data-stu-id="971be-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="971be-111">Идентификатор угрозы для **мпнотифи \_ очистки \_ угрозы \_ запустить** / **мпнотифи \_ Clean \_ Threat \_ успешно** / **мпнотифи события \_ \_ \_ сбоя очистки** .</span><span class="sxs-lookup"><span data-stu-id="971be-111">Threat identifier for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="971be-112">Верхний бит задан для выявления угроз, связанных с антивирусной программой.</span><span class="sxs-lookup"><span data-stu-id="971be-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="971be-113">**среатактион**</span><span class="sxs-lookup"><span data-stu-id="971be-113">**ThreatAction**</span></span>
</dt> <dd>

<span data-ttu-id="971be-114">Тип: **[ **\_ действие мпсреат**](mpthreat-action.md)**</span><span class="sxs-lookup"><span data-stu-id="971be-114">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)**</span></span>

</dd> <dd>

<span data-ttu-id="971be-115">Действие угрозы для **мпнотифи " \_ Очистка \_ \_ после** сбоя" мпнотифи "очистить угрозу" / **\_ \_ \_** / .**мпнотифи удалить события с \_ \_ \_ ошибками** .</span><span class="sxs-lookup"><span data-stu-id="971be-115">Threat action for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="971be-116">См. раздел [**\_ действие мпсреат**](mpthreat-action.md).</span><span class="sxs-lookup"><span data-stu-id="971be-116">See [**MPTHREAT\_ACTION**](mpthreat-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="971be-117">**Dwstatus устанавливается**</span><span class="sxs-lookup"><span data-stu-id="971be-117">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="971be-118">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="971be-118">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="971be-119">Дополнительное состояние или действия, связанные с выполняемым действием.</span><span class="sxs-lookup"><span data-stu-id="971be-119">Additional status or actions associated with the action taken.</span></span> <span data-ttu-id="971be-120">Это сочетание битовых флагов из [**\_ флага мпстатус**](mpstatus-flag.md).</span><span class="sxs-lookup"><span data-stu-id="971be-120">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="971be-121">**ресаурцеинфо**</span><span class="sxs-lookup"><span data-stu-id="971be-121">**ResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="971be-122">Тип: **пмпресаурце \_ info** .</span><span class="sxs-lookup"><span data-stu-id="971be-122">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="971be-123">Сведения о ресурсах **для \_ мпнотифи \_ очистки \_** мпнотифи об очистке угрозы "Очистка после сбоя" / **\_ \_ \_** / **мпнотифи " \_ очистить \_ угрозу \_** ".</span><span class="sxs-lookup"><span data-stu-id="971be-123">Resource information for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="971be-124">См [**. \_ сведения о мпресаурце**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="971be-124">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="971be-125">Требования</span><span class="sxs-lookup"><span data-stu-id="971be-125">Requirements</span></span>



| <span data-ttu-id="971be-126">Требование</span><span class="sxs-lookup"><span data-stu-id="971be-126">Requirement</span></span> | <span data-ttu-id="971be-127">Значение</span><span class="sxs-lookup"><span data-stu-id="971be-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="971be-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="971be-128">Minimum supported client</span></span><br/> | <span data-ttu-id="971be-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="971be-129">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="971be-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="971be-130">Minimum supported server</span></span><br/> | <span data-ttu-id="971be-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="971be-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="971be-132">Header</span><span class="sxs-lookup"><span data-stu-id="971be-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="971be-133"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="971be-133"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="971be-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="971be-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="971be-135">**\_сведения о мпресаурце**</span><span class="sxs-lookup"><span data-stu-id="971be-135">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="971be-136">**\_флаг мпстатус**</span><span class="sxs-lookup"><span data-stu-id="971be-136">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="971be-137">**\_действие мпсреат**</span><span class="sxs-lookup"><span data-stu-id="971be-137">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> </dl>

 

 





