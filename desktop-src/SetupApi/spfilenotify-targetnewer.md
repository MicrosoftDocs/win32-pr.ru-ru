---
description: Уведомление СПФИЛЕНОТИФИ \_ таржетневер отправляется в подсистему обратного вызова, если копируемый файл был поставлен в очередь с \_ \_ указанными флагами SP Copy новее или SP \_ Copy \_ Force более поздней \_ версии, а более новая версия файла уже существует в целевом каталоге.
ms.assetid: 93bcd610-f75d-4900-841c-f67946af5c4a
title: Сообщение SPFILENOTIFY_TARGETNEWER (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c432515a5ce0e9a1eddb8ea6e92f7376c318b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663563"
---
# <a name="spfilenotify_targetnewer-message"></a><span data-ttu-id="beef0-103">\_Сообщение спфиленотифи таржетневер</span><span class="sxs-lookup"><span data-stu-id="beef0-103">SPFILENOTIFY\_TARGETNEWER message</span></span>

<span data-ttu-id="beef0-104">Уведомление **спфиленотифи \_ таржетневер** отправляется в подсистему обратного вызова, если копируемый файл был поставлен в очередь с \_ \_ указанными флагами SP Copy новее или SP \_ Copy \_ Force более поздней \_ версии, а более новая версия файла уже существует в целевом каталоге.</span><span class="sxs-lookup"><span data-stu-id="beef0-104">The **SPFILENOTIFY\_TARGETNEWER** notification is sent to the callback routine if the file to be copied was queued with the SP\_COPY\_NEWER or SP\_COPY\_FORCE\_NEWER flags specified and a newer version of the file already exists in the target directory.</span></span> <span data-ttu-id="beef0-105">Его можно отправить в подпрограммы обратного вызова отдельно или ORed вместе с [**спфиленотифи \_ лангмисматч**](spfilenotify-langmismatch.md) и/или [**спфиленотифи \_ таржетексистс**](spfilenotify-targetexists.md).</span><span class="sxs-lookup"><span data-stu-id="beef0-105">It can be sent to the callback routine alone or ORed together with [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) and/or [**SPFILENOTIFY\_TARGETEXISTS**](spfilenotify-targetexists.md).</span></span>


```C++
SPFILENOTIFY_TARGETNEWER
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="beef0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="beef0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beef0-107">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="beef0-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="beef0-108">Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) , содержащую сведения о путях для исходных и целевых файлов.</span><span class="sxs-lookup"><span data-stu-id="beef0-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths for source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="beef0-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="beef0-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="beef0-110">Этот параметр не используется, если это уведомление не объединено с помощью оператора или с [**спфиленотифи \_ лангмисматч**](spfilenotify-langmismatch.md).</span><span class="sxs-lookup"><span data-stu-id="beef0-110">This parameter is not used unless this notification is combined, by using the OR operator, with [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beef0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="beef0-111">Return value</span></span>

<span data-ttu-id="beef0-112">Подпрограммы обратного вызова должны возвращать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="beef0-112">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="beef0-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="beef0-113">Return code</span></span>                                                                          | <span data-ttu-id="beef0-114">Описание</span><span class="sxs-lookup"><span data-stu-id="beef0-114">Description</span></span>                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="beef0-115"><dt>**УСЛОВИЯ**</dt></span><span class="sxs-lookup"><span data-stu-id="beef0-115"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="beef0-116">Перезапишите файл в целевом каталоге.</span><span class="sxs-lookup"><span data-stu-id="beef0-116">Overwrite the file in the target directory.</span></span><br/> |
| <dl> <span data-ttu-id="beef0-117"><dt>**ISFALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="beef0-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="beef0-118">Пропустить текущую операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="beef0-118">Skip the current copy operation.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="beef0-119">Требования</span><span class="sxs-lookup"><span data-stu-id="beef0-119">Requirements</span></span>



| <span data-ttu-id="beef0-120">Требование</span><span class="sxs-lookup"><span data-stu-id="beef0-120">Requirement</span></span> | <span data-ttu-id="beef0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="beef0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="beef0-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="beef0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="beef0-123">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="beef0-123">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="beef0-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="beef0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="beef0-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="beef0-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="beef0-126">Header</span><span class="sxs-lookup"><span data-stu-id="beef0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="beef0-127"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="beef0-127"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beef0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="beef0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beef0-129">Обзор</span><span class="sxs-lookup"><span data-stu-id="beef0-129">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="beef0-130">Уведомления</span><span class="sxs-lookup"><span data-stu-id="beef0-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="beef0-131">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="beef0-131">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="beef0-132">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="beef0-132">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="beef0-133">**сетупдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="beef0-133">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="beef0-134">**сетупинсталлфиле**</span><span class="sxs-lookup"><span data-stu-id="beef0-134">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="beef0-135">**сетупинсталлфиликс**</span><span class="sxs-lookup"><span data-stu-id="beef0-135">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="beef0-136">**сетупинсталлфроминфсектион**</span><span class="sxs-lookup"><span data-stu-id="beef0-136">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




