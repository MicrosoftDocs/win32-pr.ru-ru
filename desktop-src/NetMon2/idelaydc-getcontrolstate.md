---
description: Метод Жетконтролстате Извлекает состояние записи, которое указывает, запущена или приостановлена запись.
ms.assetid: 21b7faaa-591f-4e15-b4e9-453ea690ab4a
title: 'Метод Иделайдк:: Жетконтролстате (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8f5c3f084db788844f061ba2005d9c3ca38acef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990892"
---
# <a name="idelaydcgetcontrolstate-method"></a><span data-ttu-id="50e13-103">Метод Иделайдк:: Жетконтролстате</span><span class="sxs-lookup"><span data-stu-id="50e13-103">IDelaydC::GetControlState method</span></span>

<span data-ttu-id="50e13-104">Метод **жетконтролстате** Извлекает состояние [*записи*](c.md), которое указывает, запущена или приостановлена запись.</span><span class="sxs-lookup"><span data-stu-id="50e13-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e13-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50e13-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="50e13-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="50e13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50e13-107">*Исрунннинг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="50e13-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50e13-108">Индикатор, выполняемый текущей записью, в том числе если запись приостановлена.</span><span class="sxs-lookup"><span data-stu-id="50e13-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="50e13-109">*Приостановка* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="50e13-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50e13-110">Признак приостановки текущей записи.</span><span class="sxs-lookup"><span data-stu-id="50e13-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50e13-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50e13-111">Return value</span></span>

<span data-ttu-id="50e13-112">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="50e13-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="50e13-113">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="50e13-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="50e13-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="50e13-114">Return code</span></span>                                                                                          | <span data-ttu-id="50e13-115">Описание</span><span class="sxs-lookup"><span data-stu-id="50e13-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="50e13-116"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="50e13-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="50e13-117">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="50e13-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="50e13-118">Вызовите [иделайдк:: Connect](idelaydc-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="50e13-118">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="50e13-119"><dt>**НМЕРР \_ не \_ отложена**</dt></span><span class="sxs-lookup"><span data-stu-id="50e13-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="50e13-120">НПП подключается к сети, но не с методом [иделайдк:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="50e13-120">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="50e13-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50e13-121">Remarks</span></span>

<span data-ttu-id="50e13-122">Этот метод можно вызвать при каждом подключении НПП к сети с помощью интерфейса [иделайдк](idelaydc.md) .</span><span class="sxs-lookup"><span data-stu-id="50e13-122">This method can be called any time the NPP is connected to the network by using the [IDelaydC](idelaydc.md) interface.</span></span> <span data-ttu-id="50e13-123">Этот метод можно использовать для определения, выполняется ли запись, если запись приостановлена или если запись была остановлена, но НПП не отключен.</span><span class="sxs-lookup"><span data-stu-id="50e13-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

<span data-ttu-id="50e13-124">Методы, используемые для запуска, приостановки и остановки записи, перечислены в списке см. также ниже.</span><span class="sxs-lookup"><span data-stu-id="50e13-124">The methods used to start, pause, and, stop the capture are listed in the See Also list below.</span></span>

## <a name="requirements"></a><span data-ttu-id="50e13-125">Требования</span><span class="sxs-lookup"><span data-stu-id="50e13-125">Requirements</span></span>



| <span data-ttu-id="50e13-126">Требование</span><span class="sxs-lookup"><span data-stu-id="50e13-126">Requirement</span></span> | <span data-ttu-id="50e13-127">Значение</span><span class="sxs-lookup"><span data-stu-id="50e13-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50e13-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50e13-128">Minimum supported client</span></span><br/> | <span data-ttu-id="50e13-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50e13-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="50e13-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50e13-130">Minimum supported server</span></span><br/> | <span data-ttu-id="50e13-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50e13-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="50e13-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="50e13-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="50e13-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="50e13-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="50e13-134">DLL</span><span class="sxs-lookup"><span data-stu-id="50e13-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50e13-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50e13-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50e13-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50e13-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50e13-137">иделайдк</span><span class="sxs-lookup"><span data-stu-id="50e13-137">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="50e13-138">Иделайдк:: Connect</span><span class="sxs-lookup"><span data-stu-id="50e13-138">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="50e13-139">Иделайдк::P Аусе</span><span class="sxs-lookup"><span data-stu-id="50e13-139">IDelaydC::Pause</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="50e13-140">Иделайдк:: Start</span><span class="sxs-lookup"><span data-stu-id="50e13-140">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="50e13-141">Иделайдк:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="50e13-141">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




