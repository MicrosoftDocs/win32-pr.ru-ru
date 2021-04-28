---
description: 'Метод Истатс:: QueryStatus — метод QueryStatus получает состояние НПП.'
ms.assetid: 86b1c1ee-3a35-4603-9e93-fe09f886c32f
title: 'Метод Истатс:: QueryStatus (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7587c2fff56d305c0298948bdf8690fd801f3f3b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113482"
---
# <a name="istatsquerystatus-method"></a><span data-ttu-id="388ed-103">Метод Истатс:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="388ed-103">IStats::QueryStatus method</span></span>

<span data-ttu-id="388ed-104">Метод **QueryStatus** получает состояние НПП.</span><span class="sxs-lookup"><span data-stu-id="388ed-104">The **QueryStatus** method retrieves the status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="388ed-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="388ed-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="388ed-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="388ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="388ed-107">*пнетворкстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="388ed-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="388ed-108">Указатель на возвращаемую структуру [NETWORKSTATUS](networkstatus.md) , которая указывает текущее состояние (запись, пауза, остановка и т. д.) НПП.</span><span class="sxs-lookup"><span data-stu-id="388ed-108">Pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="388ed-109">Ответственность за выделение и освобождение памяти для структуры **NETWORKSTATUS** является обязанностью приложения.</span><span class="sxs-lookup"><span data-stu-id="388ed-109">It is the application's responsibility to allocate and free the memory for the **NETWORKSTATUS** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="388ed-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="388ed-110">Return value</span></span>

<span data-ttu-id="388ed-111">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="388ed-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="388ed-112">Если метод завершился неудачно, возвращаемое значение является следующим кодом ошибки:</span><span class="sxs-lookup"><span data-stu-id="388ed-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="388ed-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="388ed-113">Return code</span></span>                                                                                              | <span data-ttu-id="388ed-114">Описание</span><span class="sxs-lookup"><span data-stu-id="388ed-114">Description</span></span>                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="388ed-115"><dt>**НМЕРР \_ Недопустимый \_ параметр**</dt></span><span class="sxs-lookup"><span data-stu-id="388ed-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="388ed-116">Параметр *пнетворкстатус* не указывает на допустимую структуру [NETWORKSTATUS](networkstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="388ed-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="388ed-117">Выделите память для этой структуры и снова вызовите метод **истатс:: QueryStatus** .</span><span class="sxs-lookup"><span data-stu-id="388ed-117">Allocate memory for this structure and call the **IStats::QueryStatus** method again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="388ed-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="388ed-118">Remarks</span></span>

<span data-ttu-id="388ed-119">Этот метод можно вызвать в любое время после вызова метода [креатенппинтерфаце](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="388ed-119">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) method is called.</span></span> <span data-ttu-id="388ed-120">Его можно вызвать, чтобы узнать, подключен ли НПП к сети, узнать состояние текущего захвата и проверить, ожидают ли какие-либо триггеры.</span><span class="sxs-lookup"><span data-stu-id="388ed-120">It can be called to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span> <span data-ttu-id="388ed-121">Однако перед вызовом этого метода необходимо выделить память, необходимую для структуры [NETWORKSTATUS](networkstatus.md) , и освободить эту память, когда структура больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="388ed-121">Before calling this method, however, you must allocate the memory needed for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="388ed-122">Требования</span><span class="sxs-lookup"><span data-stu-id="388ed-122">Requirements</span></span>



| <span data-ttu-id="388ed-123">Требование</span><span class="sxs-lookup"><span data-stu-id="388ed-123">Requirement</span></span> | <span data-ttu-id="388ed-124">Значение</span><span class="sxs-lookup"><span data-stu-id="388ed-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="388ed-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="388ed-125">Minimum supported client</span></span><br/> | <span data-ttu-id="388ed-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="388ed-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="388ed-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="388ed-127">Minimum supported server</span></span><br/> | <span data-ttu-id="388ed-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="388ed-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="388ed-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="388ed-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="388ed-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="388ed-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="388ed-131">DLL</span><span class="sxs-lookup"><span data-stu-id="388ed-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="388ed-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="388ed-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="388ed-133">См. также</span><span class="sxs-lookup"><span data-stu-id="388ed-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="388ed-134">истатс</span><span class="sxs-lookup"><span data-stu-id="388ed-134">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="388ed-135">креатенппинтерфаце</span><span class="sxs-lookup"><span data-stu-id="388ed-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="388ed-136">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="388ed-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




