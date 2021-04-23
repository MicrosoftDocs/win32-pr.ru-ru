---
title: Управление именем входа
description: Управление именем входа
ms.assetid: 5cafcd3a-e819-4524-b7a9-580ff36fc4f8
keywords:
- Интернет-магазины проигрывателя Windows Media, Управление именами входа
- Интернет-магазины, Управление именами входа
- Тип 1 Интернет-магазины, Управление именами входа
- Интернет-магазины проигрывателя Windows Media, имена входа
- Интернет-магазины, имена входа
- Тип 1 Интернет-магазины, имена для входа
- Интернет-магазины проигрывателя Windows Media, Стандартный процесс входа
- Интерактивные магазины, Стандартный процесс входа
- Тип 1 Интернет-магазины, Стандартный процесс входа
- Интернет-магазины проигрывателя Windows Media, процесс выхода
- Интернет-магазины, процесс выхода
- Тип 1 Интернет-магазины, процесс выхода
- Стандартный процесс входа
- процесс выхода
- имена входа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633042692ab9193f46ab83415df13237d3a279e8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412527"
---
# <a name="managing-login"></a><span data-ttu-id="d92e9-118">Управление именем входа</span><span class="sxs-lookup"><span data-stu-id="d92e9-118">Managing Login</span></span>

<span data-ttu-id="d92e9-119">Проигрыватель Windows Media поддерживает различные методы входа пользователя в Интернет-магазин типа 1.</span><span class="sxs-lookup"><span data-stu-id="d92e9-119">Windows Media Player supports a variety of methods for the user to log in to a type 1 online store.</span></span> <span data-ttu-id="d92e9-120">Проигрыватель предоставляет стандартное диалоговое окно входа, но Интернет-магазин может предоставить веб-страницу, которая служит альтернативой стандартному диалоговому окну.</span><span class="sxs-lookup"><span data-stu-id="d92e9-120">The Player provides a standard log-in dialog box, but the online store can provide a webpage that serves as an alternative to the standard dialog box.</span></span>

<span data-ttu-id="d92e9-121">Пользователь может инициировать попытку входа, взаимодействуя с пользовательским интерфейсом проигрывателя Windows Media или путем взаимодействия со страницей обнаружения, предоставляемой Интернет-магазином.</span><span class="sxs-lookup"><span data-stu-id="d92e9-121">The user can initiate a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page provided by the online store.</span></span> <span data-ttu-id="d92e9-122">Если пользователь инициирует попытку входа, взаимодействуя со страницей обнаружения, сценарий на странице обнаружения вызывает [внешний метод. аттемптлогин](external-attemptlogin.md) .</span><span class="sxs-lookup"><span data-stu-id="d92e9-122">If the user initiates a log-in attempt by interacting with a discovery page, script on the discovery page calls the [External.attemptLogin](external-attemptlogin.md) method.</span></span>

<span data-ttu-id="d92e9-123">Состояние входа пользователя сохраняется в Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="d92e9-123">The user's log-in state is maintained by the online store.</span></span> <span data-ttu-id="d92e9-124">При изменении состояния входа пользователя или при неудачной попытке входа в систему подключаемый модуль интернет-магазина уведомляет проигрыватель Windows Media, вызывая [ивмпконтентпартнеркаллбакк:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), передав вмпкнлогинстатечанже в параметре *Type* .</span><span class="sxs-lookup"><span data-stu-id="d92e9-124">When the user's log-in state changes, or if a log-in attempt fails, the online store's plug-in notifies Windows Media Player by calling [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="d92e9-125">Проигрыватель передает уведомление на страницу обнаружения, вызывая событие [External. онлогинчанже](external-onloginchange-event.md) .</span><span class="sxs-lookup"><span data-stu-id="d92e9-125">The Player passes the notification along to the discovery page by raising the [External.OnLoginChange](external-onloginchange-event.md) event.</span></span>

<span data-ttu-id="d92e9-126">Вызов **онлогинчанже** не обязательно означает, что состояние входа пользователя изменилось; Это может означать, что попытка входа завершилась ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d92e9-126">A call to **OnLoginChange** does not necessarily mean that the user's log-in state changed; it could mean that an attempt to log in failed.</span></span> <span data-ttu-id="d92e9-127">Чтобы определить состояние входа пользователя, обработчик событий **онлогинчанже** может проверить свойство [External. усерлогжедин](external-userloggedin.md) .</span><span class="sxs-lookup"><span data-stu-id="d92e9-127">To determine the user's log-in state, the **OnLoginChange** event handler can inspect the [External.userLoggedIn](external-userloggedin.md) property.</span></span>

<span data-ttu-id="d92e9-128">В следующих разделах описывается стандартный процесс входа в систему, альтернативный процесс входа в систему и процесс выхода из нее.</span><span class="sxs-lookup"><span data-stu-id="d92e9-128">The following sections describe the standard log-in process, the alternative log-in process, and the log-out process.</span></span>

