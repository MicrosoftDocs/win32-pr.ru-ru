---
title: Обновление лицензий
description: Обновление лицензий
ms.assetid: b298badf-efcf-423c-8cc7-c3f50ab288a0
keywords:
- Интернет-магазины проигрывателя Windows Media, обновление лицензий
- Интернет-магазины, обновление лицензий
- Тип 1 Интернет-магазины, обновление лицензий
- Интернет-магазины проигрывателя Windows Media, обновление лицензий
- Интернет-магазины, обновление лицензий
- Тип 1 Интернет-магазины, обновление лицензий
- Обновление лицензий
- лицензии, обновление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154959b01c93719184e310b60dffaa91fe2dcfa0
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336327"
---
# <a name="updating-licenses"></a><span data-ttu-id="15ade-111">Обновление лицензий</span><span class="sxs-lookup"><span data-stu-id="15ade-111">Updating Licenses</span></span>

<span data-ttu-id="15ade-112">Интернет-магазины могут доставлять содержимое, лицензированное на определенный период времени или до определенной даты.</span><span class="sxs-lookup"><span data-stu-id="15ade-112">Online stores can deliver content that is licensed for a specific period of time or until a certain date.</span></span> <span data-ttu-id="15ade-113">Это будет обычным для музыкального содержимого, доставляемого в рамках соглашения об обслуживании подписки.</span><span class="sxs-lookup"><span data-stu-id="15ade-113">This would be normal for music content delivered as part of a subscription service agreement.</span></span> <span data-ttu-id="15ade-114">В этом случае Интернет-магазину необходимо иметь возможность обновить эти лицензии до истечения срока их действия, предполагая, что пользователь оплачивает продление своей подписки.</span><span class="sxs-lookup"><span data-stu-id="15ade-114">In this case, the online store needs an opportunity to update these licenses before they expire, assuming, of course, that the user has paid to renew his or her subscription.</span></span> <span data-ttu-id="15ade-115">(Если пользователь не обновил подписку, лицензии можно просто оставить с истекшим сроком действия.)</span><span class="sxs-lookup"><span data-stu-id="15ade-115">(If the user has not renewed the subscription, the licenses can simply be left to expire.)</span></span>

<span data-ttu-id="15ade-116">Проигрыватель Windows Media отправляет запрос к подключаемому модулю партнера по содержимому о том, сколько предварительных предупреждений должен предоставить игрок о лицензии, срок действия которой скоро истечет.</span><span class="sxs-lookup"><span data-stu-id="15ade-116">Windows Media Player queries the content partner plug-in about how much advance warning the Player should provide about a license that is about to expire.</span></span> <span data-ttu-id="15ade-117">Для этого вызывается метод [ивмпконтентпартнер:: жетконтентпартнеринфо](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), передающий константу g \_ сзконтентпартнеринфо \_ лиценсерефрешадванцеварнинг через параметр *bstrInfoName* .</span><span class="sxs-lookup"><span data-stu-id="15ade-117">It does this by calling [IWMPContentPartner::GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), passing the constant g\_szContentPartnerInfo\_LicenseRefreshAdvanceWarning through the *bstrInfoName* parameter.</span></span> <span data-ttu-id="15ade-118">Чтобы предупредить подключаемый модуль о лицензиях, срок действия которых скоро истечет, проигрыватель Windows Media вызывает [ивмпконтентпартнер:: рефрешлиценсе](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense).</span><span class="sxs-lookup"><span data-stu-id="15ade-118">To alert the plug-in about licenses that are about to expire, Windows Media Player calls [IWMPContentPartner::RefreshLicense](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense).</span></span> <span data-ttu-id="15ade-119">Этот вызов принимает параметры, предоставляющие сведения о обновляемом файле, например о том, находится ли файл на компьютере пользователя, и указывает путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="15ade-119">This call takes parameters that provide details about the file being refreshed, such as whether the file is on the user's computer, and the path to the file.</span></span> <span data-ttu-id="15ade-120">Если лицензия обновляется в ходе операции синхронизации устройства, параметр *преасонконтекст* предоставляет имя канноникал устройства.</span><span class="sxs-lookup"><span data-stu-id="15ade-120">If the license is being refreshed as part of a device synchronization operation, the *pReasonContext* parameter supplies the cannonical name of the device</span></span>

<span data-ttu-id="15ade-121">Когда проигрыватель Windows Media вызывает **рефрешлиценце**, он передает файл cookie, который идентифицирует запрос на обновление.</span><span class="sxs-lookup"><span data-stu-id="15ade-121">When Windows Media Player calls **RefreshLicence**, it passes a cookie that identifies the update request.</span></span> <span data-ttu-id="15ade-122">Когда подключаемый модуль заканчивает обработку запроса на обновление, он уведомляет проигрыватель Windows Media, вызывая [ивмпконтентпартнеркаллбакк:: рефрешлиценсекомплете](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), передавая файл cookie, идентификатор элемента мультимедиа и **значение HRESULT** , указывающее, успешно ли выполнено обновление.</span><span class="sxs-lookup"><span data-stu-id="15ade-122">When the plug-in has finished processing the update request, it notifies Windows Media Player by calling [IWMPContentPartnerCallback::RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), passing the cookie, the ID of the media item, and an **HRESULT** that indicates whether the update was successful.</span></span>

<span data-ttu-id="15ade-123">Подключаемые модули Интернет-магазина также могут проверять лицензии и обновлять их как фоновый процесс.</span><span class="sxs-lookup"><span data-stu-id="15ade-123">Online store plug-ins can also do license inspection and updates as a background process.</span></span> <span data-ttu-id="15ade-124">Проигрыватель Windows Media уведомляет подключаемый модуль о времени, когда допускается выполнение задач фоновой обработки путем вызова [ивмпконтентпартнер:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify).</span><span class="sxs-lookup"><span data-stu-id="15ade-124">Windows Media Player notifies the plug-in about times when it is permissible to perform background processing tasks by calling [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify).</span></span> <span data-ttu-id="15ade-125">Чтобы сообщить подключаемому модулю запустить фоновую обработку, проигрыватель передает значение перечисления [Вмппартнернотификатион](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) вмпснбаккграундпроцессингбегин; чтобы сообщить подключаемому модулю о необходимости отключить фоновую обработку, проигрыватель передает значение Вмпснбаккграундпроцессинженд.</span><span class="sxs-lookup"><span data-stu-id="15ade-125">To signal the plug-in to start background processing, the Player passes the [WMPPartnerNotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) enumeration value wmpsnBackgroundProcessingBegin; to signal the plug-in to stop background processing, the Player passes the value wmpsnBackgroundProcessingEnd.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15ade-126">См. также</span><span class="sxs-lookup"><span data-stu-id="15ade-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15ade-127">**Справка по программированию для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="15ade-127">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




