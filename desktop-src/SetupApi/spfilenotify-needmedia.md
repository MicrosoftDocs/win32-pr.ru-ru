---
description: Уведомление СПФИЛЕНОТИФИ \_ нидмедиа отправляется в подпрограммы обратного вызова, когда требуется новый носитель или новый CAB-файл.
ms.assetid: 6a7947de-1bb3-46e0-9334-405684e58e98
title: Сообщение SPFILENOTIFY_NEEDMEDIA (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b856a95f3c2e200d1d81cfa00c05ef592c1759
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105664813"
---
# <a name="spfilenotify_needmedia-message"></a><span data-ttu-id="06f6a-103">\_Сообщение спфиленотифи нидмедиа</span><span class="sxs-lookup"><span data-stu-id="06f6a-103">SPFILENOTIFY\_NEEDMEDIA message</span></span>

<span data-ttu-id="06f6a-104">Уведомление **спфиленотифи \_ нидмедиа** отправляется в подпрограммы обратного вызова, когда требуется новый носитель или новый CAB-файл.</span><span class="sxs-lookup"><span data-stu-id="06f6a-104">The **SPFILENOTIFY\_NEEDMEDIA** notification is sent to the callback routine when new media or a new cabinet file is required.</span></span>


```C++
SPFILENOTIFY_NEEDMEDIA
  Param1 = (UINT) SourceMediaInfo;
  Param2 = (UINT) NewPathInfo;
            
```



## <a name="parameters"></a><span data-ttu-id="06f6a-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="06f6a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06f6a-106">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="06f6a-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="06f6a-107">Указатель на [**исходную структуру \_ носителя**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) .</span><span class="sxs-lookup"><span data-stu-id="06f6a-107">Pointer to a [**SOURCE\_MEDIA**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="06f6a-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="06f6a-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="06f6a-109">Указатель на массив символов для хранения новых сведений о пути, предоставленных пользователем.</span><span class="sxs-lookup"><span data-stu-id="06f6a-109">Pointer to a character array to store new path information supplied by the user.</span></span> <span data-ttu-id="06f6a-110">Размер буфера — это массив **TCHAR** из элементов максимального \_ пути.</span><span class="sxs-lookup"><span data-stu-id="06f6a-110">The buffer size is a **TCHAR** array of MAX\_PATH elements.</span></span> <span data-ttu-id="06f6a-111">Сведения о пути, возвращаемые приложением установки, не должны превышать этот размер.</span><span class="sxs-lookup"><span data-stu-id="06f6a-111">The path information returned by your setup application should not exceed this size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06f6a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06f6a-112">Return value</span></span>

<span data-ttu-id="06f6a-113">Подпрограммы обратного вызова должны возвращать один из следующих элементов.</span><span class="sxs-lookup"><span data-stu-id="06f6a-113">The callback routine should return one of the following.</span></span>



| <span data-ttu-id="06f6a-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="06f6a-114">Return code</span></span>                                                                                    | <span data-ttu-id="06f6a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="06f6a-115">Description</span></span>                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="06f6a-116"><dt>**ФИЛЕОП \_ NewPath**</dt></span><span class="sxs-lookup"><span data-stu-id="06f6a-116"><dt>**FILEOP\_NEWPATH**</dt></span></span> </dl> | <span data-ttu-id="06f6a-117">Носитель существует, а запрошенный файл доступен по пути, указанному в буфере, на который указывает *Param2*.</span><span class="sxs-lookup"><span data-stu-id="06f6a-117">The media is present and the requested file is available at the path specified in the buffer pointed to by *Param2*.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="06f6a-118"><dt>**ФИЛЕОП \_ пропустить**</dt></span><span class="sxs-lookup"><span data-stu-id="06f6a-118"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="06f6a-119">Пропустить запрошенный файл</span><span class="sxs-lookup"><span data-stu-id="06f6a-119">Skip the requested file</span></span><br/>                                                                                                                                                                                      |
| <dl> <span data-ttu-id="06f6a-120"><dt>**прервать ФИЛЕОП \_**</dt></span><span class="sxs-lookup"><span data-stu-id="06f6a-120"><dt>**FILEOP\_ABORT**</dt></span></span> </dl>   | <span data-ttu-id="06f6a-121">Прервать обработку очереди.</span><span class="sxs-lookup"><span data-stu-id="06f6a-121">Abort queue processing.</span></span> <span data-ttu-id="06f6a-122">Функция [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="06f6a-122">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function returns **FALSE**.</span></span> <span data-ttu-id="06f6a-123">GetLastError Возвращает расширенные сведения об ошибке, такие как ошибка \_ отмены, если пользователь отменил действие.</span><span class="sxs-lookup"><span data-stu-id="06f6a-123">GetLastError returns extended error information, such as ERROR\_CANCELLED if the user canceled.</span></span><br/> |
| <dl> <span data-ttu-id="06f6a-124"><dt>**ФИЛЕОП — ДОИТ**</dt></span><span class="sxs-lookup"><span data-stu-id="06f6a-124"><dt>**FILEOP-DOIT**</dt></span></span> </dl>     | <span data-ttu-id="06f6a-125">Носитель доступен.</span><span class="sxs-lookup"><span data-stu-id="06f6a-125">The media is available.</span></span><br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="06f6a-126">Требования</span><span class="sxs-lookup"><span data-stu-id="06f6a-126">Requirements</span></span>



| <span data-ttu-id="06f6a-127">Требование</span><span class="sxs-lookup"><span data-stu-id="06f6a-127">Requirement</span></span> | <span data-ttu-id="06f6a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="06f6a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06f6a-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06f6a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="06f6a-130">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="06f6a-130">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="06f6a-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06f6a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="06f6a-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="06f6a-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06f6a-133">Header</span><span class="sxs-lookup"><span data-stu-id="06f6a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="06f6a-134"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="06f6a-134"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06f6a-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06f6a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06f6a-136">Обзор</span><span class="sxs-lookup"><span data-stu-id="06f6a-136">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="06f6a-137">Уведомления</span><span class="sxs-lookup"><span data-stu-id="06f6a-137">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="06f6a-138">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="06f6a-138">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="06f6a-139">**сетупдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="06f6a-139">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="06f6a-140">**ИСХОДНЫЙ \_ носитель**</span><span class="sxs-lookup"><span data-stu-id="06f6a-140">**SOURCE\_MEDIA**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a)
</dt> </dl>

 

 




