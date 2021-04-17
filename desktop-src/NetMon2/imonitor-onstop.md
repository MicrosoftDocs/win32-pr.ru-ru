---
description: Метод OnStop должен быть реализован монитором. МСКВК вызывает этот метод, чтобы уведомить монитор о том, что запись будет остановлена.
ms.assetid: 5988bfb8-2068-42a1-a774-6f6be9828568
title: 'Метод Имонитор:: OnStop (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStop
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: a737aa5bede443b63f2074239eec17ea8a205cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673180"
---
# <a name="imonitoronstop-method"></a><span data-ttu-id="395cc-104">Метод Имонитор:: OnStop</span><span class="sxs-lookup"><span data-stu-id="395cc-104">IMonitor::OnStop method</span></span>

<span data-ttu-id="395cc-105">Метод **OnStop** должен быть реализован монитором.</span><span class="sxs-lookup"><span data-stu-id="395cc-105">The **OnStop** method must be implemented by the monitor.</span></span> <span data-ttu-id="395cc-106">МСКВК вызывает этот метод, чтобы уведомить монитор о том, что запись будет остановлена.</span><span class="sxs-lookup"><span data-stu-id="395cc-106">The MSCVC calls this method to notify the monitor that the capture will be stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="395cc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="395cc-107">Syntax</span></span>


```C++
HRESULT OnStop();
```



## <a name="parameters"></a><span data-ttu-id="395cc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="395cc-108">Parameters</span></span>

<span data-ttu-id="395cc-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="395cc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="395cc-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="395cc-110">Return value</span></span>

<span data-ttu-id="395cc-111">Если метод выполнен успешно, возвращается значение S \_ OK (то же самое, что и ошибка).</span><span class="sxs-lookup"><span data-stu-id="395cc-111">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="395cc-112">Если метод завершается неудачно, возвращаемое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="395cc-112">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="395cc-113">При возвращении кода ошибки монитор не может быть перезапущен.</span><span class="sxs-lookup"><span data-stu-id="395cc-113">When an error code is returned, the monitor cannot be restarted.</span></span>

## <a name="remarks"></a><span data-ttu-id="395cc-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="395cc-114">Remarks</span></span>

<span data-ttu-id="395cc-115">МКСВК вызывает этот метод после вызова [ИРТК:: останавливаться](irtc-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="395cc-115">The MCSVC calls this method after [IRTC::Stop](irtc-stop.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="395cc-116">Требования</span><span class="sxs-lookup"><span data-stu-id="395cc-116">Requirements</span></span>



| <span data-ttu-id="395cc-117">Требование</span><span class="sxs-lookup"><span data-stu-id="395cc-117">Requirement</span></span> | <span data-ttu-id="395cc-118">Значение</span><span class="sxs-lookup"><span data-stu-id="395cc-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="395cc-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="395cc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="395cc-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="395cc-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="395cc-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="395cc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="395cc-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="395cc-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="395cc-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="395cc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="395cc-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="395cc-124"><dt>Netmon.h</dt></span></span> </dl> |



 

 




