---
description: '\_ \_ Уведомление SIGNERINFO спфиленотифи куеуескан отправляется в подпрограммы обратного вызова сетупсканфилекуеуе для каждого узла в подочереди копирования очереди файлов.'
ms.assetid: 5b22e8ba-9a18-461b-bad7-b2d76f83d7f3
title: Сообщение SPFILENOTIFY_QUEUESCAN_SIGNERINFO (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29bf9e9c7e0ab76303d8c2fb21a0109ec60358f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998872"
---
# <a name="spfilenotify_queuescan_signerinfo-message"></a><span data-ttu-id="290b8-103">СПФИЛЕНОТИФИ \_ куеуескан \_ SIGNERINFO сообщение</span><span class="sxs-lookup"><span data-stu-id="290b8-103">SPFILENOTIFY\_QUEUESCAN\_SIGNERINFO message</span></span>

<span data-ttu-id="290b8-104">Уведомление **\_ \_ SIGNERINFO спфиленотифи куеуескан** отправляется в подпрограммы обратного вызова [**сетупсканфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) для каждого узла в подочереди копирования очереди файлов.</span><span class="sxs-lookup"><span data-stu-id="290b8-104">The **SPFILENOTIFY\_QUEUESCAN\_SIGNERINFO** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="290b8-105">Это происходит только в том случае, если функция **сетупсканфилекуеуе** была вызвана указанием флага СПК \_ Scan \_ использовать \_ обратный вызов \_ SIGNERINFO.</span><span class="sxs-lookup"><span data-stu-id="290b8-105">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACK\_SIGNERINFO.</span></span> <span data-ttu-id="290b8-106">Доступно начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="290b8-106">Available starting with Windows XP.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN_SIGNERINFO
  Param1 = (PFILEPATHS_SIGNERINFO) Filepaths;
            
```



## <a name="parameters"></a><span data-ttu-id="290b8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="290b8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="290b8-108">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="290b8-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="290b8-109">Указатель на структуру [**\_ SIGNERINFO filePaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) .</span><span class="sxs-lookup"><span data-stu-id="290b8-109">Pointer to a [**FILEPATHS\_SIGNERINFO**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) structure.</span></span> <span data-ttu-id="290b8-110">**Целевой** элемент — это имя файла целевого файла в системе.</span><span class="sxs-lookup"><span data-stu-id="290b8-110">The **Target** member is the filename of the target file on the system.</span></span> <span data-ttu-id="290b8-111">**Исходный** элемент — это ожидаемый путь к исходному файлу.</span><span class="sxs-lookup"><span data-stu-id="290b8-111">The **Source** member is the expected path of the source file.</span></span> <span data-ttu-id="290b8-112">Элемент **Win32Error** является ошибкой подписывания.</span><span class="sxs-lookup"><span data-stu-id="290b8-112">The **Win32Error** member is the signing error.</span></span> <span data-ttu-id="290b8-113">Сведения о сигнатуре возвращаются, если подпрограммы обратного вызова возвращают **Win32Error**= = No \_ Error.</span><span class="sxs-lookup"><span data-stu-id="290b8-113">Signature information is returned if the callback routine returns **Win32Error**==NO\_ERROR.</span></span> <span data-ttu-id="290b8-114">Член **дигиталсигнер** — это цифровой подписывающий.</span><span class="sxs-lookup"><span data-stu-id="290b8-114">The **DigitalSigner** member is the digital signer.</span></span> <span data-ttu-id="290b8-115">Версия является членом **версии** .</span><span class="sxs-lookup"><span data-stu-id="290b8-115">The **Version** member is the version.</span></span> <span data-ttu-id="290b8-116">**Каталогфиле** — это файл каталога.</span><span class="sxs-lookup"><span data-stu-id="290b8-116">The **CatalogFile** is the catalog file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="290b8-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="290b8-117">Return value</span></span>

<span data-ttu-id="290b8-118">Подпрограмма обратного вызова должна возвращать [код системной ошибки](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="290b8-118">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="290b8-119">Если подпрограмма обратного вызова не возвращает \_ ошибку, сканирование очереди продолжится и возвращает значение, если процедура возвращает любой другой код ошибки, сканирование очереди прерывается, а [**Сетупсканфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) возвращает **false**.</span><span class="sxs-lookup"><span data-stu-id="290b8-119">If the callback routine returns NO\_ERROR, the queue scan continues, and returns If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="290b8-120">Это уведомление не обрабатывается функцией [**сетупдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .</span><span class="sxs-lookup"><span data-stu-id="290b8-120">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="290b8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="290b8-121">Requirements</span></span>



| <span data-ttu-id="290b8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="290b8-122">Requirement</span></span> | <span data-ttu-id="290b8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="290b8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="290b8-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="290b8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="290b8-125">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="290b8-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="290b8-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="290b8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="290b8-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="290b8-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="290b8-128">Header</span><span class="sxs-lookup"><span data-stu-id="290b8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="290b8-129"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="290b8-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="290b8-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="290b8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="290b8-131">Обзор</span><span class="sxs-lookup"><span data-stu-id="290b8-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="290b8-132">Уведомления</span><span class="sxs-lookup"><span data-stu-id="290b8-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="290b8-133">**сетупсканфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="290b8-133">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

