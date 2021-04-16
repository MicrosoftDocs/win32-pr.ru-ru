---
description: В структуре сведения о ПРИНТЕРе \_ \_ 1 указаны общие сведения о принтере.
ms.assetid: 0b0e2d0e-2625-4cab-a8f9-536185479443
title: Структура PRINTER_INFO_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_1
- _PRINTER_INFO_1A
- _PRINTER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: cbeff42a9125331c45ffd8bbbee5758fd864648c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719568"
---
# <a name="printer_info_1-structure"></a><span data-ttu-id="624b6-103">\_Структура сведений о принтере \_ 1</span><span class="sxs-lookup"><span data-stu-id="624b6-103">PRINTER\_INFO\_1 structure</span></span>

<span data-ttu-id="624b6-104">В **структуре \_ сведения \_ о принтере 1** указаны общие сведения о принтере.</span><span class="sxs-lookup"><span data-stu-id="624b6-104">The **PRINTER\_INFO\_1** structure specifies general printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="624b6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="624b6-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_1 {
  DWORD  Flags;
  LPTSTR pDescription;
  LPTSTR pName;
  LPTSTR pComment;
} PRINTER_INFO_1, *PPRINTER_INFO_1;
```



## <a name="members"></a><span data-ttu-id="624b6-106">Члены</span><span class="sxs-lookup"><span data-stu-id="624b6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="624b6-107">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="624b6-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="624b6-108">Указывает сведения о возвращенных данных.</span><span class="sxs-lookup"><span data-stu-id="624b6-108">Specifies information about the returned data.</span></span> <span data-ttu-id="624b6-109">Ниже приведены значения для этого элемента.</span><span class="sxs-lookup"><span data-stu-id="624b6-109">Following are the values for this member.</span></span>



| <span data-ttu-id="624b6-110">Значение</span><span class="sxs-lookup"><span data-stu-id="624b6-110">Value</span></span>                    | <span data-ttu-id="624b6-111">Значение</span><span class="sxs-lookup"><span data-stu-id="624b6-111">Meaning</span></span>                                                                                                                                                                                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="624b6-112">\_развернуть перечисление принтеров \_</span><span class="sxs-lookup"><span data-stu-id="624b6-112">PRINTER\_ENUM\_EXPAND</span></span>    | <span data-ttu-id="624b6-113">Поставщик печати может установить этот флаг в качестве подсказки для вызывающего приложения, чтобы перечислить этот объект дальше, если включено расширение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="624b6-113">A print provider can set this flag as a hint to a calling application to enumerate this object further if default expansion is enabled.</span></span> <span data-ttu-id="624b6-114">Например, при перечислении доменов поставщик печати может указать домен пользователя, установив этот флаг.</span><span class="sxs-lookup"><span data-stu-id="624b6-114">For example, when domains are enumerated, a print provider might indicate the user's domain by setting this flag.</span></span> |
| <span data-ttu-id="624b6-115">\_контейнер перечислителя принтеров \_</span><span class="sxs-lookup"><span data-stu-id="624b6-115">PRINTER\_ENUM\_CONTAINER</span></span> | <span data-ttu-id="624b6-116">Если этот флаг установлен, объект принтера может содержать перечислимые объекты.</span><span class="sxs-lookup"><span data-stu-id="624b6-116">If this flag is set, the printer object may contain enumerable objects.</span></span> <span data-ttu-id="624b6-117">Например, объект может быть сервером печати, который содержит принтеры.</span><span class="sxs-lookup"><span data-stu-id="624b6-117">For example, the object may be a print server that contains printers.</span></span>                                                                                                             |
| <span data-ttu-id="624b6-118">\_Icon1 перечисление принтера \_</span><span class="sxs-lookup"><span data-stu-id="624b6-118">PRINTER\_ENUM\_ICON1</span></span>     | <span data-ttu-id="624b6-119">Указывает, что в случае необходимости приложение должно отображать значок, идентифицирующий объект как сетевое имя верхнего уровня, например сеть Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="624b6-119">Indicates that, where appropriate, an application should display an icon identifying the object as a top-level network name, such as Microsoft Windows Network.</span></span>                                                                                           |
| <span data-ttu-id="624b6-120">\_ICON2 перечисление принтера \_</span><span class="sxs-lookup"><span data-stu-id="624b6-120">PRINTER\_ENUM\_ICON2</span></span>     | <span data-ttu-id="624b6-121">Указывает, что в случае необходимости приложение должно отобразить значок, идентифицирующий объект в качестве сетевого домена.</span><span class="sxs-lookup"><span data-stu-id="624b6-121">Indicates that, where appropriate, an application should display an icon that identifies the object as a network domain.</span></span>                                                                                                                                  |
| <span data-ttu-id="624b6-122">\_ICON3 перечисление принтера \_</span><span class="sxs-lookup"><span data-stu-id="624b6-122">PRINTER\_ENUM\_ICON3</span></span>     | <span data-ttu-id="624b6-123">Указывает, что в случае необходимости приложение должно отобразить значок, идентифицирующий объект как сервер печати.</span><span class="sxs-lookup"><span data-stu-id="624b6-123">Indicates that, where appropriate, an application should display an icon that identifies the object as a print server.</span></span>                                                                                                                                    |
| <span data-ttu-id="624b6-124">\_ICON4 перечисление принтера \_</span><span class="sxs-lookup"><span data-stu-id="624b6-124">PRINTER\_ENUM\_ICON4</span></span>     | <span data-ttu-id="624b6-125">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="624b6-125">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="624b6-126">\_ICON5 перечисление принтера \_</span><span class="sxs-lookup"><span data-stu-id="624b6-126">PRINTER\_ENUM\_ICON5</span></span>     | <span data-ttu-id="624b6-127">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="624b6-127">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="624b6-128">\_ICON6 перечисление принтера \_</span><span class="sxs-lookup"><span data-stu-id="624b6-128">PRINTER\_ENUM\_ICON6</span></span>     | <span data-ttu-id="624b6-129">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="624b6-129">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="624b6-130">\_ICON7 перечисление принтера \_</span><span class="sxs-lookup"><span data-stu-id="624b6-130">PRINTER\_ENUM\_ICON7</span></span>     | <span data-ttu-id="624b6-131">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="624b6-131">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="624b6-132">\_ICON8 перечисление принтера \_</span><span class="sxs-lookup"><span data-stu-id="624b6-132">PRINTER\_ENUM\_ICON8</span></span>     | <span data-ttu-id="624b6-133">Указывает, что в случае необходимости приложение должно отображать значок, идентифицирующий объект как принтер.</span><span class="sxs-lookup"><span data-stu-id="624b6-133">Indicates that, where appropriate, an application should display an icon that identifies the object as a printer.</span></span>                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="624b6-134">**пдескриптион**</span><span class="sxs-lookup"><span data-stu-id="624b6-134">**pDescription**</span></span>
</dt> <dd>

<span data-ttu-id="624b6-135">Указатель на строку, завершающуюся нулем, которая описывает содержимое структуры.</span><span class="sxs-lookup"><span data-stu-id="624b6-135">Pointer to a null-terminated string that describes the contents of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="624b6-136">**pName**</span><span class="sxs-lookup"><span data-stu-id="624b6-136">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="624b6-137">Указатель на строку, завершающуюся нулем, которая именует содержимое структуры.</span><span class="sxs-lookup"><span data-stu-id="624b6-137">Pointer to a null-terminated string that names the contents of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="624b6-138">**пкоммент**</span><span class="sxs-lookup"><span data-stu-id="624b6-138">**pComment**</span></span>
</dt> <dd>

<span data-ttu-id="624b6-139">Указатель на строку, завершающуюся нулем, которая содержит дополнительные данные, описывающие структуру.</span><span class="sxs-lookup"><span data-stu-id="624b6-139">Pointer to a null-terminated string that contains additional data describing the structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="624b6-140">Требования</span><span class="sxs-lookup"><span data-stu-id="624b6-140">Requirements</span></span>



| <span data-ttu-id="624b6-141">Требование</span><span class="sxs-lookup"><span data-stu-id="624b6-141">Requirement</span></span> | <span data-ttu-id="624b6-142">Значение</span><span class="sxs-lookup"><span data-stu-id="624b6-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="624b6-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="624b6-143">Minimum supported client</span></span><br/> | <span data-ttu-id="624b6-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="624b6-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="624b6-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="624b6-145">Minimum supported server</span></span><br/> | <span data-ttu-id="624b6-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="624b6-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="624b6-147">Заголовок</span><span class="sxs-lookup"><span data-stu-id="624b6-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="624b6-148"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="624b6-148"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="624b6-149">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="624b6-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="624b6-150">**\_ \_ Сведения о \_ принтере 1W** (Юникод) и **\_ \_ сведения о принтере \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="624b6-150">**\_PRINTER\_INFO\_1W** (Unicode) and **\_PRINTER\_INFO\_1A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="624b6-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="624b6-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="624b6-152">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="624b6-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="624b6-153">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="624b6-153">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="624b6-154">**Наложение**</span><span class="sxs-lookup"><span data-stu-id="624b6-154">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="624b6-155">**енумпринтерс**</span><span class="sxs-lookup"><span data-stu-id="624b6-155">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="624b6-156">**\_Сведения о принтере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="624b6-156">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="624b6-157">**\_Сведения о принтере \_ 3**</span><span class="sxs-lookup"><span data-stu-id="624b6-157">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="624b6-158">**\_Сведения о принтере \_ 4**</span><span class="sxs-lookup"><span data-stu-id="624b6-158">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> </dl>

 

 




