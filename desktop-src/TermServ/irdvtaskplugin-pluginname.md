---
title: Свойство PluginName Ирдвтаскплугин (Тспубплугинком. h)
description: Содержит отображаемое имя агента задач.
ms.assetid: 6f414270-e90b-4075-80fe-f918acbdd205
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства PluginName
- Службы удаленных рабочих столов свойства PluginName, интерфейс Ирдвтаскплугин
- Службы удаленных рабочих столов интерфейса Ирдвтаскплугин, свойство PluginName
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.PluginName
- IRDVTaskPlugin.get_PluginName
api_location:
- tspubplugincom.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0262472e37a8ff3e5b9bb153d2e94f4e52029b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802705"
---
# <a name="irdvtaskpluginpluginname-property"></a><span data-ttu-id="493e1-106">Ирдвтаскплугин: свойство Лугиннаме:P</span><span class="sxs-lookup"><span data-stu-id="493e1-106">IRDVTaskPlugin::PluginName property</span></span>

<span data-ttu-id="493e1-107">Содержит отображаемое имя агента задач.</span><span class="sxs-lookup"><span data-stu-id="493e1-107">Contains the display name of the task agent.</span></span> <span data-ttu-id="493e1-108">Это имя используется только в целях ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="493e1-108">This name is used for logging purposes only.</span></span>

<span data-ttu-id="493e1-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="493e1-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="493e1-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="493e1-110">Syntax</span></span>


```C++
HRESULT get_PluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="493e1-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="493e1-111">Property value</span></span>

<span data-ttu-id="493e1-112">Отображаемое имя агента задачи.</span><span class="sxs-lookup"><span data-stu-id="493e1-112">The display name of the task agent.</span></span>

## <a name="requirements"></a><span data-ttu-id="493e1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="493e1-113">Requirements</span></span>



| <span data-ttu-id="493e1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="493e1-114">Requirement</span></span> | <span data-ttu-id="493e1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="493e1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="493e1-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="493e1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="493e1-117">Windows 7 Корпоративная</span><span class="sxs-lookup"><span data-stu-id="493e1-117">Windows 7 Enterprise</span></span><br/>                                                             |
| <span data-ttu-id="493e1-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="493e1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="493e1-119">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="493e1-119">Windows Server 2008 R2</span></span><br/>                                                           |
| <span data-ttu-id="493e1-120">Header</span><span class="sxs-lookup"><span data-stu-id="493e1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="493e1-121"><dt>Тспубплугинком. h</dt></span><span class="sxs-lookup"><span data-stu-id="493e1-121"><dt>Tspubplugincom.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="493e1-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="493e1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="493e1-123">**ирдвтаскплугин**</span><span class="sxs-lookup"><span data-stu-id="493e1-123">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





