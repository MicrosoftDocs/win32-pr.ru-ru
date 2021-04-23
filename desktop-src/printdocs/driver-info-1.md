---
description: Структура драйвера \_ \_ 1 определяет драйвер принтера.
ms.assetid: 9435192b-3eba-4937-8cd3-bff4e9eb84d3
title: Структура DRIVER_INFO_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_1
- _DRIVER_INFO_1A
- _DRIVER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 21301cdab4449d0a48254660d195d4f2507a80e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712704"
---
# <a name="driver_info_1-structure"></a><span data-ttu-id="38031-103">\_Структура сведений о драйвере \_ 1</span><span class="sxs-lookup"><span data-stu-id="38031-103">DRIVER\_INFO\_1 structure</span></span>

<span data-ttu-id="38031-104">Структура **драйвера \_ \_ 1** определяет драйвер принтера.</span><span class="sxs-lookup"><span data-stu-id="38031-104">The **DRIVER\_INFO\_1** structure identifies a printer driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="38031-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38031-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_1 {
  LPTSTR pName;
} DRIVER_INFO_1, *PDRIVER_INFO_1;
```



## <a name="members"></a><span data-ttu-id="38031-106">Члены</span><span class="sxs-lookup"><span data-stu-id="38031-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="38031-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="38031-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="38031-108">Указатель на строку, завершающуюся нулем, которая указывает имя драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="38031-108">Pointer to a null-terminated string that specifies the name of a printer driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38031-109">Требования</span><span class="sxs-lookup"><span data-stu-id="38031-109">Requirements</span></span>



| <span data-ttu-id="38031-110">Требование</span><span class="sxs-lookup"><span data-stu-id="38031-110">Requirement</span></span> | <span data-ttu-id="38031-111">Значение</span><span class="sxs-lookup"><span data-stu-id="38031-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38031-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38031-112">Minimum supported client</span></span><br/> | <span data-ttu-id="38031-113">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="38031-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="38031-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38031-114">Minimum supported server</span></span><br/> | <span data-ttu-id="38031-115">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="38031-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="38031-116">Заголовок</span><span class="sxs-lookup"><span data-stu-id="38031-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="38031-117"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38031-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="38031-118">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="38031-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="38031-119">**\_ \_ Сведения о \_ драйвере 1W** (Юникод) и **\_ драйвер \_ \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="38031-119">**\_DRIVER\_INFO\_1W** (Unicode) and **\_DRIVER\_INFO\_1A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="38031-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38031-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38031-121">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="38031-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="38031-122">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="38031-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="38031-123">**енумпринтердриверс**</span><span class="sxs-lookup"><span data-stu-id="38031-123">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> </dl>

 

 




