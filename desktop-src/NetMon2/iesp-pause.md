---
description: Метод Pause приостанавливает текущую запись.
ms.assetid: efbc8947-b9fe-4dbd-8097-375b5f99845e
title: 'ИЕСП: метод:P Аусе (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0558c5dfe36f26e3aad9f31101364d2e8e5c4967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540183"
---
# <a name="iesppause-method"></a><span data-ttu-id="22fbc-103">ИЕСП: метод:P Аусе</span><span class="sxs-lookup"><span data-stu-id="22fbc-103">IESP::Pause method</span></span>

<span data-ttu-id="22fbc-104">Метод **Pause** приостанавливает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="22fbc-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="22fbc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22fbc-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="22fbc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="22fbc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22fbc-107">*лпстатс*</span><span class="sxs-lookup"><span data-stu-id="22fbc-107">*lpStats*</span></span> 
</dt> <dd>

<span data-ttu-id="22fbc-108">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="22fbc-108">Obsolete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22fbc-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22fbc-109">Return value</span></span>

<span data-ttu-id="22fbc-110">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="22fbc-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="22fbc-111">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="22fbc-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="22fbc-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="22fbc-112">Return code</span></span>                                                                                           | <span data-ttu-id="22fbc-113">Описание</span><span class="sxs-lookup"><span data-stu-id="22fbc-113">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="22fbc-114"><dt>**\_запись нмерр \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="22fbc-114"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="22fbc-115">Запись уже приостановлена.</span><span class="sxs-lookup"><span data-stu-id="22fbc-115">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="22fbc-116"><dt>**НМЕРР \_ не \_ захватывается**</dt></span><span class="sxs-lookup"><span data-stu-id="22fbc-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="22fbc-117">НПП не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="22fbc-117">The NPP is not capturing data.</span></span> <span data-ttu-id="22fbc-118">Вызовите [ИЕСП:: Start](iesp-start.md) , чтобы начать запись.</span><span class="sxs-lookup"><span data-stu-id="22fbc-118">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="22fbc-119"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="22fbc-119"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="22fbc-120">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="22fbc-120">The NPP is not connected to the network.</span></span> <span data-ttu-id="22fbc-121">Вызовите [ИЕСП:: Connect](iesp-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="22fbc-121">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="22fbc-122"><dt>**НМЕРР \_ не \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="22fbc-122"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="22fbc-123">НПП подключается к сети, но не с методом [ИЕСП:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="22fbc-123">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="22fbc-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="22fbc-124">Remarks</span></span>

<span data-ttu-id="22fbc-125">Пока запись находится в приостановленном состоянии, новые данные не добавляются в текущий [*файл записи*](c.md) до тех пор, пока не будет вызван метод [ИЕСП:: Resume](iesp-resume.md) для перезапуска записи.</span><span class="sxs-lookup"><span data-stu-id="22fbc-125">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until you call the [IESP::Resume](iesp-resume.md) method to restart the capture.</span></span> <span data-ttu-id="22fbc-126">Если **приостановка** и **возобновление** используются для остановки и перезапуска записи, вся записанная информация помещается в один и тот же файл записи.</span><span class="sxs-lookup"><span data-stu-id="22fbc-126">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="22fbc-127">При использовании методов **ИЕСП::P Аусе** и **ИЕСП:: Resume** для управления захватом сетевой монитор продолжает добавлять [*статистику беседы*](c.md) при выполнении записи.</span><span class="sxs-lookup"><span data-stu-id="22fbc-127">When you use the **IESP::Pause** and **IESP::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="22fbc-128">Чтобы перезапустить запись, вызовите метод [ИЕСП:: Resume](iesp-resume.md).</span><span class="sxs-lookup"><span data-stu-id="22fbc-128">To restart the capture, call [IESP::Resume](iesp-resume.md).</span></span> <span data-ttu-id="22fbc-129">Чтобы прерывать запись, вызовите [ИЕСП:: останавливаться](iesp-stop.md).</span><span class="sxs-lookup"><span data-stu-id="22fbc-129">To stop the capture, call [IESP::Stop](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22fbc-130">Требования</span><span class="sxs-lookup"><span data-stu-id="22fbc-130">Requirements</span></span>



| <span data-ttu-id="22fbc-131">Требование</span><span class="sxs-lookup"><span data-stu-id="22fbc-131">Requirement</span></span> | <span data-ttu-id="22fbc-132">Значение</span><span class="sxs-lookup"><span data-stu-id="22fbc-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22fbc-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22fbc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="22fbc-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="22fbc-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="22fbc-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22fbc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="22fbc-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="22fbc-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="22fbc-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="22fbc-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="22fbc-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="22fbc-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="22fbc-139">DLL</span><span class="sxs-lookup"><span data-stu-id="22fbc-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22fbc-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22fbc-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22fbc-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22fbc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22fbc-142">иесп</span><span class="sxs-lookup"><span data-stu-id="22fbc-142">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="22fbc-143">ИЕСП:: Connect</span><span class="sxs-lookup"><span data-stu-id="22fbc-143">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="22fbc-144">ИЕСП:: Resume</span><span class="sxs-lookup"><span data-stu-id="22fbc-144">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="22fbc-145">ИЕСП:: Start</span><span class="sxs-lookup"><span data-stu-id="22fbc-145">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="22fbc-146">ИЕСП:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="22fbc-146">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




