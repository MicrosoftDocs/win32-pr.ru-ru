---
description: 'Метод ИРТК:: Stop — метод Stop останавливает текущую запись.'
ms.assetid: 64a80ff1-5a48-4be8-835d-a3d304ebb324
title: 'Метод ИРТК:: останавливаться (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 10bf0886032c93288435ade05fec46077d53753c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113522"
---
# <a name="irtcstop-method"></a><span data-ttu-id="160d7-103">Метод ИРТК:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="160d7-103">IRTC::Stop method</span></span>

<span data-ttu-id="160d7-104">Метод **Stop** останавливает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="160d7-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="160d7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="160d7-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="160d7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="160d7-106">Parameters</span></span>

<span data-ttu-id="160d7-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="160d7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="160d7-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="160d7-108">Return value</span></span>

<span data-ttu-id="160d7-109">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="160d7-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="160d7-110">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="160d7-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="160d7-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="160d7-111">Return code</span></span>                                                                                          | <span data-ttu-id="160d7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="160d7-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="160d7-113"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="160d7-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="160d7-114">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="160d7-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="160d7-115">Вызовите [ИРТК:: Connect](irtc-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="160d7-115">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="160d7-116"><dt>**НМЕРР \_ не \_ захватывается**</dt></span><span class="sxs-lookup"><span data-stu-id="160d7-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="160d7-117">НПП не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="160d7-117">The NPP is not capturing data.</span></span> <span data-ttu-id="160d7-118">Вызовите [ИРТК:: Start](irtc-start.md) , чтобы начать запись.</span><span class="sxs-lookup"><span data-stu-id="160d7-118">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="160d7-119"><dt>**НМЕРР \_ не в \_ реальном времени**</dt></span><span class="sxs-lookup"><span data-stu-id="160d7-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="160d7-120">НПП подключается к сети, но не с методом [ИРТК:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="160d7-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="160d7-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="160d7-121">Remarks</span></span>

<span data-ttu-id="160d7-122">При перезапуске записи после вызова метода **ИРТК:: останавливаться** убедитесь, что вызывается [ИРТК:: Configure](irtc-configure.md) при каждом вызове [ИРТК:: Start](irtc-start.md) для перезапуска записи.</span><span class="sxs-lookup"><span data-stu-id="160d7-122">When you restart the capture after calling the **IRTC::Stop** method, make sure to call [IRTC::Configure](irtc-configure.md) each time you call [IRTC::Start](irtc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="160d7-123">Требования</span><span class="sxs-lookup"><span data-stu-id="160d7-123">Requirements</span></span>



| <span data-ttu-id="160d7-124">Требование</span><span class="sxs-lookup"><span data-stu-id="160d7-124">Requirement</span></span> | <span data-ttu-id="160d7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="160d7-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="160d7-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="160d7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="160d7-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="160d7-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="160d7-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="160d7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="160d7-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="160d7-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="160d7-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="160d7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="160d7-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="160d7-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="160d7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="160d7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="160d7-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="160d7-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="160d7-134">См. также</span><span class="sxs-lookup"><span data-stu-id="160d7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="160d7-135">иртк</span><span class="sxs-lookup"><span data-stu-id="160d7-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="160d7-136">ИРТК:: Connect</span><span class="sxs-lookup"><span data-stu-id="160d7-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="160d7-137">ИРТК:: Configure</span><span class="sxs-lookup"><span data-stu-id="160d7-137">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="160d7-138">ИРТК:: Start</span><span class="sxs-lookup"><span data-stu-id="160d7-138">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 




