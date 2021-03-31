---
description: '\_Структура сведений о задании \_ 3 используется для связывания набора заданий печати.'
ms.assetid: a110f555-dc33-450c-ae77-ea26f0f69448
title: Структура JOB_INFO_3 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76cbb6c019878d9c392d21caa40c604df3a5f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272482"
---
# <a name="job_info_3-structure"></a><span data-ttu-id="b88ef-103">\_Структура сведений о задании \_ 3</span><span class="sxs-lookup"><span data-stu-id="b88ef-103">JOB\_INFO\_3 structure</span></span>

<span data-ttu-id="b88ef-104">Структура **\_ сведений о \_ задании 3** используется для связывания набора заданий печати.</span><span class="sxs-lookup"><span data-stu-id="b88ef-104">The **JOB\_INFO\_3** structure is used to link together a set of print jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="b88ef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b88ef-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_3 {
  DWORD JobId;
  DWORD NextJobId;
  DWORD Reserved;
} JOB_INFO_3, *PJOB_INFO_3;
```



## <a name="members"></a><span data-ttu-id="b88ef-106">Члены</span><span class="sxs-lookup"><span data-stu-id="b88ef-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b88ef-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="b88ef-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="b88ef-108">Идентификатор задания печати.</span><span class="sxs-lookup"><span data-stu-id="b88ef-108">The print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b88ef-109">**некстжобид**</span><span class="sxs-lookup"><span data-stu-id="b88ef-109">**NextJobId**</span></span>
</dt> <dd>

<span data-ttu-id="b88ef-110">Идентификатор задания печати для следующего задания печати в связанном наборе заданий печати.</span><span class="sxs-lookup"><span data-stu-id="b88ef-110">The print job identifier for the next print job in the linked set of print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="b88ef-111">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="b88ef-111">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="b88ef-112">Это значение зарезервировано для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="b88ef-112">This value is reserved for future use.</span></span> <span data-ttu-id="b88ef-113">Необходимо присвоить ему нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="b88ef-113">You must set it to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b88ef-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b88ef-114">Requirements</span></span>



| <span data-ttu-id="b88ef-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b88ef-115">Requirement</span></span> | <span data-ttu-id="b88ef-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b88ef-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b88ef-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b88ef-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b88ef-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b88ef-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b88ef-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b88ef-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b88ef-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b88ef-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b88ef-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b88ef-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b88ef-122"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b88ef-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b88ef-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b88ef-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b88ef-124">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="b88ef-124">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b88ef-125">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="b88ef-125">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="b88ef-126">**енумжобс**</span><span class="sxs-lookup"><span data-stu-id="b88ef-126">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="b88ef-127">**жетжоб**</span><span class="sxs-lookup"><span data-stu-id="b88ef-127">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="b88ef-128">**сетжоб**</span><span class="sxs-lookup"><span data-stu-id="b88ef-128">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

 




