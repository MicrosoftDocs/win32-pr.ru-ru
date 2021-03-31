---
description: Регистрирует выполняющееся приложение для уведомления о событии получения образа Windows (WIA) 2,0.
ms.assetid: 978dcd41-d63b-421d-b7e1-8e9368b36180
title: 'Метод IWiaDevMgr2:: Регистеревенткаллбаккинтерфаце (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackInterface
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7cd3a7e00cff56bc5d91bfc843ab79fe71aa1123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264528"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a><span data-ttu-id="814ec-103">Метод IWiaDevMgr2:: Регистеревенткаллбаккинтерфаце</span><span class="sxs-lookup"><span data-stu-id="814ec-103">IWiaDevMgr2::RegisterEventCallbackInterface method</span></span>

<span data-ttu-id="814ec-104">Регистрирует выполняющееся приложение для уведомления о событии получения образа Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="814ec-104">Registers a running application for Windows Image Acquisition (WIA) 2.0 event notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="814ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="814ec-105">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackInterface(
  [in]        LONG              lFlags,
  [in]        BSTR              bstrDeviceID,
  [in]  const GUID              *pEventGUID,
  [in]        IWiaEventCallback *pIWiaEventCallback,
  [out]       IUnknown          **pEventObject
);
```



## <a name="parameters"></a><span data-ttu-id="814ec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="814ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="814ec-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="814ec-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="814ec-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="814ec-108">Type: **LONG**</span></span>

<span data-ttu-id="814ec-109">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="814ec-109">Currently unused.</span></span> <span data-ttu-id="814ec-110">Значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="814ec-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="814ec-111">*бстрдевицеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="814ec-111">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="814ec-112">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="814ec-112">Type: **BSTR**</span></span>

<span data-ttu-id="814ec-113">Указывает уникальный идентификатор устройства WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="814ec-113">Specifies the unique identifier of a WIA 2.0 device.</span></span> <span data-ttu-id="814ec-114">Присвойте этому параметру **значение NULL** , чтобы зарегистрировать событие на всех устройствах WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="814ec-114">Set this parameter to **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="814ec-115">*певентгуид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="814ec-115">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="814ec-116">Тип: \**константа \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="814ec-116">Type: \**const GUID\** _</span></span>

<span data-ttu-id="814ec-117">Указывает указатель на идентификатор события, для которого регистрируется приложение.</span><span class="sxs-lookup"><span data-stu-id="814ec-117">Specifies a pointer to the event identifier that the application is registering for.</span></span> <span data-ttu-id="814ec-118">См. раздел [идентификаторы событий WIA](-wia-wia-event-identifiers.md) для стандартных идентификаторов событий.</span><span class="sxs-lookup"><span data-stu-id="814ec-118">See [WIA Event Identifiers](-wia-wia-event-identifiers.md) for standard event identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="814ec-119">_pIWiaEventCallback \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="814ec-119">_pIWiaEventCallback\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="814ec-120">Тип: \**[**ивиаевенткаллбакк**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) \** _</span><span class="sxs-lookup"><span data-stu-id="814ec-120">Type: \**[**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback)\** _</span></span>

<span data-ttu-id="814ec-121">Указывает указатель на интерфейс [_ *ивиаевенткаллбакк* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) , который WIA 2,0 использует для отправки уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="814ec-121">Specifies a pointer to the [_ *IWiaEventCallback*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) interface that the WIA 2.0 uses to send event notification.</span></span>

</dd> <dt>

<span data-ttu-id="814ec-122">*певентобжект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="814ec-122">*pEventObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="814ec-123">Тип: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="814ec-123">Type: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="814ec-124">Получает адрес указателя на интерфейс [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="814ec-124">Receives the address of a pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="814ec-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="814ec-125">Return value</span></span>

<span data-ttu-id="814ec-126">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="814ec-126">Type: **HRESULT**</span></span>

<span data-ttu-id="814ec-127">Возвращает стандартные коды ошибок COM или следующие.</span><span class="sxs-lookup"><span data-stu-id="814ec-127">Returns the standard COM error codes or the following.</span></span>



| <span data-ttu-id="814ec-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="814ec-128">Return code</span></span>                                                                               | <span data-ttu-id="814ec-129">Описание</span><span class="sxs-lookup"><span data-stu-id="814ec-129">Description</span></span>                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="814ec-130"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="814ec-130"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="814ec-131">Интерфейс [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) не может быть возвращен.</span><span class="sxs-lookup"><span data-stu-id="814ec-131">The [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface cannot be returned.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="814ec-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="814ec-132">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="814ec-133">Использование методов [**ивиадевмгр:: регистеревенткаллбаккинтерфаце**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2:: регистеревенткаллбаккинтерфаце** и [**девицеманажер. RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) из того же процесса после перезапуска службы изображений может привести к нарушению прав доступа, если функции использовались до остановки службы.</span><span class="sxs-lookup"><span data-stu-id="814ec-133">Using the [**IWiaDevMgr::RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2::RegisterEventCallbackInterface**, and [**DeviceManager.RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) methods from the same process after the Still Image Service is restarted may cause an access violation, if the functions were used before the service was stopped.</span></span>

 

<span data-ttu-id="814ec-134">Когда приложения WIA 2,0 начинают выполняться, они используют этот метод для регистрации для получения событий устройства.</span><span class="sxs-lookup"><span data-stu-id="814ec-134">When WIA 2.0 applications begin executing, they use this method to register to receive hardware device events.</span></span> <span data-ttu-id="814ec-135">Это предотвращает перезапуск приложения при возникновении другого события, для которого оно зарегистрировано.</span><span class="sxs-lookup"><span data-stu-id="814ec-135">This prevents the application from being restarted when another event for which it is registered occurs.</span></span> <span data-ttu-id="814ec-136">После того как приложение вызывает **IWiaDevMgr2:: регистеревенткаллбаккинтерфаце** , чтобы зарегистрироваться для получения событий WIA 2,0 с устройства, зарегистрированные события направляются в программу WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="814ec-136">Once an application calls **IWiaDevMgr2::RegisterEventCallbackInterface** to register itself to receive WIA 2.0 events from a device, the registered events are routed to the program by WIA 2.0.</span></span>

<span data-ttu-id="814ec-137">Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *певентобжект* .</span><span class="sxs-lookup"><span data-stu-id="814ec-137">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *pEventObject* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="814ec-138">В многопоточном приложении обратный вызов уведомления о событии может находиться в другом потоке из того, который зарегистрировал обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="814ec-138">In a multithreaded application, the event notification callback may come in on a different thread from the one that registered the callback.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="814ec-139">Требования</span><span class="sxs-lookup"><span data-stu-id="814ec-139">Requirements</span></span>



| <span data-ttu-id="814ec-140">Требование</span><span class="sxs-lookup"><span data-stu-id="814ec-140">Requirement</span></span> | <span data-ttu-id="814ec-141">Значение</span><span class="sxs-lookup"><span data-stu-id="814ec-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="814ec-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="814ec-142">Minimum supported client</span></span><br/> | <span data-ttu-id="814ec-143">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="814ec-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="814ec-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="814ec-144">Minimum supported server</span></span><br/> | <span data-ttu-id="814ec-145">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="814ec-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="814ec-146">Header</span><span class="sxs-lookup"><span data-stu-id="814ec-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="814ec-147"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="814ec-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="814ec-148">IDL</span><span class="sxs-lookup"><span data-stu-id="814ec-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="814ec-149"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="814ec-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 
