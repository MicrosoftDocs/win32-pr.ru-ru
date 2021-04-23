---
description: Структура драйвера \_ \_ 2 определяет драйвер принтера, номер версии драйвера, среду, для которой был записан драйвер, имя файла, в котором хранится драйвер, и т. д.
ms.assetid: cca1227d-69b9-44df-8dac-384c2f8843ae
title: Структура DRIVER_INFO_2 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_2
- _DRIVER_INFO_2A
- _DRIVER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: a88caf5aa10828b81dccefbe8118b3a57aebce97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711934"
---
# <a name="driver_info_2-structure"></a><span data-ttu-id="59d20-103">\_Структура сведений о драйвере \_ 2</span><span class="sxs-lookup"><span data-stu-id="59d20-103">DRIVER\_INFO\_2 structure</span></span>

<span data-ttu-id="59d20-104">Структура **драйвера \_ \_ 2** определяет драйвер принтера, номер версии драйвера, среду, для которой был записан драйвер, имя файла, в котором хранится драйвер, и т. д.</span><span class="sxs-lookup"><span data-stu-id="59d20-104">The **DRIVER\_INFO\_2** structure identifies a printer driver, the driver version number, the environment for which the driver was written, the name of the file in which the driver is stored, and so on.</span></span>

## <a name="syntax"></a><span data-ttu-id="59d20-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59d20-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_2 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
} DRIVER_INFO_2, *PDRIVER_INFO_2;
```



## <a name="members"></a><span data-ttu-id="59d20-106">Члены</span><span class="sxs-lookup"><span data-stu-id="59d20-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="59d20-107">**кверсион**</span><span class="sxs-lookup"><span data-stu-id="59d20-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="59d20-108">Версия операционной системы, для которой был записан драйвер.</span><span class="sxs-lookup"><span data-stu-id="59d20-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="59d20-109">Поддерживаемое значение равно 3.</span><span class="sxs-lookup"><span data-stu-id="59d20-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="59d20-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="59d20-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="59d20-111">Указатель на строку, завершающуюся нулем, которая указывает имя драйвера (например, "QMS 810").</span><span class="sxs-lookup"><span data-stu-id="59d20-111">A pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="59d20-112">**пенвиронмент**</span><span class="sxs-lookup"><span data-stu-id="59d20-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="59d20-113">Указатель на строку, завершающуюся нулем, которая указывает среду, для которой был записан драйвер (например, Windows x86, Windows IA64 и Windows x64).</span><span class="sxs-lookup"><span data-stu-id="59d20-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="59d20-114">**пдриверпас**</span><span class="sxs-lookup"><span data-stu-id="59d20-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="59d20-115">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла для файла, содержащего драйвер устройства (например, "c: \\ drivers \\pscript.dll").</span><span class="sxs-lookup"><span data-stu-id="59d20-115">A pointer to null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, "c:\\drivers\\pscript.dll").</span></span>

</dd> <dt>

<span data-ttu-id="59d20-116">**пдатафиле**</span><span class="sxs-lookup"><span data-stu-id="59d20-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="59d20-117">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла для файла, содержащего данные драйвера (например, "c: \\ Drivers \\ Qms810. PPD").</span><span class="sxs-lookup"><span data-stu-id="59d20-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, "c:\\drivers\\Qms810.ppd").</span></span>

</dd> <dt>

<span data-ttu-id="59d20-118">**пконфигфиле**</span><span class="sxs-lookup"><span data-stu-id="59d20-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="59d20-119">Указатель на строку, завершающуюся нулем, которая указывает имя файла или полный путь и имя файла для библиотеки конфигурации. DLL драйвера устройства (например, "c: \\ drivers \\Pscrptui.dll").</span><span class="sxs-lookup"><span data-stu-id="59d20-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device-driver's configuration .dll (for example, "c:\\drivers\\Pscrptui.dll").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59d20-120">Требования</span><span class="sxs-lookup"><span data-stu-id="59d20-120">Requirements</span></span>



| <span data-ttu-id="59d20-121">Требование</span><span class="sxs-lookup"><span data-stu-id="59d20-121">Requirement</span></span> | <span data-ttu-id="59d20-122">Значение</span><span class="sxs-lookup"><span data-stu-id="59d20-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59d20-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59d20-123">Minimum supported client</span></span><br/> | <span data-ttu-id="59d20-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="59d20-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="59d20-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59d20-125">Minimum supported server</span></span><br/> | <span data-ttu-id="59d20-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="59d20-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="59d20-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="59d20-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="59d20-128"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59d20-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="59d20-129">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="59d20-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="59d20-130">**\_ \_ Сведения о \_ драйвере (2W** Unicode) и **\_ \_ сведения о драйвере \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="59d20-130">**\_DRIVER\_INFO\_2W** (Unicode) and **\_DRIVER\_INFO\_2A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="59d20-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59d20-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59d20-132">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="59d20-132">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="59d20-133">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="59d20-133">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="59d20-134">**аддпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="59d20-134">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="59d20-135">**жетпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="59d20-135">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




