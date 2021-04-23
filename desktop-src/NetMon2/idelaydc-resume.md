---
description: Метод Resume перезапускает отложенную запись.
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
ms.openlocfilehash: ba0deef666c2e9829cb5a71d91e73da9c1b7d780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808693"
---
# <a name="idelaydcresume-method"></a><span data-ttu-id="83c94-103">Метод Иделайдк:: Resume</span><span class="sxs-lookup"><span data-stu-id="83c94-103">IDelaydC::Resume method</span></span>

<span data-ttu-id="83c94-104">Метод **Resume** перезапускает отложенную запись.</span><span class="sxs-lookup"><span data-stu-id="83c94-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="83c94-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83c94-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="83c94-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="83c94-106">Parameters</span></span>

<span data-ttu-id="83c94-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="83c94-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="83c94-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83c94-108">Return value</span></span>

<span data-ttu-id="83c94-109">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="83c94-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="83c94-110">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="83c94-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="83c94-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="83c94-111">Return code</span></span>                                                                                                | <span data-ttu-id="83c94-112">Описание</span><span class="sxs-lookup"><span data-stu-id="83c94-112">Description</span></span>                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="83c94-113"><dt>**\_запись нмерр \_ не \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="83c94-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="83c94-114">Запись не приостановлена.</span><span class="sxs-lookup"><span data-stu-id="83c94-114">The capture is not paused.</span></span> <span data-ttu-id="83c94-115">Вызовите [**иделайдк::P Аусе**](idelaydc-pause.md) , чтобы приостановить запись.</span><span class="sxs-lookup"><span data-stu-id="83c94-115">Call [**IDelaydC::Pause**](idelaydc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="83c94-116"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="83c94-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="83c94-117">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="83c94-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="83c94-118">Вызовите [**иделайдк:: Connect**](idelaydc-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="83c94-118">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="83c94-119"><dt>**НМЕРР \_ не \_ отложена**</dt></span><span class="sxs-lookup"><span data-stu-id="83c94-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>         | <span data-ttu-id="83c94-120">НПП подключается к сети, но не с методом [**иделайдк:: Connect**](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="83c94-120">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="83c94-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83c94-121">Remarks</span></span>

<span data-ttu-id="83c94-122">Пока запись приостановлена, новые данные не добавляются в текущий [*файл записи*](c.md) до тех пор, пока не будет вызван метод **Иделайдк:: Resume** для перезапуска записи.</span><span class="sxs-lookup"><span data-stu-id="83c94-122">While the capture is paused, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="83c94-123">Если [**приостановка**](idelaydc-pause.md) и **возобновление** используются для остановки и перезапуска записи, вся записанная информация помещается в один и тот же файл записи.</span><span class="sxs-lookup"><span data-stu-id="83c94-123">When [**Pause**](idelaydc-pause.md) and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="83c94-124">При использовании [**приостановки**](idelaydc-pause.md) и **возобновления** для управления записью сетевой монитор продолжает добавлять [*статистику диалога*](c.md) к существующей статистике для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="83c94-124">When using [**Pause**](idelaydc-pause.md) and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="83c94-125">Чтобы прерывать запись, вызовите [**иделайдк:: останавливаться**](idelaydc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="83c94-125">To stop the capture, call [**IDelaydC::Stop**](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83c94-126">Требования</span><span class="sxs-lookup"><span data-stu-id="83c94-126">Requirements</span></span>



| <span data-ttu-id="83c94-127">Требование</span><span class="sxs-lookup"><span data-stu-id="83c94-127">Requirement</span></span> | <span data-ttu-id="83c94-128">Значение</span><span class="sxs-lookup"><span data-stu-id="83c94-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83c94-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83c94-129">Minimum supported client</span></span><br/> | <span data-ttu-id="83c94-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="83c94-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="83c94-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83c94-131">Minimum supported server</span></span><br/> | <span data-ttu-id="83c94-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="83c94-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="83c94-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="83c94-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="83c94-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="83c94-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="83c94-135">DLL</span><span class="sxs-lookup"><span data-stu-id="83c94-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83c94-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83c94-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83c94-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83c94-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83c94-138">иделайдк</span><span class="sxs-lookup"><span data-stu-id="83c94-138">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="83c94-139">**Иделайдк:: Connect**</span><span class="sxs-lookup"><span data-stu-id="83c94-139">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="83c94-140">**Иделайдк::P Аусе**</span><span class="sxs-lookup"><span data-stu-id="83c94-140">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="83c94-141">**Иделайдк:: останавливаться**</span><span class="sxs-lookup"><span data-stu-id="83c94-141">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




