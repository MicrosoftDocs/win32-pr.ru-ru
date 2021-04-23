---
title: Системмонитор. Relog, метод
description: Выполняет перезапись данных счетчиков в новый файл. Этот метод также можно использовать для указания нового типа файлов и для сокращения числа выборок, содержащихся в файле журнала.
ms.assetid: 4439f9ef-99e0-47d4-8f6f-d08afcba672d
keywords:
- Метод Relog Сисмон
- Метод Relog Сисмон, объект Системмонитор
- Системмонитор объекта Сисмон, метод Relog
topic_type:
- apiref
api_name:
- SystemMonitor.Relog
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d0a6e44ef73652bd563099929ce601670610b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135651"
---
# <a name="systemmonitorrelog-method"></a><span data-ttu-id="1f8dc-107">Системмонитор. Relog, метод</span><span class="sxs-lookup"><span data-stu-id="1f8dc-107">SystemMonitor.Relog method</span></span>

<span data-ttu-id="1f8dc-108">Выполняет перезапись данных счетчиков в новый файл.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-108">Relogs the counter data to a new file.</span></span> <span data-ttu-id="1f8dc-109">Этот метод также можно использовать для указания нового типа файлов и для сокращения числа выборок, содержащихся в файле журнала.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-109">You can also use this method to specify a new file type and to reduce the number of samples contained in the log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f8dc-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f8dc-110">Syntax</span></span>


```VB
SystemMonitor.Relog( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType, _
  ByVal filter As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="1f8dc-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f8dc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f8dc-112">*имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1f8dc-112">*fileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f8dc-113">Путь к файлу журнала.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-113">File path of the log file.</span></span> <span data-ttu-id="1f8dc-114">Путь можно указать как абсолютный, относительный или UNC-путь.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-114">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="1f8dc-115">Имя файла журнала должно иметь расширение. BLG,. tsv или. csv.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-115">The log file name extension must be either .blg, .tsv, or .csv.</span></span> <span data-ttu-id="1f8dc-116">Если папка в пути не существует, СИСМОН создаст ее.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-116">If a folder in the path does not exist, SYSMON will create it.</span></span> <span data-ttu-id="1f8dc-117">Если файл существует, файл перезаписывается.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-117">If the file exists, the file is overwritten.</span></span> <span data-ttu-id="1f8dc-118">СИСМОН применяет ACL по умолчанию из родительского каталога.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-118">SYSMON applies the default ACLs from the parent directory.</span></span>

</dd> <dt>

<span data-ttu-id="1f8dc-119">*тип* \[ файла окне\]</span><span class="sxs-lookup"><span data-stu-id="1f8dc-119">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f8dc-120">Формат данных счетчиков, сохраненных в файле журнала.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-120">Format of the counter data saved to the log file.</span></span> <span data-ttu-id="1f8dc-121">Можно указать либо [**SysmonFileType.sysмонфилеблг**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysмонфилексв**, либо **SysmonFileType.sysмонфилетсв**.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-121">You can specify either [**SysmonFileType.sysmonFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysmonFileCsv**, or **SysmonFileType.sysmonFileTsv**.</span></span>

</dd> <dt>

<span data-ttu-id="1f8dc-122">*Фильтр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1f8dc-122">*filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f8dc-123">Число выборок из старых файлов журнала для сохранения в новом файле журнала.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-123">Number of samples from the old log files to save in the new log file.</span></span> <span data-ttu-id="1f8dc-124">Укажите значение 1, чтобы сохранить все примеры из старых файлов в новые файлы.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-124">Specify 1 to save every sample from the old files to the new files.</span></span> <span data-ttu-id="1f8dc-125">Укажите значение 2, чтобы сохранить один из двух выборок из старого файла.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-125">Specify 2 to save one out of every two samples from the old file.</span></span> <span data-ttu-id="1f8dc-126">Укажите значение 3, чтобы сохранить один из трех выборок из старого файла.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-126">Specify 3 to save one out of every three samples from the old file.</span></span> <span data-ttu-id="1f8dc-127">И т. д.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-127">And so on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f8dc-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1f8dc-128">Return value</span></span>

<span data-ttu-id="1f8dc-129">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-129">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f8dc-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f8dc-130">Remarks</span></span>

<span data-ttu-id="1f8dc-131">Этот метод использует файлы журналов, содержащиеся в коллекции [**системмонитор. файл_журнала**](systemmonitor-logfiles.md) , для записи данных счетчика в журнал.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-131">This method uses the log files contained in the [**SystemMonitor.LogFiles**](systemmonitor-logfiles.md) collection to relog the counter data.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f8dc-132">Требования</span><span class="sxs-lookup"><span data-stu-id="1f8dc-132">Requirements</span></span>



| <span data-ttu-id="1f8dc-133">Требование</span><span class="sxs-lookup"><span data-stu-id="1f8dc-133">Requirement</span></span> | <span data-ttu-id="1f8dc-134">Значение</span><span class="sxs-lookup"><span data-stu-id="1f8dc-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f8dc-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f8dc-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1f8dc-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f8dc-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1f8dc-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f8dc-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1f8dc-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1f8dc-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f8dc-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1f8dc-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f8dc-140"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="1f8dc-140"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f8dc-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f8dc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f8dc-142">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="1f8dc-142">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="1f8dc-143">**Системмонитор. SaveAs**</span><span class="sxs-lookup"><span data-stu-id="1f8dc-143">**SystemMonitor.SaveAs**</span></span>](systemmonitor-saveas.md)
</dt> </dl>

 

 





