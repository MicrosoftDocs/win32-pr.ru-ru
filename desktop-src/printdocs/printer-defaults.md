---
description: Структура ПРИНТЕРов \_ по умолчанию задает тип данных, среду, данные инициализации и права доступа для принтера.
ms.assetid: df29c3a6-b1d1-4d40-887d-5ffc032a5871
title: Структура PRINTER_DEFAULTS (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_DEFAULTS
- _PRINTER_DEFAULTSA
- _PRINTER_DEFAULTSW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ad3f9b2a6647c620b2d947bca5ef5201076e23ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673949"
---
# <a name="printer_defaults-structure"></a><span data-ttu-id="52b2b-103">\_Структура по умолчанию для принтера</span><span class="sxs-lookup"><span data-stu-id="52b2b-103">PRINTER\_DEFAULTS structure</span></span>

<span data-ttu-id="52b2b-104">Структура **принтеров \_ по умолчанию** задает тип данных, среду, данные инициализации и права доступа для принтера.</span><span class="sxs-lookup"><span data-stu-id="52b2b-104">The **PRINTER\_DEFAULTS** structure specifies the default data type, environment, initialization data, and access rights for a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="52b2b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52b2b-105">Syntax</span></span>


```C++
typedef struct _PRINTER_DEFAULTS {
  LPTSTR      pDatatype;
  LPDEVMODE   pDevMode;
  ACCESS_MASK DesiredAccess;
} PRINTER_DEFAULTS, *PPRINTER_DEFAULTS;
```



## <a name="members"></a><span data-ttu-id="52b2b-106">Члены</span><span class="sxs-lookup"><span data-stu-id="52b2b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="52b2b-107">**пдататипе**</span><span class="sxs-lookup"><span data-stu-id="52b2b-107">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="52b2b-108">Указатель на строку, завершающуюся нулем, которая указывает тип данных по умолчанию для принтера.</span><span class="sxs-lookup"><span data-stu-id="52b2b-108">Pointer to a null-terminated string that specifies the default data type for a printer.</span></span>

</dd> <dt>

<span data-ttu-id="52b2b-109">**пдевмоде**</span><span class="sxs-lookup"><span data-stu-id="52b2b-109">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="52b2b-110">Указатель на структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , которая определяет среду по умолчанию и данные инициализации для принтера.</span><span class="sxs-lookup"><span data-stu-id="52b2b-110">Pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that identifies the default environment and initialization data for a printer.</span></span>

</dd> <dt>

<span data-ttu-id="52b2b-111">**DesiredAccess**</span><span class="sxs-lookup"><span data-stu-id="52b2b-111">**DesiredAccess**</span></span>
</dt> <dd>

<span data-ttu-id="52b2b-112">Задает необходимые права доступа к принтеру.</span><span class="sxs-lookup"><span data-stu-id="52b2b-112">Specifies desired access rights for a printer.</span></span> <span data-ttu-id="52b2b-113">Функция [**опенпринтер**](openprinter.md) использует этот член для задания прав доступа к принтеру.</span><span class="sxs-lookup"><span data-stu-id="52b2b-113">The [**OpenPrinter**](openprinter.md) function uses this member to set access rights to the printer.</span></span> <span data-ttu-id="52b2b-114">Эти права могут повлиять на работу функций [**сетпринтер**](setprinter.md) и [**делетепринтер**](deleteprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="52b2b-114">These rights can affect the operation of the [**SetPrinter**](setprinter.md) and [**DeletePrinter**](deleteprinter.md) functions.</span></span> <span data-ttu-id="52b2b-115">Права доступа могут быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="52b2b-115">The access rights can be one of the following.</span></span>



| <span data-ttu-id="52b2b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="52b2b-116">Value</span></span>                                       | <span data-ttu-id="52b2b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="52b2b-117">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52b2b-118">доступ к ПРИНТЕРу — \_ \_ Администрирование</span><span class="sxs-lookup"><span data-stu-id="52b2b-118">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="52b2b-119">Для выполнения административных задач, например, предоставляемых [**сетпринтер**](setprinter.md).</span><span class="sxs-lookup"><span data-stu-id="52b2b-119">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="52b2b-120">\_Использование доступа к принтерам \_</span><span class="sxs-lookup"><span data-stu-id="52b2b-120">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="52b2b-121">Для выполнения основных операций печати.</span><span class="sxs-lookup"><span data-stu-id="52b2b-121">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="52b2b-122">доступ к ПРИНТЕРу — \_ \_ Управление \_ ограниченным доступом</span><span class="sxs-lookup"><span data-stu-id="52b2b-122">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="52b2b-123">Для выполнения административных задач, например, предоставляемых [**сетпринтер**](setprinter.md) и [**сетпринтердата**](setprinterdata.md).</span><span class="sxs-lookup"><span data-stu-id="52b2b-123">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="52b2b-124">Это значение доступно начиная с Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="52b2b-124">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="52b2b-125">\_доступ ко всем принтерам \_</span><span class="sxs-lookup"><span data-stu-id="52b2b-125">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="52b2b-126">Для выполнения всех административных задач и базовых операций печати, за исключением синхронизации (см. раздел [стандартные права доступа](/windows/desktop/SecAuthZ/standard-access-rights) ).</span><span class="sxs-lookup"><span data-stu-id="52b2b-126">To perform all administrative tasks and basic printing operations except for SYNCHRONIZE (see [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights) ).</span></span>                                   |
| <span data-ttu-id="52b2b-127">универсальные значения безопасности, такие как запись \_ DAC</span><span class="sxs-lookup"><span data-stu-id="52b2b-127">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="52b2b-128">Для разрешения конкретных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="52b2b-128">To allow specific control access rights.</span></span> <span data-ttu-id="52b2b-129">См. раздел [стандартные права доступа](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="52b2b-129">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52b2b-130">Требования</span><span class="sxs-lookup"><span data-stu-id="52b2b-130">Requirements</span></span>



| <span data-ttu-id="52b2b-131">Требование</span><span class="sxs-lookup"><span data-stu-id="52b2b-131">Requirement</span></span> | <span data-ttu-id="52b2b-132">Значение</span><span class="sxs-lookup"><span data-stu-id="52b2b-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52b2b-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52b2b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="52b2b-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="52b2b-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="52b2b-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52b2b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="52b2b-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="52b2b-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="52b2b-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="52b2b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="52b2b-138"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52b2b-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="52b2b-139">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="52b2b-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="52b2b-140">**\_ Printer \_ дефаултсв** (Юникод) и **\_ \_ дефаултса принтера** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="52b2b-140">**\_PRINTER\_DEFAULTSW** (Unicode) and **\_PRINTER\_DEFAULTSA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="52b2b-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52b2b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52b2b-142">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="52b2b-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="52b2b-143">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="52b2b-143">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="52b2b-144">**делетепринтер**</span><span class="sxs-lookup"><span data-stu-id="52b2b-144">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="52b2b-145">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="52b2b-145">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="52b2b-146">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="52b2b-146">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="52b2b-147">**сетпринтер**</span><span class="sxs-lookup"><span data-stu-id="52b2b-147">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