## <a name="standard-log-in"></a><span data-ttu-id="d92e9-129">Стандартный вход</span><span class="sxs-lookup"><span data-stu-id="d92e9-129">Standard Log-in</span></span>

<span data-ttu-id="d92e9-130">Стандартный процесс входа состоит из следующих этапов.</span><span class="sxs-lookup"><span data-stu-id="d92e9-130">The standard log-in process involves the following steps:</span></span>

1.  <span data-ttu-id="d92e9-131">Пользователь инициирует попытку входа, взаимодействуя с пользовательским интерфейсом проигрывателя Windows Media или путем взаимодействия со страницей обнаружения.</span><span class="sxs-lookup"><span data-stu-id="d92e9-131">The user initiates a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="d92e9-132">Проигрыватель Windows Media отображает диалоговое окно, предлагающее пользователю ввести имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="d92e9-132">Windows Media Player displays a dialog box that prompts the user for a user-name and password.</span></span>
3.  <span data-ttu-id="d92e9-133">Когда пользователь нажимает кнопку " **Вход** " в диалоговом окне, проигрыватель Windows Media вызывает [Ивмпконтентпартнер:: login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login), который реализуется подключаемым модулем Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="d92e9-133">When the user clicks the **Sign In** button in the dialog box, Windows Media Player calls [IWMPContentPartner::Login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login), which is implemented by the online store's plug-in.</span></span>
4.  <span data-ttu-id="d92e9-134">Подключаемый модуль взаимодействует с Интернет-магазином и либо успешно, либо не может войти в систему пользователя.</span><span class="sxs-lookup"><span data-stu-id="d92e9-134">The plug-in communicates with the online store and either succeeds or fails to log in the user.</span></span>
5.  <span data-ttu-id="d92e9-135">Если вход в систему завершается успешно, подключаемый модуль уведомляет проигрыватель Windows Media, вызывая **ивмпконтентпартнеркаллбакк:: notify**, передавая вариант \_ true в члене **булвал** параметра *пконтекст* .</span><span class="sxs-lookup"><span data-stu-id="d92e9-135">If the log-in attempt succeeds, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing VARIANT\_TRUE in the **boolVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="d92e9-136">Если попытка входа завершается неудачей, подключаемый модуль уведомляет проигрыватель Windows Media, вызывая **ивмпконтентпартнеркаллбакк:: notify**, передавая 32-разрядное значение в члене **улвал** параметра *пконтекст* .</span><span class="sxs-lookup"><span data-stu-id="d92e9-136">If the log-in attempt fails, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing a 32-bit value in the **ulVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="d92e9-137">Затем проигрыватель передает это 32-разрядное значение в [ивмпконтентпартнер:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) , чтобы получить URL-адрес веб-страницы, которая может справиться со сбоем.</span><span class="sxs-lookup"><span data-stu-id="d92e9-137">The Player then passes that 32-bit value to [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) to get the URL of a webpage that can handle the failure.</span></span>

## <a name="alternative-login"></a><span data-ttu-id="d92e9-138">Альтернативное имя для входа</span><span class="sxs-lookup"><span data-stu-id="d92e9-138">Alternative Login</span></span>

<span data-ttu-id="d92e9-139">Если флаг подписки \_ \_ алтлогин установлен в записи реестра **capabilities** для подключаемого модуля интернет-магазина, проигрыватель Windows Media не использует стандартное диалоговое окно входа.</span><span class="sxs-lookup"><span data-stu-id="d92e9-139">If the SUBSCRIPTION\_CAP\_ALTLOGIN flag is set in the **Capabilities** registry entry for the online store's plug-in, Windows Media Player does not use the standard log-in dialog box.</span></span> <span data-ttu-id="d92e9-140">Вместо этого проигрыватель Windows Media вызывает **ивмпконтентпартнер:: GetItemInfo** для получения URL-адреса веб-страницы, выполняющей процесс входа в систему.</span><span class="sxs-lookup"><span data-stu-id="d92e9-140">Instead, Windows Media Player calls **IWMPContentPartner::GetItemInfo** to retrieve the URL of a webpage that performs the log-in process.</span></span> <span data-ttu-id="d92e9-141">Дополнительные сведения о записи реестра **capabilities** см. в разделе [разделы реестра и записи для Интернет-магазина типа 1](registry-keys-and-entries-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="d92e9-141">For more information about the **Capabilities** registry entry, see [Registry Keys and Entries for a Type 1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="d92e9-142">Игрок вызывает **GetItemInfo** дважды: после передачи g \_ сзитеминфо \_ алтлогинурл для получения URL-адреса веб-страницы входа и после передачи g \_ сзитеминфо \_ алтлогинкаптион для получения заголовка окна, в котором размещена веб-страница.</span><span class="sxs-lookup"><span data-stu-id="d92e9-142">The Player calls **GetItemInfo** twice: once passing g\_szItemInfo\_ALTLoginURL to retrieve the URL of the log-in webpage and once passing g\_szItemInfo\_ALTLoginCaption to retrieve the caption for the window that hosts the webpage.</span></span> <span data-ttu-id="d92e9-143">Когда **GetItemInfo** возвращает URL-адрес веб-страницы входа в систему, он может указать размер окна входа, добавив в URL-адрес следующую строку параметра:</span><span class="sxs-lookup"><span data-stu-id="d92e9-143">When **GetItemInfo** returns the URL of the log-in webpage, it can specify the size of the log-in window by appending the following parameter string to the URL:</span></span>

