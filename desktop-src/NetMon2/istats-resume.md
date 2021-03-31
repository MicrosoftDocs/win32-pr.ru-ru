---
description: Метод Resume перезапускает отложенную запись.
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: 'Метод Истатс:: Resume (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: db84f51d2a2a2c2d15e3b4164fe1fac09e72bf20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911639"
---
# <a name="istatsresume-method"></a><span data-ttu-id="531f9-103">Метод Истатс:: Resume</span><span class="sxs-lookup"><span data-stu-id="531f9-103">IStats::Resume method</span></span>

<span data-ttu-id="531f9-104">Метод **Resume** перезапускает отложенную запись.</span><span class="sxs-lookup"><span data-stu-id="531f9-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="531f9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="531f9-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="531f9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="531f9-106">Parameters</span></span>

<span data-ttu-id="531f9-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="531f9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="531f9-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="531f9-108">Return value</span></span>

<span data-ttu-id="531f9-109">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="531f9-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="531f9-110">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="531f9-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="531f9-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="531f9-111">Return code</span></span>                                                                                                | <span data-ttu-id="531f9-112">Описание</span><span class="sxs-lookup"><span data-stu-id="531f9-112">Description</span></span>                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="531f9-113"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="531f9-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="531f9-114">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="531f9-114">The NPP is not connected to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="531f9-115"><dt>**\_запись нмерр \_ не \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="531f9-115"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="531f9-116">Запись не приостановлена.</span><span class="sxs-lookup"><span data-stu-id="531f9-116">The capture is not paused.</span></span> <span data-ttu-id="531f9-117">Вызовите метод [истатс::P Аусе](istats-pause.md) , чтобы временно остановить запись.</span><span class="sxs-lookup"><span data-stu-id="531f9-117">Call the [IStats::Pause](istats-pause.md) method to temporarily stop the capture.</span></span><br/>                     |
| <dl> <span data-ttu-id="531f9-118"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="531f9-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="531f9-119">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="531f9-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="531f9-120">Вызовите метод [истатс:: Connect](istats-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="531f9-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="531f9-121"><dt>**НМЕРР \_ не \_ \_ только статистика**</dt></span><span class="sxs-lookup"><span data-stu-id="531f9-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl>     | <span data-ttu-id="531f9-122">НПП подключается к сети, но не с методом [истатс:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="531f9-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="531f9-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="531f9-123">Remarks</span></span>

<span data-ttu-id="531f9-124">Пока запись находится в приостановленном состоянии, новые данные не фиксируются до тех пор, пока не будет вызван метод Истатс:: Resume для перезапуска записи.</span><span class="sxs-lookup"><span data-stu-id="531f9-124">While the capture is in a paused state, new data is not captured until the IStats::Resume method is called to restart the capture.</span></span>

<span data-ttu-id="531f9-125">При использовании методов **Pause** и **Resume** для управления захватом сетевой монитор продолжает добавлять [*статистику диалога*](c.md) к существующей статистике для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="531f9-125">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="531f9-126">Чтобы прерывать запись, вызовите [истатс:: останавливаться](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="531f9-126">To stop the capture, call [IStats::Stop](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="531f9-127">Требования</span><span class="sxs-lookup"><span data-stu-id="531f9-127">Requirements</span></span>



| <span data-ttu-id="531f9-128">Требование</span><span class="sxs-lookup"><span data-stu-id="531f9-128">Requirement</span></span> | <span data-ttu-id="531f9-129">Значение</span><span class="sxs-lookup"><span data-stu-id="531f9-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="531f9-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="531f9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="531f9-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="531f9-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="531f9-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="531f9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="531f9-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="531f9-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="531f9-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="531f9-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="531f9-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="531f9-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="531f9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="531f9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="531f9-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="531f9-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="531f9-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="531f9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="531f9-139">истатс</span><span class="sxs-lookup"><span data-stu-id="531f9-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="531f9-140">Истатс:: Connect</span><span class="sxs-lookup"><span data-stu-id="531f9-140">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="531f9-141">Истатс::P Аусе</span><span class="sxs-lookup"><span data-stu-id="531f9-141">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="531f9-142">Истатс:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="531f9-142">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




