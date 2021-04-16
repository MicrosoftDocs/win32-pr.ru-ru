---
description: 'Метод IWiaDevMgr2:: Регистеревенткаллбаккклсид регистрирует приложение для получения событий, даже если приложение не работает.'
ms.assetid: e0d421a7-ef49-4e27-9661-c358ac819712
title: 'Метод IWiaDevMgr2:: Регистеревенткаллбаккклсид (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackCLSID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 63e69d12d47f90ba40f5cc785d8b864c40158774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542791"
---
# <a name="iwiadevmgr2registereventcallbackclsid-method"></a><span data-ttu-id="263de-103">Метод IWiaDevMgr2:: Регистеревенткаллбаккклсид</span><span class="sxs-lookup"><span data-stu-id="263de-103">IWiaDevMgr2::RegisterEventCallbackCLSID method</span></span>

<span data-ttu-id="263de-104">Метод **IWiaDevMgr2:: регистеревенткаллбаккклсид** регистрирует приложение для получения событий, даже если приложение не работает.</span><span class="sxs-lookup"><span data-stu-id="263de-104">The **IWiaDevMgr2::RegisterEventCallbackCLSID** method registers an application to receive events even if the application is not running.</span></span>

## <a name="syntax"></a><span data-ttu-id="263de-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="263de-105">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackCLSID(
  [in]               LONG lFlags,
  [in]               BSTR bstrDeviceID,
  [in]         const GUID *pEventGUID,
  [in, unique] const GUID *pClsID,
  [in]               BSTR bstrName,
  [in]               BSTR bstrDescription,
  [in]               BSTR bstrIcon
);
```



## <a name="parameters"></a><span data-ttu-id="263de-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="263de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="263de-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="263de-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="263de-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="263de-108">Type: **LONG**</span></span>

<span data-ttu-id="263de-109">Задает флаги регистрации.</span><span class="sxs-lookup"><span data-stu-id="263de-109">Specifies registration flags.</span></span> <span data-ttu-id="263de-110">Можно задать следующие значения:</span><span class="sxs-lookup"><span data-stu-id="263de-110">Can be set to the following values:</span></span>



| <span data-ttu-id="263de-111">Флаг регистрации</span><span class="sxs-lookup"><span data-stu-id="263de-111">Registration Flag</span></span>                | <span data-ttu-id="263de-112">Значение</span><span class="sxs-lookup"><span data-stu-id="263de-112">Meaning</span></span>                                           |
|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="263de-113">\_ \_ обратный вызов события регистрации WIA \_</span><span class="sxs-lookup"><span data-stu-id="263de-113">WIA\_REGISTER\_EVENT\_CALLBACK</span></span>   | <span data-ttu-id="263de-114">Зарегистрируйтесь для события.</span><span class="sxs-lookup"><span data-stu-id="263de-114">Register for the event.</span></span>                           |
| <span data-ttu-id="263de-115">\_обратный вызов для отмены регистрации \_ события WIA \_</span><span class="sxs-lookup"><span data-stu-id="263de-115">WIA\_UNREGISTER\_EVENT\_CALLBACK</span></span> | <span data-ttu-id="263de-116">Удалите регистрацию для события.</span><span class="sxs-lookup"><span data-stu-id="263de-116">Delete the registration for the event.</span></span>            |
| <span data-ttu-id="263de-117">\_ \_ обработчик по умолчанию для WIA Set \_</span><span class="sxs-lookup"><span data-stu-id="263de-117">WIA\_SET\_DEFAULT\_HANDLER</span></span>       | <span data-ttu-id="263de-118">Задайте приложение в качестве обработчика событий по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="263de-118">Set the application as the default event handler.</span></span> |



 

</dd> <dt>

<span data-ttu-id="263de-119">*бстрдевицеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="263de-119">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="263de-120">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="263de-120">Type: **BSTR**</span></span>

<span data-ttu-id="263de-121">Указывает идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="263de-121">Specifies a device identifier.</span></span> <span data-ttu-id="263de-122">Передайте **значение NULL** , чтобы зарегистрировать событие на всех устройствах WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="263de-122">Pass **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="263de-123">*певентгуид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="263de-123">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="263de-124">Тип: \**константа \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="263de-124">Type: \**const GUID\** _</span></span>

<span data-ttu-id="263de-125">Указывает событие, для которого регистрируется приложение.</span><span class="sxs-lookup"><span data-stu-id="263de-125">Specifies the event that the application is registering for.</span></span> <span data-ttu-id="263de-126">Список стандартных событий см. в разделе [идентификаторы событий WIA](-wia-wia-event-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="263de-126">For a list of standard events, see [WIA Event Identifiers](-wia-wia-event-identifiers.md).</span></span>

</dd> <dt>

<span data-ttu-id="263de-127">_pClsID \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="263de-127">_pClsID\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="263de-128">Тип: \**константа \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="263de-128">Type: \**const GUID\** _</span></span>

<span data-ttu-id="263de-129">Указатель на идентификатор класса приложения (_ \* CLSID \* \*).</span><span class="sxs-lookup"><span data-stu-id="263de-129">Pointer to the application class ID (_\*CLSID\*\*).</span></span> <span data-ttu-id="263de-130">Система времени выполнения WIA 2,0 использует **CLSID** приложения для запуска приложения при возникновении события, для которого оно зарегистрировано.</span><span class="sxs-lookup"><span data-stu-id="263de-130">The WIA 2.0 run-time system uses the application **CLSID** to start the application when an event occurs that it is registered for.</span></span>

</dd> <dt>

<span data-ttu-id="263de-131">*bstrName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="263de-131">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="263de-132">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="263de-132">Type: **BSTR**</span></span>

<span data-ttu-id="263de-133">Указывает имя приложения, которое регистрируется для события.</span><span class="sxs-lookup"><span data-stu-id="263de-133">Specifies the name of the application that registers for the event.</span></span>

</dd> <dt>

<span data-ttu-id="263de-134">*bstrDescription* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="263de-134">*bstrDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="263de-135">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="263de-135">Type: **BSTR**</span></span>

<span data-ttu-id="263de-136">Задает текстовое описание приложения, которое регистрируется для события.</span><span class="sxs-lookup"><span data-stu-id="263de-136">Specifies a text description of the application that registers for the event.</span></span>

</dd> <dt>

<span data-ttu-id="263de-137">*бстрикон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="263de-137">*bstrIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="263de-138">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="263de-138">Type: **BSTR**</span></span>

<span data-ttu-id="263de-139">Указывает имя файла изображения, используемого для значка приложения, которое регистрируется для события.</span><span class="sxs-lookup"><span data-stu-id="263de-139">Specifies the name of an image file to use for the icon for the application that registers for the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="263de-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="263de-140">Return value</span></span>

<span data-ttu-id="263de-141">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="263de-141">Type: **HRESULT**</span></span>

<span data-ttu-id="263de-142">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="263de-142">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="263de-143">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="263de-143">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="263de-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="263de-144">Remarks</span></span>

<span data-ttu-id="263de-145">Приложения WIA 2,0 используют этот метод для регистрации для получения событий аппаратного устройства.</span><span class="sxs-lookup"><span data-stu-id="263de-145">WIA 2.0 applications use this method to register to receive hardware device events.</span></span> <span data-ttu-id="263de-146">После вызова **IWiaDevMgr2:: регистеревенткаллбаккклсид** приложение регистрируется для получения событий устройства WIA 2,0, даже если оно не работает.</span><span class="sxs-lookup"><span data-stu-id="263de-146">After **IWiaDevMgr2::RegisterEventCallbackCLSID** is called, the application is registered to receive WIA 2.0 device events even if it is not running.</span></span>

<span data-ttu-id="263de-147">При возникновении события система WIA 2,0 определяет, какое приложение зарегистрировано для получения события.</span><span class="sxs-lookup"><span data-stu-id="263de-147">When the event occurs, the WIA 2.0 system determines which application is registered to receive the event.</span></span> <span data-ttu-id="263de-148">Он использует функцию [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) и CLSID, указанные в параметре *пклсид* , для создания экземпляра приложения, а затем вызывает метод [**имажеевенткаллбакк**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) для передачи сведений о событии в приложение.</span><span class="sxs-lookup"><span data-stu-id="263de-148">It uses the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function and the CLSID specified in the *pClsID* parameter to create an instance of the application, and then calls the [**ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) method to transmit the event information to the application.</span></span>

<span data-ttu-id="263de-149">Приложение может вызвать метод [**енумрегистеревентинфо**](-wia-iwiaitem2-enumregistereventinfo.md) для перечисления сведений о регистрации событий.</span><span class="sxs-lookup"><span data-stu-id="263de-149">An application can invoke the [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) method to enumerate event registration information.</span></span>

<span data-ttu-id="263de-150">Если приложение не является зарегистрированным компонентом модели COM и несовместимо с архитектурой WIA 2,0, используйте метод [**IWiaDevMgr2:: регистеревенткаллбаккпрограм**](-wia-iwiadevmgr2-registereventcallbackprogram.md) для регистрации приложения для событий устройства.</span><span class="sxs-lookup"><span data-stu-id="263de-150">If the application is not a registered Component Object Model (COM) component and is not compatible with the WIA 2.0 architecture, use the [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) method to register an application for device events.</span></span>

> [!Note]  
> <span data-ttu-id="263de-151">В многопоточном приложении нет никакой гарантии, что обратный вызов уведомления о событии возвращается в том же потоке, который зарегистрировал обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="263de-151">In a multi-threaded application, there is no guarantee that the event notification callback is returned on the same thread that registered the callback.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="263de-152">Требования</span><span class="sxs-lookup"><span data-stu-id="263de-152">Requirements</span></span>



| <span data-ttu-id="263de-153">Требование</span><span class="sxs-lookup"><span data-stu-id="263de-153">Requirement</span></span> | <span data-ttu-id="263de-154">Значение</span><span class="sxs-lookup"><span data-stu-id="263de-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="263de-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="263de-155">Minimum supported client</span></span><br/> | <span data-ttu-id="263de-156">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="263de-156">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="263de-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="263de-157">Minimum supported server</span></span><br/> | <span data-ttu-id="263de-158">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="263de-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="263de-159">Header</span><span class="sxs-lookup"><span data-stu-id="263de-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="263de-160"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="263de-160"><dt>Wia.h</dt></span></span> </dl> |



 

 
