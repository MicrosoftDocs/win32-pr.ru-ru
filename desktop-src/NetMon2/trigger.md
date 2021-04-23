---
description: Структура ТРИГГЕРа указывает действие, выполняемое драйвером в указанное время.
ms.assetid: 63541796-b0d8-456c-8544-697fedbe05f7
title: Структура ТРИГГЕРа (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TRIGGER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d9b385557e3c34bdf75f2bf959d4e5e3e47e0750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674113"
---
# <a name="trigger-structure"></a><span data-ttu-id="53a7f-103">Структура ТРИГГЕРа</span><span class="sxs-lookup"><span data-stu-id="53a7f-103">TRIGGER structure</span></span>

<span data-ttu-id="53a7f-104">Структура **триггера** указывает действие, выполняемое драйвером в указанное время.</span><span class="sxs-lookup"><span data-stu-id="53a7f-104">The **TRIGGER** structure indicates an action to be taken by the driver at a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="53a7f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53a7f-105">Syntax</span></span>


```C++
typedef struct _TRIGGER {
  BOOL         TriggerActive;
  BYTE         TriggerType;
  BYTE         TriggerAction;
  DWORD        TriggerFlags;
  PATTERNMATCH TriggerPatternMatch;
  DWORD        TriggerBufferSize;
  DWORD        Reserved;
} TRIGGER, *LPTRIGGER;
```



## <a name="members"></a><span data-ttu-id="53a7f-106">Члены</span><span class="sxs-lookup"><span data-stu-id="53a7f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="53a7f-107">**тригжерактиве**</span><span class="sxs-lookup"><span data-stu-id="53a7f-107">**TriggerActive**</span></span>
</dt> <dd>

<span data-ttu-id="53a7f-108">Логическое значение, определяющее, должен ли триггер уделять внимание драйверу.</span><span class="sxs-lookup"><span data-stu-id="53a7f-108">A Boolean value that determines if the trigger should be paid attention to by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="53a7f-109">**TriggerType может принимать**</span><span class="sxs-lookup"><span data-stu-id="53a7f-109">**TriggerType**</span></span>
</dt> <dd>

<span data-ttu-id="53a7f-110">Код Op триггера.</span><span class="sxs-lookup"><span data-stu-id="53a7f-110">The op code of the trigger.</span></span>

</dd> <dt>

<span data-ttu-id="53a7f-111">**TriggerAction**</span><span class="sxs-lookup"><span data-stu-id="53a7f-111">**TriggerAction**</span></span>
</dt> <dd>

<span data-ttu-id="53a7f-112">Действие, выполняемое триггером при срабатывании.</span><span class="sxs-lookup"><span data-stu-id="53a7f-112">Action that the trigger is to take if it is fired.</span></span>

</dd> <dt>

<span data-ttu-id="53a7f-113">**тригжерфлагс**</span><span class="sxs-lookup"><span data-stu-id="53a7f-113">**TriggerFlags**</span></span>
</dt> <dd>

<span data-ttu-id="53a7f-114">Флаги триггера.</span><span class="sxs-lookup"><span data-stu-id="53a7f-114">Trigger flags.</span></span>

</dd> <dt>

<span data-ttu-id="53a7f-115">**тригжерпаттернматч**</span><span class="sxs-lookup"><span data-stu-id="53a7f-115">**TriggerPatternMatch**</span></span>
</dt> <dd>

<span data-ttu-id="53a7f-116">Сопоставление шаблона триггера.</span><span class="sxs-lookup"><span data-stu-id="53a7f-116">The trigger pattern match.</span></span>

</dd> <dt>

<span data-ttu-id="53a7f-117">**тригжербуфферсизе**</span><span class="sxs-lookup"><span data-stu-id="53a7f-117">**TriggerBufferSize**</span></span>
</dt> <dd>

<span data-ttu-id="53a7f-118">Размер буфера триггера.</span><span class="sxs-lookup"><span data-stu-id="53a7f-118">Trigger buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="53a7f-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="53a7f-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="53a7f-120">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="53a7f-120">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53a7f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="53a7f-121">Requirements</span></span>



| <span data-ttu-id="53a7f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="53a7f-122">Requirement</span></span> | <span data-ttu-id="53a7f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="53a7f-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="53a7f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53a7f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="53a7f-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="53a7f-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="53a7f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53a7f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="53a7f-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="53a7f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="53a7f-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="53a7f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="53a7f-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="53a7f-129"><dt>Netmon.h</dt></span></span> </dl> |



 

 




