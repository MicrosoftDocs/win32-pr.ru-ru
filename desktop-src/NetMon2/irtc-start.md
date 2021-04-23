---
description: Метод Start запускает захват.
ms.assetid: 1f676e19-18ff-4c34-a83f-2723ff356be2
title: 'Метод ИРТК:: Start (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3ee30112baf7813c983230fb90cd15ea7f52e2bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898833"
---
# <a name="irtcstart-method"></a><span data-ttu-id="8cd43-103">Метод ИРТК:: Start</span><span class="sxs-lookup"><span data-stu-id="8cd43-103">IRTC::Start method</span></span>

<span data-ttu-id="8cd43-104">Метод **Start** запускает захват.</span><span class="sxs-lookup"><span data-stu-id="8cd43-104">The **Start** method starts the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cd43-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8cd43-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a><span data-ttu-id="8cd43-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8cd43-106">Parameters</span></span>

<span data-ttu-id="8cd43-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8cd43-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8cd43-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8cd43-108">Return value</span></span>

<span data-ttu-id="8cd43-109">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="8cd43-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="8cd43-110">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="8cd43-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="8cd43-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8cd43-111">Return code</span></span>                                                                                           | <span data-ttu-id="8cd43-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8cd43-112">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8cd43-113"><dt>**\_запись нмерр \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="8cd43-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="8cd43-114">Запись находится в приостановленном состоянии и должна быть остановлена, прежде чем ее можно будет перезапустить.</span><span class="sxs-lookup"><span data-stu-id="8cd43-114">The capture is in a paused state and must be stopped before it can be restarted.</span></span> <span data-ttu-id="8cd43-115">Вызовите [ИРТК:: останавливаться](idelaydc-stop.md) , чтобы прерывать запись.</span><span class="sxs-lookup"><span data-stu-id="8cd43-115">Call [IRTC::Stop](idelaydc-stop.md) to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="8cd43-116"><dt>**НМЕРР \_ запись**</dt></span><span class="sxs-lookup"><span data-stu-id="8cd43-116"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="8cd43-117">Запись уже запущена.</span><span class="sxs-lookup"><span data-stu-id="8cd43-117">The capture is already started.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="8cd43-118"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="8cd43-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="8cd43-119">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="8cd43-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="8cd43-120">Вызовите [ИРТК:: Connect](irtc-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="8cd43-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/>                         |
| <dl> <span data-ttu-id="8cd43-121"><dt>**НМЕРР \_ не в \_ реальном времени**</dt></span><span class="sxs-lookup"><span data-stu-id="8cd43-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>   | <span data-ttu-id="8cd43-122">НПП подключается к сети, но не с методом [ИРТК:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="8cd43-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="8cd43-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8cd43-123">Remarks</span></span>

<span data-ttu-id="8cd43-124">При перезапуске записи с помощью методов ИРТК:: Start и [ИРТК:: останавливают](irtc-stop.md) необходимо вызвать метод [ИРТК:: Configure](irtc-configure.md) для повторной настройки подключения при каждом вызове ИРТК:: Start для перезапуска записи данных.</span><span class="sxs-lookup"><span data-stu-id="8cd43-124">When you restart the capture by using the IRTC::Start and [IRTC::Stop](irtc-stop.md) methods, you must call the [IRTC::Configure](irtc-configure.md) method to reconfigure the connection each time you call IRTC::Start to restart the data capture.</span></span>

> [!Note]  
> <span data-ttu-id="8cd43-125">Также можно запускать и прекращать захват с помощью методов [ИРТК::P Аусе](irtc-pause.md) и [ИРТК:: Resume](irtc-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="8cd43-125">You can also start and stop the capture by using the [IRTC::Pause](irtc-pause.md) and [IRTC::Resume](irtc-resume.md) methods.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8cd43-126">Требования</span><span class="sxs-lookup"><span data-stu-id="8cd43-126">Requirements</span></span>



| <span data-ttu-id="8cd43-127">Требование</span><span class="sxs-lookup"><span data-stu-id="8cd43-127">Requirement</span></span> | <span data-ttu-id="8cd43-128">Значение</span><span class="sxs-lookup"><span data-stu-id="8cd43-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cd43-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8cd43-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8cd43-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8cd43-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="8cd43-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8cd43-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8cd43-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8cd43-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="8cd43-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8cd43-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cd43-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cd43-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="8cd43-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8cd43-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cd43-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cd43-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cd43-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8cd43-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cd43-138">иртк</span><span class="sxs-lookup"><span data-stu-id="8cd43-138">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="8cd43-139">ИРТК:: Configure</span><span class="sxs-lookup"><span data-stu-id="8cd43-139">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="8cd43-140">ИРТК:: Connect</span><span class="sxs-lookup"><span data-stu-id="8cd43-140">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="8cd43-141">ИРТК::P Аусе</span><span class="sxs-lookup"><span data-stu-id="8cd43-141">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="8cd43-142">ИРТК:: Resume</span><span class="sxs-lookup"><span data-stu-id="8cd43-142">IRTC::Resume</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="8cd43-143">ИРТК:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="8cd43-143">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




