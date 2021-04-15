---
description: Метод Stop останавливает текущую запись.
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: 'Метод Иделайдк:: останавливаться (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 42c9cc1c4b6da7b5f934dd96f26aa9348c43ac0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496983"
---
# <a name="idelaydcstop-method"></a><span data-ttu-id="81482-103">Метод Иделайдк:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="81482-103">IDelaydC::Stop method</span></span>

<span data-ttu-id="81482-104">Метод **Stop** останавливает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="81482-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="81482-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81482-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="81482-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="81482-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81482-107">*лпстатс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="81482-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81482-108">Указатель на структуру [статистики](statistics.md) , которая содержит статистику сети, например общее число кадров и общее число записанных байтов.</span><span class="sxs-lookup"><span data-stu-id="81482-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81482-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81482-109">Return value</span></span>

<span data-ttu-id="81482-110">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="81482-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="81482-111">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="81482-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="81482-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="81482-112">Return code</span></span>                                                                                          | <span data-ttu-id="81482-113">Описание</span><span class="sxs-lookup"><span data-stu-id="81482-113">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81482-114"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="81482-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="81482-115">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="81482-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="81482-116">Вызовите [иделайдк:: Connect](idelaydc-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="81482-116">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="81482-117"><dt>**НМЕРР \_ не \_ захватывается**</dt></span><span class="sxs-lookup"><span data-stu-id="81482-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="81482-118">НПП не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="81482-118">The NPP is not capturing data.</span></span> <span data-ttu-id="81482-119">Вызовите [иделайдк:: Start](idelaydc-start.md) , чтобы начать запись.</span><span class="sxs-lookup"><span data-stu-id="81482-119">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="81482-120"><dt>**НМЕРР \_ не \_ отложена**</dt></span><span class="sxs-lookup"><span data-stu-id="81482-120"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="81482-121">НПП подключается к сети, но не с методом [иделайдк:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="81482-121">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="81482-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81482-122">Remarks</span></span>

<span data-ttu-id="81482-123">При вызове **иделайдк:: Stop** сетевой монитор прекращает запись данных и закрывает [*файл записи*](c.md).</span><span class="sxs-lookup"><span data-stu-id="81482-123">When **IDelaydC::Stop** is called, Network Monitor stops capturing data and closes the [*capture file*](c.md).</span></span> <span data-ttu-id="81482-124">(Имя файла записи было возвращено при вызове [иделайдк:: Start](idelaydc-start.md) ).</span><span class="sxs-lookup"><span data-stu-id="81482-124">(The name of the capture file was returned when [IDelaydC::Start](idelaydc-start.md) was called).</span></span> <span data-ttu-id="81482-125">Теперь можно просмотреть содержимое файла записи.</span><span class="sxs-lookup"><span data-stu-id="81482-125">You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="81482-126">Когда вы останавливаете и запускаете запись, убедитесь, что вы вызываете метод [иделайдк:: Configure](idelaydc-configure.md) каждый раз, когда вызывается [Иделайдк:: Start](idelaydc-start.md) для перезапуска записи.</span><span class="sxs-lookup"><span data-stu-id="81482-126">When you stop and start the capture, make sure you call the [IDelaydC::Configure](idelaydc-configure.md) method each time you call [IDelaydC::Start](idelaydc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="81482-127">Требования</span><span class="sxs-lookup"><span data-stu-id="81482-127">Requirements</span></span>



| <span data-ttu-id="81482-128">Требование</span><span class="sxs-lookup"><span data-stu-id="81482-128">Requirement</span></span> | <span data-ttu-id="81482-129">Значение</span><span class="sxs-lookup"><span data-stu-id="81482-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81482-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81482-130">Minimum supported client</span></span><br/> | <span data-ttu-id="81482-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="81482-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="81482-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81482-132">Minimum supported server</span></span><br/> | <span data-ttu-id="81482-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="81482-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="81482-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="81482-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="81482-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="81482-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="81482-136">DLL</span><span class="sxs-lookup"><span data-stu-id="81482-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81482-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81482-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81482-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81482-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81482-139">иделайдк</span><span class="sxs-lookup"><span data-stu-id="81482-139">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="81482-140">Иделайдк:: Connect</span><span class="sxs-lookup"><span data-stu-id="81482-140">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="81482-141">Иделайдк:: Configure</span><span class="sxs-lookup"><span data-stu-id="81482-141">IDelaydC::Configure</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="81482-142">Иделайдк:: Start</span><span class="sxs-lookup"><span data-stu-id="81482-142">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="81482-143">СТАТИСТИЧЕСКИ</span><span class="sxs-lookup"><span data-stu-id="81482-143">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




