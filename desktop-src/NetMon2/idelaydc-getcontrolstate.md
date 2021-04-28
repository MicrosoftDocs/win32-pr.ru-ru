---
description: 'Метод Иделайдк:: Жетконтролстате — метод Жетконтролстате Извлекает состояние записи, которое указывает, запущена или приостановлена запись.'
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
ms.openlocfilehash: 825112ec9a33ef176d5a69765837214249e33102
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110772"
---
# <a name="idelaydcgetcontrolstate-method"></a><span data-ttu-id="712e7-103">Метод Иделайдк:: Жетконтролстате</span><span class="sxs-lookup"><span data-stu-id="712e7-103">IDelaydC::GetControlState method</span></span>

<span data-ttu-id="712e7-104">Метод **жетконтролстате** Извлекает состояние [*записи*](c.md), которое указывает, запущена или приостановлена запись.</span><span class="sxs-lookup"><span data-stu-id="712e7-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="712e7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="712e7-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="712e7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="712e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="712e7-107">*Исрунннинг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="712e7-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="712e7-108">Индикатор, выполняемый текущей записью, в том числе если запись приостановлена.</span><span class="sxs-lookup"><span data-stu-id="712e7-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="712e7-109">*Приостановка* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="712e7-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="712e7-110">Признак приостановки текущей записи.</span><span class="sxs-lookup"><span data-stu-id="712e7-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="712e7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="712e7-111">Return value</span></span>

<span data-ttu-id="712e7-112">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="712e7-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="712e7-113">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="712e7-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="712e7-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="712e7-114">Return code</span></span>                                                                                          | <span data-ttu-id="712e7-115">Описание</span><span class="sxs-lookup"><span data-stu-id="712e7-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="712e7-116"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="712e7-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="712e7-117">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="712e7-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="712e7-118">Вызовите [иделайдк:: Connect](idelaydc-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="712e7-118">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="712e7-119"><dt>**НМЕРР \_ не \_ отложена**</dt></span><span class="sxs-lookup"><span data-stu-id="712e7-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="712e7-120">НПП подключается к сети, но не с методом [иделайдк:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="712e7-120">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="712e7-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="712e7-121">Remarks</span></span>

<span data-ttu-id="712e7-122">Этот метод можно вызвать при каждом подключении НПП к сети с помощью интерфейса [иделайдк](idelaydc.md) .</span><span class="sxs-lookup"><span data-stu-id="712e7-122">This method can be called any time the NPP is connected to the network by using the [IDelaydC](idelaydc.md) interface.</span></span> <span data-ttu-id="712e7-123">Этот метод можно использовать для определения, выполняется ли запись, если запись приостановлена или если запись была остановлена, но НПП не отключен.</span><span class="sxs-lookup"><span data-stu-id="712e7-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

<span data-ttu-id="712e7-124">Методы, используемые для запуска, приостановки и остановки записи, перечислены в списке см. также ниже.</span><span class="sxs-lookup"><span data-stu-id="712e7-124">The methods used to start, pause, and, stop the capture are listed in the See Also list below.</span></span>

## <a name="requirements"></a><span data-ttu-id="712e7-125">Требования</span><span class="sxs-lookup"><span data-stu-id="712e7-125">Requirements</span></span>



| <span data-ttu-id="712e7-126">Требование</span><span class="sxs-lookup"><span data-stu-id="712e7-126">Requirement</span></span> | <span data-ttu-id="712e7-127">Значение</span><span class="sxs-lookup"><span data-stu-id="712e7-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="712e7-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="712e7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="712e7-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="712e7-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="712e7-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="712e7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="712e7-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="712e7-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="712e7-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="712e7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="712e7-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="712e7-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="712e7-134">DLL</span><span class="sxs-lookup"><span data-stu-id="712e7-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="712e7-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="712e7-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="712e7-136">См. также</span><span class="sxs-lookup"><span data-stu-id="712e7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="712e7-137">иделайдк</span><span class="sxs-lookup"><span data-stu-id="712e7-137">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="712e7-138">Иделайдк:: Connect</span><span class="sxs-lookup"><span data-stu-id="712e7-138">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="712e7-139">Иделайдк::P Аусе</span><span class="sxs-lookup"><span data-stu-id="712e7-139">IDelaydC::Pause</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="712e7-140">Иделайдк:: Start</span><span class="sxs-lookup"><span data-stu-id="712e7-140">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="712e7-141">Иделайдк:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="712e7-141">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




