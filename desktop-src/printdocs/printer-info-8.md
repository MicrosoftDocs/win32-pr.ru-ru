---
description: В \_ структуре "сведения о принтере \_ 8" указаны глобальные параметры принтера по умолчанию.
ms.assetid: 98f26a45-5302-4358-bed6-691d9bc37554
title: Структура PRINTER_INFO_8 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_8
- _PRINTER_INFO_8A
- _PRINTER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e17780dc2f39dc3041e690de1ef7b5728c8743e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912959"
---
# <a name="printer_info_8-structure"></a><span data-ttu-id="426d2-103">\_Сведения о принтере \_ 8 структура</span><span class="sxs-lookup"><span data-stu-id="426d2-103">PRINTER\_INFO\_8 structure</span></span>

<span data-ttu-id="426d2-104">В структуре " **\_ сведения о принтере \_ 8** " указаны глобальные параметры принтера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="426d2-104">The **PRINTER\_INFO\_8** structure specifies the global default printer settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="426d2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="426d2-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_8 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_8, *PPRINTER_INFO_8;
```



## <a name="members"></a><span data-ttu-id="426d2-106">Члены</span><span class="sxs-lookup"><span data-stu-id="426d2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="426d2-107">**пдевмоде**</span><span class="sxs-lookup"><span data-stu-id="426d2-107">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="426d2-108">Указатель на структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , определяющую глобальные данные принтера по умолчанию, такие как ориентация бумаги и разрешение.</span><span class="sxs-lookup"><span data-stu-id="426d2-108">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines the global default printer data such as the paper orientation and the resolution.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="426d2-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="426d2-109">Remarks</span></span>

<span data-ttu-id="426d2-110">Глобальные значения по умолчанию задаются администратором принтера, который может использоваться любым пользователем.</span><span class="sxs-lookup"><span data-stu-id="426d2-110">The global defaults are set by the administrator of a printer that can be used by anyone.</span></span> <span data-ttu-id="426d2-111">В отличие от этого значения по умолчанию для каждого пользователя влияют на конкретного пользователя или других пользователей, использующих этот профиль.</span><span class="sxs-lookup"><span data-stu-id="426d2-111">In contrast, the per-user defaults will affect a particular user or anyone else who uses the profile.</span></span> <span data-ttu-id="426d2-112">Для параметров по умолчанию для каждого пользователя [**Используйте \_ сведения \_ о принтере 9**](printer-info-9.md).</span><span class="sxs-lookup"><span data-stu-id="426d2-112">For per-user defaults, use [**PRINTER\_INFO\_9**](printer-info-9.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="426d2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="426d2-113">Requirements</span></span>



| <span data-ttu-id="426d2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="426d2-114">Requirement</span></span> | <span data-ttu-id="426d2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="426d2-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="426d2-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="426d2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="426d2-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="426d2-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="426d2-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="426d2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="426d2-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="426d2-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="426d2-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="426d2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="426d2-121"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="426d2-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="426d2-122">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="426d2-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="426d2-123">**\_ \_ Сведения о \_ принтере 8W** (Юникод) и **\_ \_ \_ 8A info** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="426d2-123">**\_PRINTER\_INFO\_8W** (Unicode) and **\_PRINTER\_INFO\_8A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="426d2-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="426d2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="426d2-125">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="426d2-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="426d2-126">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="426d2-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="426d2-127">**Наложение**</span><span class="sxs-lookup"><span data-stu-id="426d2-127">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="426d2-128">**сетпринтер**</span><span class="sxs-lookup"><span data-stu-id="426d2-128">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="426d2-129">**\_Сведения о принтере \_ 9**</span><span class="sxs-lookup"><span data-stu-id="426d2-129">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> </dl>

 

 




