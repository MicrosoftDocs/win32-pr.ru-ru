---
description: Структура ХАНДОФФТАБЛЕ определяет протоколы переданной таблицы.
ms.assetid: 6bb7465b-c1ba-4ffe-aecf-8125993c309a
title: Структура ХАНДОФФТАБЛЕ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 842ef9fde56ff6b4c420034b861aa8c151e7e6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662177"
---
# <a name="handofftable-structure"></a><span data-ttu-id="82d6a-103">Структура ХАНДОФФТАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="82d6a-103">HANDOFFTABLE structure</span></span>

<span data-ttu-id="82d6a-104">Структура **хандоффтабле** определяет протоколы переданной таблицы.</span><span class="sxs-lookup"><span data-stu-id="82d6a-104">The **HANDOFFTABLE** structure defines the protocols of a handoff table.</span></span>

<span data-ttu-id="82d6a-105">Эта структура заполняется сетевой монитор на основе информации в предоставленном пользователем ini-файле, предоставленном при вызове функции [**креатехандоффтабле**](createhandofftable.md) .</span><span class="sxs-lookup"><span data-stu-id="82d6a-105">This structure is filled in by Network Monitor based on information in a user supplied .ini file provided when calling the [**CreateHandoffTable**](createhandofftable.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="82d6a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82d6a-106">Syntax</span></span>


```C++
typedef struct HANDOFFTABLE {
  DWORD          hot_sig;
  DWORD          hot_NumEntries;
  LPHANDOFFENTRY hot_Entries;
} HANDOFFTABLE, *LPHANDOFFTABLE;
```



## <a name="members"></a><span data-ttu-id="82d6a-107">Члены</span><span class="sxs-lookup"><span data-stu-id="82d6a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="82d6a-108">**Горячая \_ подпись**</span><span class="sxs-lookup"><span data-stu-id="82d6a-108">**hot\_sig**</span></span>
</dt> <dd>

<span data-ttu-id="82d6a-109">Сигнатура, которая идентифицирует эту таблицу как таблицу переданных.</span><span class="sxs-lookup"><span data-stu-id="82d6a-109">Signature that identifies this table as a handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="82d6a-110">**горячий \_ нументриес**</span><span class="sxs-lookup"><span data-stu-id="82d6a-110">**hot\_NumEntries**</span></span>
</dt> <dd>

<span data-ttu-id="82d6a-111">Число записей, которые сетевой монитор добавить в таблицу передачи.</span><span class="sxs-lookup"><span data-stu-id="82d6a-111">Number of entries that Network Monitor added to the handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="82d6a-112">**горячий \_ записи**</span><span class="sxs-lookup"><span data-stu-id="82d6a-112">**hot\_Entries**</span></span>
</dt> <dd>

<span data-ttu-id="82d6a-113">Таблица передачи.</span><span class="sxs-lookup"><span data-stu-id="82d6a-113">Handoff table.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82d6a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82d6a-114">Remarks</span></span>

<span data-ttu-id="82d6a-115">Эта структура и связанные с ней структуры ХАНДОФФЕНТРИ заполняются с помощью сетевой монитор, когда сетевой монитор создает таблицу передачи.</span><span class="sxs-lookup"><span data-stu-id="82d6a-115">This structure, and its associated HANDOFFENTRY structures, are filled in by Network Monitor when Network Monitor creates a handoff table.</span></span>

<span data-ttu-id="82d6a-116">Сведения о протоколе, используемые при создании таблицы передачи, предоставляются в ini-файле, предоставляемом приложением при вызове [**креатехандоффтабле**](createhandofftable.md) .</span><span class="sxs-lookup"><span data-stu-id="82d6a-116">The protocol information that is used when creating a handoff table is provided in an .ini file supplied by the application when [**CreateHandoffTable**](createhandofftable.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="82d6a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="82d6a-117">Requirements</span></span>



| <span data-ttu-id="82d6a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="82d6a-118">Requirement</span></span> | <span data-ttu-id="82d6a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="82d6a-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="82d6a-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82d6a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="82d6a-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="82d6a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="82d6a-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82d6a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="82d6a-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="82d6a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="82d6a-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="82d6a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="82d6a-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="82d6a-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82d6a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82d6a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d6a-127">хандоффентри</span><span class="sxs-lookup"><span data-stu-id="82d6a-127">HANDOFFENTRY</span></span>](handoffentry.md)
</dt> <dt>

[<span data-ttu-id="82d6a-128">креатехандоффтабле</span><span class="sxs-lookup"><span data-stu-id="82d6a-128">CreateHandoffTable</span></span>](createhandofftable.md)
</dt> </dl>

 

 




