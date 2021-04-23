---
description: Структура порта \_ info \_ 1 определяет поддерживаемый порт принтера.
ms.assetid: e474fe9c-e554-406a-a5bf-de07f9a72b32
title: Структура PORT_INFO_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_1
- _PORT_INFO_1A
- _PORT_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d64e7dfa29cbe6b3f7efd3aaa0076851aea0311b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702208"
---
# <a name="port_info_1-structure"></a><span data-ttu-id="3323f-103">\_Сведения о порте \_ 1 структура</span><span class="sxs-lookup"><span data-stu-id="3323f-103">PORT\_INFO\_1 structure</span></span>

<span data-ttu-id="3323f-104">Структура **порта \_ info \_ 1** определяет поддерживаемый порт принтера.</span><span class="sxs-lookup"><span data-stu-id="3323f-104">The **PORT\_INFO\_1** structure identifies a supported printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="3323f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3323f-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_1 {
  LPTSTR pName;
} PORT_INFO_1, *PPORT_INFO_1;
```



## <a name="members"></a><span data-ttu-id="3323f-106">Члены</span><span class="sxs-lookup"><span data-stu-id="3323f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3323f-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="3323f-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="3323f-108">Указатель на строку, завершающуюся нулем, которая определяет поддерживаемый порт принтера (например, "LPT1:").</span><span class="sxs-lookup"><span data-stu-id="3323f-108">Pointer to a null-terminated string that identifies a supported printer port (for example, "LPT1:").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3323f-109">Требования</span><span class="sxs-lookup"><span data-stu-id="3323f-109">Requirements</span></span>



| <span data-ttu-id="3323f-110">Требование</span><span class="sxs-lookup"><span data-stu-id="3323f-110">Requirement</span></span> | <span data-ttu-id="3323f-111">Значение</span><span class="sxs-lookup"><span data-stu-id="3323f-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3323f-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3323f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3323f-113">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3323f-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3323f-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3323f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3323f-115">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3323f-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3323f-116">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3323f-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="3323f-117"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3323f-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3323f-118">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="3323f-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3323f-119">**\_ \_ Сведения о \_ порте 1W** (Юникод) и **\_ \_ сведения о порте \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3323f-119">**\_PORT\_INFO\_1W** (Unicode) and **\_PORT\_INFO\_1A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="3323f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3323f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3323f-121">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="3323f-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3323f-122">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="3323f-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="3323f-123">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="3323f-123">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




