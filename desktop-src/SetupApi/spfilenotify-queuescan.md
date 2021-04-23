---
description: Уведомление СПФИЛЕНОТИФИ \_ куеуескан отправляется в подпрограммы обратного вызова с помощью сетупсканфилекуеуе для каждого узла в подочереди копирования очереди файлов. Это происходит только в том случае, если функция Сетупсканфилекуеуе была вызвана указанием флага СПК \_ проверки \_ использования \_ обратного вызова.
ms.assetid: 8aacc6c0-b6fe-4b4a-bbe4-a0351baf1f30
title: Сообщение SPFILENOTIFY_QUEUESCAN (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66202a398f7e3f4e1121782f9469d2d6f299452c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664080"
---
# <a name="spfilenotify_queuescan-message"></a><span data-ttu-id="b5be3-104">\_Сообщение спфиленотифи куеуескан</span><span class="sxs-lookup"><span data-stu-id="b5be3-104">SPFILENOTIFY\_QUEUESCAN message</span></span>

<span data-ttu-id="b5be3-105">Уведомление **спфиленотифи \_ куеуескан** отправляется в подпрограммы обратного вызова с помощью [**сетупсканфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) для каждого узла в подочереди копирования очереди файлов.</span><span class="sxs-lookup"><span data-stu-id="b5be3-105">The **SPFILENOTIFY\_QUEUESCAN** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="b5be3-106">Это происходит только в том случае, если функция **сетупсканфилекуеуе** была вызвана указанием флага СПК \_ проверки \_ использования \_ обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="b5be3-106">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACK.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN
  Param1 = (UINT) TargetPath;
  Param2 = (UINT) DelayFlag;
            
```



## <a name="parameters"></a><span data-ttu-id="b5be3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5be3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5be3-108">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="b5be3-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="b5be3-109">Строка, заканчивающаяся нулем, которая указывает сведения о целевом пути для файла, помещенного в очередь текущего узла.</span><span class="sxs-lookup"><span data-stu-id="b5be3-109">Null-terminated string that specifies the target path information for the file queued in the current node.</span></span>

</dd> <dt>

<span data-ttu-id="b5be3-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="b5be3-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="b5be3-111">Если файл в текущем узле очереди используется, *Param2* принимает значение СПК \_ delay \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="b5be3-111">If the file in the current node of the queue is in use, *Param2* takes the value SPQ\_DELAYED\_COPY.</span></span> <span data-ttu-id="b5be3-112">Если файл не используется, значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b5be3-112">If the file is not in use, the value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5be3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5be3-113">Return value</span></span>

<span data-ttu-id="b5be3-114">Подпрограмма обратного вызова должна возвращать [код системной ошибки](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b5be3-114">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="b5be3-115">Если подпрограммы обратного вызова не возвращают \_ ошибок, сканирование очереди продолжится.</span><span class="sxs-lookup"><span data-stu-id="b5be3-115">If the callback routine returns NO\_ERROR, the queue scan continues.</span></span> <span data-ttu-id="b5be3-116">Если процедура возвращает любой другой код ошибки, сканирование очереди будет прервано, а [**сетупсканфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-116">If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="b5be3-117">Это уведомление не обрабатывается функцией [**сетупдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .</span><span class="sxs-lookup"><span data-stu-id="b5be3-117">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b5be3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b5be3-118">Requirements</span></span>



| <span data-ttu-id="b5be3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b5be3-119">Requirement</span></span> | <span data-ttu-id="b5be3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b5be3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5be3-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5be3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b5be3-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b5be3-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b5be3-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5be3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b5be3-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b5be3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b5be3-125">Header</span><span class="sxs-lookup"><span data-stu-id="b5be3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5be3-126"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5be3-126"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5be3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5be3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5be3-128">Обзор</span><span class="sxs-lookup"><span data-stu-id="b5be3-128">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="b5be3-129">Уведомления</span><span class="sxs-lookup"><span data-stu-id="b5be3-129">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="b5be3-130">**сетупсканфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="b5be3-130">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

