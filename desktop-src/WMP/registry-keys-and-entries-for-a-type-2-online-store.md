---
title: Разделы реестра и записи для Интернет-магазина типа 2
description: Разделы реестра и записи для Интернет-магазина типа 2
ms.assetid: 17dff940-3884-488a-9016-29bb47c51caf
keywords:
- Интернет-магазины проигрывателя Windows Media в Интернете, реестр
- Интернет-магазины, реестр
- Тип 2 Интернет-магазинов, реестр
- реестр, тип 2 Интернет-магазинов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685a26514730e7c370c698cbc9c64c29366c35ee
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104133567"
---
# <a name="registry-keys-and-entries-for-a-type-2-online-store"></a><span data-ttu-id="ceac8-107">Разделы реестра и записи для Интернет-магазина типа 2</span><span class="sxs-lookup"><span data-stu-id="ceac8-107">Registry Keys and Entries for a Type 2 Online Store</span></span>

> [!Note]  
> <span data-ttu-id="ceac8-108">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="ceac8-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="ceac8-109">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ceac8-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="ceac8-110">Чтобы сделать Интернет-магазин типа 2 доступным в проигрывателе Windows Media, поставщик Интернет-магазина должен создать следующие подразделы и записи реестра на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="ceac8-110">To make a type 2 online store available in Windows Media Player, the online store provider must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="Apartment"
```



<span data-ttu-id="ceac8-111">В предыдущем синтаксисе реестра символы курсивом являются заполнителями для имен и глобально уникальных идентификаторов (GUID), характерных для Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="ceac8-111">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the online store.</span></span> <span data-ttu-id="ceac8-112">В следующей таблице описаны эти заполнители.</span><span class="sxs-lookup"><span data-stu-id="ceac8-112">The following table describes those placeholders.</span></span>



| <span data-ttu-id="ceac8-113">Заполнитель</span><span class="sxs-lookup"><span data-stu-id="ceac8-113">Placeholder</span></span>    | <span data-ttu-id="ceac8-114">Описание</span><span class="sxs-lookup"><span data-stu-id="ceac8-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceac8-115">*keyName*</span><span class="sxs-lookup"><span data-stu-id="ceac8-115">*keyName*</span></span>      | <span data-ttu-id="ceac8-116">Строка, согласованная между корпорацией Майкрософт и Интернет-магазином.</span><span class="sxs-lookup"><span data-stu-id="ceac8-116">A string agreed upon between Microsoft and the online store.</span></span> <span data-ttu-id="ceac8-117">Эта строка уникально идентифицирует Интернет-магазин. Пример: "Proseware"</span><span class="sxs-lookup"><span data-stu-id="ceac8-117">This string uniquely identifies the online store.Example: "Proseware"</span></span><br/>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="ceac8-118">*flags*</span><span class="sxs-lookup"><span data-stu-id="ceac8-118">*flags*</span></span>        | <span data-ttu-id="ceac8-119">Побитовое **или** для одного или нескольких флагов возможностей подключаемых модулей. Эти флаги определяют, должен ли проигрыватель Windows Media вызывать определенные методы [ивмпсубскриптионсервице](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) и [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2).</span><span class="sxs-lookup"><span data-stu-id="ceac8-119">A bitwise **OR** of one or more plug-in capability flags These flags specify whether Windows Media Player should call particular methods of [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) and [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2).</span></span> <span data-ttu-id="ceac8-120">Дополнительные сведения о поддерживаемых флагах см. в таблице флагов возможностей подключаемых модулей, которые следуют за этой таблицей. Пример: 00000037</span><span class="sxs-lookup"><span data-stu-id="ceac8-120">For information about supported flags, see the table of plug-in capability flags that follows this table.Example: 00000037</span></span><br/> |
| <span data-ttu-id="ceac8-121">*этому*</span><span class="sxs-lookup"><span data-stu-id="ceac8-121">*clsid*</span></span>        | <span data-ttu-id="ceac8-122">Идентификатор GUID, который является идентификатором класса (CLSID) для класса, реализующего **ивмпсубскриптионсервице** в подключаемом модуле Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="ceac8-122">A GUID that is the class identifier (CLSID) for the class that implements **IWMPSubscriptionService** in the online store's plug-in.</span></span> <span data-ttu-id="ceac8-123">Этот GUID должен быть в формате реестра, заполненном фигурными скобками. Формат: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="ceac8-123">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                                                                                    |
| <span data-ttu-id="ceac8-124">*FriendlyName*</span><span class="sxs-lookup"><span data-stu-id="ceac8-124">*friendlyname*</span></span> | <span data-ttu-id="ceac8-125">Понятное имя Интернет-магазина. Пример: "Proseware Music Service"</span><span class="sxs-lookup"><span data-stu-id="ceac8-125">A friendly name for the online store.Example: "Proseware Music Service"</span></span><br/>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="ceac8-126">*pluginName*</span><span class="sxs-lookup"><span data-stu-id="ceac8-126">*pluginName*</span></span>   | <span data-ttu-id="ceac8-127">Имя подключаемого модуля интернет-магазина. Пример: "подключаемый модуль службы Proseware"</span><span class="sxs-lookup"><span data-stu-id="ceac8-127">A name for the online store's plug-in.Example: "Proseware Service Plug-in"</span></span><br/>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ceac8-128">*className*</span><span class="sxs-lookup"><span data-stu-id="ceac8-128">*className*</span></span>    | <span data-ttu-id="ceac8-129">Имя класса, реализующего **ивмпсубскриптионсервице** в подключаемом модуле Интернет-магазина. Пример: "Кпросеваресервице"</span><span class="sxs-lookup"><span data-stu-id="ceac8-129">The name of the class that implements **IWMPSubscriptionService** in the online store's plug-in.Example: "CProsewareService"</span></span><br/>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="ceac8-130">*moduleName*</span><span class="sxs-lookup"><span data-stu-id="ceac8-130">*moduleName*</span></span>   | <span data-ttu-id="ceac8-131">Полный путь к библиотеке DLL, которая реализует подключаемый модуль интернет-магазина. Пример: "C: \\ Program Files \\ Proseware \\ProsewareService.dll"</span><span class="sxs-lookup"><span data-stu-id="ceac8-131">The fully qualified path to the DLL that implements the online store's plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareService.dll"</span></span><br/>                                                                                                                                                                                                                                                |



 

<span data-ttu-id="ceac8-132">В следующей таблице описаны флаги возможностей подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="ceac8-132">The following table describes the plug-in capability flags.</span></span>



| <span data-ttu-id="ceac8-133">Флаг</span><span class="sxs-lookup"><span data-stu-id="ceac8-133">Flag</span></span>                                    | <span data-ttu-id="ceac8-134">Значение</span><span class="sxs-lookup"><span data-stu-id="ceac8-134">Value</span></span> | <span data-ttu-id="ceac8-135">Описание</span><span class="sxs-lookup"><span data-stu-id="ceac8-135">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceac8-136">\_алловплай ограничения \_ подписки</span><span class="sxs-lookup"><span data-stu-id="ceac8-136">SUBSCRIPTION\_CAP\_ALLOWPLAY</span></span>            | <span data-ttu-id="ceac8-137">0X1</span><span class="sxs-lookup"><span data-stu-id="ceac8-137">0X1</span></span>   | <span data-ttu-id="ceac8-138">Проигрыватель Windows Media должен вызывать [ивмпсубскриптионсервице:: алловплай](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay).</span><span class="sxs-lookup"><span data-stu-id="ceac8-138">Windows Media Player should call [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay).</span></span>                                                                                                                      |
| <span data-ttu-id="ceac8-139">\_алловкдбурн ограничения \_ подписки</span><span class="sxs-lookup"><span data-stu-id="ceac8-139">SUBSCRIPTION\_CAP\_ALLOWCDBURN</span></span>          | <span data-ttu-id="ceac8-140">0X2</span><span class="sxs-lookup"><span data-stu-id="ceac8-140">0X2</span></span>   | <span data-ttu-id="ceac8-141">Проигрыватель Windows Media должен вызывать [ивмпсубскриптионсервице:: алловкдбурн](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).</span><span class="sxs-lookup"><span data-stu-id="ceac8-141">Windows Media Player should call [IWMPSubscriptionService::allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).</span></span>                                                                                                                  |
| <span data-ttu-id="ceac8-142">\_алловпдатрансфер ограничения \_ подписки</span><span class="sxs-lookup"><span data-stu-id="ceac8-142">SUBSCRIPTION\_CAP\_ALLOWPDATRANSFER</span></span>     | <span data-ttu-id="ceac8-143">0X4</span><span class="sxs-lookup"><span data-stu-id="ceac8-143">0X4</span></span>   | <span data-ttu-id="ceac8-144">Проигрыватель Windows Media должен вызывать [ивмпсубскриптионсервице:: алловпдатрансфер](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer).</span><span class="sxs-lookup"><span data-stu-id="ceac8-144">Windows Media Player should call [IWMPSubscriptionService::allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer).</span></span>                                                                                                        |
| <span data-ttu-id="ceac8-145">\_баккграундпроцессинг ограничения \_ подписки</span><span class="sxs-lookup"><span data-stu-id="ceac8-145">SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING</span></span> | <span data-ttu-id="ceac8-146">0X8</span><span class="sxs-lookup"><span data-stu-id="ceac8-146">0X8</span></span>   | <span data-ttu-id="ceac8-147">Проигрыватель Windows Media должен вызывать [ивмпсубскриптионсервице:: стартбаккграундпроцессинг](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).</span><span class="sxs-lookup"><span data-stu-id="ceac8-147">Windows Media Player should call [IWMPSubscriptionService::startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).</span></span>                                                                                      |
| <span data-ttu-id="ceac8-148">\_девицеаваилабле ограничения \_ подписки</span><span class="sxs-lookup"><span data-stu-id="ceac8-148">SUBSCRIPTION\_CAP\_DEVICEAVAILABLE</span></span>      | <span data-ttu-id="ceac8-149">0X10</span><span class="sxs-lookup"><span data-stu-id="ceac8-149">0X10</span></span>  | <span data-ttu-id="ceac8-150">Проигрыватель Windows Media должен вызвать [IWMPSubscriptionService2::D евицеаваилабле](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).</span><span class="sxs-lookup"><span data-stu-id="ceac8-150">Windows Media Player should call [IWMPSubscriptionService2::deviceAvailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).</span></span>                                                                                                        |
| <span data-ttu-id="ceac8-151">\_препарефорсинк ограничения \_ подписки</span><span class="sxs-lookup"><span data-stu-id="ceac8-151">SUBSCRIPTION\_CAP\_PREPAREFORSYNC</span></span>       | <span data-ttu-id="ceac8-152">0X20</span><span class="sxs-lookup"><span data-stu-id="ceac8-152">0X20</span></span>  | <span data-ttu-id="ceac8-153">Проигрыватель Windows Media должен вызвать [IWMPSubscriptionService2::P репарефорсинк](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).</span><span class="sxs-lookup"><span data-stu-id="ceac8-153">Windows Media Player should call [IWMPSubscriptionService2::prepareForSync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).</span></span>                                                                                                          |
| <span data-ttu-id="ceac8-154">ПОДПИСКА \_ v1 с \_ ограничениями</span><span class="sxs-lookup"><span data-stu-id="ceac8-154">SUBSCRIPTION\_V1\_CAPS</span></span>                  | <span data-ttu-id="ceac8-155">0XF</span><span class="sxs-lookup"><span data-stu-id="ceac8-155">0XF</span></span>   | <span data-ttu-id="ceac8-156">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ceac8-156">Default.</span></span> <span data-ttu-id="ceac8-157">Это значение используется, если ни один из них не зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="ceac8-157">This value is used if none is registered.</span></span> <span data-ttu-id="ceac8-158">Это эквивалентно объединению ПОДПИСок \_ \_ алловплай, \_ алловкдбурн Cap \_ , ограничения подписки \_ \_ алловпдатрансфер и \_ ограничения подписки \_ баккграундпроцессинг.</span><span class="sxs-lookup"><span data-stu-id="ceac8-158">This is equivalent to combining SUBSCRIPTION\_CAP\_ALLOWPLAY, SUBSCRIPTION\_CAP\_ALLOWCDBURN, SUBSCRIPTION\_CAP\_ALLOWPDATRANSFER, and SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING.</span></span> |



 

<span data-ttu-id="ceac8-159">**Записи реестра для разработки и тестирования**</span><span class="sxs-lookup"><span data-stu-id="ceac8-159">**Registry Entries for Development and Testing**</span></span>

<span data-ttu-id="ceac8-160">После начала разработки Интернет-магазина Корпорация Майкрософт предоставляет два ключа: тестовый ключ и рабочий ключ.</span><span class="sxs-lookup"><span data-stu-id="ceac8-160">When you begin developing your online store, Microsoft provides you with two keys: a test key and a production key.</span></span> <span data-ttu-id="ceac8-161">На этапе разработки и тестирования Интернет-магазин будет отображаться в проигрывателе Windows Media только в том случае, если ваш тестовый ключ или рабочий ключ находится в реестре на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="ceac8-161">During the development and testing phase, your online store will appear in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="ceac8-162">Дополнительные сведения о тестовых и производственных ключах см. в разделе [тестирование и производство ключей для Интернет-магазина типа 2](test-and-production-keys-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="ceac8-162">For more information about the test and production keys, see [Test and Production Keys for a Type 2 Online Store](test-and-production-keys-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="ceac8-163">Поместите свой тестовый или рабочий ключ в следующее место в реестре.</span><span class="sxs-lookup"><span data-stu-id="ceac8-163">Place your test or production key in the following location in the registry.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



<span data-ttu-id="ceac8-164">Обратите внимание, что значение записи реестра Тестпараметер может указывать несколько тестовых или рабочих ключей.</span><span class="sxs-lookup"><span data-stu-id="ceac8-164">Note that the value of the TestParameter registry entry can specify multiple test or production keys.</span></span> <span data-ttu-id="ceac8-165">Например, предположим, что у Proseware есть тестовый ключ "1234", а Contoso — тестовый ключ "2345".</span><span class="sxs-lookup"><span data-stu-id="ceac8-165">For example, suppose that Proseware has a test key of "1234" and Contoso has a test key of "2345".</span></span> <span data-ttu-id="ceac8-166">Следующая запись реестра указывает, что хранилища тестов для Proseware и Contoso будут отображаться в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ceac8-166">The following registry entry specifies that the test stores for Proseware and Contoso will appear in Windows Media Player.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



<span data-ttu-id="ceac8-167">**Запись реестра Активесервице**</span><span class="sxs-lookup"><span data-stu-id="ceac8-167">**ActiveService Registry Entry**</span></span>

<span data-ttu-id="ceac8-168">Когда пользователь активирует Интернет-магазин, проигрыватель Windows Media записывает в реестр сведения, определяющие активное Интернет-магазин.</span><span class="sxs-lookup"><span data-stu-id="ceac8-168">When the user activates an online store, Windows Media Player writes information in the registry that identifies the active online store.</span></span> <span data-ttu-id="ceac8-169">Проигрыватель Windows Media помещает сведения в следующем расположении в реестре на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="ceac8-169">Windows Media Player places the information in the following location in the registry on the user's computer.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



<span data-ttu-id="ceac8-170">В приведенном выше синтаксисе реестра *serviceInfo* — это заполнитель для строки, содержащей описательные сведения об активном Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="ceac8-170">In the preceding registry syntax, *serviceInfo* is a placeholder for a string that contains descriptive information about the active online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ceac8-171">См. также</span><span class="sxs-lookup"><span data-stu-id="ceac8-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ceac8-172">**Справочные материалы по интернет-магазинам типа 2**</span><span class="sxs-lookup"><span data-stu-id="ceac8-172">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





