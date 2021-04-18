---
description: В \_ структуре "сведения о принтере \_ 9" указаны параметры принтера по умолчанию для каждого пользователя.
ms.assetid: 8bafb995-f31c-46e3-a950-45e240c678aa
title: Структура PRINTER_INFO_9 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_9
- _PRINTER_INFO_9A
- _PRINTER_INFO_9W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c0ae3c099da17d7fc437a67035d8da2cd00136bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719700"
---
# <a name="printer_info_9-structure"></a><span data-ttu-id="f8bb6-103">\_Структура сведений о принтере \_ 9</span><span class="sxs-lookup"><span data-stu-id="f8bb6-103">PRINTER\_INFO\_9 structure</span></span>

<span data-ttu-id="f8bb6-104">В структуре " **\_ сведения о принтере \_ 9** " указаны параметры принтера по умолчанию для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-104">The **PRINTER\_INFO\_9** structure specifies the per-user default printer settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8bb6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8bb6-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_9 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_9, *PPRINTER_INFO_9;
```



## <a name="members"></a><span data-ttu-id="f8bb6-106">Члены</span><span class="sxs-lookup"><span data-stu-id="f8bb6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f8bb6-107">**пдевмоде**</span><span class="sxs-lookup"><span data-stu-id="f8bb6-107">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="f8bb6-108">Указатель на структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , определяющую данные принтера по умолчанию для каждого пользователя, такие как ориентация бумаги и разрешение.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-108">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines the per-user default printer data such as the paper orientation and the resolution.</span></span> <span data-ttu-id="f8bb6-109">**DEVMODE** хранится в реестре пользователя.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-109">The **DEVMODE** is stored in the user's registry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8bb6-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8bb6-110">Remarks</span></span>

<span data-ttu-id="f8bb6-111">Значения по умолчанию для каждого пользователя влияют только на конкретного пользователя или всех, кто использует этот профиль.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-111">The per-user defaults will affect only a particular user or anyone who uses the profile.</span></span> <span data-ttu-id="f8bb6-112">В отличие от них глобальные значения по умолчанию устанавливаются администратором принтера, который может использоваться любым пользователем.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-112">In contrast, the global defaults are set by the administrator of a printer that can be used by anyone.</span></span> <span data-ttu-id="f8bb6-113">Для глобальных значений по умолчанию [**Используйте \_ сведения \_ о принтере 8**](printer-info-8.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb6-113">For global defaults, use [**PRINTER\_INFO\_8**](printer-info-8.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8bb6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f8bb6-114">Requirements</span></span>



| <span data-ttu-id="f8bb6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f8bb6-115">Requirement</span></span> | <span data-ttu-id="f8bb6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f8bb6-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8bb6-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8bb6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f8bb6-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f8bb6-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f8bb6-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8bb6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f8bb6-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f8bb6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f8bb6-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f8bb6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8bb6-122"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8bb6-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f8bb6-123">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f8bb6-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f8bb6-124">**\_ \_ Сведения о \_ принтере 9W** (Юникод) и **\_ \_ \_ 9a info** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f8bb6-124">**\_PRINTER\_INFO\_9W** (Unicode) and **\_PRINTER\_INFO\_9A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="f8bb6-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8bb6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8bb6-126">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="f8bb6-126">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f8bb6-127">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="f8bb6-127">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f8bb6-128">**Наложение**</span><span class="sxs-lookup"><span data-stu-id="f8bb6-128">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="f8bb6-129">**сетпринтер**</span><span class="sxs-lookup"><span data-stu-id="f8bb6-129">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="f8bb6-130">**\_Сведения о принтере \_ 8**</span><span class="sxs-lookup"><span data-stu-id="f8bb6-130">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> </dl>

 

 




