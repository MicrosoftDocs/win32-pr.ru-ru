---
description: Уведомление СПФИЛЕНОТИФИ \_ таржетексистс отправляется в подпрограммы обратного вызова, если копируемый файл был помещен в очередь с \_ \_ флагом обновления нуверврите и этот файл уже существует в целевом каталоге.
ms.assetid: 5c6e0c59-0340-4aa6-94db-8d9a5d202758
title: Сообщение SPFILENOTIFY_TARGETEXISTS (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d0c1a1ffba520789113b0dc78246657a4fe324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423982"
---
# <a name="spfilenotify_targetexists-message"></a><span data-ttu-id="938c8-103">\_Сообщение спфиленотифи таржетексистс</span><span class="sxs-lookup"><span data-stu-id="938c8-103">SPFILENOTIFY\_TARGETEXISTS message</span></span>

<span data-ttu-id="938c8-104">Уведомление **спфиленотифи \_ таржетексистс** отправляется в подпрограммы обратного вызова, если копируемый файл был помещен в очередь с \_ \_ флагом обновления нуверврите и этот файл уже существует в целевом каталоге.</span><span class="sxs-lookup"><span data-stu-id="938c8-104">The **SPFILENOTIFY\_TARGETEXISTS** notification is sent to the callback routine if the file to be copied was queued with the SP\_COPY\_NOOVERWRITE flag and that file already exists in the target directory.</span></span> <span data-ttu-id="938c8-105">Его можно отправить в подпрограммы обратного вызова отдельно или в сочетании с помощью оператора OR с уведомлениями [**спфиленотифи \_ лангмисматч**](spfilenotify-langmismatch.md) и/или [**спфиленотифи \_ таржетневер**](spfilenotify-targetnewer.md) .</span><span class="sxs-lookup"><span data-stu-id="938c8-105">It can be sent to the callback routine alone or combined, by using the OR operator, with the [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) and/or [**SPFILENOTIFY\_TARGETNEWER**](spfilenotify-targetnewer.md) notifications.</span></span>


```C++
SPFILENOTIFY_TARGETEXISTS
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="938c8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="938c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="938c8-107">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="938c8-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="938c8-108">Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) , содержащую сведения о путях для исходного и целевого файлов.</span><span class="sxs-lookup"><span data-stu-id="938c8-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths for the source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="938c8-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="938c8-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="938c8-110">Этот параметр не используется, если это уведомление не объединено с помощью оператора или с уведомлением [**спфиленотифи \_ лангмисматч**](spfilenotify-langmismatch.md) .</span><span class="sxs-lookup"><span data-stu-id="938c8-110">This parameter is not used unless this notification is combined, by using the OR operator, with the [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="938c8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="938c8-111">Return value</span></span>

<span data-ttu-id="938c8-112">Подпрограммы обратного вызова должны возвращать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="938c8-112">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="938c8-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="938c8-113">Return code</span></span>                                                                          | <span data-ttu-id="938c8-114">Описание</span><span class="sxs-lookup"><span data-stu-id="938c8-114">Description</span></span>                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="938c8-115"><dt>**УСЛОВИЯ**</dt></span><span class="sxs-lookup"><span data-stu-id="938c8-115"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="938c8-116">Перезапишите файл в целевом каталоге.</span><span class="sxs-lookup"><span data-stu-id="938c8-116">Overwrite the file in the target directory.</span></span><br/> |
| <dl> <span data-ttu-id="938c8-117"><dt>**ISFALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="938c8-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="938c8-118">Пропустить текущую операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="938c8-118">Skip the current copy operation.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="938c8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="938c8-119">Requirements</span></span>



| <span data-ttu-id="938c8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="938c8-120">Requirement</span></span> | <span data-ttu-id="938c8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="938c8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="938c8-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="938c8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="938c8-123">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="938c8-123">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="938c8-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="938c8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="938c8-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="938c8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="938c8-126">Header</span><span class="sxs-lookup"><span data-stu-id="938c8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="938c8-127"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="938c8-127"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="938c8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="938c8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="938c8-129">Обзор</span><span class="sxs-lookup"><span data-stu-id="938c8-129">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="938c8-130">Уведомления</span><span class="sxs-lookup"><span data-stu-id="938c8-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="938c8-131">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="938c8-131">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="938c8-132">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="938c8-132">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="938c8-133">**сетупдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="938c8-133">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="938c8-134">**сетупинсталлфиле**</span><span class="sxs-lookup"><span data-stu-id="938c8-134">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="938c8-135">**сетупинсталлфиликс**</span><span class="sxs-lookup"><span data-stu-id="938c8-135">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="938c8-136">**сетупинсталлфроминфсектион**</span><span class="sxs-lookup"><span data-stu-id="938c8-136">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




