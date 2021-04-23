---
title: Системмонитор Скллогсетнаме, свойство
description: Возвращает или задает понятное имя набора журналов.
ms.assetid: a4593743-6b70-4f70-8e91-3324a808d97b
keywords:
- Сисмон свойство Скллогсетнаме
- Свойство Скллогсетнаме Сисмон, интерфейс Системмонитор
- Интерфейс Системмонитор Сисмон, свойство Скллогсетнаме
topic_type:
- apiref
api_name:
- SystemMonitor.SqlLogSetName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be20ccc561eb3e9292b4a95dcc654ed7bac00ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071079"
---
# <a name="systemmonitorsqllogsetname-property"></a><span data-ttu-id="44ff2-106">Свойство Системмонитор:: Скллогсетнаме</span><span class="sxs-lookup"><span data-stu-id="44ff2-106">SystemMonitor::SqlLogSetName property</span></span>

<span data-ttu-id="44ff2-107">Возвращает или задает понятное имя набора журналов.</span><span class="sxs-lookup"><span data-stu-id="44ff2-107">Retrieves or sets the friendly name of the log set.</span></span>

## <a name="syntax"></a><span data-ttu-id="44ff2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44ff2-108">Syntax</span></span>


```VB
Property SqlLogSetName As String
```



## <a name="property-value"></a><span data-ttu-id="44ff2-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="44ff2-109">Property value</span></span>

<span data-ttu-id="44ff2-110">Понятное имя набора журналов, которое соответствует одному файлу журнала, содержащему двоичные или текстовые данные в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="44ff2-110">Friendly name of the log set, which corresponds to a single log file containing binary or text data in the SQL database.</span></span>

## <a name="remarks"></a><span data-ttu-id="44ff2-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44ff2-111">Remarks</span></span>

<span data-ttu-id="44ff2-112">**До Windows Vista:** Невозможно изменить это свойство, если для [**системмонитор. DataSourceType**](systemmonitor-datasourcetype.md) задано значение сисмонскллог.</span><span class="sxs-lookup"><span data-stu-id="44ff2-112">**Prior to Windows Vista:** You cannot modify this property if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonSqlLog.</span></span>

## <a name="requirements"></a><span data-ttu-id="44ff2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="44ff2-113">Requirements</span></span>



| <span data-ttu-id="44ff2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="44ff2-114">Requirement</span></span> | <span data-ttu-id="44ff2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="44ff2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44ff2-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44ff2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="44ff2-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="44ff2-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="44ff2-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44ff2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="44ff2-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="44ff2-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="44ff2-120">DLL</span><span class="sxs-lookup"><span data-stu-id="44ff2-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44ff2-121"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="44ff2-121"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44ff2-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44ff2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44ff2-123">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="44ff2-123">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="44ff2-124">**Системмонитор. Склдсннаме**</span><span class="sxs-lookup"><span data-stu-id="44ff2-124">**SystemMonitor.SqlDsnName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





