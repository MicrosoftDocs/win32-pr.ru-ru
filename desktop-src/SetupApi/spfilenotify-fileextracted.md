---
description: Уведомление СПФИЛЕНОТИФИ \_ филикстрактед отправляется в подпрограммы обратного вызова с помощью сетупитератекабинет, чтобы указать, что файл был извлечен из CAB-файла или что произошел сбой извлечения, а обработка CAB-файлов была отменена.
ms.assetid: 70ffe06c-e72d-4bb8-a13c-e2946ff72fa6
title: Сообщение SPFILENOTIFY_FILEEXTRACTED (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efdd66c7f218e632ba817d00a6e6c9447052e350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664457"
---
# <a name="spfilenotify_fileextracted-message"></a><span data-ttu-id="f796a-103">\_Сообщение спфиленотифи филикстрактед</span><span class="sxs-lookup"><span data-stu-id="f796a-103">SPFILENOTIFY\_FILEEXTRACTED message</span></span>

<span data-ttu-id="f796a-104">Уведомление **спфиленотифи \_ филикстрактед** отправляется в подпрограммы обратного вызова с помощью [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) , чтобы указать, что файл был извлечен из CAB-файла или что произошел сбой извлечения, а обработка CAB-файлов была отменена.</span><span class="sxs-lookup"><span data-stu-id="f796a-104">The **SPFILENOTIFY\_FILEEXTRACTED** notification is sent to a callback routine by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) to indicate either that a file was extracted from the cabinet or that an extraction failed and cabinet processing has been canceled.</span></span>


```C++
SPFILENOTIFY_FILEEXTRACTED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="f796a-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="f796a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f796a-106">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="f796a-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="f796a-107">Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) , которая содержит сведения о пути для извлеченного файла.</span><span class="sxs-lookup"><span data-stu-id="f796a-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains path information for the extracted file.</span></span> <span data-ttu-id="f796a-108">Элемент **sourceFile** структуры **FilePath** содержит полный исходный путь к CAB-файлу.</span><span class="sxs-lookup"><span data-stu-id="f796a-108">The **SourceFile** member of the **FILEPATHS** structure contains the full source path of the cabinet.</span></span> <span data-ttu-id="f796a-109">Член **TargetFile** предоставляет полный целевой путь к файлу, который должен быть установлен в системе.</span><span class="sxs-lookup"><span data-stu-id="f796a-109">The **TargetFile** member supplies the full target path of the file to be installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="f796a-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="f796a-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="f796a-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f796a-111">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f796a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f796a-112">Return value</span></span>

<span data-ttu-id="f796a-113">Подпрограммы обратного вызова CAB-файла должны возвращать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f796a-113">The cabinet callback routine should return one of the following values.</span></span>



| <span data-ttu-id="f796a-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f796a-114">Return code</span></span>                                                                               | <span data-ttu-id="f796a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="f796a-115">Description</span></span>                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f796a-116"><dt>**БЕЗ \_ ошибок**</dt></span><span class="sxs-lookup"><span data-stu-id="f796a-116"><dt>**NO\_ERROR**</dt></span></span> </dl>  | <span data-ttu-id="f796a-117">Ошибок не обнаружено, продолжить обработку CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="f796a-117">No error was encountered, continue processing the cabinet.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="f796a-118"><dt>**Ошибка \_ xxx**</dt></span><span class="sxs-lookup"><span data-stu-id="f796a-118"><dt>**ERROR\_XXX**</dt></span></span> </dl> | <span data-ttu-id="f796a-119">Произошла ошибка указанного типа.</span><span class="sxs-lookup"><span data-stu-id="f796a-119">An error of the specified type occurred.</span></span> <span data-ttu-id="f796a-120">[**Сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) будет возвращать ноль.</span><span class="sxs-lookup"><span data-stu-id="f796a-120">[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) will return zero.</span></span> <span data-ttu-id="f796a-121">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) вернет указанный код ошибки.</span><span class="sxs-lookup"><span data-stu-id="f796a-121">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the specified error code.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="f796a-122">Нет подпрограммы обратного вызова CAB-файла по умолчанию, предоставляемой API установки.</span><span class="sxs-lookup"><span data-stu-id="f796a-122">There is no default cabinet callback routine supplied with the Setup API.</span></span> <span data-ttu-id="f796a-123">Приложение установки должно предоставить подпрограммы обратного вызова для работы с уведомлениями, отправленными функцией [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .</span><span class="sxs-lookup"><span data-stu-id="f796a-123">Your setup application should supply a callback routine to handle the notifications sent by the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f796a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f796a-124">Requirements</span></span>



| <span data-ttu-id="f796a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f796a-125">Requirement</span></span> | <span data-ttu-id="f796a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f796a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f796a-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f796a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f796a-128">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f796a-128">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f796a-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f796a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f796a-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f796a-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f796a-131">Header</span><span class="sxs-lookup"><span data-stu-id="f796a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f796a-132"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f796a-132"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f796a-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f796a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f796a-134">Обзор</span><span class="sxs-lookup"><span data-stu-id="f796a-134">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="f796a-135">Уведомления</span><span class="sxs-lookup"><span data-stu-id="f796a-135">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="f796a-136">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="f796a-136">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="f796a-137">**сетупитератекабинет**</span><span class="sxs-lookup"><span data-stu-id="f796a-137">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

