---
description: Метод Disconnect отключает НПП от сети.
ms.assetid: 962e033d-a51c-47a2-83dc-cee1e7150ab8
title: ИЕСП::D метода соединения (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b0dac1843083d77121883b2609c32addffbae290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143768"
---
# <a name="iespdisconnect-method"></a><span data-ttu-id="2e101-103">ИЕСП::D метода соединения</span><span class="sxs-lookup"><span data-stu-id="2e101-103">IESP::Disconnect method</span></span>

<span data-ttu-id="2e101-104">Метод **Disconnect** отключает НПП от сети.</span><span class="sxs-lookup"><span data-stu-id="2e101-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e101-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e101-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="2e101-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e101-106">Parameters</span></span>

<span data-ttu-id="2e101-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2e101-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e101-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e101-108">Return value</span></span>

<span data-ttu-id="2e101-109">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="2e101-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2e101-110">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="2e101-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="2e101-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2e101-111">Return code</span></span>                                                                                          | <span data-ttu-id="2e101-112">Описание</span><span class="sxs-lookup"><span data-stu-id="2e101-112">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2e101-113"><dt>**НМЕРР \_ запись**</dt></span><span class="sxs-lookup"><span data-stu-id="2e101-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="2e101-114">НПП захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="2e101-114">The NPP is capturing data.</span></span> <span data-ttu-id="2e101-115">Невозможно отключиться от сети, пока выполняется сбор данных.</span><span class="sxs-lookup"><span data-stu-id="2e101-115">You cannot disconnect from the network while data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="2e101-116"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="2e101-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="2e101-117">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="2e101-117">The NPP is not connected to the network.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="2e101-118"><dt>**НМЕРР \_ не \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="2e101-118"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="2e101-119">НПП подключается к сети, но не с методом [ИЕСП:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="2e101-119">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="2e101-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e101-120">Remarks</span></span>

<span data-ttu-id="2e101-121">Этот метод не может быть вызван, когда НПП захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="2e101-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="2e101-122">Необходимо вызвать метод **ИЕСП:: останавливаться** перед вызовом **ИЕСП::D соединения**.</span><span class="sxs-lookup"><span data-stu-id="2e101-122">You must call the **IESP::Stop** method before calling **IESP::Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e101-123">Требования</span><span class="sxs-lookup"><span data-stu-id="2e101-123">Requirements</span></span>



| <span data-ttu-id="2e101-124">Требование</span><span class="sxs-lookup"><span data-stu-id="2e101-124">Requirement</span></span> | <span data-ttu-id="2e101-125">Значение</span><span class="sxs-lookup"><span data-stu-id="2e101-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e101-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e101-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2e101-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2e101-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="2e101-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e101-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2e101-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2e101-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="2e101-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2e101-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e101-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e101-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="2e101-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2e101-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e101-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e101-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e101-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e101-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e101-135">иесп</span><span class="sxs-lookup"><span data-stu-id="2e101-135">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="2e101-136">ИЕСП:: Connect</span><span class="sxs-lookup"><span data-stu-id="2e101-136">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="2e101-137">ИЕСП:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="2e101-137">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




