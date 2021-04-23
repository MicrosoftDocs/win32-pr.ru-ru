---
description: Структура драйвера \_ \_ 4 содержит сведения о драйвере принтера.
ms.assetid: 63000de6-74e7-4427-98d7-7bbd2dd61080
title: Структура DRIVER_INFO_4 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_4
- _DRIVER_INFO_4A
- _DRIVER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b737947b19e93a6b8de0563128a0f1be412101ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264335"
---
# <a name="driver_info_4-structure"></a><span data-ttu-id="65c5d-103">\_Структура сведений о драйвере \_ 4</span><span class="sxs-lookup"><span data-stu-id="65c5d-103">DRIVER\_INFO\_4 structure</span></span>

<span data-ttu-id="65c5d-104">Структура **драйвера \_ \_ 4** содержит сведения о драйвере принтера.</span><span class="sxs-lookup"><span data-stu-id="65c5d-104">The **DRIVER\_INFO\_4** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="65c5d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65c5d-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_4 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  LPTSTR pHelpFile;
  LPTSTR pDependentFiles;
  LPTSTR pMonitorName;
  LPTSTR pDefaultDataType;
  LPTSTR pszzPreviousNames;
} DRIVER_INFO_4, *PDRIVER_INFO_4;
```



## <a name="members"></a><span data-ttu-id="65c5d-106">Члены</span><span class="sxs-lookup"><span data-stu-id="65c5d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="65c5d-107">**кверсион**</span><span class="sxs-lookup"><span data-stu-id="65c5d-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="65c5d-108">Версия операционной системы, для которой был записан драйвер.</span><span class="sxs-lookup"><span data-stu-id="65c5d-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="65c5d-109">Поддерживаемое значение равно 3.</span><span class="sxs-lookup"><span data-stu-id="65c5d-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="65c5d-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="65c5d-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="65c5d-111">Указатель на строку, завершающуюся нулем, которая указывает имя драйвера (например, "QMS 810").</span><span class="sxs-lookup"><span data-stu-id="65c5d-111">Pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="65c5d-112">**пенвиронмент**</span><span class="sxs-lookup"><span data-stu-id="65c5d-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="65c5d-113">Указатель на строку, завершающуюся нулем, которая указывает среду, для которой был записан драйвер (например, Windows x86, Windows IA64 и Windows x64).</span><span class="sxs-lookup"><span data-stu-id="65c5d-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="65c5d-114">**пдриверпас**</span><span class="sxs-lookup"><span data-stu-id="65c5d-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="65c5d-115">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла для файла, содержащего драйвер устройства (например, C: \\ drivers \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="65c5d-115">Pointer to a null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="65c5d-116">**пдатафиле**</span><span class="sxs-lookup"><span data-stu-id="65c5d-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="65c5d-117">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла для файла, содержащего данные драйвера (например, C: \\ Drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="65c5d-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="65c5d-118">**пконфигфиле**</span><span class="sxs-lookup"><span data-stu-id="65c5d-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="65c5d-119">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла для библиотеки динамической компоновки конфигурации драйвера устройства (например, C: \\ drivers \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="65c5d-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="65c5d-120">**фелпфиле**</span><span class="sxs-lookup"><span data-stu-id="65c5d-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="65c5d-121">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла справки драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="65c5d-121">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file.</span></span>

</dd> <dt>

<span data-ttu-id="65c5d-122">**пдепендентфилес**</span><span class="sxs-lookup"><span data-stu-id="65c5d-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="65c5d-123">Указатель на буфер Мултисз, содержащий последовательность строк, заканчивающихся нулем.</span><span class="sxs-lookup"><span data-stu-id="65c5d-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="65c5d-124">Каждая строка в буфере, завершающаяся нулем, содержит имя файла, от которого зависит драйвер.</span><span class="sxs-lookup"><span data-stu-id="65c5d-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="65c5d-125">Последовательность строк завершается пустой строкой нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="65c5d-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="65c5d-126">Если **пдепендентфилес** не имеет **значение NULL** и не содержит имен файлов, он будет указывать на буфер, содержащий две пустые строки.</span><span class="sxs-lookup"><span data-stu-id="65c5d-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="65c5d-127">**пмониторнаме**</span><span class="sxs-lookup"><span data-stu-id="65c5d-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="65c5d-128">Указатель на строку, завершающуюся нулем, которая указывает монитор языка (например, "монитор PJL").</span><span class="sxs-lookup"><span data-stu-id="65c5d-128">A pointer to a null-terminated string that specifies a language monitor (for example, PJL monitor).</span></span> <span data-ttu-id="65c5d-129">Этот элемент может иметь **значение NULL** и указываться только для принтеров, поддерживающих двунаправленный обмен данными.</span><span class="sxs-lookup"><span data-stu-id="65c5d-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="65c5d-130">**пдефаултдататипе**</span><span class="sxs-lookup"><span data-stu-id="65c5d-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="65c5d-131">Указатель на строку, завершающуюся нулем, которая указывает тип данных по умолчанию для задания печати (например, EMF).</span><span class="sxs-lookup"><span data-stu-id="65c5d-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, EMF).</span></span>

</dd> <dt>

<span data-ttu-id="65c5d-132">**псззпревиауснамес**</span><span class="sxs-lookup"><span data-stu-id="65c5d-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="65c5d-133">Указатель на строку, завершающуюся нулем, которая указывает предыдущие имена драйверов принтеров, совместимые с этим драйвером.</span><span class="sxs-lookup"><span data-stu-id="65c5d-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="65c5d-134">Например, OldName1 \\ 0OldName2 \\ 0 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="65c5d-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65c5d-135">Требования</span><span class="sxs-lookup"><span data-stu-id="65c5d-135">Requirements</span></span>



| <span data-ttu-id="65c5d-136">Требование</span><span class="sxs-lookup"><span data-stu-id="65c5d-136">Requirement</span></span> | <span data-ttu-id="65c5d-137">Значение</span><span class="sxs-lookup"><span data-stu-id="65c5d-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65c5d-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65c5d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="65c5d-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="65c5d-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="65c5d-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65c5d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="65c5d-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="65c5d-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="65c5d-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="65c5d-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="65c5d-143"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65c5d-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="65c5d-144">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="65c5d-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="65c5d-145">**\_ \_ Сведения о \_ драйвере 4W** (Юникод) и **\_ \_ сведения о драйвере \_ 4A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="65c5d-145">**\_DRIVER\_INFO\_4W** (Unicode) and **\_DRIVER\_INFO\_4A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="65c5d-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65c5d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65c5d-147">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="65c5d-147">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="65c5d-148">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="65c5d-148">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="65c5d-149">**аддпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="65c5d-149">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="65c5d-150">**енумпринтердриверс**</span><span class="sxs-lookup"><span data-stu-id="65c5d-150">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="65c5d-151">**жетпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="65c5d-151">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




