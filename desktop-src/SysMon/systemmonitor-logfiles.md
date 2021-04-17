---
title: Системмонитор. файл_журнала, свойство
description: Коллекция из одного или нескольких файлов журнала, используемых в качестве источника значений счетчиков, отображаемых в системном мониторе.
ms.assetid: 6e9e7205-3516-404d-b67d-777e484900da
keywords:
- Свойства файлов журнала Сисмон
- Свойство Файл_журналаs Сисмон, объект Системмонитор
- Системмонитор объекта Сисмон, свойство файл_журнала
topic_type:
- apiref
api_name:
- SystemMonitor.LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8127433319290b44498b272834923784b714052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661891"
---
# <a name="systemmonitorlogfiles-property"></a><span data-ttu-id="c01f8-106">Системмонитор. файл_журнала, свойство</span><span class="sxs-lookup"><span data-stu-id="c01f8-106">SystemMonitor.LogFiles property</span></span>

<span data-ttu-id="c01f8-107">Коллекция из одного или нескольких файлов журнала, используемых в качестве источника значений счетчиков, отображаемых в системном мониторе.</span><span class="sxs-lookup"><span data-stu-id="c01f8-107">Collection of one or more log files to use as the source of counter values displayed in the System Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="c01f8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c01f8-108">Syntax</span></span>


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a><span data-ttu-id="c01f8-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c01f8-109">Property value</span></span>

<span data-ttu-id="c01f8-110">Коллекция объектов [**логфилеитем**](logfileitem.md) , которые указывают файлы журналов, используемые в качестве источника данных для графа.</span><span class="sxs-lookup"><span data-stu-id="c01f8-110">Collection of [**LogFileItem**](logfileitem.md) objects that specify the log files used as the data source for the graph.</span></span>

## <a name="remarks"></a><span data-ttu-id="c01f8-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c01f8-111">Remarks</span></span>

<span data-ttu-id="c01f8-112">Чтобы добавить или удалить файл журнала из коллекции файлов журнала, значение [**системмонитор. DataSourceType**](systemmonitor-datasourcetype.md) не должно быть установлено в сисмонлогфилес.</span><span class="sxs-lookup"><span data-stu-id="c01f8-112">To add or remove a log file from the log file collection, the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) must not be set to sysmonLogFiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="c01f8-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c01f8-113">Requirements</span></span>



| <span data-ttu-id="c01f8-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c01f8-114">Requirement</span></span> | <span data-ttu-id="c01f8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c01f8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c01f8-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c01f8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c01f8-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c01f8-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c01f8-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c01f8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c01f8-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c01f8-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c01f8-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c01f8-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c01f8-121"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="c01f8-121"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c01f8-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c01f8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c01f8-123">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="c01f8-123">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="c01f8-124">**Системмонитор. DataSourceType**</span><span class="sxs-lookup"><span data-stu-id="c01f8-124">**SystemMonitor.DataSourceType**</span></span>](systemmonitor-datasourcetype.md)
</dt> <dt>

[<span data-ttu-id="c01f8-125">**Системмонитор. Логвиевстарт**</span><span class="sxs-lookup"><span data-stu-id="c01f8-125">**SystemMonitor.LogViewStart**</span></span>](systemmonitor-logviewstart.md)
</dt> <dt>

[<span data-ttu-id="c01f8-126">**Системмонитор. Логвиевстоп**</span><span class="sxs-lookup"><span data-stu-id="c01f8-126">**SystemMonitor.LogViewStop**</span></span>](systemmonitor-logviewstop.md)
</dt> <dt>

[<span data-ttu-id="c01f8-127">**Системмонитор. Скллогсетнаме**</span><span class="sxs-lookup"><span data-stu-id="c01f8-127">**SystemMonitor.SqlLogSetName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





