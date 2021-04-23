---
title: Структура MPTHREAT_DATA (Мпклиент. h)
description: Данные уведомления передаются из-за обнаружения или изменения угроз.
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- MPTHREAT_DATA структуры устаревшие функции среды Windows
- Функции PMPTHREAT_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPTHREAT_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cafbb11dbb3b1a34b38ffd0448db96fd1409efd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710549"
---
# <a name="mpthreat_data-structure"></a><span data-ttu-id="10bd4-105">\_Структура данных мпсреат</span><span class="sxs-lookup"><span data-stu-id="10bd4-105">MPTHREAT\_DATA structure</span></span>

<span data-ttu-id="10bd4-106">Данные уведомления передаются из-за обнаружения или изменения угроз.</span><span class="sxs-lookup"><span data-stu-id="10bd4-106">Notification data passed due to threat detection or modification.</span></span>

## <a name="syntax"></a><span data-ttu-id="10bd4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10bd4-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_DATA {
  MPTHREAT_ID     ThreatID;
  DWORD           dwSessionID;
  MPTHREAT_ACTION ThreatAction;
  DWORD           dwStatus;
} MPTHREAT_DATA, *PMPTHREAT_DATA;
```



## <a name="members"></a><span data-ttu-id="10bd4-108">Члены</span><span class="sxs-lookup"><span data-stu-id="10bd4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="10bd4-109">**среатид**</span><span class="sxs-lookup"><span data-stu-id="10bd4-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="10bd4-110">Тип: **мпсреат \_ ID**</span><span class="sxs-lookup"><span data-stu-id="10bd4-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="10bd4-111">Идентификатор угрозы.</span><span class="sxs-lookup"><span data-stu-id="10bd4-111">Threat identifier.</span></span> <span data-ttu-id="10bd4-112">Верхний бит задан для выявления угроз, связанных с антивирусной программой.</span><span class="sxs-lookup"><span data-stu-id="10bd4-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="10bd4-113">**двсессионид**</span><span class="sxs-lookup"><span data-stu-id="10bd4-113">**dwSessionID**</span></span>
</dt> <dd>

<span data-ttu-id="10bd4-114">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="10bd4-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="10bd4-115">Сеанс, связанный с угрозой.</span><span class="sxs-lookup"><span data-stu-id="10bd4-115">Session associated with the threat.</span></span> <span data-ttu-id="10bd4-116">Установите значение-1, если сведения о конкретном сеансе недоступны.</span><span class="sxs-lookup"><span data-stu-id="10bd4-116">Set to -1 if no session specific information is available.</span></span>

</dd> <dt>

<span data-ttu-id="10bd4-117">**среатактион**</span><span class="sxs-lookup"><span data-stu-id="10bd4-117">**ThreatAction**</span></span>
</dt> <dd>

<span data-ttu-id="10bd4-118">Тип: **[ **\_ действие мпсреат**](mpthreat-action.md)**</span><span class="sxs-lookup"><span data-stu-id="10bd4-118">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)**</span></span>

</dd> <dd>

<span data-ttu-id="10bd4-119">Действие угрозы попыталось **выполнить \_ \_ \_ очистку** от / **\_ \_ \_ сбоев** мпнотифи Threat мпнотифи.</span><span class="sxs-lookup"><span data-stu-id="10bd4-119">Threat action tried for the **MPNOTIFY\_THREAT\_CLEAN\_SUCCEEDED**/**MPNOTIFY\_THREAT\_CLEAN\_FAILED** events.</span></span>

</dd> <dt>

<span data-ttu-id="10bd4-120">**Dwstatus устанавливается**</span><span class="sxs-lookup"><span data-stu-id="10bd4-120">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="10bd4-121">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="10bd4-121">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="10bd4-122">Дополнительное состояние или действия, связанные с выполняемым действием.</span><span class="sxs-lookup"><span data-stu-id="10bd4-122">Additional status or actions associated with the action taken.</span></span> <span data-ttu-id="10bd4-123">Это сочетание битовых флагов из [**\_ флага мпстатус**](mpstatus-flag.md).</span><span class="sxs-lookup"><span data-stu-id="10bd4-123">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10bd4-124">Требования</span><span class="sxs-lookup"><span data-stu-id="10bd4-124">Requirements</span></span>



| <span data-ttu-id="10bd4-125">Требование</span><span class="sxs-lookup"><span data-stu-id="10bd4-125">Requirement</span></span> | <span data-ttu-id="10bd4-126">Значение</span><span class="sxs-lookup"><span data-stu-id="10bd4-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10bd4-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10bd4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="10bd4-128">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="10bd4-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="10bd4-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10bd4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="10bd4-130">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="10bd4-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10bd4-131">Header</span><span class="sxs-lookup"><span data-stu-id="10bd4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="10bd4-132"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="10bd4-132"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10bd4-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10bd4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10bd4-134">**\_флаг мпстатус**</span><span class="sxs-lookup"><span data-stu-id="10bd4-134">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="10bd4-135">**\_действие мпсреат**</span><span class="sxs-lookup"><span data-stu-id="10bd4-135">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> </dl>

 

 





