---
title: Метод Ивмвиртуалпцевентс Оневентлогжед (Впккоминтерфацес. h)
description: Получает уведомление о том, что Windows Virtual PC регистрирует событие.
ms.assetid: 89439e8e-e9bf-409e-a129-525b9feb8fdd
keywords:
- Метод Оневентлогжед Virtual PC
- Метод Оневентлогжед Virtual PC, интерфейс Ивмвиртуалпцевентс
- Ивмвиртуалпцевентс интерфейс Virtual PC, метод Оневентлогжед
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnEventLogged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196d480383f488c9c0885e95857c8d1a053d5887
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534391"
---
# <a name="ivmvirtualpceventsoneventlogged-method"></a><span data-ttu-id="42d0b-106">Метод Ивмвиртуалпцевентс:: Оневентлогжед</span><span class="sxs-lookup"><span data-stu-id="42d0b-106">IVMVirtualPCEvents::OnEventLogged method</span></span>

<span data-ttu-id="42d0b-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="42d0b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="42d0b-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="42d0b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="42d0b-109">Получает уведомление о том, что Windows Virtual PC регистрирует событие.</span><span class="sxs-lookup"><span data-stu-id="42d0b-109">Receives notification that Windows Virtual PC logs an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="42d0b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42d0b-110">Syntax</span></span>


```C++
HRESULT OnEventLogged(
  [in] long logMessageID
);
```



## <a name="parameters"></a><span data-ttu-id="42d0b-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="42d0b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42d0b-112">*логмессажеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42d0b-112">*logMessageID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42d0b-113">Идентификатор сообщения журнала событий, который был занесен в журнал.</span><span class="sxs-lookup"><span data-stu-id="42d0b-113">The message identifier of the event log message that was logged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42d0b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42d0b-114">Return value</span></span>

<span data-ttu-id="42d0b-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="42d0b-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="42d0b-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="42d0b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="42d0b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42d0b-117">Remarks</span></span>

<span data-ttu-id="42d0b-118">Этот метод вызывается, когда Windows Virtual PC регистрирует сообщение в журнале событий Windows.</span><span class="sxs-lookup"><span data-stu-id="42d0b-118">This method is called when Windows Virtual PC logs a message to the Windows event log.</span></span> <span data-ttu-id="42d0b-119">Клиентская программа должна реализовать этот метод интерфейса для получения уведомления о событии **вмвиртуалпцевент \_ евентлогжед** , исходящем от [**ивмвиртуалпк**](ivmvirtualpc.md).</span><span class="sxs-lookup"><span data-stu-id="42d0b-119">The client program must implement this interface method to receive notification of the **vmVirtualPCEvent\_EventLogged** event originating from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42d0b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="42d0b-120">Requirements</span></span>



| <span data-ttu-id="42d0b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="42d0b-121">Requirement</span></span> | <span data-ttu-id="42d0b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="42d0b-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="42d0b-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42d0b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="42d0b-124">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="42d0b-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="42d0b-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42d0b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="42d0b-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="42d0b-126">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="42d0b-127">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="42d0b-127">End of client support</span></span><br/>    | <span data-ttu-id="42d0b-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="42d0b-128">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="42d0b-129">Продукт</span><span class="sxs-lookup"><span data-stu-id="42d0b-129">Product</span></span><br/>                  | <span data-ttu-id="42d0b-130">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="42d0b-130">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="42d0b-131">Header</span><span class="sxs-lookup"><span data-stu-id="42d0b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="42d0b-132"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="42d0b-132"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="42d0b-133">IID</span><span class="sxs-lookup"><span data-stu-id="42d0b-133">IID</span></span><br/>                      | <span data-ttu-id="42d0b-134">ДИИД \_ ивмвиртуалпцевентс определяется как efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span><span class="sxs-lookup"><span data-stu-id="42d0b-134">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="42d0b-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42d0b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42d0b-136">**ивмвиртуалпцевентс**</span><span class="sxs-lookup"><span data-stu-id="42d0b-136">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

