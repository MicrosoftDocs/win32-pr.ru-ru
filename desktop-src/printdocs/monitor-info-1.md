---
description: Структура монитора \_ info \_ 1 определяет установленный монитор.
ms.assetid: 7a4660bd-5df8-49dd-92f6-9574f451f10d
title: Структура MONITOR_INFO_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_1
- _MONITOR_INFO_1A
- _MONITOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b6af1e1b9111ac6221273f2faf68fc6ed70e07a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693060"
---
# <a name="monitor_info_1-structure"></a><span data-ttu-id="a99b6-103">\_Структура мониторинга info \_ 1</span><span class="sxs-lookup"><span data-stu-id="a99b6-103">MONITOR\_INFO\_1 structure</span></span>

<span data-ttu-id="a99b6-104">Структура **монитора \_ info \_ 1** определяет установленный монитор.</span><span class="sxs-lookup"><span data-stu-id="a99b6-104">The **MONITOR\_INFO\_1** structure identifies an installed monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="a99b6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a99b6-105">Syntax</span></span>


```C++
typedef struct _MONITOR_INFO_1 {
  LPTSTR pName;
} MONITOR_INFO_1, *PMONITOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="a99b6-106">Члены</span><span class="sxs-lookup"><span data-stu-id="a99b6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a99b6-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="a99b6-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="a99b6-108">Указатель на строку, завершающуюся нулем, которая определяет установленный монитор.</span><span class="sxs-lookup"><span data-stu-id="a99b6-108">A pointer to a null-terminated string that identifies an installed monitor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a99b6-109">Требования</span><span class="sxs-lookup"><span data-stu-id="a99b6-109">Requirements</span></span>



| <span data-ttu-id="a99b6-110">Требование</span><span class="sxs-lookup"><span data-stu-id="a99b6-110">Requirement</span></span> | <span data-ttu-id="a99b6-111">Значение</span><span class="sxs-lookup"><span data-stu-id="a99b6-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a99b6-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a99b6-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a99b6-113">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a99b6-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a99b6-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a99b6-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a99b6-115">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a99b6-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a99b6-116">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a99b6-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="a99b6-117"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a99b6-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a99b6-118">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="a99b6-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a99b6-119">**\_ Сведения об мониторе \_ \_ 1W** (Юникод) и **\_ \_ сведения об мониторе \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a99b6-119">**\_MONITOR\_INFO\_1W** (Unicode) and **\_MONITOR\_INFO\_1A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="a99b6-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a99b6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a99b6-121">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="a99b6-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a99b6-122">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="a99b6-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="a99b6-123">**енуммониторс**</span><span class="sxs-lookup"><span data-stu-id="a99b6-123">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="a99b6-124">**\_Сведения о мониторе \_ 2**</span><span class="sxs-lookup"><span data-stu-id="a99b6-124">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

 




