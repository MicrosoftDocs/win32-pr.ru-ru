---
title: Использование модели событий Media Foundation
description: Использование модели событий Media Foundation
ms.assetid: c07425dc-25d0-430b-a1f6-6373303a0cc7
keywords:
- Windows Media Format SDK, модель событий DRM Media Foundation
- Windows Media Format SDK, Media Foundation модель событий
- Windows Media Format SDK, модель событий DRM
- Управление цифровыми правами (DRM), модель событий Media Foundation
- DRM (Управление цифровыми правами), модель событий Media Foundation
- Управление цифровыми правами (DRM), модель событий
- DRM (Управление цифровыми правами), модель событий
- Управление цифровыми правами (DRM), интерфейс Ивмдрмевентженератор
- DRM (Управление цифровыми правами), интерфейс Ивмдрмевентженератор
- Media Foundation
- ивмдрмевентженератор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58d48157072cf8814ff8ac74d97a965f9e772e3
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104069638"
---
# <a name="using-the-media-foundation-event-model"></a><span data-ttu-id="a3baa-114">Использование модели событий Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a3baa-114">Using the Media Foundation Event Model</span></span>

<span data-ttu-id="a3baa-115">Асинхронные методы, поддерживаемые расширенными API клиента DRM Windows Media, используют ту же модель событий, которая используется пакетом SDK для Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a3baa-115">The asynchronous methods supported by the Windows Media DRM Client Extended APIs use the same event model that is used by the Media Foundation SDK.</span></span> <span data-ttu-id="a3baa-116">Каждый объект, поддерживающий асинхронные методы, реализует интерфейс [**ивмдрмевентженератор**](iwmdrmeventgenerator.md) , который можно использовать для получения события после завершения асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="a3baa-116">Each object that supports asynchronous methods implements the [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md) interface, which can be used to retrieve an event when an asynchronous operation is complete.</span></span>

<span data-ttu-id="a3baa-117">Интерфейс **ивмдрмевентженератор** наследуется от интерфейса **имфмедиаевентженератор** , который описан в документации по Media Foundation SDK.</span><span class="sxs-lookup"><span data-stu-id="a3baa-117">The **IWMDRMEventGenerator** interface inherits from the **IMFMediaEventGenerator** interface, which is documented in the Media Foundation SDK documentation.</span></span>

<span data-ttu-id="a3baa-118">В примере кода в [примере индивидуализации DRM](drm-individualization-example.md) используется метод **имфмедиаевентженератор::** at для извлечения событий из очереди по одному за раз.</span><span class="sxs-lookup"><span data-stu-id="a3baa-118">The example code in the [DRM Individualization Example](drm-individualization-example.md) uses the **IMFMediaEventGenerator::GetEvent** method to retrieve events from the queue one at a time.</span></span> <span data-ttu-id="a3baa-119">Использование функции **четный** является более простым, чем использование **Имфмедиаевентженератор:: бегинжетевент** и **имфмедиаевентженератор:: енджетевент** с обратным вызовом, что упрощает понимание примеров кода.</span><span class="sxs-lookup"><span data-stu-id="a3baa-119">Using **GetEvent** is more straightforward than using **IMFMediaEventGenerator::BeginGetEvent** and **IMFMediaEventGenerator::EndGetEvent** with a callback, which makes the code examples easier to understand.</span></span> <span data-ttu-id="a3baa-120">Независимо от того, используете ли **вы в коде** или реализуете **Имфасинккаллбакк** и используете **бегинжетевент** и **енджетевент**, логика обработки события после получения идентична.</span><span class="sxs-lookup"><span data-stu-id="a3baa-120">Whether you use **GetEvent** in your code or implement **IMFAsyncCallback** and use **BeginGetEvent** and **EndGetEvent**, the logic to handle the event after it has been received is the same.</span></span>

<span data-ttu-id="a3baa-121">Несколько асинхронных методов создают события, содержащие ссылки на объекты, которые можно использовать для получения более подробных сведений о состоянии.</span><span class="sxs-lookup"><span data-stu-id="a3baa-121">Several of the asynchronous methods generate events that contain references to objects that can be used to obtain more detailed status information.</span></span> <span data-ttu-id="a3baa-122">В таких случаях созданное событие имеет в качестве значения указатель **IUnknown** , который можно запросить для получения интерфейса состояния.</span><span class="sxs-lookup"><span data-stu-id="a3baa-122">In these cases, the generated event has an **IUnknown** pointer as its value, which can be queried to retrieve the status interface.</span></span> <span data-ttu-id="a3baa-123">В следующем списке перечислены связи между асинхронными вызовами, созданными событиями и другими интерфейсами.</span><span class="sxs-lookup"><span data-stu-id="a3baa-123">The following list summarizes the relationships between asynchronous calls, generated events, and other interfaces.</span></span>

-   <span data-ttu-id="a3baa-124">Метод [**ивмдрмлиценсеманажемент:: баккуплиценсес**](iwmdrmlicensemanagement-backuplicenses.md) создает события **мевмдрмлиценсебаккуппрогресс** с связанными интерфейсами [**ивмдрмлиценсебаккупресторестатус**](iwmdrmlicensebackuprestorestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="a3baa-124">The [**IWMDRMLicenseManagement::BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) method generates **MEWMDRMLicenseBackupProgress** events with associated [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interfaces.</span></span>
-   <span data-ttu-id="a3baa-125">Метод [**ивмдрмлиценсеманажемент:: ресторелиценсес**](iwmdrmlicensemanagement-restorelicenses.md) создает события **мевмдрмлиценсересторепрогресс** с связанными интерфейсами [**ивмдрмлиценсебаккупресторестатус**](iwmdrmlicensebackuprestorestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="a3baa-125">The [**IWMDRMLicenseManagement::RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md) method generates **MEWMDRMLicenseRestoreProgress** events with associated [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interfaces.</span></span>
-   <span data-ttu-id="a3baa-126">Метод [**ивмдрмсекурити::P ерформсекуритюпдате**](iwmdrmsecurity-performsecurityupdate.md) , используемый для выполнения индивидуализации, создает события **мевмдрминдивидуализатионпрогресс** с связанными интерфейсами [**ивмдрминдивидуализатионстатус**](iwmdrmindividualizationstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="a3baa-126">The [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method, when used to perform individualization, generates **MEWMDRMIndividualizationProgress** events with associated [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interfaces.</span></span>
-   <span data-ttu-id="a3baa-127">Метод [**ивмдрмлиценсеманажемент:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) , используемый для подготовки данных к неавтоматическому приобретению лицензий, создает событие **мевмдрмлиценсеаккуиситионкомплетед** с связанным интерфейсом [**ивмдрмнонсилентлиценсеакуиситион**](iwmdrmnonsilentlicenseaquisition.md) .</span><span class="sxs-lookup"><span data-stu-id="a3baa-127">The [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method, when used to prepare data for non-silent license acquisition, generates an **MEWMDRMLicenseAcquisitionCompleted** event with an associated [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3baa-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a3baa-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3baa-129">**Пример индивидуализации DRM**</span><span class="sxs-lookup"><span data-stu-id="a3baa-129">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="a3baa-130">**Приступая к работе**</span><span class="sxs-lookup"><span data-stu-id="a3baa-130">**Getting Started**</span></span>](drm-getting-started.md)
</dt> <dt>

[<span data-ttu-id="a3baa-131">Документация по Media Foundation SDK</span><span class="sxs-lookup"><span data-stu-id="a3baa-131">Media Foundation SDK Documentation</span></span>](https://www.microsoft.com/?ref=go)
</dt> </dl>

 

 




