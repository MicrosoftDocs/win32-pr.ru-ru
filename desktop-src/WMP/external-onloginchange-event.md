---
title: Внешнее событие Онлогинчанже
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | Внешнее событие Онлогинчанже
ms.assetid: 096794d5-977a-414f-8a98-b7998674c268
keywords:
- Проигрыватель Windows Media для события external. Онлогинчанже
topic_type:
- apiref
api_name:
- External.OnLoginChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b7d54da86ffdde896a44580567b0cd381725d5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694496"
---
# <a name="externalonloginchange-event"></a><span data-ttu-id="7e77d-105">Внешнее событие Онлогинчанже</span><span class="sxs-lookup"><span data-stu-id="7e77d-105">External.OnLoginChange Event</span></span>

> [!Note]  
> <span data-ttu-id="7e77d-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="7e77d-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="7e77d-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7e77d-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="7e77d-108">Событие **онлогинчанже** возникает при изменении состояния входа пользователя или при сбое попытки входа.</span><span class="sxs-lookup"><span data-stu-id="7e77d-108">The **OnLoginChange** event occurs when the user's log-in status changes or when an attempt to log in fails.</span></span>

``` syntax
window.external.OnLoginChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="7e77d-109">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="7e77d-109">Possible Values</span></span>

<span data-ttu-id="7e77d-110">Это свойство только для записи, которое указывает имя функции в скрипте, которое вызывает проигрыватель Windows Media при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="7e77d-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="7e77d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e77d-111">Parameters</span></span>

<span data-ttu-id="7e77d-112">Функция, обрабатывающая это событие, не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7e77d-112">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e77d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e77d-113">Remarks</span></span>

<span data-ttu-id="7e77d-114">Это событие возникает каждый раз, когда подключаемый модуль интернет-магазина вызывает [ивмпконтентпартнеркаллбакк:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), передав вмпкнлогинстатечанже в параметре *типа* .</span><span class="sxs-lookup"><span data-stu-id="7e77d-114">This event occurs every time the online store's plug-in calls [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="7e77d-115">Иногда подключаемый модуль выполняет этот вызов для уведомления проигрывателя Windows Media о том, что произошло изменение в состоянии входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="7e77d-115">Sometimes the plug-in makes this call to notify Windows Media Player that there was a change in the user's log-in state.</span></span> <span data-ttu-id="7e77d-116">В других случаях подключаемый модуль выполняет этот вызов для уведомления проигрывателя о том, что попытка входа окончилась неудачей.</span><span class="sxs-lookup"><span data-stu-id="7e77d-116">Other times, the plug-in makes this call to notify the Player that an attempt to log in failed.</span></span> <span data-ttu-id="7e77d-117">Параметр *пконтекст* метода **Notify** указывает, предназначено ли уведомление для изменения состояния входа в систему или для неудачной попытки входа в систему.</span><span class="sxs-lookup"><span data-stu-id="7e77d-117">The *pContext* parameter of the **Notify** method specifies whether the notification is for a change of log-in state or for a failed log-in attempt.</span></span>

<span data-ttu-id="7e77d-118">Поскольку каждый вызов `Notify(wmpcnLoginStateChange, ...)` заставляет проигрыватель Windows Media вызывать событие **онлогинчанже** , обработчик событий **онлогинчанже** вызывается иногда в результате изменения состояния входа в систему и иногда в результате неудачной попытки входа в систему.</span><span class="sxs-lookup"><span data-stu-id="7e77d-118">Because every call to `Notify(wmpcnLoginStateChange, ...)` causes Windows Media Player to raise the **OnLoginChange** event, the **OnLoginChange** event handler is called sometimes as the result of a change in log-in state and sometimes as the result of a failed log-in attempt.</span></span> <span data-ttu-id="7e77d-119">Чтобы определить текущее состояние входа пользователя, обработчик событий **онлогинчанже** должен вызвать [External. усерлогжедин](external-userloggedin.md).</span><span class="sxs-lookup"><span data-stu-id="7e77d-119">To determine the user's current log-in state, the **OnLoginChange** event handler must call [External.userLoggedIn](external-userloggedin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e77d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7e77d-120">Requirements</span></span>



| <span data-ttu-id="7e77d-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7e77d-121">Requirement</span></span> | <span data-ttu-id="7e77d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7e77d-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7e77d-123">Версия</span><span class="sxs-lookup"><span data-stu-id="7e77d-123">Version</span></span><br/> | <span data-ttu-id="7e77d-124">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="7e77d-124">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="7e77d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7e77d-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="7e77d-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e77d-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e77d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e77d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e77d-128">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="7e77d-128">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="7e77d-129">**External. Аттемптлогин**</span><span class="sxs-lookup"><span data-stu-id="7e77d-129">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="7e77d-130">**External. Усерлогжедин**</span><span class="sxs-lookup"><span data-stu-id="7e77d-130">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





