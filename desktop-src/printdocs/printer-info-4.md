---
description: В структуре "сведения о ПРИНТЕРе \_ \_ 4" указаны общие сведения о принтере. Структуру можно использовать для получения минимальных сведений о принтерах при вызове Енумпринтерс.
ms.assetid: 81bd0eab-dc1e-4cf1-8f63-3686f1711c1f
title: Структура PRINTER_INFO_4 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_4
- _PRINTER_INFO_4A
- _PRINTER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9a1501008f0235ea303dd1457fc8756c28abc21c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265869"
---
# <a name="printer_info_4-structure"></a><span data-ttu-id="5fe34-103">\_Структура сведений о принтере \_ 4</span><span class="sxs-lookup"><span data-stu-id="5fe34-103">PRINTER\_INFO\_4 structure</span></span>

<span data-ttu-id="5fe34-104">В структуре " **сведения о принтере \_ \_ 4** " указаны общие сведения о принтере.</span><span class="sxs-lookup"><span data-stu-id="5fe34-104">The **PRINTER\_INFO\_4** structure specifies general printer information.</span></span>

<span data-ttu-id="5fe34-105">Структуру можно использовать для получения минимальных сведений о принтерах при вызове [**енумпринтерс**](enumprinters.md).</span><span class="sxs-lookup"><span data-stu-id="5fe34-105">The structure can be used to retrieve minimal printer information on a call to [**EnumPrinters**](enumprinters.md).</span></span> <span data-ttu-id="5fe34-106">Такой вызов — это быстрый и простой способ получения имен и атрибутов всех локально установленных принтеров в системе и всех подключений удаленного принтера, установленных пользователем.</span><span class="sxs-lookup"><span data-stu-id="5fe34-106">Such a call is a fast and easy way to retrieve the names and attributes of all locally installed printers on a system and all remote printer connections that a user has established.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fe34-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fe34-107">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_4 {
  LPTSTR pPrinterName;
  LPTSTR pServerName;
  DWORD  Attributes;
} PRINTER_INFO_4, *PPRINTER_INFO_4;
```



## <a name="members"></a><span data-ttu-id="5fe34-108">Члены</span><span class="sxs-lookup"><span data-stu-id="5fe34-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5fe34-109">**ппринтернаме**</span><span class="sxs-lookup"><span data-stu-id="5fe34-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="5fe34-110">Указатель на строку, завершающуюся нулем, которая указывает имя принтера (локальный или удаленный).</span><span class="sxs-lookup"><span data-stu-id="5fe34-110">Pointer to a null-terminated string that specifies the name of the printer (local or remote).</span></span>

</dd> <dt>

<span data-ttu-id="5fe34-111">**псервернаме**</span><span class="sxs-lookup"><span data-stu-id="5fe34-111">**pServerName**</span></span>
</dt> <dd>

<span data-ttu-id="5fe34-112">Указатель на строку, завершающуюся нулем, которая является именем сервера.</span><span class="sxs-lookup"><span data-stu-id="5fe34-112">Pointer to a null-terminated string that is the name of the server.</span></span>

</dd> <dt>

<span data-ttu-id="5fe34-113">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="5fe34-113">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="5fe34-114">Указывает сведения о возвращенных данных.</span><span class="sxs-lookup"><span data-stu-id="5fe34-114">Specifies information about the returned data.</span></span>



| <span data-ttu-id="5fe34-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5fe34-115">Value</span></span>                       | <span data-ttu-id="5fe34-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5fe34-116">Meaning</span></span>                          |
|-----------------------------|----------------------------------|
| <span data-ttu-id="5fe34-117">\_локальный атрибут \_ принтера</span><span class="sxs-lookup"><span data-stu-id="5fe34-117">PRINTER\_ATTRIBUTE\_LOCAL</span></span>   | <span data-ttu-id="5fe34-118">Принтер является локальным принтером.</span><span class="sxs-lookup"><span data-stu-id="5fe34-118">The printer is a local printer.</span></span>  |
| <span data-ttu-id="5fe34-119">\_сеть АТРИБУТОВ \_ принтера</span><span class="sxs-lookup"><span data-stu-id="5fe34-119">PRINTER\_ATTRIBUTE\_NETWORK</span></span> | <span data-ttu-id="5fe34-120">Принтер является удаленным принтером.</span><span class="sxs-lookup"><span data-stu-id="5fe34-120">The printer is a remote printer.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5fe34-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5fe34-121">Remarks</span></span>

<span data-ttu-id="5fe34-122">Структура **Printer \_ info \_ 4** обеспечивает простой и быстрый способ получения имен принтеров, установленных на локальном компьютере, а также удаленных подключений, которые пользователь установил.</span><span class="sxs-lookup"><span data-stu-id="5fe34-122">The **PRINTER\_INFO\_4** structure provides an easy and extremely fast way to retrieve the names of the printers installed on a local machine, as well as the remote connections that a user has established.</span></span> <span data-ttu-id="5fe34-123">Когда [**енумпринтерс**](enumprinters.md) вызывается со структурой данных **Printer \_ \_ 4** , эта функция запрашивает в реестре указанные сведения, а затем сразу же возвращает.</span><span class="sxs-lookup"><span data-stu-id="5fe34-123">When [**EnumPrinters**](enumprinters.md) is called with a **PRINTER\_INFO\_4** data structure, that function queries the registry for the specified information, then returns immediately.</span></span> <span data-ttu-id="5fe34-124">Это отличается от поведения **енумпринтерс** при вызове с другими уровнями структур **данных \_ принтера \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="5fe34-124">This differs from the behavior of **EnumPrinters** when called with other levels of **PRINTER\_INFO\_xxx** data structures.</span></span> <span data-ttu-id="5fe34-125">В частности, если **енумпринтерс** вызывается со структурой данных уровня 2 (**\_ сведения о принтере \_ 2** ), она выполняет вызов **опенпринтер** для каждого удаленного соединения.</span><span class="sxs-lookup"><span data-stu-id="5fe34-125">In particular, when **EnumPrinters** is called with a level 2 (**PRINTER\_INFO\_2** ) data structure, it performs an **OpenPrinter** call on each remote connection.</span></span> <span data-ttu-id="5fe34-126">Если удаленное подключение не работает, если удаленный сервер больше не существует или удаленный принтер больше не существует, функция должна ожидать истечения времени ожидания RPC и, следовательно, вызвать сбой вызова **опенпринтер** .</span><span class="sxs-lookup"><span data-stu-id="5fe34-126">If a remote connection is down, if the remote server no longer exists, or if the remote printer no longer exists, the function must wait for RPC to time out and consequently fail the **OpenPrinter** call.</span></span> <span data-ttu-id="5fe34-127">Это может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="5fe34-127">This can take a while.</span></span> <span data-ttu-id="5fe34-128">Передача структуры **" \_ сведения \_ о принтере 4** " позволяет приложению получить минимально необходимую информацию. Если требуется более подробная информация, можно выполнить следующий вызов **енумпринтер** уровня 2.</span><span class="sxs-lookup"><span data-stu-id="5fe34-128">Passing a **PRINTER\_INFO\_4** structure lets an application retrieve a bare minimum of required information; if more detailed information is desired, a subsequent **EnumPrinter** level 2 call can be made.</span></span>

<span data-ttu-id="5fe34-129">**Атрибуты** также могут содержать значения, определенные в поле **атрибуты** в **\_ сведениях о принтере \_ 2**.</span><span class="sxs-lookup"><span data-stu-id="5fe34-129">**Attributes** can also contain values that are defined in the **Attributes** field of **PRINTER\_INFO\_2**.</span></span>

<span data-ttu-id="5fe34-130">Некоторые конфигурации принтеров, например подключения принтеров к некоторым серверам печати, отличным от Windows, могут возвращать как атрибуты принтера, так и **\_ \_ локальную** **\_ \_ сеть атрибутов принтера**.</span><span class="sxs-lookup"><span data-stu-id="5fe34-130">Some printer configurations, such as printer connections to some non-Windows-based print servers, might return both **PRINTER\_ATTRIBUTE\_LOCAL** and **PRINTER\_ATTRIBUTE\_NETWORK**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fe34-131">Требования</span><span class="sxs-lookup"><span data-stu-id="5fe34-131">Requirements</span></span>



| <span data-ttu-id="5fe34-132">Требование</span><span class="sxs-lookup"><span data-stu-id="5fe34-132">Requirement</span></span> | <span data-ttu-id="5fe34-133">Значение</span><span class="sxs-lookup"><span data-stu-id="5fe34-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fe34-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5fe34-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5fe34-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5fe34-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5fe34-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5fe34-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5fe34-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5fe34-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5fe34-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5fe34-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fe34-139"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5fe34-139"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5fe34-140">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="5fe34-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5fe34-141">**\_ \_ Сведения о \_ принтере 4W** (Юникод) и **\_ \_ \_ 4A info** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5fe34-141">**\_PRINTER\_INFO\_4W** (Unicode) and **\_PRINTER\_INFO\_4A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="5fe34-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5fe34-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fe34-143">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="5fe34-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5fe34-144">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="5fe34-144">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="5fe34-145">**Наложение**</span><span class="sxs-lookup"><span data-stu-id="5fe34-145">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="5fe34-146">**енумпринтерс**</span><span class="sxs-lookup"><span data-stu-id="5fe34-146">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="5fe34-147">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="5fe34-147">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="5fe34-148">**\_Сведения о принтере \_ 1**</span><span class="sxs-lookup"><span data-stu-id="5fe34-148">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="5fe34-149">**\_Сведения о принтере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="5fe34-149">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="5fe34-150">**\_Сведения о принтере \_ 3**</span><span class="sxs-lookup"><span data-stu-id="5fe34-150">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> </dl>

 

 




