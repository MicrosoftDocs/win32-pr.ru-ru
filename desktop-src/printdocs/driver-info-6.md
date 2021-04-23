---
description: Структура драйвера \_ \_ 6 содержит сведения о драйвере принтера.
ms.assetid: 9771cbb5-caaa-4b7d-9a96-d24234440bac
title: Структура DRIVER_INFO_6 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_6
- _DRIVER_INFO_6A
- _DRIVER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 20edef2aca2c6948984f5195b16711b78112354a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693037"
---
# <a name="driver_info_6-structure"></a><span data-ttu-id="611ef-103">\_Сведения о драйвере \_ 6 структура</span><span class="sxs-lookup"><span data-stu-id="611ef-103">DRIVER\_INFO\_6 structure</span></span>

<span data-ttu-id="611ef-104">Структура **драйвера \_ \_ 6** содержит сведения о драйвере принтера.</span><span class="sxs-lookup"><span data-stu-id="611ef-104">The **DRIVER\_INFO\_6** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="611ef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="611ef-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_6 {
  DWORD     cVersion;
  LPTSTR    pName;
  LPTSTR    pEnvironment;
  LPTSTR    pDriverPath;
  LPTSTR    pDataFile;
  LPTSTR    pConfigFile;
  LPTSTR    pHelpFile;
  LPTSTR    pDependentFiles;
  LPTSTR    pMonitorName;
  LPTSTR    pDefaultDataType;
  LPTSTR    pszzPreviousNames;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  LPTSTR    pszMfgName;
  LPTSTR    pszOEMUrl;
  LPTSTR    pszHardwareID;
  LPTSTR    pszProvider;
} DRIVER_INFO_6, *PDRIVER_INFO_6, *LPDRIVER_INFO_6;
```



## <a name="members"></a><span data-ttu-id="611ef-106">Члены</span><span class="sxs-lookup"><span data-stu-id="611ef-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="611ef-107">**кверсион**</span><span class="sxs-lookup"><span data-stu-id="611ef-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="611ef-108">Версия операционной системы, для которой был записан драйвер.</span><span class="sxs-lookup"><span data-stu-id="611ef-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="611ef-109">Поддерживаемое значение равно 3.</span><span class="sxs-lookup"><span data-stu-id="611ef-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="611ef-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="611ef-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="611ef-111">Указатель на строку, завершающуюся нулем, которая указывает имя драйвера (например, QMS 810).</span><span class="sxs-lookup"><span data-stu-id="611ef-111">Pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="611ef-112">**пенвиронмент**</span><span class="sxs-lookup"><span data-stu-id="611ef-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="611ef-113">Указатель на строку, завершающуюся нулем, которая указывает среду, для которой был записан драйвер (например, Windows NT x86, Windows IA64 и Windows x64.</span><span class="sxs-lookup"><span data-stu-id="611ef-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows NT x86, Windows IA64, and Windows x64.</span></span>

</dd> <dt>

<span data-ttu-id="611ef-114">**пдриверпас**</span><span class="sxs-lookup"><span data-stu-id="611ef-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="611ef-115">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла для файла, содержащего драйвер устройства (например, C: \\ drivers \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="611ef-115">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="611ef-116">**пдатафиле**</span><span class="sxs-lookup"><span data-stu-id="611ef-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="611ef-117">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла для файла, содержащего данные драйвера (например, C: \\ Drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="611ef-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="611ef-118">**пконфигфиле**</span><span class="sxs-lookup"><span data-stu-id="611ef-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="611ef-119">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла для библиотеки динамической компоновки конфигурации драйвера устройства (например, C: \\ drivers \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="611ef-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="611ef-120">**фелпфиле**</span><span class="sxs-lookup"><span data-stu-id="611ef-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="611ef-121">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла справки драйвера устройства (например, C: \\ Drivers \\ пскрптуи. hlp).</span><span class="sxs-lookup"><span data-stu-id="611ef-121">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file (for example, C:\\DRIVERS\\Pscrptui.hlp).</span></span>

</dd> <dt>

<span data-ttu-id="611ef-122">**пдепендентфилес**</span><span class="sxs-lookup"><span data-stu-id="611ef-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="611ef-123">Указатель на буфер Мултисз, содержащий последовательность строк, заканчивающихся нулем.</span><span class="sxs-lookup"><span data-stu-id="611ef-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="611ef-124">Каждая строка в буфере, завершающаяся нулем, содержит имя файла, от которого зависит драйвер.</span><span class="sxs-lookup"><span data-stu-id="611ef-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="611ef-125">Последовательность строк завершается пустой строкой нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="611ef-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="611ef-126">Если **пдепендентфилес** не имеет **значение NULL** и не содержит имен файлов, он будет указывать на буфер, содержащий две пустые строки.</span><span class="sxs-lookup"><span data-stu-id="611ef-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="611ef-127">**пмониторнаме**</span><span class="sxs-lookup"><span data-stu-id="611ef-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="611ef-128">Указатель на строку, завершающуюся нулем, которая указывает монитор языка (например, "монитор PJL").</span><span class="sxs-lookup"><span data-stu-id="611ef-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="611ef-129">Этот элемент может иметь **значение NULL** и указываться только для принтеров, поддерживающих двунаправленный обмен данными.</span><span class="sxs-lookup"><span data-stu-id="611ef-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="611ef-130">**пдефаултдататипе**</span><span class="sxs-lookup"><span data-stu-id="611ef-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="611ef-131">Указатель на строку, завершающуюся нулем, которая указывает тип данных по умолчанию для задания печати (например, "EMF").</span><span class="sxs-lookup"><span data-stu-id="611ef-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> <dt>

<span data-ttu-id="611ef-132">**псззпревиауснамес**</span><span class="sxs-lookup"><span data-stu-id="611ef-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="611ef-133">Указатель на строку, завершающуюся нулем, которая указывает предыдущие имена драйверов принтеров, совместимые с этим драйвером.</span><span class="sxs-lookup"><span data-stu-id="611ef-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="611ef-134">Например, OldName1 \\ 0OldName2 \\ 0 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="611ef-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> <dt>

<span data-ttu-id="611ef-135">**фтдривердате**</span><span class="sxs-lookup"><span data-stu-id="611ef-135">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="611ef-136">Дата пакета драйверов, закодированная в файлах драйверов.</span><span class="sxs-lookup"><span data-stu-id="611ef-136">The date of the driver package, as coded in the driver files.</span></span>

</dd> <dt>

<span data-ttu-id="611ef-137">**двлдриверверсион**</span><span class="sxs-lookup"><span data-stu-id="611ef-137">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="611ef-138">Номер версии драйвера.</span><span class="sxs-lookup"><span data-stu-id="611ef-138">Version number of the driver.</span></span> <span data-ttu-id="611ef-139">Она выходит из структуры версии драйвера.</span><span class="sxs-lookup"><span data-stu-id="611ef-139">This comes out of the version structure of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="611ef-140">**псзмфгнаме**</span><span class="sxs-lookup"><span data-stu-id="611ef-140">**pszMfgName**</span></span>
</dt> <dd>

<span data-ttu-id="611ef-141">Указатель на строку, завершающуюся нулем, которая указывает имя производителя.</span><span class="sxs-lookup"><span data-stu-id="611ef-141">Pointer to a null-terminated string that specifies the manufacturer's name.</span></span>

</dd> <dt>

<span data-ttu-id="611ef-142">**псзоемурл**</span><span class="sxs-lookup"><span data-stu-id="611ef-142">**pszOEMUrl**</span></span>
</dt> <dd>

<span data-ttu-id="611ef-143">Указатель на строку, завершающуюся нулем, которая указывает URL-адрес производителя.</span><span class="sxs-lookup"><span data-stu-id="611ef-143">Pointer to a null-terminated string that specifies the URL for the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="611ef-144">**псзардвареид**</span><span class="sxs-lookup"><span data-stu-id="611ef-144">**pszHardwareID**</span></span>
</dt> <dd>

<span data-ttu-id="611ef-145">Указатель на строку, завершающуюся нулем, которая указывает идентификатор оборудования для драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="611ef-145">Pointer to a null-terminated string that specifies the hardware ID for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="611ef-146">**псзпровидер**</span><span class="sxs-lookup"><span data-stu-id="611ef-146">**pszProvider**</span></span>
</dt> <dd>

<span data-ttu-id="611ef-147">Указатель на строку, завершающуюся нулем, которая указывает поставщика драйвера принтера (например, "Microsoft Windows 2000")</span><span class="sxs-lookup"><span data-stu-id="611ef-147">Pointer to a null-terminated string that specifies the provider of the printer driver (for example, "Microsoft Windows 2000")</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="611ef-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="611ef-148">Remarks</span></span>

<span data-ttu-id="611ef-149">Строки для этих элементов содержатся в INF-файле, который используется для добавления драйвера.</span><span class="sxs-lookup"><span data-stu-id="611ef-149">The strings for these members are contained in the .inf file that is used to add the driver.</span></span>

<span data-ttu-id="611ef-150">Если вы вызываете [**аддпринтердривер**](addprinterdriver.md) или [**аддпринтердриверекс**](addprinterdriverex.md) с *уровнем* не равным 6, а затем вызываете [**жетпринтердривер**](getprinterdriver.md) или [**Енумпринтердриверс**](enumprinterdrivers.md) с *уровнем* , равным 6, структура **драйвера \_ \_ 6** возвращается с **псзмфгнаме**, **pszOEMUrl**, **pszHardwareID**, и **pszProvider** устанавливается в **null**, **dwlDriverVersion** устанавливается в 0, а **ftDriverDate** — в значение (0, 0).</span><span class="sxs-lookup"><span data-stu-id="611ef-150">If you call [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md) with *Level* not equal to 6, and then you call [**GetPrinterDriver**](getprinterdriver.md) or [**EnumPrinterDrivers**](enumprinterdrivers.md) with *Level* equal to 6, the **DRIVER\_INFO\_6** structure is returned with **pszMfgName**, **pszOEMUrl**, **pszHardwareID**, and **pszProvider** set to **NULL**, **dwlDriverVersion** set to 0, and **ftDriverDate** set to (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="611ef-151">Требования</span><span class="sxs-lookup"><span data-stu-id="611ef-151">Requirements</span></span>



| <span data-ttu-id="611ef-152">Требование</span><span class="sxs-lookup"><span data-stu-id="611ef-152">Requirement</span></span> | <span data-ttu-id="611ef-153">Значение</span><span class="sxs-lookup"><span data-stu-id="611ef-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="611ef-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="611ef-154">Minimum supported client</span></span><br/> | <span data-ttu-id="611ef-155">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="611ef-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="611ef-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="611ef-156">Minimum supported server</span></span><br/> | <span data-ttu-id="611ef-157">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="611ef-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="611ef-158">Заголовок</span><span class="sxs-lookup"><span data-stu-id="611ef-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="611ef-159"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="611ef-159"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="611ef-160">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="611ef-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="611ef-161">**\_ \_ Сведения о \_ драйвере 6W** (Юникод) и **\_ \_ сведения о драйвере \_ 6a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="611ef-161">**\_DRIVER\_INFO\_6W** (Unicode) and **\_DRIVER\_INFO\_6A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="611ef-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="611ef-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="611ef-163">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="611ef-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="611ef-164">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="611ef-164">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="611ef-165">**аддпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="611ef-165">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="611ef-166">**аддпринтердриверекс**</span><span class="sxs-lookup"><span data-stu-id="611ef-166">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="611ef-167">**енумпринтердриверс**</span><span class="sxs-lookup"><span data-stu-id="611ef-167">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="611ef-168">**жетпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="611ef-168">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




