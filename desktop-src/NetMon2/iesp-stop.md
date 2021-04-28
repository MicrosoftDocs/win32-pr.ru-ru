---
description: 'Метод ИЕСП:: Stop — метод Stop останавливает текущую запись.'
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: 'Метод ИЕСП:: останавливаться (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ac262d8da5ab218db7300ea38da59d5c738421c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103772"
---
# <a name="iespstop-method"></a><span data-ttu-id="c8abe-103">Метод ИЕСП:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="c8abe-103">IESP::Stop method</span></span>

<span data-ttu-id="c8abe-104">Метод **Stop** останавливает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="c8abe-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8abe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8abe-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="c8abe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8abe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8abe-107">*лпстатс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c8abe-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8abe-108">Указатель на структуру [статистики](statistics.md) , которая содержит статистику сети, например общее число кадров и общее число записанных байтов.</span><span class="sxs-lookup"><span data-stu-id="c8abe-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8abe-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8abe-109">Return value</span></span>

<span data-ttu-id="c8abe-110">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c8abe-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c8abe-111">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="c8abe-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="c8abe-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c8abe-112">Return code</span></span>                                                                                          | <span data-ttu-id="c8abe-113">Описание</span><span class="sxs-lookup"><span data-stu-id="c8abe-113">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8abe-114"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="c8abe-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="c8abe-115">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="c8abe-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="c8abe-116">Вызовите [ИЕСП:: Connect](iesp-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="c8abe-116">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="c8abe-117"><dt>**НМЕРР \_ не \_ захватывается**</dt></span><span class="sxs-lookup"><span data-stu-id="c8abe-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="c8abe-118">НПП не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="c8abe-118">The NPP is not capturing data.</span></span> <span data-ttu-id="c8abe-119">Вызовите [ИЕСП:: Start](iesp-start.md) , чтобы начать запись.</span><span class="sxs-lookup"><span data-stu-id="c8abe-119">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="c8abe-120"><dt>**НМЕРР \_ не \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="c8abe-120"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="c8abe-121">НПП подключается к сети, но не с методом [ИЕСП:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="c8abe-121">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="c8abe-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="c8abe-122">Remarks</span></span>

<span data-ttu-id="c8abe-123">При вызове метода **ИЕСП:: Stop** сетевой монитор прекращает запись данных и закрывает [*файл записи.*](c.md)</span><span class="sxs-lookup"><span data-stu-id="c8abe-123">When the **IESP::Stop** method is called, Network Monitor stops capturing data and closes the [*capture file.*](c.md)</span></span> <span data-ttu-id="c8abe-124">(Имя файла записи было возвращено при вызове [ИЕСП:: Start](iesp-start.md) .) Теперь можно просмотреть содержимое файла записи.</span><span class="sxs-lookup"><span data-stu-id="c8abe-124">(The name of the capture file was returned when [IESP::Start](iesp-start.md) was called.) You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="c8abe-125">При запуске и перезапуске записи обязательно вызывайте метод [ИЕСП:: Configure](iesp-configure.md) каждый раз при вызове [ИЕСП:: Start](iesp-start.md) для перезапуска записи.</span><span class="sxs-lookup"><span data-stu-id="c8abe-125">When you stop and restart the capture, make sure to call the [IESP::Configure](iesp-configure.md) method each time you call [IESP::Start](iesp-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8abe-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c8abe-126">Requirements</span></span>



| <span data-ttu-id="c8abe-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c8abe-127">Requirement</span></span> | <span data-ttu-id="c8abe-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c8abe-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8abe-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8abe-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c8abe-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c8abe-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c8abe-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8abe-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c8abe-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c8abe-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c8abe-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c8abe-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8abe-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8abe-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c8abe-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c8abe-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8abe-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8abe-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8abe-137">См. также</span><span class="sxs-lookup"><span data-stu-id="c8abe-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8abe-138">иесп</span><span class="sxs-lookup"><span data-stu-id="c8abe-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="c8abe-139">ИЕСП:: Connect</span><span class="sxs-lookup"><span data-stu-id="c8abe-139">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="c8abe-140">ИЕСП:: Start</span><span class="sxs-lookup"><span data-stu-id="c8abe-140">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="c8abe-141">СТАТИСТИЧЕСКИ</span><span class="sxs-lookup"><span data-stu-id="c8abe-141">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




