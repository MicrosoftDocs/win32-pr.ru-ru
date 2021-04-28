---
description: Иделайдк::D метода соединения. метод Disconnect отключает НПП от сети.
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: Иделайдк::D метода соединения (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 967bd9674cb28363804b8c8af12c541bcb8675ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110812"
---
# <a name="idelaydcdisconnect-method"></a><span data-ttu-id="d3022-103">Иделайдк::D метода соединения</span><span class="sxs-lookup"><span data-stu-id="d3022-103">IDelaydC::Disconnect method</span></span>

<span data-ttu-id="d3022-104">Метод **Disconnect** отключает НПП от сети.</span><span class="sxs-lookup"><span data-stu-id="d3022-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3022-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3022-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="d3022-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3022-106">Parameters</span></span>

<span data-ttu-id="d3022-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d3022-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3022-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3022-108">Return value</span></span>

<span data-ttu-id="d3022-109">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d3022-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d3022-110">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="d3022-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="d3022-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d3022-111">Return code</span></span>                                                                                          | <span data-ttu-id="d3022-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d3022-112">Description</span></span>                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d3022-113"><dt>**НМЕРР \_ запись**</dt></span><span class="sxs-lookup"><span data-stu-id="d3022-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="d3022-114">НПП захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="d3022-114">The NPP is capturing data.</span></span> <span data-ttu-id="d3022-115">Невозможно отключить НПП от сети во время записи.</span><span class="sxs-lookup"><span data-stu-id="d3022-115">You cannot disconnect the NPP from the network during a capture.</span></span><br/>            |
| <dl> <span data-ttu-id="d3022-116"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="d3022-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d3022-117">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="d3022-117">The NPP is not connected to the network.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="d3022-118"><dt>**НМЕРР \_ не \_ отложена**</dt></span><span class="sxs-lookup"><span data-stu-id="d3022-118"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="d3022-119">НПП подключается к сети, но не с методом [иделайдк:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="d3022-119">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d3022-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="d3022-120">Remarks</span></span>

<span data-ttu-id="d3022-121">Этот метод не может быть вызван, когда НПП захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="d3022-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="d3022-122">Перед вызовом **Disconnect** необходимо вызвать метод **Иделайдк:: останавливаться** .</span><span class="sxs-lookup"><span data-stu-id="d3022-122">You must call the **IDelaydC::Stop** method before calling **Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3022-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d3022-123">Requirements</span></span>



| <span data-ttu-id="d3022-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d3022-124">Requirement</span></span> | <span data-ttu-id="d3022-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d3022-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3022-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3022-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d3022-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d3022-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="d3022-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3022-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d3022-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d3022-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="d3022-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d3022-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3022-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3022-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="d3022-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d3022-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3022-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3022-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3022-134">См. также</span><span class="sxs-lookup"><span data-stu-id="d3022-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3022-135">иделайдк</span><span class="sxs-lookup"><span data-stu-id="d3022-135">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="d3022-136">Иделайдк:: Connect</span><span class="sxs-lookup"><span data-stu-id="d3022-136">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="d3022-137">Иделайдк:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="d3022-137">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




