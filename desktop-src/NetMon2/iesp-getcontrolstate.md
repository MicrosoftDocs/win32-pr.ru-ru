---
description: Метод Жетконтролстате Извлекает состояние записи, которое указывает, запущена или приостановлена запись.
ms.assetid: 19cc3095-3aa3-4482-95f5-959b19f76cea
title: 'Метод ИЕСП:: Жетконтролстате (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: c791d5dc1f5d5321268fef2fb5cf91e04d9ecff3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682465"
---
# <a name="iespgetcontrolstate-method"></a><span data-ttu-id="d4ffc-103">Метод ИЕСП:: Жетконтролстате</span><span class="sxs-lookup"><span data-stu-id="d4ffc-103">IESP::GetControlState method</span></span>

<span data-ttu-id="d4ffc-104">Метод **жетконтролстате** Извлекает состояние [*записи*](c.md), которое указывает, запущена или приостановлена запись.</span><span class="sxs-lookup"><span data-stu-id="d4ffc-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ffc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4ffc-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="d4ffc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4ffc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4ffc-107">*Исрунннинг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d4ffc-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ffc-108">Индикатор, выполняемый текущей записью, в том числе если запись приостановлена.</span><span class="sxs-lookup"><span data-stu-id="d4ffc-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="d4ffc-109">*Приостановка* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d4ffc-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ffc-110">Признак приостановки текущей записи.</span><span class="sxs-lookup"><span data-stu-id="d4ffc-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4ffc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4ffc-111">Return value</span></span>

<span data-ttu-id="d4ffc-112">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d4ffc-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d4ffc-113">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="d4ffc-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="d4ffc-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d4ffc-114">Return code</span></span>                                                                                          | <span data-ttu-id="d4ffc-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d4ffc-115">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d4ffc-116"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="d4ffc-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d4ffc-117">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="d4ffc-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="d4ffc-118">Вызовите [ИЕСП:: Connect](iesp-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="d4ffc-118">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="d4ffc-119"><dt>**НМЕРР \_ не \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="d4ffc-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="d4ffc-120">НПП подключается к сети, но не с методом [ИЕСП:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="d4ffc-120">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="d4ffc-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4ffc-121">Remarks</span></span>

<span data-ttu-id="d4ffc-122">Этот метод можно вызвать при каждом подключении НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="d4ffc-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="d4ffc-123">Этот метод можно использовать для определения того, выполняется ли запись, если запись приостановлена или если запись была остановлена, но НПП все еще подключена.</span><span class="sxs-lookup"><span data-stu-id="d4ffc-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ffc-124">Требования</span><span class="sxs-lookup"><span data-stu-id="d4ffc-124">Requirements</span></span>



| <span data-ttu-id="d4ffc-125">Требование</span><span class="sxs-lookup"><span data-stu-id="d4ffc-125">Requirement</span></span> | <span data-ttu-id="d4ffc-126">Значение</span><span class="sxs-lookup"><span data-stu-id="d4ffc-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ffc-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4ffc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d4ffc-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d4ffc-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="d4ffc-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4ffc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d4ffc-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d4ffc-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="d4ffc-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d4ffc-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4ffc-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4ffc-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="d4ffc-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d4ffc-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4ffc-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4ffc-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4ffc-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4ffc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ffc-136">иесп</span><span class="sxs-lookup"><span data-stu-id="d4ffc-136">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="d4ffc-137">ИЕСП:: Connect</span><span class="sxs-lookup"><span data-stu-id="d4ffc-137">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="d4ffc-138">ИЕСП::P Аусе</span><span class="sxs-lookup"><span data-stu-id="d4ffc-138">IESP::Pause</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="d4ffc-139">ИЕСП:: Start</span><span class="sxs-lookup"><span data-stu-id="d4ffc-139">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="d4ffc-140">ИЕСП:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="d4ffc-140">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




