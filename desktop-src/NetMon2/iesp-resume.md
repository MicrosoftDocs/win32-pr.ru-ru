---
description: Метод Resume перезапускает отложенную запись.
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: 'Метод ИЕСП:: Resume (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 01bbb748fc91bcc5a78b281ec9ebdd2a6d479888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682463"
---
# <a name="iespresume-method"></a><span data-ttu-id="3b58b-103">Метод ИЕСП:: Resume</span><span class="sxs-lookup"><span data-stu-id="3b58b-103">IESP::Resume method</span></span>

<span data-ttu-id="3b58b-104">Метод **Resume** перезапускает отложенную запись.</span><span class="sxs-lookup"><span data-stu-id="3b58b-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b58b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b58b-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="3b58b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b58b-106">Parameters</span></span>

<span data-ttu-id="3b58b-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3b58b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3b58b-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b58b-108">Return value</span></span>

<span data-ttu-id="3b58b-109">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3b58b-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3b58b-110">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="3b58b-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="3b58b-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3b58b-111">Return code</span></span>                                                                                                | <span data-ttu-id="3b58b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="3b58b-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3b58b-113"><dt>**\_запись нмерр \_ не \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="3b58b-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="3b58b-114">Запись не приостановлена.</span><span class="sxs-lookup"><span data-stu-id="3b58b-114">The capture is not paused.</span></span> <span data-ttu-id="3b58b-115">Вызовите [**ИЕСП::P Аусе**](iesp-pause.md) , чтобы приостановить запись.</span><span class="sxs-lookup"><span data-stu-id="3b58b-115">Call [**IESP::Pause**](iesp-pause.md) to pause the capture.</span></span><br/>                        |
| <dl> <span data-ttu-id="3b58b-116"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="3b58b-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="3b58b-117">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="3b58b-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="3b58b-118">Вызовите [**ИЕСП:: Connect**](iesp-connect.md) , чтобы подключиться к сети.</span><span class="sxs-lookup"><span data-stu-id="3b58b-118">Call [**IESP::Connect**](iesp-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="3b58b-119"><dt>**НМЕРР \_ не \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="3b58b-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>             | <span data-ttu-id="3b58b-120">НПП подключается к сети, но не с методом [**ИЕСП:: Connect**](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="3b58b-120">The NPP is connected to the network, but not with the [**IESP::Connect**](iesp-connect.md) method.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="3b58b-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b58b-121">Remarks</span></span>

<span data-ttu-id="3b58b-122">Пока запись находится в приостановленном состоянии, новые данные не добавляются в текущий [*файл записи*](c.md) до тех пор, пока не будет вызван метод **ИЕСП:: Resume** для перезапуска записи.</span><span class="sxs-lookup"><span data-stu-id="3b58b-122">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until **IESP::Resume** is called to restart the capture.</span></span> <span data-ttu-id="3b58b-123">Если **приостановка** и **возобновление** используются для остановки и перезапуска записи, вся записанная информация помещается в один и тот же файл записи.</span><span class="sxs-lookup"><span data-stu-id="3b58b-123">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="3b58b-124">При использовании **приостановки** и **возобновления** для управления записью сетевой монитор продолжает добавлять [*статистику диалога*](c.md) к существующей статистике для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3b58b-124">When using **Pause** and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="3b58b-125">Чтобы прерывать запись, вызовите [**ИЕСП:: останавливаться**](iesp-stop.md).</span><span class="sxs-lookup"><span data-stu-id="3b58b-125">To stop the capture, call [**IESP::Stop**](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b58b-126">Требования</span><span class="sxs-lookup"><span data-stu-id="3b58b-126">Requirements</span></span>



| <span data-ttu-id="3b58b-127">Требование</span><span class="sxs-lookup"><span data-stu-id="3b58b-127">Requirement</span></span> | <span data-ttu-id="3b58b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3b58b-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b58b-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b58b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3b58b-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3b58b-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="3b58b-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b58b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3b58b-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3b58b-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="3b58b-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3b58b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b58b-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b58b-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="3b58b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3b58b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b58b-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b58b-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b58b-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b58b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b58b-138">иесп</span><span class="sxs-lookup"><span data-stu-id="3b58b-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="3b58b-139">**ИЕСП:: Connect**</span><span class="sxs-lookup"><span data-stu-id="3b58b-139">**IESP::Connect**</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="3b58b-140">**ИЕСП::P Аусе**</span><span class="sxs-lookup"><span data-stu-id="3b58b-140">**IESP::Pause**</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="3b58b-141">**ИЕСП:: останавливаться**</span><span class="sxs-lookup"><span data-stu-id="3b58b-141">**IESP::Stop**</span></span>](iesp-stop.md)
</dt> </dl>

 

 




