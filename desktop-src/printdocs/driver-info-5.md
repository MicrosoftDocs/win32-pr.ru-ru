---
description: Структура драйвера \_ \_ 5 содержит сведения о драйвере принтера.
ms.assetid: 6fb63a9f-5227-46a3-97dc-8de1968e9d63
title: Структура DRIVER_INFO_5 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_5
- _DRIVER_INFO_5A
- _DRIVER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 11281e69b70b2d87d354138a6313c8bca6673944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693574"
---
# <a name="driver_info_5-structure"></a><span data-ttu-id="64156-103">\_Сведения о драйвере \_ 5 структура</span><span class="sxs-lookup"><span data-stu-id="64156-103">DRIVER\_INFO\_5 structure</span></span>

<span data-ttu-id="64156-104">Структура **драйвера \_ \_ 5** содержит сведения о драйвере принтера.</span><span class="sxs-lookup"><span data-stu-id="64156-104">The **DRIVER\_INFO\_5** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="64156-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64156-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_5 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  DWORD  dwDriverAttributes;
  DWORD  dwConfigVersion;
  DWORD  dwDriverVersion;
} DRIVER_INFO_5, *PDRIVER_INFO_5;
```



## <a name="members"></a><span data-ttu-id="64156-106">Члены</span><span class="sxs-lookup"><span data-stu-id="64156-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="64156-107">**кверсион**</span><span class="sxs-lookup"><span data-stu-id="64156-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="64156-108">Версия операционной системы, для которой был записан драйвер.</span><span class="sxs-lookup"><span data-stu-id="64156-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="64156-109">Поддерживаемое значение равно 3.</span><span class="sxs-lookup"><span data-stu-id="64156-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="64156-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="64156-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="64156-111">Указатель на строку, завершающуюся нулем, которая указывает имя драйвера (например, QMS 810).</span><span class="sxs-lookup"><span data-stu-id="64156-111">Pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="64156-112">**пенвиронмент**</span><span class="sxs-lookup"><span data-stu-id="64156-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="64156-113">Указатель на строку, завершающуюся нулем, которая указывает среду, для которой был записан драйвер (например, Windows x86, Windows IA64 и Windows x64).</span><span class="sxs-lookup"><span data-stu-id="64156-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="64156-114">**пдриверпас**</span><span class="sxs-lookup"><span data-stu-id="64156-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="64156-115">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла для файла, содержащего драйвер устройства (например, C: \\ drivers \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="64156-115">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="64156-116">**пдатафиле**</span><span class="sxs-lookup"><span data-stu-id="64156-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="64156-117">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла для файла, содержащего данные драйвера (например, C: \\ Drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="64156-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="64156-118">**пконфигфиле**</span><span class="sxs-lookup"><span data-stu-id="64156-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="64156-119">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла для библиотеки динамической компоновки конфигурации драйвера устройства (например, C: \\ drivers \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="64156-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="64156-120">**двдривераттрибутес**</span><span class="sxs-lookup"><span data-stu-id="64156-120">**dwDriverAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="64156-121">Атрибуты драйвера, например УМПД/КМПД.</span><span class="sxs-lookup"><span data-stu-id="64156-121">Driver attributes, like UMPD/KMPD.</span></span>

</dd> <dt>

<span data-ttu-id="64156-122">**двконфигверсион**</span><span class="sxs-lookup"><span data-stu-id="64156-122">**dwConfigVersion**</span></span>
</dt> <dd>

<span data-ttu-id="64156-123">Количество раз, когда файл конфигурации для этого драйвера был обновлен или понижен с момента последнего перезапуска диспетчера очереди печати.</span><span class="sxs-lookup"><span data-stu-id="64156-123">Number of times the configuration file for this driver has been upgraded or downgraded since the last spooler restart.</span></span>

</dd> <dt>

<span data-ttu-id="64156-124">**двдриверверсион**</span><span class="sxs-lookup"><span data-stu-id="64156-124">**dwDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="64156-125">Число обновлений или понижения уровня файла драйвера для этого драйвера с момента последнего перезапуска диспетчера очереди печати.</span><span class="sxs-lookup"><span data-stu-id="64156-125">Number of times the driver file for this driver has been upgraded or downgraded since the last spooler restart.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64156-126">Требования</span><span class="sxs-lookup"><span data-stu-id="64156-126">Requirements</span></span>



| <span data-ttu-id="64156-127">Требование</span><span class="sxs-lookup"><span data-stu-id="64156-127">Requirement</span></span> | <span data-ttu-id="64156-128">Значение</span><span class="sxs-lookup"><span data-stu-id="64156-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64156-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64156-129">Minimum supported client</span></span><br/> | <span data-ttu-id="64156-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="64156-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="64156-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="64156-131">Minimum supported server</span></span><br/> | <span data-ttu-id="64156-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="64156-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="64156-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="64156-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="64156-134"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="64156-134"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="64156-135">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="64156-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="64156-136">**\_ \_ Сведения о \_ драйвере 5W** (Юникод) и **\_ \_ сведения о драйвере \_ 5A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="64156-136">**\_DRIVER\_INFO\_5W** (Unicode) and **\_DRIVER\_INFO\_5A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="64156-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64156-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64156-138">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="64156-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="64156-139">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="64156-139">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="64156-140">**аддпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="64156-140">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="64156-141">**енумпринтердриверс**</span><span class="sxs-lookup"><span data-stu-id="64156-141">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="64156-142">**жетпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="64156-142">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




