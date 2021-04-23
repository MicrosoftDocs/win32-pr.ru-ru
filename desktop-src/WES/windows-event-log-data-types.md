---
title: Типы данных журнала событий Windows (Виневт. h)
description: Журнал событий Windows определяет следующие типы данных
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a93794d8cc3a254fe182c439698324dccdfc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802189"
---
# <a name="windows-event-log-data-types"></a><span data-ttu-id="c0e8c-106">Типы данных журнала событий Windows</span><span class="sxs-lookup"><span data-stu-id="c0e8c-106">Windows Event Log Data Types</span></span>

<span data-ttu-id="c0e8c-107">Журнал событий Windows определяет следующие типы данных:</span><span class="sxs-lookup"><span data-stu-id="c0e8c-107">Windows Event Log defines the following data types:</span></span>


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

<span data-ttu-id="c0e8c-108">**\_обработчик evt**</span><span class="sxs-lookup"><span data-stu-id="c0e8c-108">**EVT\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="c0e8c-109">Маркер объекта журнала событий Windows.</span><span class="sxs-lookup"><span data-stu-id="c0e8c-109">A handle to a Windows Event Log object.</span></span>

</dd> <dt>

<span data-ttu-id="c0e8c-110">**ПЕВТ, \_ обработчик**</span><span class="sxs-lookup"><span data-stu-id="c0e8c-110">**PEVT\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="c0e8c-111">Указатель на маркер объекта журнала событий Windows.</span><span class="sxs-lookup"><span data-stu-id="c0e8c-111">A pointer to the handle of a Windows Event Log object.</span></span>

</dd> <dt>

<span data-ttu-id="c0e8c-112">**\_ \_ \_ маркер свойства массива объектов \_ evt**</span><span class="sxs-lookup"><span data-stu-id="c0e8c-112">**EVT\_OBJECT\_ARRAY\_PROPERTY\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="c0e8c-113">Маркер массива объектов журнала событий Windows.</span><span class="sxs-lookup"><span data-stu-id="c0e8c-113">A handle to an array of Windows Event Log objects.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0e8c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c0e8c-114">Requirements</span></span>



| <span data-ttu-id="c0e8c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c0e8c-115">Requirement</span></span> | <span data-ttu-id="c0e8c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c0e8c-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c0e8c-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0e8c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c0e8c-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0e8c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c0e8c-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0e8c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c0e8c-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c0e8c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c0e8c-121">Header</span><span class="sxs-lookup"><span data-stu-id="c0e8c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0e8c-122"><dt>Виневт. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0e8c-122"><dt>WinEvt.h</dt></span></span> </dl> |



 

 





