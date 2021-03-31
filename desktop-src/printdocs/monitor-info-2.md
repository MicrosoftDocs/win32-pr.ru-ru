---
description: В структуре MONITORing \_ \_ 2 определяется монитор.
ms.assetid: 4dd1ca15-6983-403e-8159-1a6d35a88162
title: Структура MONITOR_INFO_2 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_2
- _MONITOR_INFO_2A
- _MONITOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9d3ad70a0728ca6e73c4dbefb248df58e858a996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817897"
---
# <a name="monitor_info_2-structure"></a><span data-ttu-id="d975f-103">\_Структура мониторинга информации \_ 2</span><span class="sxs-lookup"><span data-stu-id="d975f-103">MONITOR\_INFO\_2 structure</span></span>

<span data-ttu-id="d975f-104">В структуре **Monitoring \_ \_ 2** определяется монитор.</span><span class="sxs-lookup"><span data-stu-id="d975f-104">The **MONITOR\_INFO\_2** structure identifies a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="d975f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d975f-105">Syntax</span></span>


```C++
typedef struct _MONITOR_INFO_2 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} MONITOR_INFO_2, *PMONITOR_INFO_2;
```



## <a name="members"></a><span data-ttu-id="d975f-106">Члены</span><span class="sxs-lookup"><span data-stu-id="d975f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d975f-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="d975f-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="d975f-108">Указатель на строку, завершающуюся нулем, которая является именем монитора.</span><span class="sxs-lookup"><span data-stu-id="d975f-108">A pointer to a null-terminated string that is the name of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="d975f-109">**пенвиронмент**</span><span class="sxs-lookup"><span data-stu-id="d975f-109">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="d975f-110">Указатель на строку, завершающуюся нулем, которая указывает среду, для которой был записан монитор (например, Windows NT x86, Windows IA64, Windows x64).</span><span class="sxs-lookup"><span data-stu-id="d975f-110">A pointer to a null-terminated string that specifies the environment for which the monitor was written (for example, Windows NT x86, Windows IA64, Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="d975f-111">**пдллнаме**</span><span class="sxs-lookup"><span data-stu-id="d975f-111">**pDLLName**</span></span>
</dt> <dd>

<span data-ttu-id="d975f-112">Указатель на строку, завершающуюся нулем, которая является именем библиотеки DLL монитора.</span><span class="sxs-lookup"><span data-stu-id="d975f-112">A pointer to a null-terminated string that is the name of the monitor DLL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d975f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d975f-113">Requirements</span></span>



| <span data-ttu-id="d975f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d975f-114">Requirement</span></span> | <span data-ttu-id="d975f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d975f-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d975f-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d975f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d975f-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d975f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d975f-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d975f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d975f-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d975f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d975f-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d975f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d975f-121"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d975f-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d975f-122">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="d975f-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d975f-123">**\_ \_ Сведения о \_ мониторинге 2W** (Юникод) и **\_ \_ сведения об мониторе \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d975f-123">**\_MONITOR\_INFO\_2W** (Unicode) and **\_MONITOR\_INFO\_2A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="d975f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d975f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d975f-125">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="d975f-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d975f-126">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="d975f-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="d975f-127">**аддмонитор**</span><span class="sxs-lookup"><span data-stu-id="d975f-127">**AddMonitor**</span></span>](addmonitor.md)
</dt> <dt>

[<span data-ttu-id="d975f-128">**енуммониторс**</span><span class="sxs-lookup"><span data-stu-id="d975f-128">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="d975f-129">**\_Сведения о мониторе \_ 1**</span><span class="sxs-lookup"><span data-stu-id="d975f-129">**MONITOR\_INFO\_1**</span></span>](monitor-info-1.md)
</dt> </dl>

 

 




