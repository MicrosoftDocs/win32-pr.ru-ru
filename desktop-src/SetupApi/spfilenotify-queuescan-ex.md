---
description: Уведомление СПФИЛЕНОТИФИ \_ куеуескан \_ ex отправляется в подпрограммы обратного вызова с помощью сетупсканфилекуеуе для каждого узла в подочереди копирования очереди файлов.
ms.assetid: 293e63f9-9567-4ea7-b7e5-e5046c8a704b
title: Сообщение SPFILENOTIFY_QUEUESCAN_EX (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e18cf1cdb1cd007dcf46793d2d018dedd80037
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908808"
---
# <a name="spfilenotify_queuescan_ex-message"></a><span data-ttu-id="6c792-103">\_Сообщение спфиленотифи куеуескан \_ ex</span><span class="sxs-lookup"><span data-stu-id="6c792-103">SPFILENOTIFY\_QUEUESCAN\_EX message</span></span>

<span data-ttu-id="6c792-104">Уведомление **спфиленотифи \_ куеуескан \_ ex** отправляется в подпрограммы обратного вызова с помощью [**сетупсканфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) для каждого узла в подочереди копирования очереди файлов.</span><span class="sxs-lookup"><span data-stu-id="6c792-104">The **SPFILENOTIFY\_QUEUESCAN\_EX** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="6c792-105">Это происходит только в том случае, если функция **сетупсканфилекуеуе** была вызвана указанием флага СПК \_ Scan \_ использовать \_ каллбаккекс.</span><span class="sxs-lookup"><span data-stu-id="6c792-105">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACKEX.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN_EX
  Param1 = (PFILEPATHS) Filepaths;
            
```



## <a name="parameters"></a><span data-ttu-id="6c792-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c792-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c792-107">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="6c792-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="6c792-108">Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="6c792-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="6c792-109">**Целевой** элемент — это имя файла целевого файла в системе.</span><span class="sxs-lookup"><span data-stu-id="6c792-109">The **Target** member is the filename of the target file on the system.</span></span> <span data-ttu-id="6c792-110">**Исходный** элемент — это ожидаемый путь к исходному файлу.</span><span class="sxs-lookup"><span data-stu-id="6c792-110">The **Source** member is the expected path of the source file.</span></span> <span data-ttu-id="6c792-111">Элемент **Win32Error** является ошибкой подписывания.</span><span class="sxs-lookup"><span data-stu-id="6c792-111">The **Win32Error** member is the signing error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c792-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c792-112">Return value</span></span>

<span data-ttu-id="6c792-113">Подпрограмма обратного вызова должна возвращать [код системной ошибки](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="6c792-113">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="6c792-114">Если подпрограммы обратного вызова не возвращают \_ ошибок, сканирование очереди продолжится.</span><span class="sxs-lookup"><span data-stu-id="6c792-114">If the callback routine returns NO\_ERROR, the queue scan continues.</span></span> <span data-ttu-id="6c792-115">Если процедура возвращает любой другой код ошибки, сканирование очереди будет прервано, а [**сетупсканфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) возвращает значение false.</span><span class="sxs-lookup"><span data-stu-id="6c792-115">If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns FALSE.</span></span>

> [!Note]  
> <span data-ttu-id="6c792-116">Это уведомление не обрабатывается функцией [**сетупдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .</span><span class="sxs-lookup"><span data-stu-id="6c792-116">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6c792-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6c792-117">Requirements</span></span>



| <span data-ttu-id="6c792-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6c792-118">Requirement</span></span> | <span data-ttu-id="6c792-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6c792-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c792-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c792-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6c792-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6c792-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6c792-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c792-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6c792-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6c792-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c792-124">Header</span><span class="sxs-lookup"><span data-stu-id="6c792-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c792-125"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c792-125"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c792-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c792-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c792-127">Обзор</span><span class="sxs-lookup"><span data-stu-id="6c792-127">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="6c792-128">Уведомления</span><span class="sxs-lookup"><span data-stu-id="6c792-128">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="6c792-129">**сетупсканфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="6c792-129">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

