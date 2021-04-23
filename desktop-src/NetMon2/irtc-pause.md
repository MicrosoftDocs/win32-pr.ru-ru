---
description: Метод Pause приостанавливает текущую запись.
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
ms.openlocfilehash: d2593c380d0fea52d030586da2f473a3f3fa9446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263950"
---
# <a name="irtcpause-method"></a><span data-ttu-id="0e479-103">ИРТК: метод:P Аусе</span><span class="sxs-lookup"><span data-stu-id="0e479-103">IRTC::Pause method</span></span>

<span data-ttu-id="0e479-104">Метод **Pause** приостанавливает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="0e479-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e479-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e479-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="0e479-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e479-106">Parameters</span></span>

<span data-ttu-id="0e479-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0e479-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e479-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e479-108">Return value</span></span>

<span data-ttu-id="0e479-109">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0e479-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0e479-110">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="0e479-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="0e479-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0e479-111">Return code</span></span>                                                                                           | <span data-ttu-id="0e479-112">Описание</span><span class="sxs-lookup"><span data-stu-id="0e479-112">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e479-113"><dt>**\_запись нмерр \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="0e479-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="0e479-114">Запись уже приостановлена.</span><span class="sxs-lookup"><span data-stu-id="0e479-114">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="0e479-115"><dt>**НМЕРР \_ не \_ захватывается**</dt></span><span class="sxs-lookup"><span data-stu-id="0e479-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="0e479-116">НПП не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="0e479-116">The NPP is not capturing data.</span></span> <span data-ttu-id="0e479-117">Вызовите [ИРТК:: Start](irtc-start.md) , чтобы начать запись.</span><span class="sxs-lookup"><span data-stu-id="0e479-117">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="0e479-118"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="0e479-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="0e479-119">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="0e479-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="0e479-120">Вызовите [ИРТК:: Connect](irtc-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="0e479-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="0e479-121"><dt>**НМЕРР \_ не в \_ реальном времени**</dt></span><span class="sxs-lookup"><span data-stu-id="0e479-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>   | <span data-ttu-id="0e479-122">НПП подключается к сети, но не с методом [ИРТК:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="0e479-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="0e479-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e479-123">Remarks</span></span>

<span data-ttu-id="0e479-124">Пока запись находится в приостановленном состоянии, новые кадры не фиксируются до тех пор, пока не будет вызван метод [ИРТК:: Resume](irtc-resume.md) для перезапуска записи.</span><span class="sxs-lookup"><span data-stu-id="0e479-124">While the capture is in a paused state, new frames are not captured until the [IRTC::Resume](irtc-resume.md) method is called to restart the capture.</span></span>

<span data-ttu-id="0e479-125">При использовании методов **ИРТК::P Аусе** и **ИРТК:: Resume** для управления захватом сетевой монитор продолжает добавлять [*статистику беседы*](c.md) при выполнении записи.</span><span class="sxs-lookup"><span data-stu-id="0e479-125">When you use the **IRTC::Pause** and **IRTC::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="0e479-126">Чтобы перезапустить захват [ИРТК:: Resume](irtc-resume.md).</span><span class="sxs-lookup"><span data-stu-id="0e479-126">To restart the capture call [IRTC::Resume](irtc-resume.md).</span></span> <span data-ttu-id="0e479-127">Чтобы прерывать запись, вызовите [ИРТК:: останавливаться](irtc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="0e479-127">To stop the capture, call [IRTC::Stop](irtc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e479-128">Требования</span><span class="sxs-lookup"><span data-stu-id="0e479-128">Requirements</span></span>



| <span data-ttu-id="0e479-129">Требование</span><span class="sxs-lookup"><span data-stu-id="0e479-129">Requirement</span></span> | <span data-ttu-id="0e479-130">Значение</span><span class="sxs-lookup"><span data-stu-id="0e479-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e479-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e479-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0e479-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0e479-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0e479-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e479-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0e479-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0e479-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0e479-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0e479-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e479-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e479-136"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0e479-137">DLL</span><span class="sxs-lookup"><span data-stu-id="0e479-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e479-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e479-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e479-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e479-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e479-140">иртк</span><span class="sxs-lookup"><span data-stu-id="0e479-140">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="0e479-141">ИРТК:: Connect</span><span class="sxs-lookup"><span data-stu-id="0e479-141">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="0e479-142">ИРТК:: Resume</span><span class="sxs-lookup"><span data-stu-id="0e479-142">IRTC::Resume</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="0e479-143">ИРТК:: Start</span><span class="sxs-lookup"><span data-stu-id="0e479-143">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="0e479-144">ИРТК:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="0e479-144">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




