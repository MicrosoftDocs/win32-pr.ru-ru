---
description: Метод Stop останавливает текущую запись.
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: 'Метод Истатс:: останавливаться (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7b7b58527e7bde0c3bbdec4fc162b705dd178c10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650571"
---
# <a name="istatsstop-method"></a><span data-ttu-id="6e4c2-103">Метод Истатс:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="6e4c2-103">IStats::Stop method</span></span>

<span data-ttu-id="6e4c2-104">Метод **Stop** останавливает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="6e4c2-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e4c2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e4c2-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="6e4c2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e4c2-106">Parameters</span></span>

<span data-ttu-id="6e4c2-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="6e4c2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e4c2-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e4c2-108">Return value</span></span>

<span data-ttu-id="6e4c2-109">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6e4c2-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6e4c2-110">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="6e4c2-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="6e4c2-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6e4c2-111">Return code</span></span>                                                                                            | <span data-ttu-id="6e4c2-112">Описание</span><span class="sxs-lookup"><span data-stu-id="6e4c2-112">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6e4c2-113"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="6e4c2-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="6e4c2-114">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="6e4c2-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="6e4c2-115">Вызовите метод [истатс:: Connect](istats-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="6e4c2-115">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="6e4c2-116"><dt>**НМЕРР \_ не \_ захватывается**</dt></span><span class="sxs-lookup"><span data-stu-id="6e4c2-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="6e4c2-117">НПП не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="6e4c2-117">The NPP is not capturing data.</span></span> <span data-ttu-id="6e4c2-118">Вызовите метод [истатс:: Start](istats-start.md) , чтобы начать запись.</span><span class="sxs-lookup"><span data-stu-id="6e4c2-118">Call the [IStats::Start](istats-start.md) method to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="6e4c2-119"><dt>**НМЕРР \_ не \_ \_ только статистика**</dt></span><span class="sxs-lookup"><span data-stu-id="6e4c2-119"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="6e4c2-120">НПП подключается к сети, но не с методом [истатс:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="6e4c2-120">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="6e4c2-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e4c2-121">Remarks</span></span>

<span data-ttu-id="6e4c2-122">При перезапуске записи после вызова **истатс:: останавливаться** убедитесь, что вы вызываете метод [Истатс:: Configure](istats-configure.md) каждый раз, когда вызывается [истатс:: Start](istats-start.md) для перезапуска записи.</span><span class="sxs-lookup"><span data-stu-id="6e4c2-122">When restarting the capture after **IStats::Stop** has been called, make sure you call the [IStats::Configure](istats-configure.md) method each time you call [IStats::Start](istats-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e4c2-123">Требования</span><span class="sxs-lookup"><span data-stu-id="6e4c2-123">Requirements</span></span>



| <span data-ttu-id="6e4c2-124">Требование</span><span class="sxs-lookup"><span data-stu-id="6e4c2-124">Requirement</span></span> | <span data-ttu-id="6e4c2-125">Значение</span><span class="sxs-lookup"><span data-stu-id="6e4c2-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e4c2-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e4c2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6e4c2-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6e4c2-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="6e4c2-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e4c2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6e4c2-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6e4c2-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="6e4c2-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6e4c2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e4c2-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e4c2-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="6e4c2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6e4c2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e4c2-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e4c2-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e4c2-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e4c2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e4c2-135">истатс</span><span class="sxs-lookup"><span data-stu-id="6e4c2-135">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="6e4c2-136">Истатс:: Connect</span><span class="sxs-lookup"><span data-stu-id="6e4c2-136">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="6e4c2-137">Истатс:: Configure</span><span class="sxs-lookup"><span data-stu-id="6e4c2-137">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="6e4c2-138">Истатс:: Start</span><span class="sxs-lookup"><span data-stu-id="6e4c2-138">IStats::Start</span></span>](istats-start.md)
</dt> </dl>

 

 




