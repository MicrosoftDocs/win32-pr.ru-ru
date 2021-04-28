---
description: ИРТК::D метода соединения. метод Disconnect отключает НПП от сети.
ms.assetid: 47a0cce0-a50d-4bad-9787-672cc3d13d07
title: ИРТК::D метода соединения (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 43acb88e2c7b6108a162c4715de02375121021f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110722"
---
# <a name="irtcdisconnect-method"></a><span data-ttu-id="7dca9-103">ИРТК::D метода соединения</span><span class="sxs-lookup"><span data-stu-id="7dca9-103">IRTC::Disconnect method</span></span>

<span data-ttu-id="7dca9-104">Метод **Disconnect** отключает НПП от сети.</span><span class="sxs-lookup"><span data-stu-id="7dca9-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dca9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7dca9-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="7dca9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7dca9-106">Parameters</span></span>

<span data-ttu-id="7dca9-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7dca9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7dca9-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7dca9-108">Return value</span></span>

<span data-ttu-id="7dca9-109">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="7dca9-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="7dca9-110">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="7dca9-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="7dca9-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7dca9-111">Return code</span></span>                                                                                          | <span data-ttu-id="7dca9-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7dca9-112">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7dca9-113"><dt>**НМЕРР \_ запись**</dt></span><span class="sxs-lookup"><span data-stu-id="7dca9-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="7dca9-114">НПП захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="7dca9-114">The NPP is capturing data.</span></span> <span data-ttu-id="7dca9-115">Невозможно отключиться от сети, пока выполняется сбор данных.</span><span class="sxs-lookup"><span data-stu-id="7dca9-115">You cannot disconnect from the network while the data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="7dca9-116"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="7dca9-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="7dca9-117">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="7dca9-117">The NPP is not connected to the network.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="7dca9-118"><dt>**НМЕРР \_ не в \_ реальном времени**</dt></span><span class="sxs-lookup"><span data-stu-id="7dca9-118"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="7dca9-119">НПП подключается к сети, но не с методом [ИРТК:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="7dca9-119">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="7dca9-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="7dca9-120">Remarks</span></span>

<span data-ttu-id="7dca9-121">Этот метод не может быть вызван, когда НПП захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="7dca9-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="7dca9-122">Необходимо вызвать метод [ИРТК:: останавливаться](irtc-stop.md) перед вызовом иртк::D соединения.</span><span class="sxs-lookup"><span data-stu-id="7dca9-122">You must call the [IRTC::Stop](irtc-stop.md) method before calling IRTC::Disconnect.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dca9-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7dca9-123">Requirements</span></span>



| <span data-ttu-id="7dca9-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7dca9-124">Requirement</span></span> | <span data-ttu-id="7dca9-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7dca9-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dca9-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7dca9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7dca9-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7dca9-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="7dca9-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7dca9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7dca9-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7dca9-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="7dca9-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7dca9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dca9-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dca9-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="7dca9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7dca9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dca9-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dca9-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dca9-134">См. также</span><span class="sxs-lookup"><span data-stu-id="7dca9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dca9-135">иртк</span><span class="sxs-lookup"><span data-stu-id="7dca9-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="7dca9-136">ИРТК:: Connect</span><span class="sxs-lookup"><span data-stu-id="7dca9-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="7dca9-137">ИРТК:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="7dca9-137">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




