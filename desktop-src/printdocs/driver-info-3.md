---
description: Структура драйвера \_ info \_ 3 содержит сведения о драйвере принтера.
ms.assetid: ccf87319-0bcf-4f71-8de3-0190459d2b0e
title: Структура DRIVER_INFO_3 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_3
- _DRIVER_INFO_3A
- _DRIVER_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 64509977a85bc33cb13dac4e6ba2817502c06cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712703"
---
# <a name="driver_info_3-structure"></a><span data-ttu-id="840ca-103">\_Структура сведений о драйвере \_ 3</span><span class="sxs-lookup"><span data-stu-id="840ca-103">DRIVER\_INFO\_3 structure</span></span>

<span data-ttu-id="840ca-104">Структура **драйвера \_ info \_ 3** содержит сведения о драйвере принтера.</span><span class="sxs-lookup"><span data-stu-id="840ca-104">The **DRIVER\_INFO\_3** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="840ca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="840ca-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_3 {
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
} DRIVER_INFO_3, *PDRIVER_INFO_3;
```



## <a name="members"></a><span data-ttu-id="840ca-106">Члены</span><span class="sxs-lookup"><span data-stu-id="840ca-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="840ca-107">**кверсион**</span><span class="sxs-lookup"><span data-stu-id="840ca-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="840ca-108">Версия операционной системы, для которой был записан драйвер.</span><span class="sxs-lookup"><span data-stu-id="840ca-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="840ca-109">Поддерживаются значения 3 и 4, которые представляют драйверы v3 и v4 соответственно.</span><span class="sxs-lookup"><span data-stu-id="840ca-109">The supported values are 3 and 4, which represent the V3 and V4 drivers, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="840ca-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="840ca-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="840ca-111">Указатель на строку, завершающуюся нулем, которая указывает имя драйвера (например, "QMS 810").</span><span class="sxs-lookup"><span data-stu-id="840ca-111">A pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="840ca-112">**пенвиронмент**</span><span class="sxs-lookup"><span data-stu-id="840ca-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="840ca-113">Указатель на строку, завершающуюся нулем, которая указывает среду, для которой был записан драйвер (например, Windows x86, Windows IA64 и Windows x64).</span><span class="sxs-lookup"><span data-stu-id="840ca-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="840ca-114">**пдриверпас**</span><span class="sxs-lookup"><span data-stu-id="840ca-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="840ca-115">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла для файла, содержащего драйвер устройства (например, "C: \\ drivers \\Pscript.dll").</span><span class="sxs-lookup"><span data-stu-id="840ca-115">A pointer to a null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, "C:\\DRIVERS\\Pscript.dll").</span></span>

</dd> <dt>

<span data-ttu-id="840ca-116">**пдатафиле**</span><span class="sxs-lookup"><span data-stu-id="840ca-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="840ca-117">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла для файла, содержащего данные драйвера (например, "C: \\ Drivers \\ Qms810. PPD").</span><span class="sxs-lookup"><span data-stu-id="840ca-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, "C:\\DRIVERS\\Qms810.ppd").</span></span>

</dd> <dt>

<span data-ttu-id="840ca-118">**пконфигфиле**</span><span class="sxs-lookup"><span data-stu-id="840ca-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="840ca-119">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла для библиотеки динамической компоновки конфигурации драйвера устройства (например, "C: \\ drivers \\Pscrptui.dll").</span><span class="sxs-lookup"><span data-stu-id="840ca-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, "C:\\DRIVERS\\Pscrptui.dll").</span></span>

</dd> <dt>

<span data-ttu-id="840ca-120">**фелпфиле**</span><span class="sxs-lookup"><span data-stu-id="840ca-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="840ca-121">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла справки драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="840ca-121">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file.</span></span>

</dd> <dt>

<span data-ttu-id="840ca-122">**пдепендентфилес**</span><span class="sxs-lookup"><span data-stu-id="840ca-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="840ca-123">Указатель на буфер Мултисз, содержащий последовательность строк, заканчивающихся нулем.</span><span class="sxs-lookup"><span data-stu-id="840ca-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="840ca-124">Каждая строка в буфере, завершающаяся нулем, содержит имя файла, от которого зависит драйвер.</span><span class="sxs-lookup"><span data-stu-id="840ca-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="840ca-125">Последовательность строк завершается пустой строкой нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="840ca-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="840ca-126">Если **пдепендентфилес** не имеет **значение NULL** и не содержит имен файлов, он будет указывать на буфер, содержащий две пустые строки.</span><span class="sxs-lookup"><span data-stu-id="840ca-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="840ca-127">**пмониторнаме**</span><span class="sxs-lookup"><span data-stu-id="840ca-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="840ca-128">Указатель на строку, завершающуюся нулем, которая указывает монитор языка (например, "монитор PJL").</span><span class="sxs-lookup"><span data-stu-id="840ca-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="840ca-129">Этот элемент может иметь **значение NULL** и указываться только для принтеров, поддерживающих двунаправленный обмен данными.</span><span class="sxs-lookup"><span data-stu-id="840ca-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="840ca-130">**пдефаултдататипе**</span><span class="sxs-lookup"><span data-stu-id="840ca-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="840ca-131">Указатель на строку, завершающуюся нулем, которая указывает тип данных по умолчанию для задания печати (например, "EMF").</span><span class="sxs-lookup"><span data-stu-id="840ca-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="840ca-132">Требования</span><span class="sxs-lookup"><span data-stu-id="840ca-132">Requirements</span></span>



| <span data-ttu-id="840ca-133">Требование</span><span class="sxs-lookup"><span data-stu-id="840ca-133">Requirement</span></span> | <span data-ttu-id="840ca-134">Значение</span><span class="sxs-lookup"><span data-stu-id="840ca-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="840ca-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="840ca-135">Minimum supported client</span></span><br/> | <span data-ttu-id="840ca-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="840ca-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="840ca-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="840ca-137">Minimum supported server</span></span><br/> | <span data-ttu-id="840ca-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="840ca-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="840ca-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="840ca-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="840ca-140"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="840ca-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="840ca-141">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="840ca-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="840ca-142">**\_ \_ Сведения о \_ драйвере «кто** (Юникод) и **\_ \_ сведения о драйвере \_ 3a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="840ca-142">**\_DRIVER\_INFO\_3W** (Unicode) and **\_DRIVER\_INFO\_3A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="840ca-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="840ca-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="840ca-144">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="840ca-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="840ca-145">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="840ca-145">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="840ca-146">**аддпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="840ca-146">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="840ca-147">**енумпринтердриверс**</span><span class="sxs-lookup"><span data-stu-id="840ca-147">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="840ca-148">**жетпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="840ca-148">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




