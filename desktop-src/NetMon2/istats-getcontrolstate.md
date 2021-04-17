---
description: Метод Жетконтролстате Извлекает состояние записи, которое указывает, запущена или приостановлена запись.
ms.assetid: 0faf2300-d9ff-4fe0-9d50-18beafd1daea
title: 'Метод Истатс:: Жетконтролстате (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a83b5d20461b28b7022bfdc3ddbf3d5d92149c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684678"
---
# <a name="istatsgetcontrolstate-method"></a><span data-ttu-id="85420-103">Метод Истатс:: Жетконтролстате</span><span class="sxs-lookup"><span data-stu-id="85420-103">IStats::GetControlState method</span></span>

<span data-ttu-id="85420-104">Метод **жетконтролстате** Извлекает состояние [*записи*](c.md), которое указывает, запущена или приостановлена запись.</span><span class="sxs-lookup"><span data-stu-id="85420-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="85420-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85420-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="85420-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85420-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85420-107">*Исрунннинг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="85420-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85420-108">Индикатор, выполняемый текущей записью, в том числе если запись приостановлена.</span><span class="sxs-lookup"><span data-stu-id="85420-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="85420-109">*Приостановка* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="85420-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85420-110">Признак приостановки текущей записи.</span><span class="sxs-lookup"><span data-stu-id="85420-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85420-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85420-111">Return value</span></span>

<span data-ttu-id="85420-112">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="85420-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="85420-113">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="85420-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="85420-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="85420-114">Return code</span></span>                                                                                            | <span data-ttu-id="85420-115">Описание</span><span class="sxs-lookup"><span data-stu-id="85420-115">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="85420-116"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="85420-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="85420-117">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="85420-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="85420-118">Вызовите [истатс:: Connect](istats-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="85420-118">Call [IStats::Connect](istats-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="85420-119"><dt>**НМЕРР \_ не \_ \_ только статистика**</dt></span><span class="sxs-lookup"><span data-stu-id="85420-119"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="85420-120">НПП подключается к сети, но не с методом [истатс:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="85420-120">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="85420-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85420-121">Remarks</span></span>

<span data-ttu-id="85420-122">Этот метод можно вызвать при каждом подключении НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="85420-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="85420-123">Этот метод можно использовать для определения, выполняется ли запись, если запись приостановлена или если запись была остановлена, но НПП не отключен.</span><span class="sxs-lookup"><span data-stu-id="85420-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="85420-124">Требования</span><span class="sxs-lookup"><span data-stu-id="85420-124">Requirements</span></span>



| <span data-ttu-id="85420-125">Требование</span><span class="sxs-lookup"><span data-stu-id="85420-125">Requirement</span></span> | <span data-ttu-id="85420-126">Значение</span><span class="sxs-lookup"><span data-stu-id="85420-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85420-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="85420-127">Minimum supported client</span></span><br/> | <span data-ttu-id="85420-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="85420-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="85420-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="85420-129">Minimum supported server</span></span><br/> | <span data-ttu-id="85420-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="85420-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="85420-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="85420-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="85420-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="85420-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="85420-133">DLL</span><span class="sxs-lookup"><span data-stu-id="85420-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85420-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85420-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85420-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85420-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85420-136">истатс</span><span class="sxs-lookup"><span data-stu-id="85420-136">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="85420-137">Истатс:: Connect</span><span class="sxs-lookup"><span data-stu-id="85420-137">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="85420-138">Истатс::P Аусе</span><span class="sxs-lookup"><span data-stu-id="85420-138">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="85420-139">Истатск:: Start</span><span class="sxs-lookup"><span data-stu-id="85420-139">IStatsC::Start</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="85420-140">Истатск:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="85420-140">IStatsC::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




