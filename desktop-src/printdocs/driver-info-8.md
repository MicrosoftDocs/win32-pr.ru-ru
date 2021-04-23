---
description: Содержит сведения о драйвере принтера.
ms.assetid: 6237def2-ffd4-4d93-b3a4-56f225793457
title: Структура DRIVER_INFO_8 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_8
- _DRIVER_INFO_8A
- _DRIVER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3cc174fdc8617a8ff59afc5a12740eaba715114f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349092"
---
# <a name="driver_info_8-structure"></a><span data-ttu-id="c3f08-103">\_Структура сведений о драйвере \_ 8</span><span class="sxs-lookup"><span data-stu-id="c3f08-103">DRIVER\_INFO\_8 structure</span></span>

<span data-ttu-id="c3f08-104">Содержит сведения о драйвере принтера.</span><span class="sxs-lookup"><span data-stu-id="c3f08-104">Contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f08-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3f08-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_8 {
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
  LPTSTR    pszPrintProcessor;
  LPTSTR    pszVendorSetup;
  LPTSTR    pszzColorProfiles;
  LPTSTR    pszInfPath;
  DWORD     dwPrinterDriverAttributes;
  LPTSTR    pszzCoreDriverDependencies;
  FILETIME  ftMinInboxDriverVerDate;
  DWORDLONG dwlMinInboxDriverVerVersion;
} DRIVER_INFO_8, *PDRIVER_INFO_8, *LPDRIVER_INFO_8;
```



## <a name="members"></a><span data-ttu-id="c3f08-106">Члены</span><span class="sxs-lookup"><span data-stu-id="c3f08-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c3f08-107">**кверсион**</span><span class="sxs-lookup"><span data-stu-id="c3f08-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-108">Версия операционной системы, для которой был записан драйвер.</span><span class="sxs-lookup"><span data-stu-id="c3f08-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="c3f08-109">Поддерживаемое значение равно 3.</span><span class="sxs-lookup"><span data-stu-id="c3f08-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="c3f08-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-111">Указатель на строку, завершающуюся нулем, которая указывает имя драйвера (например, QMS 810).</span><span class="sxs-lookup"><span data-stu-id="c3f08-111">A pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-112">**пенвиронмент**</span><span class="sxs-lookup"><span data-stu-id="c3f08-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-113">Указатель на строку, завершающуюся нулем, которая указывает среду, для которой был записан драйвер (например, Windows x86, Windows IA64 и Windows x64.</span><span class="sxs-lookup"><span data-stu-id="c3f08-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64.</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-114">**пдриверпас**</span><span class="sxs-lookup"><span data-stu-id="c3f08-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-115">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла для файла, содержащего драйвер устройства (например, C: \\ drivers \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="c3f08-115">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-116">**пдатафиле**</span><span class="sxs-lookup"><span data-stu-id="c3f08-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-117">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла для файла, содержащего данные драйвера (например, C: \\ Drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="c3f08-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-118">**пконфигфиле**</span><span class="sxs-lookup"><span data-stu-id="c3f08-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-119">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла для библиотеки динамической компоновки конфигурации драйвера устройства (например, C: \\ drivers \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="c3f08-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-120">**фелпфиле**</span><span class="sxs-lookup"><span data-stu-id="c3f08-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-121">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла справки драйвера устройства (например, C: \\ Drivers \\ пскрптуи. hlp).</span><span class="sxs-lookup"><span data-stu-id="c3f08-121">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file (for example, C:\\DRIVERS\\Pscrptui.hlp).</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-122">**пдепендентфилес**</span><span class="sxs-lookup"><span data-stu-id="c3f08-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-123">Указатель на буфер Мултисз, содержащий последовательность строк, заканчивающихся нулем.</span><span class="sxs-lookup"><span data-stu-id="c3f08-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="c3f08-124">Каждая строка в буфере, завершающаяся нулем, содержит имя файла, от которого зависит драйвер.</span><span class="sxs-lookup"><span data-stu-id="c3f08-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="c3f08-125">Последовательность строк завершается пустой строкой нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="c3f08-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="c3f08-126">Если **пдепендентфилес** не имеет **значение NULL** и не содержит имен файлов, он будет указывать на буфер, содержащий две пустые строки.</span><span class="sxs-lookup"><span data-stu-id="c3f08-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-127">**пмониторнаме**</span><span class="sxs-lookup"><span data-stu-id="c3f08-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-128">Указатель на строку, завершающуюся нулем, которая указывает монитор языка (например, "монитор PJL").</span><span class="sxs-lookup"><span data-stu-id="c3f08-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="c3f08-129">Этот элемент может иметь **значение NULL** и указываться только для принтеров, поддерживающих двунаправленный обмен данными.</span><span class="sxs-lookup"><span data-stu-id="c3f08-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-130">**пдефаултдататипе**</span><span class="sxs-lookup"><span data-stu-id="c3f08-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-131">Указатель на строку, завершающуюся нулем, которая указывает тип данных по умолчанию для задания печати (например, "EMF").</span><span class="sxs-lookup"><span data-stu-id="c3f08-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-132">**псззпревиауснамес**</span><span class="sxs-lookup"><span data-stu-id="c3f08-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-133">Указатель на строку, завершающуюся нулем, которая указывает предыдущие имена драйверов принтеров, совместимые с этим драйвером.</span><span class="sxs-lookup"><span data-stu-id="c3f08-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="c3f08-134">Например, OldName1 \\ 0OldName2 \\ 0 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="c3f08-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-135">**фтдривердате**</span><span class="sxs-lookup"><span data-stu-id="c3f08-135">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-136">Дата пакета драйверов, закодированная в файлах драйверов.</span><span class="sxs-lookup"><span data-stu-id="c3f08-136">The date of the driver package, as coded in the driver files.</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-137">**двлдриверверсион**</span><span class="sxs-lookup"><span data-stu-id="c3f08-137">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-138">Номер версии драйвера.</span><span class="sxs-lookup"><span data-stu-id="c3f08-138">The version number of the driver.</span></span> <span data-ttu-id="c3f08-139">Это происходит из структуры версии драйвера.</span><span class="sxs-lookup"><span data-stu-id="c3f08-139">This comes from the version structure of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-140">**псзмфгнаме**</span><span class="sxs-lookup"><span data-stu-id="c3f08-140">**pszMfgName**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-141">Указатель на строку, завершающуюся нулем, которая указывает имя производителя.</span><span class="sxs-lookup"><span data-stu-id="c3f08-141">A pointer to a null-terminated string that specifies the manufacturer's name.</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-142">**псзоемурл**</span><span class="sxs-lookup"><span data-stu-id="c3f08-142">**pszOEMUrl**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-143">Указатель на строку, завершающуюся нулем, которая указывает URL-адрес производителя.</span><span class="sxs-lookup"><span data-stu-id="c3f08-143">A pointer to a null-terminated string that specifies the URL for the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-144">**псзардвареид**</span><span class="sxs-lookup"><span data-stu-id="c3f08-144">**pszHardwareID**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-145">Указатель на строку, завершающуюся нулем, которая указывает идентификатор оборудования для драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="c3f08-145">A pointer to a null-terminated string that specifies the hardware ID for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-146">**псзпровидер**</span><span class="sxs-lookup"><span data-stu-id="c3f08-146">**pszProvider**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-147">Указатель на строку, завершающуюся нулем, которая указывает поставщика драйвера принтера (например, "Microsoft Windows 2000").</span><span class="sxs-lookup"><span data-stu-id="c3f08-147">A pointer to a null-terminated string that specifies the provider of the printer driver (for example, "Microsoft Windows 2000").</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-148">**псзпринтпроцессор**</span><span class="sxs-lookup"><span data-stu-id="c3f08-148">**pszPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-149">Указатель на строку, завершающуюся нулем, которая указывает обработчик заданий печати (например, "Винпринт").</span><span class="sxs-lookup"><span data-stu-id="c3f08-149">A pointer to a null-terminated string that specifies the print processor (for example, "WinPrint").</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-150">**псзвендорсетуп**</span><span class="sxs-lookup"><span data-stu-id="c3f08-150">**pszVendorSetup**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-151">Указатель на строку, завершающуюся нулем, которая указывает библиотеку DLL для установки драйвера поставщика и точку входа.</span><span class="sxs-lookup"><span data-stu-id="c3f08-151">A pointer to a null-terminated string that specifies the vendor's driver setup DLL and entry point.</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-152">**псззколорпрофилес**</span><span class="sxs-lookup"><span data-stu-id="c3f08-152">**pszzColorProfiles**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-153">Указатель на строку, завершающуюся нулем, которая указывает цветовые профили, связанные с драйвером.</span><span class="sxs-lookup"><span data-stu-id="c3f08-153">A pointer to a null-terminated string that specifies the color profiles associated with the driver.</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-154">**псзинфпас**</span><span class="sxs-lookup"><span data-stu-id="c3f08-154">**pszInfPath**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-155">Указатель на строку, завершающуюся нулем, которая указывает путь к INF-файлу драйвера в хранилище драйверов.</span><span class="sxs-lookup"><span data-stu-id="c3f08-155">A pointer to a null-terminated string that specifies the path to the driver's .inf file in the driver store.</span></span> <span data-ttu-id="c3f08-156">(См. раздел Примечания.) Это значение должно быть **равно NULL** , если \_ сведения о драйвере \_ 8 передаются в [**аддпринтердривер**](addprinterdriver.md) или [**аддпринтердриверекс**](addprinterdriverex.md).</span><span class="sxs-lookup"><span data-stu-id="c3f08-156">(See Remarks.) This must be **NULL** if the DRIVER\_INFO\_8 is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-157">**двпринтердривераттрибутес**</span><span class="sxs-lookup"><span data-stu-id="c3f08-157">**dwPrinterDriverAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-158">Флаги атрибутов для драйверов принтера.</span><span class="sxs-lookup"><span data-stu-id="c3f08-158">Attribute flags for printer drivers.</span></span> <span data-ttu-id="c3f08-159">Это значение должно быть равно 0, если \_ сведения о драйвере \_ 8 передаются в [**аддпринтердривер**](addprinterdriver.md) или [**аддпринтердриверекс**](addprinterdriverex.md).</span><span class="sxs-lookup"><span data-stu-id="c3f08-159">This must be 0 if the DRIVER\_INFO\_8 is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span> <span data-ttu-id="c3f08-160">В противном случае это может быть любое сочетание следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="c3f08-160">Otherwise, it can be any combination of the following flags:</span></span>



| <span data-ttu-id="c3f08-161">Имя и значение флага</span><span class="sxs-lookup"><span data-stu-id="c3f08-161">Flag name/value</span></span>                                                         | <span data-ttu-id="c3f08-162">Значение</span><span class="sxs-lookup"><span data-stu-id="c3f08-162">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="c3f08-163">Минимальная ОС</span><span class="sxs-lookup"><span data-stu-id="c3f08-163">Minimum OS</span></span>                                             |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="c3f08-164">с \_ \_ учетом пакета драйвера принтера \_</span><span class="sxs-lookup"><span data-stu-id="c3f08-164">PRINTER\_DRIVER\_PACKAGE\_AWARE</span></span><br/> <span data-ttu-id="c3f08-165">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3f08-165">0x00000001</span></span><br/>        | <span data-ttu-id="c3f08-166">Драйвер принтера является частью пакета драйверов.</span><span class="sxs-lookup"><span data-stu-id="c3f08-166">The printer driver is part of a driver package.</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="c3f08-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3f08-167">Windows Vista</span></span>                                          |
| <span data-ttu-id="c3f08-168">\_драйвер принтера \_ XPS</span><span class="sxs-lookup"><span data-stu-id="c3f08-168">PRINTER\_DRIVER\_XPS</span></span><br/> <span data-ttu-id="c3f08-169">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3f08-169">0x00000002</span></span><br/>                   | <span data-ttu-id="c3f08-170">Драйвер принтера поддерживает формат Microsoft XPS, описанный в [спецификации XML-документа: обзор](/previous-versions/windows/hardware/design/dn641615(v=vs.85)), а также в [поведении продукта раздел <27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span><span class="sxs-lookup"><span data-stu-id="c3f08-170">The printer driver supports the Microsoft XPS format described in the [XML Paper Specification: Overview](/previous-versions/windows/hardware/design/dn641615(v=vs.85)), and also in [Product Behavior, section <27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span></span>                        | <span data-ttu-id="c3f08-171">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c3f08-171">Windows 8</span></span><br/> <span data-ttu-id="c3f08-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3f08-172">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="c3f08-173">\_ \_ "песочница" драйвера принтера \_ включена</span><span class="sxs-lookup"><span data-stu-id="c3f08-173">PRINTER\_DRIVER\_SANDBOX\_ENABLED</span></span><br/> <span data-ttu-id="c3f08-174">0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3f08-174">0x00000004</span></span><br/>      | <span data-ttu-id="c3f08-175">Драйвер принтера совместим с [изоляцией драйвера принтера](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="c3f08-175">The printer driver is compatible with [printer driver isolation](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span> <span data-ttu-id="c3f08-176">Дополнительные сведения см. в [разделе поведение продукта, раздел <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span><span class="sxs-lookup"><span data-stu-id="c3f08-176">For more information, see [Product Behavior, section <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span></span> | <span data-ttu-id="c3f08-177">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c3f08-177">Windows 7</span></span><br/> <span data-ttu-id="c3f08-178">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c3f08-178">Windows Server 2008 R2</span></span><br/> |
| <span data-ttu-id="c3f08-179">\_класс драйвера \_ принтера</span><span class="sxs-lookup"><span data-stu-id="c3f08-179">PRINTER\_DRIVER\_CLASS</span></span><br/> <span data-ttu-id="c3f08-180">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c3f08-180">0x00000008</span></span><br/>                 | <span data-ttu-id="c3f08-181">Драйвер принтера является [драйвером принтера класса](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="c3f08-181">The printer driver is a [class printer driver](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                       | <span data-ttu-id="c3f08-182">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c3f08-182">Windows 8</span></span><br/> <span data-ttu-id="c3f08-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3f08-183">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="c3f08-184">\_ \_ производный драйвер принтера</span><span class="sxs-lookup"><span data-stu-id="c3f08-184">PRINTER\_DRIVER\_DERIVED</span></span><br/> <span data-ttu-id="c3f08-185">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3f08-185">0x00000010</span></span><br/>               | <span data-ttu-id="c3f08-186">Драйвер принтера является [производным драйвером принтера](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="c3f08-186">The printer driver is a [derived printer driver](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                   | <span data-ttu-id="c3f08-187">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c3f08-187">Windows 8</span></span><br/> <span data-ttu-id="c3f08-188">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3f08-188">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="c3f08-189">\_драйвер принтера \_ не является \_ общим</span><span class="sxs-lookup"><span data-stu-id="c3f08-189">PRINTER\_DRIVER\_NOT\_SHAREABLE</span></span><br/> <span data-ttu-id="c3f08-190">0x00000020</span><span class="sxs-lookup"><span data-stu-id="c3f08-190">0x00000020</span></span><br/>        | <span data-ttu-id="c3f08-191">Принтеры, использующие этот драйвер принтера, не могут быть общими.</span><span class="sxs-lookup"><span data-stu-id="c3f08-191">Printers using this printer driver cannot be shared.</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="c3f08-192">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c3f08-192">Windows 8</span></span><br/> <span data-ttu-id="c3f08-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3f08-193">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="c3f08-194">\_ \_ Факс категории драйвера \_ принтера</span><span class="sxs-lookup"><span data-stu-id="c3f08-194">PRINTER\_DRIVER\_CATEGORY\_FAX</span></span><br/> <span data-ttu-id="c3f08-195">0x00000040</span><span class="sxs-lookup"><span data-stu-id="c3f08-195">0x00000040</span></span><br/>         | <span data-ttu-id="c3f08-196">Драйвер принтера предназначен для использования с [принтерами факсов](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="c3f08-196">The printer driver is intended for use with [fax printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                    | <span data-ttu-id="c3f08-197">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c3f08-197">Windows 8</span></span><br/> <span data-ttu-id="c3f08-198">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3f08-198">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="c3f08-199">\_ \_ файл категории драйверов \_ принтера</span><span class="sxs-lookup"><span data-stu-id="c3f08-199">PRINTER\_DRIVER\_CATEGORY\_FILE</span></span><br/> <span data-ttu-id="c3f08-200">0x00000080</span><span class="sxs-lookup"><span data-stu-id="c3f08-200">0x00000080</span></span><br/>        | <span data-ttu-id="c3f08-201">Драйвер принтера предназначен для использования с [файловыми принтерами](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="c3f08-201">The printer driver is intended for use with [file printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                  | <span data-ttu-id="c3f08-202">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c3f08-202">Windows 8</span></span><br/> <span data-ttu-id="c3f08-203">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3f08-203">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="c3f08-204">\_Категория драйвера \_ принтера \_ виртуальный</span><span class="sxs-lookup"><span data-stu-id="c3f08-204">PRINTER\_DRIVER\_CATEGORY\_VIRTUAL</span></span><br/> <span data-ttu-id="c3f08-205">0x00000100</span><span class="sxs-lookup"><span data-stu-id="c3f08-205">0x00000100</span></span><br/>     | <span data-ttu-id="c3f08-206">Драйвер принтера предназначен для использования с [виртуальными принтерами](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="c3f08-206">The printer driver is intended for use with [virtual printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                            | <span data-ttu-id="c3f08-207">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c3f08-207">Windows 8</span></span><br/> <span data-ttu-id="c3f08-208">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3f08-208">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="c3f08-209">\_ \_ Служба категории драйверов \_ принтера</span><span class="sxs-lookup"><span data-stu-id="c3f08-209">PRINTER\_DRIVER\_CATEGORY\_SERVICE</span></span><br/> <span data-ttu-id="c3f08-210">0x00000200</span><span class="sxs-lookup"><span data-stu-id="c3f08-210">0x00000200</span></span><br/>     | <span data-ttu-id="c3f08-211">Драйвер принтера предназначен для использования с [принтерами служб](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="c3f08-211">The printer driver is intended for use with [service printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                            | <span data-ttu-id="c3f08-212">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c3f08-212">Windows 8</span></span><br/> <span data-ttu-id="c3f08-213">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3f08-213">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="c3f08-214">\_ \_ требуется программный \_ Сброс \_ драйвера принтера</span><span class="sxs-lookup"><span data-stu-id="c3f08-214">PRINTER\_DRIVER\_SOFT\_RESET\_REQUIRED</span></span><br/> <span data-ttu-id="c3f08-215">0x00000400</span><span class="sxs-lookup"><span data-stu-id="c3f08-215">0x00000400</span></span><br/> | <span data-ttu-id="c3f08-216">Принтеры, использующие этот драйвер принтера, должны следовать рекомендациям, описанным в определении класса USB-устройства.</span><span class="sxs-lookup"><span data-stu-id="c3f08-216">Printers that use this printer driver should follow the guidelines outlined in the USB Device Class Definition.</span></span> <span data-ttu-id="c3f08-217">Дополнительные сведения см. в [разделе поведение продукта, раздел <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)</span><span class="sxs-lookup"><span data-stu-id="c3f08-217">For more information, see [Product Behavior, section <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)</span></span>                                                                      | <span data-ttu-id="c3f08-218">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c3f08-218">Windows 8</span></span><br/> <span data-ttu-id="c3f08-219">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3f08-219">Windows Server 2012</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="c3f08-220">**псззкоредривердепенденЦиес**</span><span class="sxs-lookup"><span data-stu-id="c3f08-220">**pszzCoreDriverDependencies**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-221">Указатель на многострочную строку, завершающуюся нулем, которая указывает все основные драйверы принтера, от которых зависит драйвер.</span><span class="sxs-lookup"><span data-stu-id="c3f08-221">A pointer to a null-terminated multi-string that specifies all the core printer drivers that the driver depends on.</span></span> <span data-ttu-id="c3f08-222">Это значение должно быть **равно NULL** , если **\_ сведения о драйвере \_ 8** передаются в [**аддпринтердривер**](addprinterdriver.md) или [**аддпринтердриверекс**](addprinterdriverex.md).</span><span class="sxs-lookup"><span data-stu-id="c3f08-222">This must be **NULL** if the **DRIVER\_INFO\_8** is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-223">**фтмининбоксдривервердате**</span><span class="sxs-lookup"><span data-stu-id="c3f08-223">**ftMinInboxDriverVerDate**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-224">Самая ранняя допустимая дата всех драйверов, поставляемых вместе с Windows, а также от которых зависит этот драйвер.</span><span class="sxs-lookup"><span data-stu-id="c3f08-224">The earliest allowed date of any drivers that shipped with Windows and on which this driver depends.</span></span>

</dd> <dt>

<span data-ttu-id="c3f08-225">**двлмининбоксдриверверверсион**</span><span class="sxs-lookup"><span data-stu-id="c3f08-225">**dwlMinInboxDriverVerVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c3f08-226">Самая ранняя разрешенная версия всех драйверов, поставляемых вместе с Windows и для которой зависит этот драйвер.</span><span class="sxs-lookup"><span data-stu-id="c3f08-226">The earliest allowed version of any drivers that shipped with Windows and on which this driver depends.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3f08-227">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3f08-227">Remarks</span></span>

<span data-ttu-id="c3f08-228">Строки для этих элементов содержатся в INF-файле, который используется для добавления драйвера.</span><span class="sxs-lookup"><span data-stu-id="c3f08-228">The strings for these members are contained in the .inf file that is used to add the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3f08-229">Требования</span><span class="sxs-lookup"><span data-stu-id="c3f08-229">Requirements</span></span>



| <span data-ttu-id="c3f08-230">Требование</span><span class="sxs-lookup"><span data-stu-id="c3f08-230">Requirement</span></span> | <span data-ttu-id="c3f08-231">Значение</span><span class="sxs-lookup"><span data-stu-id="c3f08-231">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f08-232">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3f08-232">Minimum supported client</span></span><br/> | <span data-ttu-id="c3f08-233">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c3f08-233">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c3f08-234">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3f08-234">Minimum supported server</span></span><br/> | <span data-ttu-id="c3f08-235">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c3f08-235">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c3f08-236">Header</span><span class="sxs-lookup"><span data-stu-id="c3f08-236">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3f08-237"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3f08-237"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c3f08-238">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="c3f08-238">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c3f08-239">**\_ \_ Сведения о \_ драйвере 8W** (Юникод) и **\_ \_ сведения о драйвере \_ 8A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c3f08-239">**\_DRIVER\_INFO\_8W** (Unicode) and **\_DRIVER\_INFO\_8A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="c3f08-240">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3f08-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3f08-241">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="c3f08-241">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c3f08-242">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="c3f08-242">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="c3f08-243">**аддпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="c3f08-243">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="c3f08-244">**аддпринтердриверекс**</span><span class="sxs-lookup"><span data-stu-id="c3f08-244">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> </dl>

 

