---
description: Метод QueryStatus получает состояние НПП.
ms.assetid: 4517eb34-087a-491c-97b5-cbe9190fa7a2
title: 'Метод ИРТК:: QueryStatus (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e05120353cd39db661cf1b4309353034c184cd66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650672"
---
# <a name="irtcquerystatus-method"></a><span data-ttu-id="c0b10-103">Метод ИРТК:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="c0b10-103">IRTC::QueryStatus method</span></span>

<span data-ttu-id="c0b10-104">Метод **QueryStatus** получает состояние НПП.</span><span class="sxs-lookup"><span data-stu-id="c0b10-104">The **QueryStatus** method retrieves the status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0b10-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0b10-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="c0b10-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0b10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0b10-107">*пнетворкстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c0b10-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b10-108">Указатель на возвращаемую структуру [NETWORKSTATUS](networkstatus.md) , которая указывает текущее состояние (запись, пауза, остановка и т. д.) НПП.</span><span class="sxs-lookup"><span data-stu-id="c0b10-108">Pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="c0b10-109">Ответственность за выделение и освобождение памяти для структуры **NETWORKSTATUS** является обязанностью приложения.</span><span class="sxs-lookup"><span data-stu-id="c0b10-109">It is the application's responsibility to allocate and free the memory for the **NETWORKSTATUS** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0b10-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0b10-110">Return value</span></span>

<span data-ttu-id="c0b10-111">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c0b10-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c0b10-112">Если метод завершился неудачно, возвращаемое значение является следующим кодом ошибки:</span><span class="sxs-lookup"><span data-stu-id="c0b10-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="c0b10-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c0b10-113">Return code</span></span>                                                                                              | <span data-ttu-id="c0b10-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c0b10-114">Description</span></span>                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0b10-115"><dt>**НМЕРР \_ Недопустимый \_ параметр**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b10-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="c0b10-116">Параметр *пнетворкстатус* не указывает на допустимую структуру [NETWORKSTATUS](networkstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="c0b10-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="c0b10-117">Выделите память для этой структуры и снова вызовите **ИРТК:: QueryStatus** .</span><span class="sxs-lookup"><span data-stu-id="c0b10-117">Allocate memory for this structure and call **IRTC::QueryStatus** again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c0b10-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0b10-118">Remarks</span></span>

<span data-ttu-id="c0b10-119">Этот метод можно вызвать в любое время после вызова метода [креатенппинтерфаце](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="c0b10-119">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) method is called.</span></span> <span data-ttu-id="c0b10-120">Этот метод можно вызвать, чтобы узнать, подключен ли НПП к сети, узнать состояние текущего захвата и проверить, ожидают ли какие-либо триггеры.</span><span class="sxs-lookup"><span data-stu-id="c0b10-120">You can call this method to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span> <span data-ttu-id="c0b10-121">Однако перед вызовом этого метода необходимо выделить память, необходимую для структуры [NETWORKSTATUS](networkstatus.md) , и освободить эту память, когда структура больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="c0b10-121">Before calling this method, however, you must allocate the memory needed for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0b10-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c0b10-122">Requirements</span></span>



| <span data-ttu-id="c0b10-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c0b10-123">Requirement</span></span> | <span data-ttu-id="c0b10-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c0b10-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b10-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0b10-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c0b10-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c0b10-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c0b10-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0b10-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c0b10-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c0b10-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c0b10-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c0b10-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0b10-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0b10-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c0b10-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c0b10-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0b10-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0b10-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0b10-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0b10-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0b10-134">иртк</span><span class="sxs-lookup"><span data-stu-id="c0b10-134">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="c0b10-135">креатенппинтерфаце</span><span class="sxs-lookup"><span data-stu-id="c0b10-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="c0b10-136">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="c0b10-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




