---
description: Метод Resume перезапускает отложенную запись.
ms.assetid: 685dfdee-3bd0-44b3-ac4f-c9960cf77c5c
title: 'Метод ИРТК:: Resume (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 991f70944b44ce13641318219788d9d6122b15c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673551"
---
# <a name="irtcresume-method"></a><span data-ttu-id="92076-103">Метод ИРТК:: Resume</span><span class="sxs-lookup"><span data-stu-id="92076-103">IRTC::Resume method</span></span>

<span data-ttu-id="92076-104">Метод **Resume** перезапускает отложенную запись.</span><span class="sxs-lookup"><span data-stu-id="92076-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="92076-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92076-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="92076-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92076-106">Parameters</span></span>

<span data-ttu-id="92076-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="92076-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="92076-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92076-108">Return value</span></span>

<span data-ttu-id="92076-109">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="92076-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="92076-110">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="92076-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="92076-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="92076-111">Return code</span></span>                                                                                                | <span data-ttu-id="92076-112">Описание</span><span class="sxs-lookup"><span data-stu-id="92076-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="92076-113"><dt>**\_запись нмерр \_ не \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="92076-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="92076-114">Запись не приостановлена.</span><span class="sxs-lookup"><span data-stu-id="92076-114">The capture is not paused.</span></span> <span data-ttu-id="92076-115">Вызовите [ИРТК::P Аусе](irtc-pause.md) , чтобы приостановить запись.</span><span class="sxs-lookup"><span data-stu-id="92076-115">Call [IRTC::Pause](irtc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="92076-116"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="92076-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="92076-117">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="92076-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="92076-118">Вызовите [ИРТК:: Connect](irtc-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="92076-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="92076-119"><dt>**НМЕРР \_ не в \_ реальном времени**</dt></span><span class="sxs-lookup"><span data-stu-id="92076-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>        | <span data-ttu-id="92076-120">НПП подключается к сети, но не с методом [ИРТК:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="92076-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="92076-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92076-121">Remarks</span></span>

<span data-ttu-id="92076-122">Пока захват находится в приостановленном состоянии, новые данные не фиксируются до тех пор, пока вызов метода [ИРТК:: Resume](idelaydc-resume.md) не перезапустит запись.</span><span class="sxs-lookup"><span data-stu-id="92076-122">While the capture is in a paused state, new data is not captured until a call to the [IRTC::Resume](idelaydc-resume.md) method restarts the capture.</span></span>

<span data-ttu-id="92076-123">При использовании методов **Pause** и **Resume** для управления захватом сетевой монитор продолжает добавлять [*статистику диалога*](c.md) к существующей статистике для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="92076-123">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="92076-124">Чтобы прерывать запись, вызовите метод [ИРТК:: останавливаться](irtc-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="92076-124">To stop the capture, call the [IRTC::Stop](irtc-stop.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="92076-125">Требования</span><span class="sxs-lookup"><span data-stu-id="92076-125">Requirements</span></span>



| <span data-ttu-id="92076-126">Требование</span><span class="sxs-lookup"><span data-stu-id="92076-126">Requirement</span></span> | <span data-ttu-id="92076-127">Значение</span><span class="sxs-lookup"><span data-stu-id="92076-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92076-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92076-128">Minimum supported client</span></span><br/> | <span data-ttu-id="92076-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="92076-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="92076-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92076-130">Minimum supported server</span></span><br/> | <span data-ttu-id="92076-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="92076-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="92076-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="92076-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="92076-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="92076-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="92076-134">DLL</span><span class="sxs-lookup"><span data-stu-id="92076-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92076-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92076-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92076-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92076-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92076-137">иртк</span><span class="sxs-lookup"><span data-stu-id="92076-137">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="92076-138">ИРТК:: Connect</span><span class="sxs-lookup"><span data-stu-id="92076-138">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="92076-139">ИРТК::P Аусе</span><span class="sxs-lookup"><span data-stu-id="92076-139">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="92076-140">ИРТК:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="92076-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




