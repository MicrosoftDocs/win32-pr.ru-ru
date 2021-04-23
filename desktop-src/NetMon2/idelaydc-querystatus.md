---
description: Метод QueryStatus получает состояние НПП.
ms.assetid: b035d495-a078-4436-9501-0a30fbfa7268
title: 'Метод Иделайдк:: QueryStatus (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: cff92dfec95555076f9edba5a1b591f0ef905c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683229"
---
# <a name="idelaydcquerystatus-method"></a><span data-ttu-id="f1fd6-103">Метод Иделайдк:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="f1fd6-103">IDelaydC::QueryStatus method</span></span>

<span data-ttu-id="f1fd6-104">Метод **QueryStatus** получает состояние НПП.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-104">The **QueryStatus** method retrieves the status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1fd6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1fd6-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="f1fd6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1fd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1fd6-107">*пнетворкстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f1fd6-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1fd6-108">Указатель на возвращаемую структуру [NETWORKSTATUS](networkstatus.md) , которая указывает текущее состояние (запись, пауза, остановка и т. д.) НПП.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-108">Pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="f1fd6-109">Вы обязаны выделять и освобождать память, связанную со структурой **NETWORKSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="f1fd6-109">It is your responsibility to allocate and free the memory associated with the **NETWORKSTATUS** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1fd6-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1fd6-110">Return value</span></span>

<span data-ttu-id="f1fd6-111">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f1fd6-112">Если метод завершился неудачно, возвращаемое значение является следующим кодом ошибки:</span><span class="sxs-lookup"><span data-stu-id="f1fd6-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="f1fd6-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f1fd6-113">Return code</span></span>                                                                                              | <span data-ttu-id="f1fd6-114">Описание</span><span class="sxs-lookup"><span data-stu-id="f1fd6-114">Description</span></span>                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f1fd6-115"><dt>**НМЕРР \_ Недопустимый \_ параметр**</dt></span><span class="sxs-lookup"><span data-stu-id="f1fd6-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="f1fd6-116">Параметр *пнетворкстатус* не указывает на допустимую структуру [NETWORKSTATUS](networkstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="f1fd6-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="f1fd6-117">Выделите память для этой структуры и снова вызовите метод **иделайдк:: QueryStatus** .</span><span class="sxs-lookup"><span data-stu-id="f1fd6-117">Allocate memory for this structure and call the **IDelaydC::QueryStatus** method again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f1fd6-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1fd6-118">Remarks</span></span>

<span data-ttu-id="f1fd6-119">Этот метод можно вызвать в любое время после вызова [креатенппинтерфаце](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="f1fd6-119">This method can be called at any time after [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="f1fd6-120">Его можно вызвать, чтобы узнать, подключен ли НПП к сети, узнать состояние текущего захвата и проверить, ожидают ли какие-либо триггеры.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-120">It can be called to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span>

<span data-ttu-id="f1fd6-121">Перед вызовом этого метода необходимо выделить память, необходимую для структуры [NETWORKSTATUS](networkstatus.md) , и освободить эту память, когда структура больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="f1fd6-121">Before calling this method, you must allocate the memory needed for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1fd6-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f1fd6-122">Requirements</span></span>



| <span data-ttu-id="f1fd6-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f1fd6-123">Requirement</span></span> | <span data-ttu-id="f1fd6-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f1fd6-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1fd6-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1fd6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f1fd6-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f1fd6-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="f1fd6-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1fd6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f1fd6-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f1fd6-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="f1fd6-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f1fd6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1fd6-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1fd6-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="f1fd6-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f1fd6-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1fd6-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1fd6-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1fd6-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1fd6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1fd6-134">иделайдк</span><span class="sxs-lookup"><span data-stu-id="f1fd6-134">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="f1fd6-135">креатенппинтерфаце</span><span class="sxs-lookup"><span data-stu-id="f1fd6-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="f1fd6-136">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="f1fd6-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




