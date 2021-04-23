---
description: Метод Pause временно останавливает текущую запись.
ms.assetid: 43176e9e-1502-484c-a8af-4e7bbf5f6474
title: 'Истатс: метод:P Аусе (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d9e9f04ce3d25399866c711dad7a853f2c43c2ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674482"
---
# <a name="istatspause-method"></a><span data-ttu-id="29944-103">Истатс: метод:P Аусе</span><span class="sxs-lookup"><span data-stu-id="29944-103">IStats::Pause method</span></span>

<span data-ttu-id="29944-104">Метод **Pause** временно останавливает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="29944-104">The **Pause** method temporarily stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="29944-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29944-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="29944-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="29944-106">Parameters</span></span>

<span data-ttu-id="29944-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="29944-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="29944-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29944-108">Return value</span></span>

<span data-ttu-id="29944-109">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="29944-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="29944-110">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="29944-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="29944-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="29944-111">Return code</span></span>                                                                                            | <span data-ttu-id="29944-112">Описание</span><span class="sxs-lookup"><span data-stu-id="29944-112">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="29944-113"><dt>**\_запись нмерр \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="29944-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl>  | <span data-ttu-id="29944-114">Запись уже приостановлена.</span><span class="sxs-lookup"><span data-stu-id="29944-114">The capture is already paused.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="29944-115"><dt>**НМЕРР \_ не \_ захватывается**</dt></span><span class="sxs-lookup"><span data-stu-id="29944-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="29944-116">НПП не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="29944-116">The NPP is not capturing data.</span></span> <span data-ttu-id="29944-117">Вызовите метод [истатс:: Start](istats-start.md) , чтобы начать запись.</span><span class="sxs-lookup"><span data-stu-id="29944-117">Call the [IStats::Start](istats-start.md) method to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="29944-118"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="29944-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="29944-119">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="29944-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="29944-120">Вызовите метод [истатс:: Connect](istats-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="29944-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="29944-121"><dt>**НМЕРР \_ не \_ \_ только статистика**</dt></span><span class="sxs-lookup"><span data-stu-id="29944-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="29944-122">НПП подключается к сети, но не с методом [истатс:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="29944-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="29944-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29944-123">Remarks</span></span>

<span data-ttu-id="29944-124">Пока захват приостановлен, новые кадры не фиксируются, пока вызов метода [истатс:: Resume](istats-resume.md) не перезапустит запись.</span><span class="sxs-lookup"><span data-stu-id="29944-124">While the capture is paused, new frames are not captured until a call to the [IStats::Resume](istats-resume.md) method restarts the capture.</span></span>

<span data-ttu-id="29944-125">При использовании методов **истатс::P Аусе** и **Истатс:: Resume** для управления захватом сетевой монитор продолжает добавлять [*статистику беседы*](c.md) при выполнении записи.</span><span class="sxs-lookup"><span data-stu-id="29944-125">When you use the **IStats::Pause** and **IStats::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="29944-126">Чтобы перезапустить захват [истатс:: Resume](istats-resume.md).</span><span class="sxs-lookup"><span data-stu-id="29944-126">To restart the capture call [IStats::Resume](istats-resume.md).</span></span> <span data-ttu-id="29944-127">Чтобы прерывать запись, вызовите [истатс:: останавливаться](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="29944-127">To stop the capture, call [IStats::Stop](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29944-128">Требования</span><span class="sxs-lookup"><span data-stu-id="29944-128">Requirements</span></span>



| <span data-ttu-id="29944-129">Требование</span><span class="sxs-lookup"><span data-stu-id="29944-129">Requirement</span></span> | <span data-ttu-id="29944-130">Значение</span><span class="sxs-lookup"><span data-stu-id="29944-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29944-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29944-131">Minimum supported client</span></span><br/> | <span data-ttu-id="29944-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="29944-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="29944-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29944-133">Minimum supported server</span></span><br/> | <span data-ttu-id="29944-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="29944-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="29944-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="29944-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="29944-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="29944-136"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="29944-137">DLL</span><span class="sxs-lookup"><span data-stu-id="29944-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29944-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29944-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29944-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29944-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29944-140">истатс</span><span class="sxs-lookup"><span data-stu-id="29944-140">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="29944-141">Истатс:: Connect</span><span class="sxs-lookup"><span data-stu-id="29944-141">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="29944-142">Истатс:: Resume</span><span class="sxs-lookup"><span data-stu-id="29944-142">IStats::Resume</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="29944-143">Истатс:: Start</span><span class="sxs-lookup"><span data-stu-id="29944-143">IStats::Start</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="29944-144">Истатс:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="29944-144">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




