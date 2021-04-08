---
description: Возвращает операцию приостановки приложения.
ms.assetid: 33FCAED5-7568-4483-A643-A536B53F7003
title: 'Свойство Исуспендинжевентаргс:: Суспендингоператион (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs.SuspendingOperation
- ISuspendingEventArgs.get_SuspendingOperation
- ISuspendingEventArgs.put_SuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e12ccbb372d7c712585766bba8d7921fae57a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897381"
---
# <a name="isuspendingeventargssuspendingoperation-property"></a><span data-ttu-id="f44ac-103">Свойство Исуспендинжевентаргс:: Суспендингоператион</span><span class="sxs-lookup"><span data-stu-id="f44ac-103">ISuspendingEventArgs::SuspendingOperation property</span></span>

<span data-ttu-id="f44ac-104">Возвращает операцию приостановки приложения.</span><span class="sxs-lookup"><span data-stu-id="f44ac-104">Gets the app suspending operation.</span></span>

<span data-ttu-id="f44ac-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f44ac-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f44ac-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f44ac-106">Syntax</span></span>


```C++
HRESULT put_SuspendingOperation();

HRESULT get_SuspendingOperation(
  [out, retval] ISuspendingOperation **value
);
```



## <a name="property-value"></a><span data-ttu-id="f44ac-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f44ac-107">Property value</span></span>

<span data-ttu-id="f44ac-108">Приостановка операции.</span><span class="sxs-lookup"><span data-stu-id="f44ac-108">The suspending operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="f44ac-109">Требования</span><span class="sxs-lookup"><span data-stu-id="f44ac-109">Requirements</span></span>



| <span data-ttu-id="f44ac-110">Требование</span><span class="sxs-lookup"><span data-stu-id="f44ac-110">Requirement</span></span> | <span data-ttu-id="f44ac-111">Значение</span><span class="sxs-lookup"><span data-stu-id="f44ac-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f44ac-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f44ac-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f44ac-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f44ac-113">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f44ac-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f44ac-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f44ac-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f44ac-115">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f44ac-116">Header</span><span class="sxs-lookup"><span data-stu-id="f44ac-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="f44ac-117"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="f44ac-117"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="f44ac-118">IDL</span><span class="sxs-lookup"><span data-stu-id="f44ac-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f44ac-119"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f44ac-119"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f44ac-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f44ac-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f44ac-121">**исуспендинжевентаргс**</span><span class="sxs-lookup"><span data-stu-id="f44ac-121">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> </dl>

 

 




