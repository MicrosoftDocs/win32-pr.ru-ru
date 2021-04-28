---
description: 'Метод Иделайдк:: Start — запускает захват с помощью метода Start.'
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: 'Метод Иделайдк:: Start (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 25bf778d9cccce20c736c5f8b83e6af9754ac933
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118442"
---
# <a name="idelaydcstart-method"></a><span data-ttu-id="f156a-103">Метод Иделайдк:: Start</span><span class="sxs-lookup"><span data-stu-id="f156a-103">IDelaydC::Start method</span></span>

<span data-ttu-id="f156a-104">Метод **Start** запускает захват.</span><span class="sxs-lookup"><span data-stu-id="f156a-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f156a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f156a-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="f156a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f156a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f156a-107">*пфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f156a-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f156a-108">Указатель на имя [*файла записи*](c.md) , используемого для хранения сетевых данных.</span><span class="sxs-lookup"><span data-stu-id="f156a-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="f156a-109">Не забудьте кэшировать это имя файла, если это необходимо для дальнейшего использования.</span><span class="sxs-lookup"><span data-stu-id="f156a-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f156a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f156a-110">Return value</span></span>

<span data-ttu-id="f156a-111">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="f156a-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f156a-112">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="f156a-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="f156a-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f156a-113">Return code</span></span>                                                                                           | <span data-ttu-id="f156a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="f156a-114">Description</span></span>                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f156a-115"><dt>**\_запись нмерр \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="f156a-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="f156a-116">Запись находится в приостановленном состоянии и должна быть остановлена, прежде чем ее можно будет перезапустить.</span><span class="sxs-lookup"><span data-stu-id="f156a-116">The capture is in a paused state and must be stopped before it can be restarted.</span></span> <span data-ttu-id="f156a-117">Вызовите [**иделайдк:: останавливаться**](idelaydc-stop.md) , чтобы прерывать запись.</span><span class="sxs-lookup"><span data-stu-id="f156a-117">Call [**IDelaydC::Stop**](idelaydc-stop.md) to stop the capture.</span></span> <span data-ttu-id="f156a-118">Дополнительные сведения см. в подразделе "Примечания" этого раздела.</span><span class="sxs-lookup"><span data-stu-id="f156a-118">For more information, see the Remarks section in this topic.</span></span><br/> |
| <dl> <span data-ttu-id="f156a-119"><dt>**НМЕРР \_ запись**</dt></span><span class="sxs-lookup"><span data-stu-id="f156a-119"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="f156a-120">Запись уже запущена.</span><span class="sxs-lookup"><span data-stu-id="f156a-120">The capture is already started.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="f156a-121"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="f156a-121"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="f156a-122">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="f156a-122">The NPP is not connected to the network.</span></span> <span data-ttu-id="f156a-123">Вызовите [**иделайдк:: Connect**](idelaydc-connect.md) , чтобы подключиться к сети.</span><span class="sxs-lookup"><span data-stu-id="f156a-123">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="f156a-124"><dt>**НМЕРР \_ не \_ отложена**</dt></span><span class="sxs-lookup"><span data-stu-id="f156a-124"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="f156a-125">НПП подключается к сети, но не с методом [**иделайдк:: Connect**](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="f156a-125">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="f156a-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="f156a-126">Remarks</span></span>

<span data-ttu-id="f156a-127">Расположение [*файла записи*](c.md) указывается в реестре Windows, но для изменения расположения файла можно использовать сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="f156a-127">The location of the [*capture file*](c.md) is specified in your Windows registry, but you can use Network Monitor to change the file's location.</span></span>

<span data-ttu-id="f156a-128">Чтобы перезапустить запись с помощью **иделайдк:: Start** и [**Иделайдк:: останавливаться**](idelaydc-stop.md), необходимо вызвать метод [**иделайдк:: Configure**](idelaydc-configure.md) для повторной настройки подключения при каждом вызове метода **иделайдк:: Start** для перезапуска записи данных.</span><span class="sxs-lookup"><span data-stu-id="f156a-128">To restart the capture by using **IDelaydC::Start** and [**IDelaydC::Stop**](idelaydc-stop.md), you must call the [**IDelaydC::Configure**](idelaydc-configure.md) method to reconfigure the connection each time you call the **IDelaydC::Start** method to restart capturing data.</span></span> <span data-ttu-id="f156a-129">При запуске и отмене записи с помощью этих трех методов создается новый файл записи при каждом запуске записи.</span><span class="sxs-lookup"><span data-stu-id="f156a-129">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="f156a-130">Также можно запускать и прекращать захват с помощью методов [**иделайдк::P Аусе**](idelaydc-pause.md) и [**Иделайдк:: Resume**](idelaydc-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="f156a-130">You can also start and stop the capture by using the [**IDelaydC::Pause**](idelaydc-pause.md) and [**IDelaydC::Resume**](idelaydc-resume.md) methods.</span></span> <span data-ttu-id="f156a-131">При использовании этих двух методов захваченные данные хранятся в одном файле записи.</span><span class="sxs-lookup"><span data-stu-id="f156a-131">When you use these two methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f156a-132">Требования</span><span class="sxs-lookup"><span data-stu-id="f156a-132">Requirements</span></span>



| <span data-ttu-id="f156a-133">Требование</span><span class="sxs-lookup"><span data-stu-id="f156a-133">Requirement</span></span> | <span data-ttu-id="f156a-134">Значение</span><span class="sxs-lookup"><span data-stu-id="f156a-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f156a-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f156a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f156a-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f156a-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="f156a-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f156a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f156a-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f156a-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="f156a-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f156a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="f156a-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f156a-140"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="f156a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f156a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f156a-142"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f156a-142"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f156a-143">См. также</span><span class="sxs-lookup"><span data-stu-id="f156a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f156a-144">иделайдк</span><span class="sxs-lookup"><span data-stu-id="f156a-144">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="f156a-145">**Иделайдк:: Configure**</span><span class="sxs-lookup"><span data-stu-id="f156a-145">**IDelaydC::Configure**</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="f156a-146">**Иделайдк:: Connect**</span><span class="sxs-lookup"><span data-stu-id="f156a-146">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="f156a-147">**Иделайдк::P Аусе**</span><span class="sxs-lookup"><span data-stu-id="f156a-147">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="f156a-148">**Иделайдк:: Resume**</span><span class="sxs-lookup"><span data-stu-id="f156a-148">**IDelaydC::Resume**</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="f156a-149">**Иделайдк:: останавливаться**</span><span class="sxs-lookup"><span data-stu-id="f156a-149">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




