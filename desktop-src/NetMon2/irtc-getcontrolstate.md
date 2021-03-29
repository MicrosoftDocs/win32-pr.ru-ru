---
description: Метод Жетконтролстате Извлекает состояние записи, которое указывает, запущена или приостановлена запись.
ms.assetid: ae0cf869-bf5b-4c23-a924-014554053c92
title: 'Метод ИРТК:: Жетконтролстате (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d437d9463ed3225cd3a474e78220acf1f07af4bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898841"
---
# <a name="irtcgetcontrolstate-method"></a><span data-ttu-id="333c2-103">Метод ИРТК:: Жетконтролстате</span><span class="sxs-lookup"><span data-stu-id="333c2-103">IRTC::GetControlState method</span></span>

<span data-ttu-id="333c2-104">Метод **жетконтролстате** Извлекает состояние [*записи*](c.md), которое указывает, запущена или приостановлена запись.</span><span class="sxs-lookup"><span data-stu-id="333c2-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="333c2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="333c2-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="333c2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="333c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="333c2-107">*Исрунннинг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="333c2-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="333c2-108">Индикатор, выполняемый текущей записью, в том числе если запись приостановлена.</span><span class="sxs-lookup"><span data-stu-id="333c2-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="333c2-109">*Приостановка* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="333c2-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="333c2-110">Признак приостановки текущей записи.</span><span class="sxs-lookup"><span data-stu-id="333c2-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="333c2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="333c2-111">Return value</span></span>

<span data-ttu-id="333c2-112">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="333c2-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="333c2-113">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="333c2-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="333c2-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="333c2-114">Return code</span></span>                                                                                          | <span data-ttu-id="333c2-115">Описание</span><span class="sxs-lookup"><span data-stu-id="333c2-115">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="333c2-116"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="333c2-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="333c2-117">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="333c2-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="333c2-118">Вызовите [ИРТК:: Connect](irtc-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="333c2-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="333c2-119"><dt>**НМЕРР \_ не в \_ реальном времени**</dt></span><span class="sxs-lookup"><span data-stu-id="333c2-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="333c2-120">НПП подключается к сети, но не с методом [ИРТК:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="333c2-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="333c2-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="333c2-121">Remarks</span></span>

<span data-ttu-id="333c2-122">Этот метод можно вызвать при каждом подключении НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="333c2-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="333c2-123">Этот метод можно использовать для определения того, выполняется ли запись, если запись приостановлена или если запись была остановлена, но НПП все еще подключена.</span><span class="sxs-lookup"><span data-stu-id="333c2-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="333c2-124">Требования</span><span class="sxs-lookup"><span data-stu-id="333c2-124">Requirements</span></span>



| <span data-ttu-id="333c2-125">Требование</span><span class="sxs-lookup"><span data-stu-id="333c2-125">Requirement</span></span> | <span data-ttu-id="333c2-126">Значение</span><span class="sxs-lookup"><span data-stu-id="333c2-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="333c2-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="333c2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="333c2-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="333c2-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="333c2-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="333c2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="333c2-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="333c2-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="333c2-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="333c2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="333c2-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="333c2-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="333c2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="333c2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="333c2-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="333c2-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="333c2-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="333c2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="333c2-136">иртк</span><span class="sxs-lookup"><span data-stu-id="333c2-136">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="333c2-137">ИРТК:: Connect</span><span class="sxs-lookup"><span data-stu-id="333c2-137">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="333c2-138">ИРТК::P Аусе</span><span class="sxs-lookup"><span data-stu-id="333c2-138">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="333c2-139">ИРТК:: Start</span><span class="sxs-lookup"><span data-stu-id="333c2-139">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="333c2-140">ИРТК:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="333c2-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




