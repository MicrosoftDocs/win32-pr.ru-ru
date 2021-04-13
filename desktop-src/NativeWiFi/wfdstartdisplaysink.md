---
description: Выполняет необходимую инициализацию, чтобы вызывающее приложение стало приемником дисплея Miracast.
ms.assetid: D87B427B-0B7F-44BB-BC34-726FDF87CCCC
title: Функция Вфддисплайсинкстарт (Вфдсинк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStartDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423ca68364fbe7c4beb89ab3b1d9f8e8fdb891be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544234"
---
# <a name="wfddisplaysinkstart-function"></a><span data-ttu-id="5a7dc-103">Функция Вфддисплайсинкстарт</span><span class="sxs-lookup"><span data-stu-id="5a7dc-103">WFDDisplaySinkStart function</span></span>

<span data-ttu-id="5a7dc-104">Выполняет необходимую инициализацию, чтобы вызывающее приложение стало приемником дисплея Miracast.</span><span class="sxs-lookup"><span data-stu-id="5a7dc-104">Performs the necessary initialization to allow the calling app to become a Miracast display sink.</span></span> <span data-ttu-id="5a7dc-105">Приложение должно вызывать его один раз при запуске.</span><span class="sxs-lookup"><span data-stu-id="5a7dc-105">Your app should call this once on startup.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a7dc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a7dc-106">Syntax</span></span>


```C++
DWORD WINAPI WFDStartDisplaySink(
  _In_     USHORT                                 uDeviceCategory,
  _In_     USHORT                                 uSubCategory,
  _In_opt_ PVOID                                  pCallbackContext,
  _In_     WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK *pfnCallback
);
```



## <a name="parameters"></a><span data-ttu-id="5a7dc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a7dc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a7dc-108">*удевицекатегори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a7dc-108">*uDeviceCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a7dc-109">Категория устройства.</span><span class="sxs-lookup"><span data-stu-id="5a7dc-109">The device category.</span></span>

</dd> <dt>

<span data-ttu-id="5a7dc-110">*усубкатегори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a7dc-110">*uSubCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a7dc-111">Подкатегория устройства.</span><span class="sxs-lookup"><span data-stu-id="5a7dc-111">The device subcategory.</span></span>

</dd> <dt>

<span data-ttu-id="5a7dc-112">*пкаллбаккконтекст* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5a7dc-112">*pCallbackContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5a7dc-113">Необязательный указатель контекста, который передается функции обратного вызова, указанной в параметре *пфнкаллбакк* .</span><span class="sxs-lookup"><span data-stu-id="5a7dc-113">An optional context pointer which is passed to the callback function specified in the *pfnCallback* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5a7dc-114">*пфнкаллбакк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a7dc-114">*pfnCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a7dc-115">Указатель на функцию обратного вызова, вызываемую при наличии уведомления для приложения.</span><span class="sxs-lookup"><span data-stu-id="5a7dc-115">A pointer to the callback function to be called whenever there is a notification for the app.</span></span> <span data-ttu-id="5a7dc-116">Уведомления, которые могут быть отправлены, описаны в [**\_ \_ \_ \_ обратном вызове уведомлений о приемнике для монитора WFD**](wfd-display-sink-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="5a7dc-116">Notifications that can be sent are described in [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a7dc-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a7dc-117">Return value</span></span>

<span data-ttu-id="5a7dc-118">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5a7dc-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="5a7dc-119">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="5a7dc-119">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="5a7dc-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5a7dc-120">Return code</span></span>                                                                                          | <span data-ttu-id="5a7dc-121">Описание</span><span class="sxs-lookup"><span data-stu-id="5a7dc-121">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="5a7dc-122"><dt>**Ошибка \_ не \_ поддерживается**</dt></span><span class="sxs-lookup"><span data-stu-id="5a7dc-122"><dt>**ERROR\_NOT\_SUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="5a7dc-123">Приемник дисплея не поддерживается на этом оборудовании.</span><span class="sxs-lookup"><span data-stu-id="5a7dc-123">The display sink is not supported on this hardware.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5a7dc-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a7dc-124">Remarks</span></span>

<span data-ttu-id="5a7dc-125">Эта функция выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="5a7dc-125">This function performs the following tasks:</span></span>

-   <span data-ttu-id="5a7dc-126">Делает компьютер обнаруживаемым</span><span class="sxs-lookup"><span data-stu-id="5a7dc-126">Makes the PC discoverable</span></span>
-   <span data-ttu-id="5a7dc-127">Задает сведения о ОДНОРАНГОВОм устройстве, отражающие указанную категорию и подкатегорию</span><span class="sxs-lookup"><span data-stu-id="5a7dc-127">Sets the P2P device info to reflect the category and sub category specified</span></span>
-   <span data-ttu-id="5a7dc-128">Устанавливает наборы устройств Miracast для всех Wi-Fi прямых кадров с типом устройства в качестве приемника.</span><span class="sxs-lookup"><span data-stu-id="5a7dc-128">Sets the Miracast IEs on all Wi-Fi Direct frames with the device type as the sink</span></span>
-   <span data-ttu-id="5a7dc-129">Регистрирует указанный обратный вызов для вызова при наличии входящего подключения.</span><span class="sxs-lookup"><span data-stu-id="5a7dc-129">Registers the specified callback to be invoked whenever there is an incoming connection</span></span>

## <a name="requirements"></a><span data-ttu-id="5a7dc-130">Требования</span><span class="sxs-lookup"><span data-stu-id="5a7dc-130">Requirements</span></span>



| <span data-ttu-id="5a7dc-131">Требование</span><span class="sxs-lookup"><span data-stu-id="5a7dc-131">Requirement</span></span> | <span data-ttu-id="5a7dc-132">Значение</span><span class="sxs-lookup"><span data-stu-id="5a7dc-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a7dc-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a7dc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5a7dc-134">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5a7dc-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5a7dc-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a7dc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5a7dc-136">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a7dc-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5a7dc-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="5a7dc-137">End of client support</span></span><br/>    | <span data-ttu-id="5a7dc-138">Windows 10</span><span class="sxs-lookup"><span data-stu-id="5a7dc-138">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="5a7dc-139">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="5a7dc-139">End of server support</span></span><br/>    | <span data-ttu-id="5a7dc-140">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5a7dc-140">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="5a7dc-141">Header</span><span class="sxs-lookup"><span data-stu-id="5a7dc-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a7dc-142"><dt>Вфдсинк. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a7dc-142"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="5a7dc-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5a7dc-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="5a7dc-144"><dt>Вифидисплай. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a7dc-144"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="5a7dc-145">DLL</span><span class="sxs-lookup"><span data-stu-id="5a7dc-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a7dc-146"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a7dc-146"><dt>Wifidisplay.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a7dc-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a7dc-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a7dc-148">**\_ \_ \_ обратный вызов уведомления приемника для дисплея WFD \_**</span><span class="sxs-lookup"><span data-stu-id="5a7dc-148">**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**</span></span>](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




