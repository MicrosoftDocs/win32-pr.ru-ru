---
description: Метод Start запускает захват.
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
ms.openlocfilehash: 2d9fc3a75fc82964f6fc5a5660ef77414ae065d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683228"
---
# <a name="iespstart-method"></a><span data-ttu-id="bf506-103">Метод ИЕСП:: Start</span><span class="sxs-lookup"><span data-stu-id="bf506-103">IESP::Start method</span></span>

<span data-ttu-id="bf506-104">Метод **Start** запускает захват.</span><span class="sxs-lookup"><span data-stu-id="bf506-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf506-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf506-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="bf506-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf506-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf506-107">*пфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bf506-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf506-108">Указатель на имя [*файла записи*](c.md) , используемого для хранения сетевых данных.</span><span class="sxs-lookup"><span data-stu-id="bf506-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="bf506-109">Не забудьте кэшировать это имя файла, если это необходимо для дальнейшего использования.</span><span class="sxs-lookup"><span data-stu-id="bf506-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf506-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf506-110">Return value</span></span>

<span data-ttu-id="bf506-111">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="bf506-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="bf506-112">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="bf506-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="bf506-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bf506-113">Return code</span></span>                                                                                           | <span data-ttu-id="bf506-114">Описание</span><span class="sxs-lookup"><span data-stu-id="bf506-114">Description</span></span>                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bf506-115"><dt>**\_запись нмерр \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="bf506-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="bf506-116">Запись приостановлена и должна быть остановлена, прежде чем ее можно будет перезапустить.</span><span class="sxs-lookup"><span data-stu-id="bf506-116">The capture is paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="bf506-117">Вызовите [ИЕСП:: останавливаться](iesp-stop.md) , чтобы прерывать запись.</span><span class="sxs-lookup"><span data-stu-id="bf506-117">Call [IESP::Stop](iesp-stop.md) to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="bf506-118"><dt>**НМЕРР \_ запись**</dt></span><span class="sxs-lookup"><span data-stu-id="bf506-118"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="bf506-119">Запись уже запущена.</span><span class="sxs-lookup"><span data-stu-id="bf506-119">The capture is already started.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="bf506-120"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="bf506-120"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="bf506-121">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="bf506-121">The NPP is not connected to the network.</span></span> <span data-ttu-id="bf506-122">Вызовите [ИЕСП:: Connect](iesp-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="bf506-122">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/>          |
| <dl> <span data-ttu-id="bf506-123"><dt>**НМЕРР \_ не \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="bf506-123"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="bf506-124">НПП подключается к сети, но не с методом [ИЕСП:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="bf506-124">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="bf506-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf506-125">Remarks</span></span>

<span data-ttu-id="bf506-126">Расположение [*файла записи*](c.md) указывается в реестре Windows, но для изменения расположения каталога можно использовать сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="bf506-126">The location of the [*capture file*](c.md) is specified in the Windows registry, but you can use Network Monitor to change the directory location.</span></span>

<span data-ttu-id="bf506-127">При перезапуске записи с помощью методов ИЕСП:: Start и [ИЕСП:: останавливают](iesp-stop.md) необходимо вызвать метод [ИЕСП:: Configure](iesp-configure.md) для повторной настройки подключения при каждом вызове ИЕСП:: Start для перезапуска записи данных.</span><span class="sxs-lookup"><span data-stu-id="bf506-127">When you restart the capture by using the IESP::Start and [IESP::Stop](iesp-stop.md) methods, you must call the [IESP::Configure](iesp-configure.md) method to reconfigure the connection each time you call IESP::Start to restart capturing data.</span></span> <span data-ttu-id="bf506-128">При запуске и отмене записи с помощью этих трех методов создается новый файл записи при каждом запуске записи.</span><span class="sxs-lookup"><span data-stu-id="bf506-128">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="bf506-129">Также можно запускать и прекращать захват с помощью методов [ИЕСП::P Аусе](iesp-pause.md) и [ИЕСП:: Resume](iesp-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="bf506-129">You can also start and stop the capture by using the [IESP::Pause](iesp-pause.md) and [IESP::Resume](iesp-resume.md) methods.</span></span> <span data-ttu-id="bf506-130">При использовании этих двух методов захваченные данные хранятся в одном файле записи.</span><span class="sxs-lookup"><span data-stu-id="bf506-130">When these two methods are used, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bf506-131">Требования</span><span class="sxs-lookup"><span data-stu-id="bf506-131">Requirements</span></span>



| <span data-ttu-id="bf506-132">Требование</span><span class="sxs-lookup"><span data-stu-id="bf506-132">Requirement</span></span> | <span data-ttu-id="bf506-133">Значение</span><span class="sxs-lookup"><span data-stu-id="bf506-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf506-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf506-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bf506-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bf506-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="bf506-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf506-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bf506-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bf506-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="bf506-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bf506-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf506-139"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf506-139"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="bf506-140">DLL</span><span class="sxs-lookup"><span data-stu-id="bf506-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf506-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf506-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf506-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf506-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf506-143">иесп</span><span class="sxs-lookup"><span data-stu-id="bf506-143">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="bf506-144">ИЕСП:: Configure</span><span class="sxs-lookup"><span data-stu-id="bf506-144">IESP::Configure</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="bf506-145">ИЕСП:: Connect</span><span class="sxs-lookup"><span data-stu-id="bf506-145">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="bf506-146">ИЕСП::P Аусе</span><span class="sxs-lookup"><span data-stu-id="bf506-146">IESP::Pause</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="bf506-147">ИЕСП:: Resume</span><span class="sxs-lookup"><span data-stu-id="bf506-147">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="bf506-148">ИЕСП:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="bf506-148">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




