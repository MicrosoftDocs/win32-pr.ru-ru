---
title: Системмонитор. SaveAs, метод
description: Сохраняет значения счетчиков в представлении графа в файле журнала.
ms.assetid: 34824c54-d8f4-4c2b-b417-aa0914c7164b
keywords:
- SaveAs, метод Сисмон
- Метод SaveAs Сисмон, объект Системмонитор
- Системмонитор объекта Сисмон, метод SaveAs
topic_type:
- apiref
api_name:
- SystemMonitor.SaveAs
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c6eee811a27ba295f9c6bc5c2adb20d7b715e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661887"
---
# <a name="systemmonitorsaveas-method"></a><span data-ttu-id="6be7c-106">Системмонитор. SaveAs, метод</span><span class="sxs-lookup"><span data-stu-id="6be7c-106">SystemMonitor.SaveAs method</span></span>

<span data-ttu-id="6be7c-107">Сохраняет значения счетчиков в представлении графа в файле журнала.</span><span class="sxs-lookup"><span data-stu-id="6be7c-107">Saves the counter values in the graph view to a log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6be7c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6be7c-108">Syntax</span></span>


```VB
SystemMonitor.SaveAs( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType _
)
```



## <a name="parameters"></a><span data-ttu-id="6be7c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6be7c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6be7c-110">*имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6be7c-110">*fileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6be7c-111">Путь к файлу журнала.</span><span class="sxs-lookup"><span data-stu-id="6be7c-111">File path of the log file.</span></span> <span data-ttu-id="6be7c-112">Путь можно указать как абсолютный, относительный или UNC-путь.</span><span class="sxs-lookup"><span data-stu-id="6be7c-112">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="6be7c-113">Имя файла журнала должно быть либо. TSV, либо htm.</span><span class="sxs-lookup"><span data-stu-id="6be7c-113">The log file name extension must be either .tsv or .htm.</span></span> <span data-ttu-id="6be7c-114">Если папка в пути не существует, СИСМОН создаст ее.</span><span class="sxs-lookup"><span data-stu-id="6be7c-114">If a folder in the path does not exist, SYSMON will create it.</span></span> <span data-ttu-id="6be7c-115">Если файл существует, файл перезаписывается.</span><span class="sxs-lookup"><span data-stu-id="6be7c-115">If the file exists, the file is overwritten.</span></span> <span data-ttu-id="6be7c-116">СИСМОН применяет ACL по умолчанию из родительского каталога.</span><span class="sxs-lookup"><span data-stu-id="6be7c-116">SYSMON applies the default ACLs from the parent directory.</span></span>

</dd> <dt>

<span data-ttu-id="6be7c-117">*тип* \[ файла окне\]</span><span class="sxs-lookup"><span data-stu-id="6be7c-117">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6be7c-118">Формат данных счетчиков, сохраненных в файле журнала.</span><span class="sxs-lookup"><span data-stu-id="6be7c-118">Format of the counter data saved to the log file.</span></span> <span data-ttu-id="6be7c-119">Можно указать либо [**SysmonFileType.sysмонфилехтмл**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) , либо **SysmonFileType.sysмонфилетсв**.</span><span class="sxs-lookup"><span data-stu-id="6be7c-119">You can specify either [**SysmonFileType.sysmonFileHtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) or **SysmonFileType.sysmonFileTsv**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6be7c-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6be7c-120">Return value</span></span>

<span data-ttu-id="6be7c-121">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6be7c-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6be7c-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6be7c-122">Remarks</span></span>

<span data-ttu-id="6be7c-123">Сохраняются только данные счетчиков, видимые в представлении графа (фактическое число сохраняемых точек данных, см. в разделе [**системмонитор. датапоинткаунт**](systemmonitor-datapointcount.md)).</span><span class="sxs-lookup"><span data-stu-id="6be7c-123">Only the counter data visible in the graph view is saved (for the actual number of data points saved, see [**SystemMonitor.DataPointCount**](systemmonitor-datapointcount.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="6be7c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="6be7c-124">Requirements</span></span>



| <span data-ttu-id="6be7c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="6be7c-125">Requirement</span></span> | <span data-ttu-id="6be7c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="6be7c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6be7c-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6be7c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6be7c-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6be7c-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6be7c-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6be7c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6be7c-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6be7c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6be7c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6be7c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6be7c-132"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="6be7c-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6be7c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6be7c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6be7c-134">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="6be7c-134">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="6be7c-135">**Системмонитор. Relog**</span><span class="sxs-lookup"><span data-stu-id="6be7c-135">**SystemMonitor.Relog**</span></span>](systemmonitor-relog.md)
</dt> </dl>

 

 





