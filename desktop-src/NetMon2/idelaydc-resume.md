---
description: 'Метод Иделайдк:: Resume. метод Resume перезапускает отложенную запись.'
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: 'Метод Иделайдк:: Resume (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9c8c3b505e0e9fb306a444111cce22c8c580d015
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109192"
---
# <a name="idelaydcresume-method"></a><span data-ttu-id="2c067-103">Метод Иделайдк:: Resume</span><span class="sxs-lookup"><span data-stu-id="2c067-103">IDelaydC::Resume method</span></span>

<span data-ttu-id="2c067-104">Метод **Resume** перезапускает отложенную запись.</span><span class="sxs-lookup"><span data-stu-id="2c067-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c067-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c067-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="2c067-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c067-106">Parameters</span></span>

<span data-ttu-id="2c067-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2c067-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2c067-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c067-108">Return value</span></span>

<span data-ttu-id="2c067-109">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="2c067-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2c067-110">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="2c067-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="2c067-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2c067-111">Return code</span></span>                                                                                                | <span data-ttu-id="2c067-112">Описание</span><span class="sxs-lookup"><span data-stu-id="2c067-112">Description</span></span>                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2c067-113"><dt>**\_запись нмерр \_ не \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="2c067-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="2c067-114">Запись не приостановлена.</span><span class="sxs-lookup"><span data-stu-id="2c067-114">The capture is not paused.</span></span> <span data-ttu-id="2c067-115">Вызовите [**иделайдк::P Аусе**](idelaydc-pause.md) , чтобы приостановить запись.</span><span class="sxs-lookup"><span data-stu-id="2c067-115">Call [**IDelaydC::Pause**](idelaydc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="2c067-116"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="2c067-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="2c067-117">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="2c067-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="2c067-118">Вызовите [**иделайдк:: Connect**](idelaydc-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="2c067-118">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="2c067-119"><dt>**НМЕРР \_ не \_ отложена**</dt></span><span class="sxs-lookup"><span data-stu-id="2c067-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>         | <span data-ttu-id="2c067-120">НПП подключается к сети, но не с методом [**иделайдк:: Connect**](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="2c067-120">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="2c067-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="2c067-121">Remarks</span></span>

<span data-ttu-id="2c067-122">Пока запись приостановлена, новые данные не добавляются в текущий [*файл записи*](c.md) до тех пор, пока не будет вызван метод **Иделайдк:: Resume** для перезапуска записи.</span><span class="sxs-lookup"><span data-stu-id="2c067-122">While the capture is paused, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="2c067-123">Если [**приостановка**](idelaydc-pause.md) и **возобновление** используются для остановки и перезапуска записи, вся записанная информация помещается в один и тот же файл записи.</span><span class="sxs-lookup"><span data-stu-id="2c067-123">When [**Pause**](idelaydc-pause.md) and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="2c067-124">При использовании [**приостановки**](idelaydc-pause.md) и **возобновления** для управления записью сетевой монитор продолжает добавлять [*статистику диалога*](c.md) к существующей статистике для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="2c067-124">When using [**Pause**](idelaydc-pause.md) and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="2c067-125">Чтобы прерывать запись, вызовите [**иделайдк:: останавливаться**](idelaydc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="2c067-125">To stop the capture, call [**IDelaydC::Stop**](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c067-126">Требования</span><span class="sxs-lookup"><span data-stu-id="2c067-126">Requirements</span></span>



| <span data-ttu-id="2c067-127">Требование</span><span class="sxs-lookup"><span data-stu-id="2c067-127">Requirement</span></span> | <span data-ttu-id="2c067-128">Значение</span><span class="sxs-lookup"><span data-stu-id="2c067-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c067-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c067-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2c067-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2c067-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="2c067-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c067-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2c067-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2c067-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="2c067-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2c067-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c067-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c067-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="2c067-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2c067-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c067-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c067-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c067-137">См. также</span><span class="sxs-lookup"><span data-stu-id="2c067-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c067-138">иделайдк</span><span class="sxs-lookup"><span data-stu-id="2c067-138">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="2c067-139">**Иделайдк:: Connect**</span><span class="sxs-lookup"><span data-stu-id="2c067-139">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="2c067-140">**Иделайдк::P Аусе**</span><span class="sxs-lookup"><span data-stu-id="2c067-140">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="2c067-141">**Иделайдк:: останавливаться**</span><span class="sxs-lookup"><span data-stu-id="2c067-141">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




