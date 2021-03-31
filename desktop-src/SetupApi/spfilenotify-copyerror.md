---
description: Уведомление СПФИЛЕНОТИФИ \_ коперрор отправляется в подпрограммы обратного вызова, если во время операции копирования файла возникает ошибка.
ms.assetid: d6096954-c6a5-44d4-a358-c1320c50730a
title: Сообщение SPFILENOTIFY_COPYERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cd44daabd6a4aed5e61a716bab3df44f35fc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910332"
---
# <a name="spfilenotify_copyerror-message"></a><span data-ttu-id="9ee7b-103">\_Сообщение спфиленотифи коперрор</span><span class="sxs-lookup"><span data-stu-id="9ee7b-103">SPFILENOTIFY\_COPYERROR message</span></span>

<span data-ttu-id="9ee7b-104">Уведомление **спфиленотифи \_ коперрор** отправляется в подпрограммы обратного вызова, если во время операции копирования файла возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="9ee7b-104">The **SPFILENOTIFY\_COPYERROR** notification is sent to the callback routine if an error occurs during a file copy operation.</span></span>


```C++
SPFILENOTIFY_COPYERROR
  Param1 = (UINT_PTR) FilePathInfo;
  Param2 = (UINT_PTR) ReturnBuffer;
            
```



## <a name="parameters"></a><span data-ttu-id="9ee7b-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ee7b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ee7b-106">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="9ee7b-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="9ee7b-107">Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="9ee7b-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9ee7b-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="9ee7b-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="9ee7b-109">Указатель на буфер (максимальный размер символов пути), в \_ котором хранятся новые сведения о пути, указанные пользователем.</span><span class="sxs-lookup"><span data-stu-id="9ee7b-109">Pointer to a buffer, of size MAX\_PATH characters, that stores new path information specified by the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ee7b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ee7b-110">Return value</span></span>

<span data-ttu-id="9ee7b-111">Обратный вызов должен возвращать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9ee7b-111">The callback should return one of the following values.</span></span>



| <span data-ttu-id="9ee7b-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9ee7b-112">Return code</span></span>                                                                                    | <span data-ttu-id="9ee7b-113">Описание</span><span class="sxs-lookup"><span data-stu-id="9ee7b-113">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9ee7b-114"><dt>**прервать ФИЛЕОП \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9ee7b-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl>   | <span data-ttu-id="9ee7b-115">Обработка очереди должна быть отменена.</span><span class="sxs-lookup"><span data-stu-id="9ee7b-115">Queue processing should be canceled.</span></span> <span data-ttu-id="9ee7b-116">[**Сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) возвращает ноль, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) Возвращает расширенные сведения об ошибке, такие как ошибка \_ отмены (если пользователь был отменен) или ошибка \_ не \_ хватает \_ памяти.</span><span class="sxs-lookup"><span data-stu-id="9ee7b-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |
| <dl> <span data-ttu-id="9ee7b-117"><dt>**ФИЛЕОП \_ NewPath**</dt></span><span class="sxs-lookup"><span data-stu-id="9ee7b-117"><dt>**FILEOP\_NEWPATH**</dt></span></span> </dl> | <span data-ttu-id="9ee7b-118">Повторите операцию копирования, используя путь функции обратного вызова, помещенной в буфер, на который указывает параметр *Param2* .</span><span class="sxs-lookup"><span data-stu-id="9ee7b-118">Retry the copy operation using the path the callback function placed in the buffer pointed to by the *Param2* parameter.</span></span> <span data-ttu-id="9ee7b-119">Подпрограммы обратного вызова должны обеспечить, чтобы путь не переполнить размер буфера в массиве TCHAR из \_ элементов максимального пути.</span><span class="sxs-lookup"><span data-stu-id="9ee7b-119">The callback routine should ensure that the path does not overflow the buffer size of a TCHAR array of MAX\_PATH elements.</span></span><br/>                |
| <dl> <span data-ttu-id="9ee7b-120"><dt>**ФИЛЕОП \_ Повтор**</dt></span><span class="sxs-lookup"><span data-stu-id="9ee7b-120"><dt>**FILEOP\_RETRY**</dt></span></span> </dl>   | <span data-ttu-id="9ee7b-121">Пользователь пытается повторить операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="9ee7b-121">The user is attempting the copy operation again.</span></span><br/>                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="9ee7b-122"><dt>**ФИЛЕОП \_ пропустить**</dt></span><span class="sxs-lookup"><span data-stu-id="9ee7b-122"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="9ee7b-123">Пользователь пропускает операцию копирования файла.</span><span class="sxs-lookup"><span data-stu-id="9ee7b-123">The user is skipping the file copy operation.</span></span><br/>                                                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="9ee7b-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9ee7b-124">Requirements</span></span>



| <span data-ttu-id="9ee7b-125">Требование</span><span class="sxs-lookup"><span data-stu-id="9ee7b-125">Requirement</span></span> | <span data-ttu-id="9ee7b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9ee7b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ee7b-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ee7b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9ee7b-128">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9ee7b-128">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9ee7b-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ee7b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9ee7b-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9ee7b-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ee7b-131">Header</span><span class="sxs-lookup"><span data-stu-id="9ee7b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ee7b-132"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ee7b-132"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ee7b-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ee7b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ee7b-134">Обзор</span><span class="sxs-lookup"><span data-stu-id="9ee7b-134">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="9ee7b-135">Уведомления</span><span class="sxs-lookup"><span data-stu-id="9ee7b-135">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="9ee7b-136">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="9ee7b-136">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="9ee7b-137">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="9ee7b-137">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="9ee7b-138">**сетупдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="9ee7b-138">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

