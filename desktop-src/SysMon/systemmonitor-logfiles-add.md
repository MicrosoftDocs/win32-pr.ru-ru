---
title: Файл журнала. Add, метод
description: Добавляет файл журнала в коллекцию.
ms.assetid: f6b671ea-9620-49a7-8b0c-0c8e1d9819b0
keywords:
- Добавить метод Сисмон
- Метод Add Сисмон, класс LogFile
- Файл_журнала класса Сисмон, Add метод
topic_type:
- apiref
api_name:
- LogFiles.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f690670606cd7ee307ba945fc2daabe92953e81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135998"
---
# <a name="logfilesadd-method"></a><span data-ttu-id="72cf1-106">Файл журнала. Add, метод</span><span class="sxs-lookup"><span data-stu-id="72cf1-106">LogFiles.Add method</span></span>

<span data-ttu-id="72cf1-107">Добавляет файл журнала в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="72cf1-107">Adds a log file to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="72cf1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72cf1-108">Syntax</span></span>


```VB
LogFiles.Add( _
  ByVal pathname As String _
) As LogFileItem
```



## <a name="parameters"></a><span data-ttu-id="72cf1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="72cf1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72cf1-110">*путь к файлу* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="72cf1-110">*pathname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72cf1-111">Путь к файлу журнала.</span><span class="sxs-lookup"><span data-stu-id="72cf1-111">Path to the log file.</span></span> <span data-ttu-id="72cf1-112">Путь можно указать как абсолютный, относительный или UNC-путь.</span><span class="sxs-lookup"><span data-stu-id="72cf1-112">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="72cf1-113">Имя файла журнала должно иметь расширение CSV, TSV или BLG.</span><span class="sxs-lookup"><span data-stu-id="72cf1-113">The log file name extension must be either .csv, .tsv, or .blg.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72cf1-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="72cf1-114">Remarks</span></span>

<span data-ttu-id="72cf1-115">Для создания файлов журналов, добавляемых в эту коллекцию, необходимо использовать средство Logman.exe или оснастку MMC Perfmon. msc.</span><span class="sxs-lookup"><span data-stu-id="72cf1-115">You must use the Logman.exe tool or the Perfmon.msc MMC snap-in to generate the log files that you add to this collection.</span></span> <span data-ttu-id="72cf1-116">Для Perfmon. msc журналы счетчиков находятся в папке **журналы и оповещения производительности**.</span><span class="sxs-lookup"><span data-stu-id="72cf1-116">For Perfmon.msc, the counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="72cf1-117">Дополнительные сведения об использовании Logman.exe или Perfmon. msc см. в подокне **центра справки и поддержки**, которое можно найти по программе Logman.</span><span class="sxs-lookup"><span data-stu-id="72cf1-117">For details on using Logman.exe or Perfmon.msc, search for Logman or Using Performance, respectively, in the **Help and Support Center**.</span></span>

<span data-ttu-id="72cf1-118">**До Windows Vista:** Невозможно добавить файлы журнала в [**коллекцию файлов журнала**](systemmonitor-logfiles.md) , если для [**системмонитор. DataSourceType**](systemmonitor-datasourcetype.md) задано значение [**DataSourceTypeConstants.sysмонлогфилес**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="72cf1-118">**Prior to Windows Vista:** You cannot add log files to the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="72cf1-119">Сначала задайте **системмонитор. DataSourceType** для **DataSourceTypeConstants.sysмоннуллдатасаурце**, добавьте файлы журнала и счетчики, а затем установите **Системмонитор. DataSourceType** в **DataSourceTypeConstants.sysмонлогфилес**.</span><span class="sxs-lookup"><span data-stu-id="72cf1-119">First, set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonNullDataSource**, add your log files and counters, and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonLogFiles**.</span></span>

## <a name="requirements"></a><span data-ttu-id="72cf1-120">Требования</span><span class="sxs-lookup"><span data-stu-id="72cf1-120">Requirements</span></span>



| <span data-ttu-id="72cf1-121">Требование</span><span class="sxs-lookup"><span data-stu-id="72cf1-121">Requirement</span></span> | <span data-ttu-id="72cf1-122">Значение</span><span class="sxs-lookup"><span data-stu-id="72cf1-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72cf1-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="72cf1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="72cf1-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="72cf1-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="72cf1-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="72cf1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="72cf1-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="72cf1-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72cf1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="72cf1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72cf1-128"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="72cf1-128"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72cf1-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72cf1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72cf1-130">LogFiles</span><span class="sxs-lookup"><span data-stu-id="72cf1-130">LogFiles</span></span>](logfiles.md)
</dt> <dt>

[<span data-ttu-id="72cf1-131">**логфилеитем**</span><span class="sxs-lookup"><span data-stu-id="72cf1-131">**LogFileItem**</span></span>](logfileitem.md)
</dt> <dt>

[<span data-ttu-id="72cf1-132">**LogFiles**</span><span class="sxs-lookup"><span data-stu-id="72cf1-132">**LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> </dl>

 

 





