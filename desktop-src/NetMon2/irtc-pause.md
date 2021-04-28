---
description: ИРТК::P метод Аусе — метод Pause приостанавливает текущую запись.
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: 'ИРТК: метод:P Аусе (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d42af1912365a4237889e4e46d0fb3343377c772
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110682"
---
# <a name="irtcpause-method"></a><span data-ttu-id="101fd-103">ИРТК: метод:P Аусе</span><span class="sxs-lookup"><span data-stu-id="101fd-103">IRTC::Pause method</span></span>

<span data-ttu-id="101fd-104">Метод **Pause** приостанавливает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="101fd-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="101fd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="101fd-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="101fd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="101fd-106">Parameters</span></span>

<span data-ttu-id="101fd-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="101fd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="101fd-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="101fd-108">Return value</span></span>

<span data-ttu-id="101fd-109">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="101fd-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="101fd-110">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="101fd-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="101fd-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="101fd-111">Return code</span></span>                                                                                           | <span data-ttu-id="101fd-112">Описание</span><span class="sxs-lookup"><span data-stu-id="101fd-112">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="101fd-113"><dt>**\_запись нмерр \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="101fd-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="101fd-114">Запись уже приостановлена.</span><span class="sxs-lookup"><span data-stu-id="101fd-114">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="101fd-115"><dt>**НМЕРР \_ не \_ захватывается**</dt></span><span class="sxs-lookup"><span data-stu-id="101fd-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="101fd-116">НПП не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="101fd-116">The NPP is not capturing data.</span></span> <span data-ttu-id="101fd-117">Вызовите [ИРТК:: Start](irtc-start.md) , чтобы начать запись.</span><span class="sxs-lookup"><span data-stu-id="101fd-117">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="101fd-118"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="101fd-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="101fd-119">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="101fd-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="101fd-120">Вызовите [ИРТК:: Connect](irtc-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="101fd-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="101fd-121"><dt>**НМЕРР \_ не в \_ реальном времени**</dt></span><span class="sxs-lookup"><span data-stu-id="101fd-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>   | <span data-ttu-id="101fd-122">НПП подключается к сети, но не с методом [ИРТК:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="101fd-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="101fd-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="101fd-123">Remarks</span></span>

<span data-ttu-id="101fd-124">Пока запись находится в приостановленном состоянии, новые кадры не фиксируются до тех пор, пока не будет вызван метод [ИРТК:: Resume](irtc-resume.md) для перезапуска записи.</span><span class="sxs-lookup"><span data-stu-id="101fd-124">While the capture is in a paused state, new frames are not captured until the [IRTC::Resume](irtc-resume.md) method is called to restart the capture.</span></span>

<span data-ttu-id="101fd-125">При использовании методов **ИРТК::P Аусе** и **ИРТК:: Resume** для управления захватом сетевой монитор продолжает добавлять [*статистику беседы*](c.md) при выполнении записи.</span><span class="sxs-lookup"><span data-stu-id="101fd-125">When you use the **IRTC::Pause** and **IRTC::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="101fd-126">Чтобы перезапустить захват [ИРТК:: Resume](irtc-resume.md).</span><span class="sxs-lookup"><span data-stu-id="101fd-126">To restart the capture call [IRTC::Resume](irtc-resume.md).</span></span> <span data-ttu-id="101fd-127">Чтобы прерывать запись, вызовите [ИРТК:: останавливаться](irtc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="101fd-127">To stop the capture, call [IRTC::Stop](irtc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="101fd-128">Требования</span><span class="sxs-lookup"><span data-stu-id="101fd-128">Requirements</span></span>



| <span data-ttu-id="101fd-129">Требование</span><span class="sxs-lookup"><span data-stu-id="101fd-129">Requirement</span></span> | <span data-ttu-id="101fd-130">Значение</span><span class="sxs-lookup"><span data-stu-id="101fd-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="101fd-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="101fd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="101fd-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="101fd-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="101fd-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="101fd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="101fd-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="101fd-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="101fd-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="101fd-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="101fd-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="101fd-136"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="101fd-137">DLL</span><span class="sxs-lookup"><span data-stu-id="101fd-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="101fd-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="101fd-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="101fd-139">См. также</span><span class="sxs-lookup"><span data-stu-id="101fd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="101fd-140">иртк</span><span class="sxs-lookup"><span data-stu-id="101fd-140">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="101fd-141">ИРТК:: Connect</span><span class="sxs-lookup"><span data-stu-id="101fd-141">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="101fd-142">ИРТК:: Resume</span><span class="sxs-lookup"><span data-stu-id="101fd-142">IRTC::Resume</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="101fd-143">ИРТК:: Start</span><span class="sxs-lookup"><span data-stu-id="101fd-143">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="101fd-144">ИРТК:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="101fd-144">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




