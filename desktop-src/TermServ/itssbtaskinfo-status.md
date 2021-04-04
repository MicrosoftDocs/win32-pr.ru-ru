---
title: Итссбтаскинфо, свойство состояния
description: Извлекает \_ \_ значение перечисления состояния задачи RDV, представляющее состояние задачи.
ms.assetid: 779af127-133c-47ff-8fca-bfd2c96c9768
ms.tgt_platform: multiple
keywords:
- Свойство Status службы удаленных рабочих столов
- Свойство Status службы удаленных рабочих столов, интерфейс Итссбтаскинфо
- Службы удаленных рабочих столов интерфейса Итссбтаскинфо, свойство Status
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Status
- ITsSbTaskInfo.get_Status
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3206013c32ee6cf3323f19c9e95e89c8d6756eb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802134"
---
# <a name="itssbtaskinfostatus-property"></a><span data-ttu-id="f0aee-106">Свойство Итссбтаскинфо:: Status</span><span class="sxs-lookup"><span data-stu-id="f0aee-106">ITsSbTaskInfo::Status property</span></span>

<span data-ttu-id="f0aee-107">Извлекает значение [**перечисления \_ \_ состояния задачи RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) , представляющее состояние задачи.</span><span class="sxs-lookup"><span data-stu-id="f0aee-107">Retrieves an [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

<span data-ttu-id="f0aee-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f0aee-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0aee-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0aee-109">Syntax</span></span>


```C++
HRESULT get_Status(
  [out, retval] RDV_TASK_STATUS *pStatus
);
```



## <a name="property-value"></a><span data-ttu-id="f0aee-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f0aee-110">Property value</span></span>

<span data-ttu-id="f0aee-111">Значение [**перечисления \_ \_ состояния задачи RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) , представляющее состояние задачи.</span><span class="sxs-lookup"><span data-stu-id="f0aee-111">An [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0aee-112">Требования</span><span class="sxs-lookup"><span data-stu-id="f0aee-112">Requirements</span></span>



| <span data-ttu-id="f0aee-113">Требование</span><span class="sxs-lookup"><span data-stu-id="f0aee-113">Requirement</span></span> | <span data-ttu-id="f0aee-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f0aee-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f0aee-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0aee-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f0aee-116">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f0aee-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="f0aee-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0aee-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f0aee-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f0aee-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="f0aee-119">IDL</span><span class="sxs-lookup"><span data-stu-id="f0aee-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f0aee-120"><dt>Сбтсв. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f0aee-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0aee-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0aee-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0aee-122">**итссбтаскинфо**</span><span class="sxs-lookup"><span data-stu-id="f0aee-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





