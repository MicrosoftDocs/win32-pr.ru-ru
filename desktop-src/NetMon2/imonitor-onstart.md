---
description: Метод OnStart является необязательным методом, который может быть реализован монитором. МКСВК вызывает этот метод, чтобы запрашивать, что монитор начинает запись.
ms.assetid: 992ee27e-aaba-4e65-989b-e3f0fbd542ea
title: 'Метод Имонитор:: OnStart (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStart
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: ca9e5e17de1d6baf2c79cc0077c5e2036a2a6246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143762"
---
# <a name="imonitoronstart-method"></a><span data-ttu-id="15be2-104">Метод Имонитор:: OnStart</span><span class="sxs-lookup"><span data-stu-id="15be2-104">IMonitor::OnStart method</span></span>

<span data-ttu-id="15be2-105">Метод **OnStart** является необязательным методом, который может быть реализован монитором.</span><span class="sxs-lookup"><span data-stu-id="15be2-105">The **OnStart** method is an optional method that can be implemented by the monitor.</span></span> <span data-ttu-id="15be2-106">МКСВК вызывает этот метод, чтобы запрашивать, что монитор начинает запись.</span><span class="sxs-lookup"><span data-stu-id="15be2-106">The MCSVC calls this method to request that the monitor start the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="15be2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15be2-107">Syntax</span></span>


```C++
HRESULT OnStart(
  [in] IUnknown *pUnkNPP
);
```



## <a name="parameters"></a><span data-ttu-id="15be2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="15be2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15be2-109">*пункнпп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="15be2-109">*pUnkNPP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15be2-110">Указатель [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) на интерфейс [ИРТК](irtc.md) .</span><span class="sxs-lookup"><span data-stu-id="15be2-110">An [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer to the [IRTC](irtc.md) interface.</span></span> <span data-ttu-id="15be2-111">Монитор может использовать этот интерфейс для получения статистики, которую можно использовать для определения того, следует ли начать запись.</span><span class="sxs-lookup"><span data-stu-id="15be2-111">The monitor can use this interface to obtain statistics that can be used to determine if the capture should be started.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15be2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15be2-112">Return value</span></span>

<span data-ttu-id="15be2-113">Если метод выполнен успешно, возвращается значение S \_ OK (то же самое, что и ошибка).</span><span class="sxs-lookup"><span data-stu-id="15be2-113">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span> <span data-ttu-id="15be2-114">Когда возвращается значение S \_ ОК, мксвк вызывает метод [ИРТК:: Start](irtc-start.md) .</span><span class="sxs-lookup"><span data-stu-id="15be2-114">When S\_OK is returned, the MCSVC calls the [IRTC::Start](irtc-start.md) method.</span></span>

<span data-ttu-id="15be2-115">Если метод завершается неудачно, возвращаемое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="15be2-115">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="15be2-116">МКСВК не запустит запись, если возвращается любой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="15be2-116">The MCSVC will not start the capture if any error code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="15be2-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15be2-117">Remarks</span></span>

<span data-ttu-id="15be2-118">МКСВК вызывает этот метод перед вызовом метода [ИРТК:: Start](irtc-start.md) НПП для запуска записи.</span><span class="sxs-lookup"><span data-stu-id="15be2-118">The MCSVC calls this method before the NPP's [IRTC::Start](irtc-start.md) method is called to start the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="15be2-119">Требования</span><span class="sxs-lookup"><span data-stu-id="15be2-119">Requirements</span></span>



| <span data-ttu-id="15be2-120">Требование</span><span class="sxs-lookup"><span data-stu-id="15be2-120">Requirement</span></span> | <span data-ttu-id="15be2-121">Значение</span><span class="sxs-lookup"><span data-stu-id="15be2-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="15be2-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15be2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="15be2-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="15be2-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="15be2-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15be2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="15be2-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="15be2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="15be2-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="15be2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="15be2-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="15be2-127"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15be2-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15be2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15be2-129">имонитор</span><span class="sxs-lookup"><span data-stu-id="15be2-129">IMonitor</span></span>](imonitor.md)
</dt> <dt>

[<span data-ttu-id="15be2-130">Поставщики сетевых пакетов</span><span class="sxs-lookup"><span data-stu-id="15be2-130">Network Packet Providers</span></span>](network-packet-providers.md)
</dt> </dl>

 

