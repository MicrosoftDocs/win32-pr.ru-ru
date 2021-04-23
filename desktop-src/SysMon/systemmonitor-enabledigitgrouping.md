---
title: Системмонитор. Енабледигитграупинг, свойство
description: Возвращает или задает значение, определяющее, использует ли СИСМОН группирование цифр при отображении числовых значений.
ms.assetid: 6a277960-fd01-423c-af2a-b35ed46c6d9a
keywords:
- Сисмон свойство Енабледигитграупинг
- Свойство Енабледигитграупинг Сисмон, объект Системмонитор
- Сисмон объекта Системмонитор, свойство Енабледигитграупинг
topic_type:
- apiref
api_name:
- SystemMonitor.EnableDigitGrouping
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66da0ad5ade7f3e01f58ef29bbd1094634c01b37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415592"
---
# <a name="systemmonitorenabledigitgrouping-property"></a><span data-ttu-id="32272-106">Системмонитор. Енабледигитграупинг, свойство</span><span class="sxs-lookup"><span data-stu-id="32272-106">SystemMonitor.EnableDigitGrouping property</span></span>

<span data-ttu-id="32272-107">Возвращает или задает значение, определяющее, использует ли СИСМОН группирование цифр при отображении числовых значений.</span><span class="sxs-lookup"><span data-stu-id="32272-107">Retrieves or sets a value that determines if SYSMON uses digit grouping when displaying numeric values.</span></span>

## <a name="syntax"></a><span data-ttu-id="32272-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32272-108">Syntax</span></span>


```VB
Property EnableDigitGrouping As Boolean
```



## <a name="property-value"></a><span data-ttu-id="32272-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="32272-109">Property value</span></span>

<span data-ttu-id="32272-110">Если значение равно true, СИСМОН будет Группировать цифры при отображении числовых значений, например 1 214.</span><span class="sxs-lookup"><span data-stu-id="32272-110">If True, SYSMON will group digits when displaying numeric values, for example, 1,214.</span></span> <span data-ttu-id="32272-111">Если значение равно false, то числовые значения не группируются, например 1214.</span><span class="sxs-lookup"><span data-stu-id="32272-111">If False, numeric values are not grouped, for example, 1214.</span></span> <span data-ttu-id="32272-112">Значение true используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="32272-112">True is the default.</span></span>

## <a name="remarks"></a><span data-ttu-id="32272-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32272-113">Remarks</span></span>

<span data-ttu-id="32272-114">Символ группирования цифр локализован.</span><span class="sxs-lookup"><span data-stu-id="32272-114">The digit grouping symbol is localized.</span></span>

## <a name="requirements"></a><span data-ttu-id="32272-115">Требования</span><span class="sxs-lookup"><span data-stu-id="32272-115">Requirements</span></span>



| <span data-ttu-id="32272-116">Требование</span><span class="sxs-lookup"><span data-stu-id="32272-116">Requirement</span></span> | <span data-ttu-id="32272-117">Значение</span><span class="sxs-lookup"><span data-stu-id="32272-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32272-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32272-118">Minimum supported client</span></span><br/> | <span data-ttu-id="32272-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32272-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32272-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32272-120">Minimum supported server</span></span><br/> | <span data-ttu-id="32272-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="32272-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32272-122">DLL</span><span class="sxs-lookup"><span data-stu-id="32272-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32272-123"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="32272-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





