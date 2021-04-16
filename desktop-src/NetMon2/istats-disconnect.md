---
description: Отключает НПП от сети.
ms.assetid: 01ff8fc2-aa27-4df8-a499-c7b00c1fa2e8
title: Истатс::D метода соединения (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a5fa56c05036380b5dba42089979b43d776a4b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650996"
---
# <a name="istatsdisconnect-method"></a><span data-ttu-id="443c2-103">Истатс::D метода соединения</span><span class="sxs-lookup"><span data-stu-id="443c2-103">IStats::Disconnect method</span></span>

<span data-ttu-id="443c2-104">Метод **Disconnect** отключает НПП от сети.</span><span class="sxs-lookup"><span data-stu-id="443c2-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="443c2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="443c2-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="443c2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="443c2-106">Parameters</span></span>

<span data-ttu-id="443c2-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="443c2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="443c2-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="443c2-108">Return value</span></span>

<span data-ttu-id="443c2-109">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="443c2-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="443c2-110">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="443c2-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="443c2-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="443c2-111">Return code</span></span>                                                                                            | <span data-ttu-id="443c2-112">Описание</span><span class="sxs-lookup"><span data-stu-id="443c2-112">Description</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="443c2-113"><dt>**НМЕРР \_ запись**</dt></span><span class="sxs-lookup"><span data-stu-id="443c2-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>        | <span data-ttu-id="443c2-114">НПП в настоящее время фиксирует данные.</span><span class="sxs-lookup"><span data-stu-id="443c2-114">The NPP is currently capturing data.</span></span> <span data-ttu-id="443c2-115">Невозможно отключиться от сети, пока выполняется сбор данных.</span><span class="sxs-lookup"><span data-stu-id="443c2-115">You cannot disconnect from the network while a data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="443c2-116"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="443c2-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="443c2-117">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="443c2-117">The NPP is not connected to the network.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="443c2-118"><dt>**НМЕРР \_ не \_ \_ только статистика**</dt></span><span class="sxs-lookup"><span data-stu-id="443c2-118"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="443c2-119">НПП подключается к сети, но не с методом [**истатс:: Connect**](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="443c2-119">The NPP is connected to the network, but not with the [**IStats::Connect**](istats-connect.md) method.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="443c2-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="443c2-120">Remarks</span></span>

<span data-ttu-id="443c2-121">Этот метод не может быть вызван, когда НПП захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="443c2-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="443c2-122">Сначала вызовите метод **истатс::D соединения** , а затем вызовите [**Истатс:: останавливаться**](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="443c2-122">Call the **IStats::Disconnect** method first and then call [**IStats::Stop**](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="443c2-123">Требования</span><span class="sxs-lookup"><span data-stu-id="443c2-123">Requirements</span></span>



| <span data-ttu-id="443c2-124">Требование</span><span class="sxs-lookup"><span data-stu-id="443c2-124">Requirement</span></span> | <span data-ttu-id="443c2-125">Значение</span><span class="sxs-lookup"><span data-stu-id="443c2-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="443c2-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="443c2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="443c2-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="443c2-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="443c2-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="443c2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="443c2-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="443c2-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="443c2-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="443c2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="443c2-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="443c2-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="443c2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="443c2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="443c2-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="443c2-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="443c2-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="443c2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="443c2-135">**истатс**</span><span class="sxs-lookup"><span data-stu-id="443c2-135">**IStats**</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="443c2-136">**Истатс:: Connect**</span><span class="sxs-lookup"><span data-stu-id="443c2-136">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="443c2-137">**Истатс:: останавливаться**</span><span class="sxs-lookup"><span data-stu-id="443c2-137">**IStats::Stop**</span></span>](istats-stop.md)
</dt> </dl>

 

 




