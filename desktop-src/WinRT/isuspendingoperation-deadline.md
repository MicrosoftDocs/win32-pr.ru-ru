---
description: Возвращает время, оставшееся до того, как будет продолжаться операция приостановки отложенного приложения.
ms.assetid: A90347F3-75CB-4EEB-930D-30882F43D192
title: 'Исуспендингоператион: свойство еадлине:D (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.Deadline
- ISuspendingOperation.get_Deadline
- ISuspendingOperation.put_Deadline
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 305610108b7a138693ccdce97e35ddbe90451806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991122"
---
# <a name="isuspendingoperationdeadline-property"></a><span data-ttu-id="e08ab-103">Исуспендингоператион: свойство еадлине:D</span><span class="sxs-lookup"><span data-stu-id="e08ab-103">ISuspendingOperation::Deadline property</span></span>

<span data-ttu-id="e08ab-104">Возвращает время, оставшееся до того, как будет продолжаться операция приостановки отложенного приложения.</span><span class="sxs-lookup"><span data-stu-id="e08ab-104">Gets the time remaining before a delayed app suspending operation continues.</span></span>

<span data-ttu-id="e08ab-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e08ab-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e08ab-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e08ab-106">Syntax</span></span>


```C++
HRESULT put_Deadline();

HRESULT get_Deadline(
  [out, retval] DateTime *value
);
```



## <a name="property-value"></a><span data-ttu-id="e08ab-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e08ab-107">Property value</span></span>

<span data-ttu-id="e08ab-108">Время, оставшееся до того, как будет приостановлена отложенная операция приостановки приложения.</span><span class="sxs-lookup"><span data-stu-id="e08ab-108">The time remaining before a delayed app suspending operation continues.</span></span>

## <a name="requirements"></a><span data-ttu-id="e08ab-109">Требования</span><span class="sxs-lookup"><span data-stu-id="e08ab-109">Requirements</span></span>



| <span data-ttu-id="e08ab-110">Требование</span><span class="sxs-lookup"><span data-stu-id="e08ab-110">Requirement</span></span> | <span data-ttu-id="e08ab-111">Значение</span><span class="sxs-lookup"><span data-stu-id="e08ab-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e08ab-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e08ab-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e08ab-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e08ab-113">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e08ab-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e08ab-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e08ab-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e08ab-115">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e08ab-116">Header</span><span class="sxs-lookup"><span data-stu-id="e08ab-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="e08ab-117"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="e08ab-117"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="e08ab-118">IDL</span><span class="sxs-lookup"><span data-stu-id="e08ab-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e08ab-119"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e08ab-119"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e08ab-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e08ab-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e08ab-121">**исуспендингоператион**</span><span class="sxs-lookup"><span data-stu-id="e08ab-121">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 




