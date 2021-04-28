---
description: 'Метод ИЕСП:: Start — запускает захват с помощью метода Start.'
ms.assetid: 8bf8c0c7-20be-4404-8ea5-b28b4c658523
title: 'Метод ИЕСП:: Start (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 6dd0d1159132e594b6d48ea6799da5846eeb626e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103802"
---
# <a name="iespstart-method"></a><span data-ttu-id="ca2bd-103">Метод ИЕСП:: Start</span><span class="sxs-lookup"><span data-stu-id="ca2bd-103">IESP::Start method</span></span>

<span data-ttu-id="ca2bd-104">Метод **Start** запускает захват.</span><span class="sxs-lookup"><span data-stu-id="ca2bd-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca2bd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca2bd-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="ca2bd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca2bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca2bd-107">*пфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ca2bd-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca2bd-108">Указатель на имя [*файла записи*](c.md) , используемого для хранения сетевых данных.</span><span class="sxs-lookup"><span data-stu-id="ca2bd-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="ca2bd-109">Не забудьте кэшировать это имя файла, если это необходимо для дальнейшего использования.</span><span class="sxs-lookup"><span data-stu-id="ca2bd-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca2bd-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca2bd-110">Return value</span></span>

<span data-ttu-id="ca2bd-111">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ca2bd-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ca2bd-112">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="ca2bd-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="ca2bd-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ca2bd-113">Return code</span></span>                                                                                           | <span data-ttu-id="ca2bd-114">Описание</span><span class="sxs-lookup"><span data-stu-id="ca2bd-114">Description</span></span>                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ca2bd-115"><dt>**\_запись нмерр \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="ca2bd-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="ca2bd-116">Запись приостановлена и должна быть остановлена, прежде чем ее можно будет перезапустить.</span><span class="sxs-lookup"><span data-stu-id="ca2bd-116">The capture is paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="ca2bd-117">Вызовите [ИЕСП:: останавливаться](iesp-stop.md) , чтобы прерывать запись.</span><span class="sxs-lookup"><span data-stu-id="ca2bd-117">Call [IESP::Stop](iesp-stop.md) to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="ca2bd-118"><dt>**НМЕРР \_ запись**</dt></span><span class="sxs-lookup"><span data-stu-id="ca2bd-118"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="ca2bd-119">Запись уже запущена.</span><span class="sxs-lookup"><span data-stu-id="ca2bd-119">The capture is already started.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="ca2bd-120"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="ca2bd-120"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="ca2bd-121">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="ca2bd-121">The NPP is not connected to the network.</span></span> <span data-ttu-id="ca2bd-122">Вызовите [ИЕСП:: Connect](iesp-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="ca2bd-122">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/>          |
| <dl> <span data-ttu-id="ca2bd-123"><dt>**НМЕРР \_ не \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="ca2bd-123"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="ca2bd-124">НПП подключается к сети, но не с методом [ИЕСП:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="ca2bd-124">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="ca2bd-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="ca2bd-125">Remarks</span></span>

<span data-ttu-id="ca2bd-126">Расположение [*файла записи*](c.md) указывается в реестре Windows, но для изменения расположения каталога можно использовать сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="ca2bd-126">The location of the [*capture file*](c.md) is specified in the Windows registry, but you can use Network Monitor to change the directory location.</span></span>

<span data-ttu-id="ca2bd-127">При перезапуске записи с помощью методов ИЕСП:: Start и [ИЕСП:: останавливают](iesp-stop.md) необходимо вызвать метод [ИЕСП:: Configure](iesp-configure.md) для повторной настройки подключения при каждом вызове ИЕСП:: Start для перезапуска записи данных.</span><span class="sxs-lookup"><span data-stu-id="ca2bd-127">When you restart the capture by using the IESP::Start and [IESP::Stop](iesp-stop.md) methods, you must call the [IESP::Configure](iesp-configure.md) method to reconfigure the connection each time you call IESP::Start to restart capturing data.</span></span> <span data-ttu-id="ca2bd-128">При запуске и отмене записи с помощью этих трех методов создается новый файл записи при каждом запуске записи.</span><span class="sxs-lookup"><span data-stu-id="ca2bd-128">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="ca2bd-129">Также можно запускать и прекращать захват с помощью методов [ИЕСП::P Аусе](iesp-pause.md) и [ИЕСП:: Resume](iesp-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="ca2bd-129">You can also start and stop the capture by using the [IESP::Pause](iesp-pause.md) and [IESP::Resume](iesp-resume.md) methods.</span></span> <span data-ttu-id="ca2bd-130">При использовании этих двух методов захваченные данные хранятся в одном файле записи.</span><span class="sxs-lookup"><span data-stu-id="ca2bd-130">When these two methods are used, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ca2bd-131">Требования</span><span class="sxs-lookup"><span data-stu-id="ca2bd-131">Requirements</span></span>



| <span data-ttu-id="ca2bd-132">Требование</span><span class="sxs-lookup"><span data-stu-id="ca2bd-132">Requirement</span></span> | <span data-ttu-id="ca2bd-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ca2bd-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca2bd-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca2bd-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ca2bd-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ca2bd-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="ca2bd-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca2bd-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ca2bd-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ca2bd-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="ca2bd-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ca2bd-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca2bd-139"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca2bd-139"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="ca2bd-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ca2bd-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca2bd-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca2bd-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca2bd-142">См. также</span><span class="sxs-lookup"><span data-stu-id="ca2bd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca2bd-143">иесп</span><span class="sxs-lookup"><span data-stu-id="ca2bd-143">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="ca2bd-144">ИЕСП:: Configure</span><span class="sxs-lookup"><span data-stu-id="ca2bd-144">IESP::Configure</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="ca2bd-145">ИЕСП:: Connect</span><span class="sxs-lookup"><span data-stu-id="ca2bd-145">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="ca2bd-146">ИЕСП::P Аусе</span><span class="sxs-lookup"><span data-stu-id="ca2bd-146">IESP::Pause</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="ca2bd-147">ИЕСП:: Resume</span><span class="sxs-lookup"><span data-stu-id="ca2bd-147">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="ca2bd-148">ИЕСП:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="ca2bd-148">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




