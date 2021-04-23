---
description: Метод Pause приостанавливает текущую запись.
ms.assetid: 9d5e11d1-8c45-4cf5-9fea-10c9e7a6fe86
title: 'Иделайдк: метод:P Аусе (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d44ae7792388d9ca637232b45e63d618a37acb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896762"
---
# <a name="idelaydcpause-method"></a><span data-ttu-id="c55bb-103">Иделайдк: метод:P Аусе</span><span class="sxs-lookup"><span data-stu-id="c55bb-103">IDelaydC::Pause method</span></span>

<span data-ttu-id="c55bb-104">Метод **Pause** приостанавливает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="c55bb-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c55bb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c55bb-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="c55bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c55bb-106">Parameters</span></span>

<span data-ttu-id="c55bb-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c55bb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c55bb-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c55bb-108">Return value</span></span>

<span data-ttu-id="c55bb-109">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c55bb-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c55bb-110">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="c55bb-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="c55bb-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c55bb-111">Return code</span></span>                                                                                           | <span data-ttu-id="c55bb-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c55bb-112">Description</span></span>                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c55bb-113"><dt>**\_запись нмерр \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="c55bb-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="c55bb-114">Запись уже находится в приостановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="c55bb-114">The capture is already in a paused state.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="c55bb-115"><dt>**НМЕРР \_ не \_ захватывается**</dt></span><span class="sxs-lookup"><span data-stu-id="c55bb-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="c55bb-116">НПП не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="c55bb-116">The NPP is not capturing data.</span></span> <span data-ttu-id="c55bb-117">Вызовите [иделайдк:: Start](idelaydc-start.md) , чтобы начать запись.</span><span class="sxs-lookup"><span data-stu-id="c55bb-117">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="c55bb-118"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="c55bb-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="c55bb-119">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="c55bb-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="c55bb-120">Вызовите [иделайдк:: Connect](idelaydc-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="c55bb-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="c55bb-121"><dt>**НМЕРР \_ не \_ отложена**</dt></span><span class="sxs-lookup"><span data-stu-id="c55bb-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="c55bb-122">НПП подключается к сети, но не с методом [иделайдк:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="c55bb-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="c55bb-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c55bb-123">Remarks</span></span>

<span data-ttu-id="c55bb-124">Пока запись находится в приостановленном состоянии, новые данные не добавляются в текущий [*файл записи*](c.md) до тех пор, пока не будет вызван метод **Иделайдк:: Resume** для перезапуска записи.</span><span class="sxs-lookup"><span data-stu-id="c55bb-124">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="c55bb-125">Если **приостановка** и **возобновление** используются для остановки и перезапуска записи, вся записанная информация помещается в один и тот же файл записи.</span><span class="sxs-lookup"><span data-stu-id="c55bb-125">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="c55bb-126">При использовании **иделайдк::P Аусе** и **Иделайдк:: Resume** для управления записью сетевой монитор продолжает добавлять [*статистику беседы*](c.md) при выполнении записи.</span><span class="sxs-lookup"><span data-stu-id="c55bb-126">When using **IDelaydC::Pause** and **IDelaydC::Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="c55bb-127">Чтобы перезапустить запись, вызовите метод [иделайдк:: Resume](idelaydc-resume.md).</span><span class="sxs-lookup"><span data-stu-id="c55bb-127">To restart the capture, call [IDelaydC::Resume](idelaydc-resume.md).</span></span>

<span data-ttu-id="c55bb-128">Чтобы прерывать запись, вызовите [иделайдк:: останавливаться](idelaydc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="c55bb-128">To stop the capture, call [IDelaydC::Stop](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c55bb-129">Требования</span><span class="sxs-lookup"><span data-stu-id="c55bb-129">Requirements</span></span>



| <span data-ttu-id="c55bb-130">Требование</span><span class="sxs-lookup"><span data-stu-id="c55bb-130">Requirement</span></span> | <span data-ttu-id="c55bb-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c55bb-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c55bb-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c55bb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c55bb-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c55bb-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c55bb-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c55bb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c55bb-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c55bb-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c55bb-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c55bb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c55bb-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c55bb-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c55bb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c55bb-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c55bb-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c55bb-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c55bb-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c55bb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c55bb-141">иделайдк</span><span class="sxs-lookup"><span data-stu-id="c55bb-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="c55bb-142">Иделайдк:: Connect</span><span class="sxs-lookup"><span data-stu-id="c55bb-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="c55bb-143">Иделайдк:: Resume</span><span class="sxs-lookup"><span data-stu-id="c55bb-143">IDelaydC::Resume</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="c55bb-144">Иделайдк:: Start</span><span class="sxs-lookup"><span data-stu-id="c55bb-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="c55bb-145">Иделайдк:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="c55bb-145">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




