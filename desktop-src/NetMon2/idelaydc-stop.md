---
description: 'Метод Иделайдк:: Stop — метод Stop останавливает текущую запись.'
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: 'Метод Иделайдк:: останавливаться (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 38be5b6ba4c3f6edcd716f4d0235150e96dd692a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110782"
---
# <a name="idelaydcstop-method"></a><span data-ttu-id="cd0a3-103">Метод Иделайдк:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="cd0a3-103">IDelaydC::Stop method</span></span>

<span data-ttu-id="cd0a3-104">Метод **Stop** останавливает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="cd0a3-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd0a3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd0a3-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="cd0a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd0a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd0a3-107">*лпстатс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cd0a3-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd0a3-108">Указатель на структуру [статистики](statistics.md) , которая содержит статистику сети, например общее число кадров и общее число записанных байтов.</span><span class="sxs-lookup"><span data-stu-id="cd0a3-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd0a3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd0a3-109">Return value</span></span>

<span data-ttu-id="cd0a3-110">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="cd0a3-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="cd0a3-111">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="cd0a3-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="cd0a3-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cd0a3-112">Return code</span></span>                                                                                          | <span data-ttu-id="cd0a3-113">Описание</span><span class="sxs-lookup"><span data-stu-id="cd0a3-113">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cd0a3-114"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="cd0a3-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="cd0a3-115">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="cd0a3-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="cd0a3-116">Вызовите [иделайдк:: Connect](idelaydc-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="cd0a3-116">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="cd0a3-117"><dt>**НМЕРР \_ не \_ захватывается**</dt></span><span class="sxs-lookup"><span data-stu-id="cd0a3-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="cd0a3-118">НПП не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="cd0a3-118">The NPP is not capturing data.</span></span> <span data-ttu-id="cd0a3-119">Вызовите [иделайдк:: Start](idelaydc-start.md) , чтобы начать запись.</span><span class="sxs-lookup"><span data-stu-id="cd0a3-119">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="cd0a3-120"><dt>**НМЕРР \_ не \_ отложена**</dt></span><span class="sxs-lookup"><span data-stu-id="cd0a3-120"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="cd0a3-121">НПП подключается к сети, но не с методом [иделайдк:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="cd0a3-121">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="cd0a3-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="cd0a3-122">Remarks</span></span>

<span data-ttu-id="cd0a3-123">При вызове **иделайдк:: Stop** сетевой монитор прекращает запись данных и закрывает [*файл записи*](c.md).</span><span class="sxs-lookup"><span data-stu-id="cd0a3-123">When **IDelaydC::Stop** is called, Network Monitor stops capturing data and closes the [*capture file*](c.md).</span></span> <span data-ttu-id="cd0a3-124">(Имя файла записи было возвращено при вызове [иделайдк:: Start](idelaydc-start.md) ).</span><span class="sxs-lookup"><span data-stu-id="cd0a3-124">(The name of the capture file was returned when [IDelaydC::Start](idelaydc-start.md) was called).</span></span> <span data-ttu-id="cd0a3-125">Теперь можно просмотреть содержимое файла записи.</span><span class="sxs-lookup"><span data-stu-id="cd0a3-125">You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="cd0a3-126">Когда вы останавливаете и запускаете запись, убедитесь, что вы вызываете метод [иделайдк:: Configure](idelaydc-configure.md) каждый раз, когда вызывается [Иделайдк:: Start](idelaydc-start.md) для перезапуска записи.</span><span class="sxs-lookup"><span data-stu-id="cd0a3-126">When you stop and start the capture, make sure you call the [IDelaydC::Configure](idelaydc-configure.md) method each time you call [IDelaydC::Start](idelaydc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd0a3-127">Требования</span><span class="sxs-lookup"><span data-stu-id="cd0a3-127">Requirements</span></span>



| <span data-ttu-id="cd0a3-128">Требование</span><span class="sxs-lookup"><span data-stu-id="cd0a3-128">Requirement</span></span> | <span data-ttu-id="cd0a3-129">Значение</span><span class="sxs-lookup"><span data-stu-id="cd0a3-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd0a3-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd0a3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cd0a3-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cd0a3-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="cd0a3-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd0a3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cd0a3-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cd0a3-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="cd0a3-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cd0a3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd0a3-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd0a3-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="cd0a3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cd0a3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd0a3-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd0a3-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd0a3-138">См. также</span><span class="sxs-lookup"><span data-stu-id="cd0a3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd0a3-139">иделайдк</span><span class="sxs-lookup"><span data-stu-id="cd0a3-139">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="cd0a3-140">Иделайдк:: Connect</span><span class="sxs-lookup"><span data-stu-id="cd0a3-140">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="cd0a3-141">Иделайдк:: Configure</span><span class="sxs-lookup"><span data-stu-id="cd0a3-141">IDelaydC::Configure</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="cd0a3-142">Иделайдк:: Start</span><span class="sxs-lookup"><span data-stu-id="cd0a3-142">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="cd0a3-143">СТАТИСТИЧЕСКИ</span><span class="sxs-lookup"><span data-stu-id="cd0a3-143">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




