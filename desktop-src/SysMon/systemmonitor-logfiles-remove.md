---
title: Метод LogFile. Remove
description: Удаляет указанный экземпляр Логфилеитем из коллекции.
ms.assetid: d2885ffd-5957-472c-9a67-2f1469d9b48b
keywords:
- Удалить метод Сисмон
- Remove Method Сисмон, класс файл_журнала
- Файл_журнала класса Сисмон, Remove, метод
topic_type:
- apiref
api_name:
- LogFiles.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057607c57db600ca7a28c8a5bb6d75d5570829cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803352"
---
# <a name="logfilesremove-method"></a><span data-ttu-id="4178b-106">Метод LogFile. Remove</span><span class="sxs-lookup"><span data-stu-id="4178b-106">LogFiles.Remove method</span></span>

<span data-ttu-id="4178b-107">Удаляет указанный экземпляр [**логфилеитем**](logfileitem.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="4178b-107">Removes the specified [**LogFileItem**](logfileitem.md) instance from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4178b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4178b-108">Syntax</span></span>


```VB
LogFiles.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="4178b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4178b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4178b-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4178b-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4178b-111">Целочисленный индекс файла журнала, который необходимо удалить из коллекции.</span><span class="sxs-lookup"><span data-stu-id="4178b-111">Integer index of the log file to remove from the collection.</span></span> <span data-ttu-id="4178b-112">Индекс основан на единицах.</span><span class="sxs-lookup"><span data-stu-id="4178b-112">The index is one-based.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4178b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4178b-113">Return value</span></span>

<span data-ttu-id="4178b-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4178b-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4178b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4178b-115">Remarks</span></span>

<span data-ttu-id="4178b-116">**До Windows Vista:** Невозможно удалить файлы журнала из [**коллекции файлов журнала**](systemmonitor-logfiles.md) , если для [**системмонитор. DataSourceType**](systemmonitor-datasourcetype.md) задано значение сисмонлогфилес.</span><span class="sxs-lookup"><span data-stu-id="4178b-116">**Prior to Windows Vista:** You cannot remove log files from the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonLogFiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="4178b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4178b-117">Requirements</span></span>



| <span data-ttu-id="4178b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4178b-118">Requirement</span></span> | <span data-ttu-id="4178b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4178b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4178b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4178b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4178b-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4178b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4178b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4178b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4178b-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4178b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4178b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4178b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4178b-125"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="4178b-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4178b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4178b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4178b-127">LogFiles</span><span class="sxs-lookup"><span data-stu-id="4178b-127">LogFiles</span></span>](logfiles.md)
</dt> <dt>

[<span data-ttu-id="4178b-128">**логфилеитем**</span><span class="sxs-lookup"><span data-stu-id="4178b-128">**LogFileItem**</span></span>](logfileitem.md)
</dt> <dt>

[<span data-ttu-id="4178b-129">**LogFiles**</span><span class="sxs-lookup"><span data-stu-id="4178b-129">**LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> </dl>

 

 





