---
description: Метод Start запускает захват.
ms.assetid: d4086e30-e5ed-4f29-90f0-d65125d9af6d
title: 'Метод Истатс:: Start (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d58821ecc06e0a25d6a260bb2ba9393162dcdca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897802"
---
# <a name="istatsstart-method"></a><span data-ttu-id="1f719-103">Метод Истатс:: Start</span><span class="sxs-lookup"><span data-stu-id="1f719-103">IStats::Start method</span></span>

<span data-ttu-id="1f719-104">Метод **Start** запускает захват.</span><span class="sxs-lookup"><span data-stu-id="1f719-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f719-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f719-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a><span data-ttu-id="1f719-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f719-106">Parameters</span></span>

<span data-ttu-id="1f719-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1f719-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1f719-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1f719-108">Return value</span></span>

<span data-ttu-id="1f719-109">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1f719-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1f719-110">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="1f719-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="1f719-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1f719-111">Return code</span></span>                                                                                            | <span data-ttu-id="1f719-112">Описание</span><span class="sxs-lookup"><span data-stu-id="1f719-112">Description</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1f719-113"><dt>**\_запись нмерр \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="1f719-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl>  | <span data-ttu-id="1f719-114">Запись приостановлена и должна быть остановлена, прежде чем ее можно будет перезапустить.</span><span class="sxs-lookup"><span data-stu-id="1f719-114">The capture has paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="1f719-115">Вызовите метод [истатс:: останавливаться](istats-stop.md) , чтобы прерывать запись.</span><span class="sxs-lookup"><span data-stu-id="1f719-115">Call the [IStats::Stop](istats-stop.md) method to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="1f719-116"><dt>**НМЕРР \_ запись**</dt></span><span class="sxs-lookup"><span data-stu-id="1f719-116"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>        | <span data-ttu-id="1f719-117">Запись уже запущена.</span><span class="sxs-lookup"><span data-stu-id="1f719-117">The capture has already started.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="1f719-118"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="1f719-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="1f719-119">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="1f719-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="1f719-120">Вызовите метод [истатс:: Connect](istats-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="1f719-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/>           |
| <dl> <span data-ttu-id="1f719-121"><dt>**НМЕРР \_ не \_ \_ только статистика**</dt></span><span class="sxs-lookup"><span data-stu-id="1f719-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="1f719-122">НПП подключается к сети, но не с методом [истатс:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="1f719-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="1f719-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f719-123">Remarks</span></span>

<span data-ttu-id="1f719-124">При перезапуске записи с помощью методов Истатс:: Start и [истатс:: останавливают](istats-stop.md) необходимо вызвать метод [Истатс:: Configure](istats-configure.md) для повторной настройки подключения при каждом вызове истатс:: Start для перезапуска записи данных.</span><span class="sxs-lookup"><span data-stu-id="1f719-124">When restarting the capture by using the IStats::Start and [IStats::Stop](istats-stop.md) methods, you must call the [IStats::Configure](istats-configure.md) method to reconfigure the connection each time you call IStats::Start to restart the data capture.</span></span>

> [!Note]  
> <span data-ttu-id="1f719-125">Также можно запускать и прекращать захват с помощью методов [истатс::P Аусе](istats-pause.md) и [Истатс:: Resume](istats-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="1f719-125">You can also start and stop the capture by using the [IStats::Pause](istats-pause.md) and [IStats::Resume](istats-resume.md) methods.</span></span> <span data-ttu-id="1f719-126">При использовании этих методов захваченные данные хранятся в одном файле записи.</span><span class="sxs-lookup"><span data-stu-id="1f719-126">When you use these methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1f719-127">Требования</span><span class="sxs-lookup"><span data-stu-id="1f719-127">Requirements</span></span>



| <span data-ttu-id="1f719-128">Требование</span><span class="sxs-lookup"><span data-stu-id="1f719-128">Requirement</span></span> | <span data-ttu-id="1f719-129">Значение</span><span class="sxs-lookup"><span data-stu-id="1f719-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f719-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f719-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1f719-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1f719-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="1f719-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f719-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1f719-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1f719-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="1f719-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1f719-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f719-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f719-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="1f719-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1f719-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f719-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f719-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f719-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f719-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f719-139">истатс</span><span class="sxs-lookup"><span data-stu-id="1f719-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="1f719-140">Истатс:: Configure</span><span class="sxs-lookup"><span data-stu-id="1f719-140">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="1f719-141">Истатс:: Connect</span><span class="sxs-lookup"><span data-stu-id="1f719-141">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="1f719-142">Истатс::P Аусе</span><span class="sxs-lookup"><span data-stu-id="1f719-142">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="1f719-143">Истатс:: Resume</span><span class="sxs-lookup"><span data-stu-id="1f719-143">IStats::Resume</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="1f719-144">Истатс:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="1f719-144">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