<span data-ttu-id="d92e9-144">? Длгкс =*ширина*&длги =*Высота*</span><span class="sxs-lookup"><span data-stu-id="d92e9-144">?DlgX=*width*&DlgY=*height*</span></span>

<span data-ttu-id="d92e9-145">В строке параметра *Width* и *Height* — ширина и высота окна в пикселях.</span><span class="sxs-lookup"><span data-stu-id="d92e9-145">In the parameter string, *width* and *height* are the width and height of the window in pixels.</span></span> <span data-ttu-id="d92e9-146">Например, **GetItemInfo** может вернуть следующую строку, чтобы указать, что AltLogin.htm должны отображаться в окне с шириной 800 пикселей и высотой 400 пикселей.</span><span class="sxs-lookup"><span data-stu-id="d92e9-146">For example **GetItemInfo** could return the following string to specify that AltLogin.htm should be displayed in a window that has a width of 800 pixels and a height of 400 pixels</span></span>


```C++
https://proseware.com/AltLogin.htm?DlgX=800&DlgY=400
```



<span data-ttu-id="d92e9-147">Альтернативный процесс входа состоит из следующих этапов.</span><span class="sxs-lookup"><span data-stu-id="d92e9-147">The alternative log-in process involves the following steps:</span></span>

1.  <span data-ttu-id="d92e9-148">Пользователь инициирует попытку входа, взаимодействуя с пользовательским интерфейсом проигрывателя Windows Media или путем взаимодействия со страницей обнаружения.</span><span class="sxs-lookup"><span data-stu-id="d92e9-148">The user initiates a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="d92e9-149">Проигрыватель Windows Media открывает модальное окно, в котором отображается веб-страница входа, предоставляемая Интернет-магазином.</span><span class="sxs-lookup"><span data-stu-id="d92e9-149">Windows Media Player opens a modal window that displays the log-in webpage provided by the online store.</span></span>
3.  <span data-ttu-id="d92e9-150">Веб-страница взаимодействует с Интернет-магазином и либо завершается успешно, либо не может войти в систему пользователя.</span><span class="sxs-lookup"><span data-stu-id="d92e9-150">The webpage communicates with the online store and either succeeds or fails to log in the user.</span></span>
4.  <span data-ttu-id="d92e9-151">Если попытка входа завершается, веб-страница уведомляет подключаемый модуль интерактивного хранилища, вызывая [External. SendMessage](external-sendmessage.md), что приводит к вызову [Ивмпконтентпартнер:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="d92e9-151">If the log-in attempt succeeds, the webpage notifies the online store's plug-in by calling [External.sendMessage](external-sendmessage.md), which results in a call to [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage).</span></span> <span data-ttu-id="d92e9-152">Подключаемый модуль интернет-магазина определяет, что попытка входа прошла успешно, проверив параметры, переданные в **ивмпконтентпартнер:: SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="d92e9-152">The online store's plug-in determines that the log-in attempt succeeded by inspecting the parameters passed to **IWMPContentPartner::SendMessage**.</span></span> <span data-ttu-id="d92e9-153">Эти параметры не обрабатываются проигрывателем Windows Media; они имеют значение только в Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="d92e9-153">Those parameters are not interpreted by Windows Media Player; they have meaning only to the online store.</span></span> <span data-ttu-id="d92e9-154">Подключаемый модуль вызывает **ивмпконтентпартнеркаллбакк:: notify**, передавая вариант \_ true в члене **булвал** параметра *пконтекст* .</span><span class="sxs-lookup"><span data-stu-id="d92e9-154">The plug-in calls **IWMPContentPartnerCallback::Notify**, passing VARIANT\_TRUE in the **boolVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="d92e9-155">В случае сбоя входа в Интернет-магазин должен определить, как помочь пользователю.</span><span class="sxs-lookup"><span data-stu-id="d92e9-155">If the log-in fails, the online store must determine how to assist the user.</span></span> <span data-ttu-id="d92e9-156">Одна из возможных вариантов — отобразить новую веб-страницу в модальном окне, где размещена альтернативная веб-страница входа в систему.</span><span class="sxs-lookup"><span data-stu-id="d92e9-156">One possibility is to display a new webpage in the modal window that hosts the alternative log-in webpage.</span></span>

## <a name="log-out"></a><span data-ttu-id="d92e9-157">Выход из журнала</span><span class="sxs-lookup"><span data-stu-id="d92e9-157">Log-out</span></span>

<span data-ttu-id="d92e9-158">Процесс выхода состоит из следующих шагов.</span><span class="sxs-lookup"><span data-stu-id="d92e9-158">The log-out process involves the following steps.</span></span>

1.  <span data-ttu-id="d92e9-159">Пользователь инициирует попытку выхода из системы путем взаимодействия с пользовательским интерфейсом проигрывателя Windows Media или путем взаимодействия со страницей обнаружения.</span><span class="sxs-lookup"><span data-stu-id="d92e9-159">The user initiates a log-out attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="d92e9-160">Проигрыватель Windows Media вызывает [ивмпконтентпартнер:: Logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout), который реализуется подключаемым модулем Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="d92e9-160">Windows Media Player calls [IWMPContentPartner::Logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout), which is implemented by the online store's plug-in.</span></span>
3.  <span data-ttu-id="d92e9-161">Подключаемый модуль взаимодействует с Интернет-магазином и либо завершается успешно, либо не может выполнить выход пользователя из системы.</span><span class="sxs-lookup"><span data-stu-id="d92e9-161">The plug-in communicates with the online store and either succeeds or fails to log out the user.</span></span>
4.  <span data-ttu-id="d92e9-162">Если попытки выхода из системы завершаются успешно, подключаемый модуль уведомляет проигрыватель Windows Media, вызывая **ивмпконтентпартнеркаллбакк:: notify**, передающий вариант \_ false в члене **булвал** параметра *пконтекст* .</span><span class="sxs-lookup"><span data-stu-id="d92e9-162">If the log-out attempt succeeds, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing VARIANT\_FALSE in the **boolVal** member of the *pContext* parameter.</span></span>

<span data-ttu-id="d92e9-163">Если попытка входа или выхода выполнена успешно, подключаемый модуль интернет-магазина вызывает **ивмпконтентпартнеркаллбакк:: notify**, передав вмпкнлогинстатечанже в параметре *типа* .</span><span class="sxs-lookup"><span data-stu-id="d92e9-163">When an attempt to log in or out is successful, the online store's plug-in calls **IWMPContentPartnerCallback::Notify**, passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="d92e9-164">Подключаемый модуль использует параметр *пконтекст* для указания текущего состояния входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="d92e9-164">The plug-in uses the *pContext* parameter to specify the user's current log-in state.</span></span> <span data-ttu-id="d92e9-165">Если подключаемый модуль устанавливает *пконтекст* -> **булвал** в вариант \_ true, пользователь входит в систему.</span><span class="sxs-lookup"><span data-stu-id="d92e9-165">If the plug-in sets *pContext*->**boolVal** to VARIANT\_TRUE, the user is logged in.</span></span> <span data-ttu-id="d92e9-166">Если подключаемый модуль устанавливает *пконтекст* -> **булвал** в вариант \_ false, пользователь выходит из системы. Обратите внимание, что *пконтекст* не указывает на успех или неудачу попытки; Вместо этого он указывает на текущее состояние входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="d92e9-166">If the plug-in sets *pContext*->**boolVal** to VARIANT\_FALSE, the user is logged out. Note that *pContext* does not indicate the success or failure of the attempt; rather, it indicates user's current log-in state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d92e9-167">См. также</span><span class="sxs-lookup"><span data-stu-id="d92e9-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d92e9-168">**External. Аттемптлогин**</span><span class="sxs-lookup"><span data-stu-id="d92e9-168">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="d92e9-169">**Внешнее событие Онлогинчанже**</span><span class="sxs-lookup"><span data-stu-id="d92e9-169">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> <dt>

[<span data-ttu-id="d92e9-170">**External. Усерлогжедин**</span><span class="sxs-lookup"><span data-stu-id="d92e9-170">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> <dt>

[<span data-ttu-id="d92e9-171">**Ивмпконтентпартнер:: login**</span><span class="sxs-lookup"><span data-stu-id="d92e9-171">**IWMPContentPartner::Login**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[<span data-ttu-id="d92e9-172">**Ивмпконтентпартнер:: Logout**</span><span class="sxs-lookup"><span data-stu-id="d92e9-172">**IWMPContentPartner::Logout**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)
</dt> <dt>

[<span data-ttu-id="d92e9-173">**Справка по программированию для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="d92e9-173">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




