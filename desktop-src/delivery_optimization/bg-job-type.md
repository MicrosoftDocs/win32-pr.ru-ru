---
title: Перечисление BG_JOB_TYPE (Deliveryoptimization. h)
description: Перечисление BG_JOB_TYPE определяет постоянные значения, указывающие тип задания перемещения, например download.
ms.assetid: 696A43C3-1FA2-436D-B34A-3544E7C9A66A
keywords:
- Перечисление BG_JOB_TYPE
topic_type:
- apiref
api_name:
- BG_JOB_TYPE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1f672bcf2d2538bfaa9b9573fa1dfa71ee7b9cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490065"
---
# <a name="bg_job_type-enumeration"></a><span data-ttu-id="05ac3-104">Перечисление BG_JOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="05ac3-104">BG_JOB_TYPE enumeration</span></span>

<span data-ttu-id="05ac3-105">Перечисление **BG_JOB_TYPE** определяет постоянные значения, указывающие тип задания перемещения, например download.</span><span class="sxs-lookup"><span data-stu-id="05ac3-105">The **BG_JOB_TYPE** enumeration defines constant values that specify the type of transfer job, such as download.</span></span>

## <a name="syntax"></a><span data-ttu-id="05ac3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05ac3-106">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_TYPE_DOWNLOAD
} BG_JOB_TYPE;
```



## <a name="constants"></a><span data-ttu-id="05ac3-107">Константы</span><span class="sxs-lookup"><span data-stu-id="05ac3-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="05ac3-108"><span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**</span><span class="sxs-lookup"><span data-stu-id="05ac3-108"><span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="05ac3-109">Указывает, что задание загружает файлы на клиент.</span><span class="sxs-lookup"><span data-stu-id="05ac3-109">Specifies that the job downloads files to the client.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05ac3-110">Требования</span><span class="sxs-lookup"><span data-stu-id="05ac3-110">Requirements</span></span>



| <span data-ttu-id="05ac3-111">Требование</span><span class="sxs-lookup"><span data-stu-id="05ac3-111">Requirement</span></span> | <span data-ttu-id="05ac3-112">Значение</span><span class="sxs-lookup"><span data-stu-id="05ac3-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05ac3-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="05ac3-113">Minimum supported client</span></span><br/> | <span data-ttu-id="05ac3-114">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="05ac3-114">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="05ac3-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="05ac3-115">Minimum supported server</span></span><br/> | <span data-ttu-id="05ac3-116">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="05ac3-116">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="05ac3-117">Header</span><span class="sxs-lookup"><span data-stu-id="05ac3-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="05ac3-118"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="05ac3-118"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05ac3-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05ac3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05ac3-120">**Использованием метода ibackgroundcopyjob:: GetType**</span><span class="sxs-lookup"><span data-stu-id="05ac3-120">**IBackgroundCopyJob::GetType**</span></span>](ibackgroundcopyjob-gettype.md)
</dt> <dt>

[<span data-ttu-id="05ac3-121">**Ибаккграундкопиманажер:: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="05ac3-121">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





