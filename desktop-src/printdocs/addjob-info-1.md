---
description: Структура ADDJOB \_ info \_ 1 определяет задание печати, а также каталог и файл, в котором приложение может сохранить это задание.
ms.assetid: de915932-11a7-47e8-9be9-edab76d94189
title: Структура ADDJOB_INFO_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDJOB_INFO_1
- _ADDJOB_INFO_1A
- _ADDJOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 08197a6a72da7e38a349014e08d2d2c2c946f6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272492"
---
# <a name="addjob_info_1-structure"></a><span data-ttu-id="0749c-103">\_Структура ADDJOB info \_ 1</span><span class="sxs-lookup"><span data-stu-id="0749c-103">ADDJOB\_INFO\_1 structure</span></span>

<span data-ttu-id="0749c-104">Структура **ADDJOB \_ info \_ 1** определяет задание печати, а также каталог и файл, в котором приложение может сохранить это задание.</span><span class="sxs-lookup"><span data-stu-id="0749c-104">The **ADDJOB\_INFO\_1** structure identifies a print job as well as the directory and file in which an application can store that job.</span></span>

## <a name="syntax"></a><span data-ttu-id="0749c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0749c-105">Syntax</span></span>


```C++
typedef struct _ADDJOB_INFO_1 {
  LPTSTR Path;
  DWORD  JobId;
} ADDJOB_INFO_1, *PADDJOB_INFO_1;
```



## <a name="members"></a><span data-ttu-id="0749c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="0749c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0749c-107">**Путь**</span><span class="sxs-lookup"><span data-stu-id="0749c-107">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="0749c-108">Указатель на строку, завершающуюся нулем, которая содержит путь и имя файла, которые приложение может использовать для хранения задания печати.</span><span class="sxs-lookup"><span data-stu-id="0749c-108">Pointer to a null-terminated string that contains the path and file name that the application can use to store the print job.</span></span>

</dd> <dt>

<span data-ttu-id="0749c-109">**JobId**</span><span class="sxs-lookup"><span data-stu-id="0749c-109">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="0749c-110">Маркер задания печати.</span><span class="sxs-lookup"><span data-stu-id="0749c-110">A handle to the print job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0749c-111">Требования</span><span class="sxs-lookup"><span data-stu-id="0749c-111">Requirements</span></span>



| <span data-ttu-id="0749c-112">Требование</span><span class="sxs-lookup"><span data-stu-id="0749c-112">Requirement</span></span> | <span data-ttu-id="0749c-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0749c-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0749c-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0749c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0749c-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0749c-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0749c-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0749c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0749c-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0749c-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0749c-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0749c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0749c-119"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0749c-119"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0749c-120">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="0749c-120">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0749c-121">**\_ \_ Сведения о ADDJOB \_ 1W** (Юникод) и **\_ ADDJOB \_ info \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0749c-121">**\_ADDJOB\_INFO\_1W** (Unicode) and **\_ADDJOB\_INFO\_1A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="0749c-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0749c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0749c-123">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="0749c-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0749c-124">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="0749c-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="0749c-125">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="0749c-125">**AddJob**</span></span>](addjob.md)
</dt> </dl>

 

 




