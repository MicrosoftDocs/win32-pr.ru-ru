---
description: Уведомление СПФИЛЕНОТИФИ \_ нидневкабинет отправляется сетупитератекабинет, чтобы указать, что текущий файл продолжится в другом CAB-файле.
ms.assetid: 01207429-11fb-4e2c-89ba-54321992e953
title: Сообщение SPFILENOTIFY_NEEDNEWCABINET (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3187d48b89579c329a4d0163e151824288462344
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272439"
---
# <a name="spfilenotify_neednewcabinet-message"></a><span data-ttu-id="dc611-103">\_Сообщение спфиленотифи нидневкабинет</span><span class="sxs-lookup"><span data-stu-id="dc611-103">SPFILENOTIFY\_NEEDNEWCABINET message</span></span>

<span data-ttu-id="dc611-104">Уведомление **спфиленотифи \_ нидневкабинет** отправляется [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) , чтобы указать, что текущий файл продолжится в другом CAB-файле.</span><span class="sxs-lookup"><span data-stu-id="dc611-104">The **SPFILENOTIFY\_NEEDNEWCABINET** notification is sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) to indicate that the current file continues in another cabinet.</span></span> <span data-ttu-id="dc611-105">Затем подпрограммы обратного вызова могут вызвать [**сетуппромптфордиск**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)или создать собственное диалоговое окно, предлагающее пользователю вставить следующий диск.</span><span class="sxs-lookup"><span data-stu-id="dc611-105">Your callback routine can then call [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), or create its own dialog box to prompt the user to insert the next disk.</span></span>


```C++
SPFILENOTIFY_NEEDNEWCABINET
  Param1 = (UINT) CabinetInfo;
  Param2 = (UINT) NewPath;
            
```



## <a name="parameters"></a><span data-ttu-id="dc611-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc611-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc611-107">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="dc611-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="dc611-108">Указатель на [**\_ информационную структуру CAB**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) -файла, содержащий сведения о ящике и извлекаемом файле.</span><span class="sxs-lookup"><span data-stu-id="dc611-108">Pointer to a [**CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) structure that contains information about the cabinet and the file to be extracted.</span></span>

</dd> <dt>

<span data-ttu-id="dc611-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="dc611-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="dc611-110">Если обратный вызов не возвращает \_ ошибку, этот параметр является указателем на строку, завершающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="dc611-110">If the callback returns NO\_ERROR, this parameter is a pointer to a null-terminated string.</span></span> <span data-ttu-id="dc611-111">Если строка не пуста, она указывает новый путь к CAB-файлу.</span><span class="sxs-lookup"><span data-stu-id="dc611-111">If the string is not empty, it specifies a new path to the cabinet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc611-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc611-112">Return value</span></span>

<span data-ttu-id="dc611-113">Ваша подпрограммы должна возвращать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="dc611-113">Your routine should return one of the following values.</span></span>



| <span data-ttu-id="dc611-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dc611-114">Return code</span></span>                                                                                 | <span data-ttu-id="dc611-115">Описание</span><span class="sxs-lookup"><span data-stu-id="dc611-115">Description</span></span>                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dc611-116"><dt>**БЕЗ \_ ошибок**</dt></span><span class="sxs-lookup"><span data-stu-id="dc611-116"><dt>**NO\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="dc611-117">Ошибок не обнаружено, продолжить обработку CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="dc611-117">No error was encountered, continue processing the cabinet.</span></span><br/>                                                                                                                                                                        |
| <dl> <span data-ttu-id="dc611-118"><dt>\**Ошибка \_ при* XXX \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="dc611-118"><dt>\**ERROR\_* XXX\*\*\*</dt></span></span> </dl> | <span data-ttu-id="dc611-119">Произошла ошибка указанного типа.</span><span class="sxs-lookup"><span data-stu-id="dc611-119">An error of the specified type occurred.</span></span> <span data-ttu-id="dc611-120">Функция [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) вернет **значение false**, а указанный код ошибки будет возвращен вызовом [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="dc611-120">The [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function will return **FALSE**, and the specified error code will be returned by a call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="dc611-121">Нет подпрограммы обратного вызова CAB-файла по умолчанию; Поэтому необходимо предоставить подпрограммы обратного вызова для работы с уведомлениями, отправленными [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="dc611-121">There is no default cabinet callback routine; thus, you must supply a callback routine to handle the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

 

## <a name="remarks"></a><span data-ttu-id="dc611-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc611-122">Remarks</span></span>

<span data-ttu-id="dc611-123">Если подпрограммы обратного вызова не возвращают \_ ошибку, [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) проверяет буфер, на который указывает *Param2*.</span><span class="sxs-lookup"><span data-stu-id="dc611-123">If the callback routine returns NO\_ERROR, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) checks the buffer pointed to by *Param2*.</span></span> <span data-ttu-id="dc611-124">Если буфер не пуст, он содержит новый исходный путь.</span><span class="sxs-lookup"><span data-stu-id="dc611-124">If the buffer is not empty, then it contains a new source path.</span></span> <span data-ttu-id="dc611-125">Если буфер пуст, предполагается, что исходный путь не изменен.</span><span class="sxs-lookup"><span data-stu-id="dc611-125">If the buffer is empty, the source path is assumed to be unchanged.</span></span>

<span data-ttu-id="dc611-126">Функция обратного вызова должна обеспечить доступность CAB-файла перед возвратом, вызвав функцию [**сетуппромптфордиск**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) , если требуется вставить новый носитель.</span><span class="sxs-lookup"><span data-stu-id="dc611-126">Your callback function should ensure that the cabinet is accessible before it returns, calling the [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) function, if new media needs to be inserted.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc611-127">Требования</span><span class="sxs-lookup"><span data-stu-id="dc611-127">Requirements</span></span>



| <span data-ttu-id="dc611-128">Требование</span><span class="sxs-lookup"><span data-stu-id="dc611-128">Requirement</span></span> | <span data-ttu-id="dc611-129">Значение</span><span class="sxs-lookup"><span data-stu-id="dc611-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc611-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc611-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dc611-131">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dc611-131">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dc611-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc611-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dc611-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dc611-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc611-134">Header</span><span class="sxs-lookup"><span data-stu-id="dc611-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc611-135"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc611-135"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc611-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc611-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc611-137">Обзор</span><span class="sxs-lookup"><span data-stu-id="dc611-137">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="dc611-138">Уведомления</span><span class="sxs-lookup"><span data-stu-id="dc611-138">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="dc611-139">**сведения о CAB-файле \_**</span><span class="sxs-lookup"><span data-stu-id="dc611-139">**CABINET\_INFO**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a)
</dt> <dt>

[<span data-ttu-id="dc611-140">**сетупитератекабинет**</span><span class="sxs-lookup"><span data-stu-id="dc611-140">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

