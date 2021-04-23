---
title: Системмонитор. LogFileName, свойство
description: Возвращает или задает имя файла журнала, используемого в качестве источника значений счетчиков, отображаемых в системном мониторе.
ms.assetid: a93d1c98-4875-4d8e-940c-4443d1e585e6
keywords:
- Сисмон свойство LogFileName
- LogFileName Property Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, свойство LogFileName
topic_type:
- apiref
api_name:
- SystemMonitor.LogFileName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6168f416d1bdab47a4c2952ac60ee7e67397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415580"
---
# <a name="systemmonitorlogfilename-property"></a><span data-ttu-id="a3398-106">Системмонитор. LogFileName, свойство</span><span class="sxs-lookup"><span data-stu-id="a3398-106">SystemMonitor.LogFileName property</span></span>

<span data-ttu-id="a3398-107">Возвращает или задает имя файла журнала, используемого в качестве источника значений счетчиков, отображаемых в системном мониторе.</span><span class="sxs-lookup"><span data-stu-id="a3398-107">Retrieves or sets the name of a log file to use as the source of counter values displayed in the System Monitor.</span></span>

> [!Note]  
> <span data-ttu-id="a3398-108">Это свойство стало устаревшим в свойстве [**файл_журнала**](systemmonitor-logfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="a3398-108">This property has been made obsolete by the [**LogFiles**](systemmonitor-logfiles.md) property.</span></span>

 

<span data-ttu-id="a3398-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a3398-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3398-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3398-110">Syntax</span></span>


```VB
Property LogFileName As String
```



## <a name="property-value"></a><span data-ttu-id="a3398-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a3398-111">Property value</span></span>

<span data-ttu-id="a3398-112">Путь к файлу журнала.</span><span class="sxs-lookup"><span data-stu-id="a3398-112">Path to the log file.</span></span> <span data-ttu-id="a3398-113">Можно указать абсолютный, относительный или UNC-путь.</span><span class="sxs-lookup"><span data-stu-id="a3398-113">You can specify an absolute, relative, or UNC path.</span></span> <span data-ttu-id="a3398-114">Имя файла журнала должно иметь расширение CSV, TSV или BLG.</span><span class="sxs-lookup"><span data-stu-id="a3398-114">The log file name extension must be either .csv, .tsv, or .blg.</span></span>

## <a name="exceptions"></a><span data-ttu-id="a3398-115">Исключения</span><span class="sxs-lookup"><span data-stu-id="a3398-115">Exceptions</span></span>



| <span data-ttu-id="a3398-116">Тип исключения</span><span class="sxs-lookup"><span data-stu-id="a3398-116">Exception type</span></span>                                  | <span data-ttu-id="a3398-117">Условие</span><span class="sxs-lookup"><span data-stu-id="a3398-117">Condition</span></span>                                                              |
|-------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="a3398-118">**System. Runtime. InteropServices. COMException**</span><span class="sxs-lookup"><span data-stu-id="a3398-118">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="a3398-119">Не удалось найти указанный файл.</span><span class="sxs-lookup"><span data-stu-id="a3398-119">Unable to find the specified file.</span></span> <span data-ttu-id="a3398-120">Значение Err. Number — 0xC0000BD1.</span><span class="sxs-lookup"><span data-stu-id="a3398-120">The Err.Number value is 0xC0000BD1.</span></span> |
| <span data-ttu-id="a3398-121">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="a3398-121">**System.ArgumentException**</span></span>                    | <span data-ttu-id="a3398-122">Нельзя задавать пустую строку.</span><span class="sxs-lookup"><span data-stu-id="a3398-122">You cannot specify an empty string.</span></span>                                    |



 

## <a name="remarks"></a><span data-ttu-id="a3398-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3398-123">Remarks</span></span>

<span data-ttu-id="a3398-124">Это свойство возвращает имя файла журнала из первого члена коллекции файлов [**журнала**](systemmonitor-logfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="a3398-124">This property returns the log file name from the first member of the [**LogFiles**](systemmonitor-logfiles.md) collection.</span></span>

<span data-ttu-id="a3398-125">Установка этого свойства завершится ошибкой, если коллекция файлов [**журнала**](systemmonitor-logfiles.md) содержит один или несколько элементов.</span><span class="sxs-lookup"><span data-stu-id="a3398-125">Setting this property will fail if the [**LogFiles**](systemmonitor-logfiles.md) collection contains one or more members.</span></span>

<span data-ttu-id="a3398-126">Для создания файлов журналов, добавляемых в эту коллекцию, необходимо использовать средство Logman.exe или оснастку MMC Perfmon. msc.</span><span class="sxs-lookup"><span data-stu-id="a3398-126">You must use the Logman.exe tool or the Perfmon.msc MMC snap-in to generate the log files that you add to this collection.</span></span> <span data-ttu-id="a3398-127">Для Perfmon. msc журналы счетчиков находятся в папке **журналы и оповещения производительности**.</span><span class="sxs-lookup"><span data-stu-id="a3398-127">For Perfmon.msc, the counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="a3398-128">Дополнительные сведения об использовании Logman.exe или Perfmon. msc см. в подокне **центра справки и поддержки**, которое можно найти по программе Logman.</span><span class="sxs-lookup"><span data-stu-id="a3398-128">For details on using Logman.exe or Perfmon.msc, search for Logman or Using Performance, respectively, in the **Help and Support Center**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3398-129">Требования</span><span class="sxs-lookup"><span data-stu-id="a3398-129">Requirements</span></span>



| <span data-ttu-id="a3398-130">Требование</span><span class="sxs-lookup"><span data-stu-id="a3398-130">Requirement</span></span> | <span data-ttu-id="a3398-131">Значение</span><span class="sxs-lookup"><span data-stu-id="a3398-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3398-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3398-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a3398-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a3398-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a3398-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3398-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a3398-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a3398-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a3398-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a3398-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3398-137"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="a3398-137"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3398-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3398-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3398-139">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="a3398-139">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="a3398-140">**Системмонитор. DataSourceType**</span><span class="sxs-lookup"><span data-stu-id="a3398-140">**SystemMonitor.DataSourceType**</span></span>](systemmonitor-datasourcetype.md)
</dt> </dl>

 

 





