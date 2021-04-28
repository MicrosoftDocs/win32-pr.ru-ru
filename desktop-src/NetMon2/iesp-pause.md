---
description: ИЕСП::P метод Аусе — метод Pause приостанавливает текущую запись.
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
ms.openlocfilehash: 486c7aedc7092e0dd0f9f68cc1ea2ccad08d9438
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084242"
---
# <a name="iesppause-method"></a><span data-ttu-id="b64e8-103">ИЕСП: метод:P Аусе</span><span class="sxs-lookup"><span data-stu-id="b64e8-103">IESP::Pause method</span></span>

<span data-ttu-id="b64e8-104">Метод **Pause** приостанавливает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="b64e8-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="b64e8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b64e8-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="b64e8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b64e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b64e8-107">*лпстатс*</span><span class="sxs-lookup"><span data-stu-id="b64e8-107">*lpStats*</span></span> 
</dt> <dd>

<span data-ttu-id="b64e8-108">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="b64e8-108">Obsolete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b64e8-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b64e8-109">Return value</span></span>

<span data-ttu-id="b64e8-110">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b64e8-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b64e8-111">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="b64e8-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="b64e8-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b64e8-112">Return code</span></span>                                                                                           | <span data-ttu-id="b64e8-113">Описание</span><span class="sxs-lookup"><span data-stu-id="b64e8-113">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b64e8-114"><dt>**\_запись нмерр \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="b64e8-114"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="b64e8-115">Запись уже приостановлена.</span><span class="sxs-lookup"><span data-stu-id="b64e8-115">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="b64e8-116"><dt>**НМЕРР \_ не \_ захватывается**</dt></span><span class="sxs-lookup"><span data-stu-id="b64e8-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="b64e8-117">НПП не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="b64e8-117">The NPP is not capturing data.</span></span> <span data-ttu-id="b64e8-118">Вызовите [ИЕСП:: Start](iesp-start.md) , чтобы начать запись.</span><span class="sxs-lookup"><span data-stu-id="b64e8-118">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="b64e8-119"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="b64e8-119"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="b64e8-120">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="b64e8-120">The NPP is not connected to the network.</span></span> <span data-ttu-id="b64e8-121">Вызовите [ИЕСП:: Connect](iesp-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="b64e8-121">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="b64e8-122"><dt>**НМЕРР \_ не \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="b64e8-122"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="b64e8-123">НПП подключается к сети, но не с методом [ИЕСП:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="b64e8-123">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="b64e8-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="b64e8-124">Remarks</span></span>

<span data-ttu-id="b64e8-125">Пока запись находится в приостановленном состоянии, новые данные не добавляются в текущий [*файл записи*](c.md) до тех пор, пока не будет вызван метод [ИЕСП:: Resume](iesp-resume.md) для перезапуска записи.</span><span class="sxs-lookup"><span data-stu-id="b64e8-125">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until you call the [IESP::Resume](iesp-resume.md) method to restart the capture.</span></span> <span data-ttu-id="b64e8-126">Если **приостановка** и **возобновление** используются для остановки и перезапуска записи, вся записанная информация помещается в один и тот же файл записи.</span><span class="sxs-lookup"><span data-stu-id="b64e8-126">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="b64e8-127">При использовании методов **ИЕСП::P Аусе** и **ИЕСП:: Resume** для управления захватом сетевой монитор продолжает добавлять [*статистику беседы*](c.md) при выполнении записи.</span><span class="sxs-lookup"><span data-stu-id="b64e8-127">When you use the **IESP::Pause** and **IESP::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="b64e8-128">Чтобы перезапустить запись, вызовите метод [ИЕСП:: Resume](iesp-resume.md).</span><span class="sxs-lookup"><span data-stu-id="b64e8-128">To restart the capture, call [IESP::Resume](iesp-resume.md).</span></span> <span data-ttu-id="b64e8-129">Чтобы прерывать запись, вызовите [ИЕСП:: останавливаться](iesp-stop.md).</span><span class="sxs-lookup"><span data-stu-id="b64e8-129">To stop the capture, call [IESP::Stop](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b64e8-130">Требования</span><span class="sxs-lookup"><span data-stu-id="b64e8-130">Requirements</span></span>



| <span data-ttu-id="b64e8-131">Требование</span><span class="sxs-lookup"><span data-stu-id="b64e8-131">Requirement</span></span> | <span data-ttu-id="b64e8-132">Значение</span><span class="sxs-lookup"><span data-stu-id="b64e8-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b64e8-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b64e8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b64e8-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b64e8-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="b64e8-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b64e8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b64e8-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b64e8-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="b64e8-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b64e8-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b64e8-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b64e8-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="b64e8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b64e8-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b64e8-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b64e8-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b64e8-141">См. также</span><span class="sxs-lookup"><span data-stu-id="b64e8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b64e8-142">иесп</span><span class="sxs-lookup"><span data-stu-id="b64e8-142">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="b64e8-143">ИЕСП:: Connect</span><span class="sxs-lookup"><span data-stu-id="b64e8-143">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="b64e8-144">ИЕСП:: Resume</span><span class="sxs-lookup"><span data-stu-id="b64e8-144">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="b64e8-145">ИЕСП:: Start</span><span class="sxs-lookup"><span data-stu-id="b64e8-145">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="b64e8-146">ИЕСП:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="b64e8-146">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




