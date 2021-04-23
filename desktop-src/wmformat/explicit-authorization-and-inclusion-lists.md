---
title: Явные списки авторизации и включений
description: Явные списки авторизации и включений
ms.assetid: b2e1cdd4-ea3c-4b05-a53a-2cdc12440645
keywords:
- Windows Media Format SDK, экспорт DRM
- Пакет Windows Media Format SDK, экспорт
- Пакет SDK для Windows Media Format, явная авторизация и списки включения
- Windows Media Format SDK, списки авторизации
- Пакет SDK для формата Windows Media, списки включений
- Управление цифровыми правами (DRM), экспорт
- DRM (Управление цифровыми правами), экспорт
- Управление цифровыми правами (DRM), явные разрешения и списки включения
- DRM (Управление цифровыми правами), явные разрешения и списки включения
- Управление цифровыми правами (DRM), списки авторизации
- DRM (Управление цифровыми правами), списки авторизации
- Управление цифровыми правами (DRM), списки включения
- DRM (Управление цифровыми правами), списки включения
- Расширенные API клиента DRM, явные списки авторизации и включения
- Расширенные API клиента, явные списки авторизации и включения
- Расширенные API клиента DRM, списки авторизации
- Расширенные API клиента, списки авторизации
- Расширенные API клиента DRM, списки включения
- Расширенные API клиента, списки включения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2309bed28ffd3add2a75c1cd90488b9ef454659b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412495"
---
# <a name="explicit-authorization-and-inclusion-lists"></a><span data-ttu-id="e0375-122">Явные списки авторизации и включений</span><span class="sxs-lookup"><span data-stu-id="e0375-122">Explicit Authorization and Inclusion Lists</span></span>

<span data-ttu-id="e0375-123">Лицензии могут содержать список включений для явной авторизации экспорта содержимого, защищенного с помощью Windows Media DRM, в другие схемы защиты содержимого (CPS).</span><span class="sxs-lookup"><span data-stu-id="e0375-123">Licenses can contain an inclusion list to explicitly authorize the exporting of content protected by Windows Media DRM to other content protection schemes (CPS).</span></span> <span data-ttu-id="e0375-124">В соответствии с условиями лицензионного соглашения, введенного в корпорацию Майкрософт для включения экспорта DRM, можно экспортировать только на допустимый сервер публикаций Contribute, указанный в списке включения лицензии.</span><span class="sxs-lookup"><span data-stu-id="e0375-124">As per the terms of the license agreement you enter into with Microsoft to enable DRM Export you can export only to a valid CPS that is identified in the inclusion list of a license.</span></span>

<span data-ttu-id="e0375-125">Список включения — это ограниченный массив глобальных уникальных идентификаторов (GUID), каждый из которых представляет конкретный полномочный сервер публикаций Contribute, на который можно экспортировать содержимое.</span><span class="sxs-lookup"><span data-stu-id="e0375-125">An inclusion list is a bounded array of globally unique identifiers (GUIDs) that each represents a specific authorized CPS to which the content can be exported.</span></span> <span data-ttu-id="e0375-126">Идентификаторы GUID, перечисленные в списке включения, не зависят от уровней защиты выходных данных (ОПЛ) и уровней защиты содержимого (CPL).</span><span class="sxs-lookup"><span data-stu-id="e0375-126">The GUIDs listed in an inclusion list are independent of the output protection levels (OPL) and content protection levels (CPL).</span></span> <span data-ttu-id="e0375-127">Применение этих ограничений несет ответственность за работу приложения.</span><span class="sxs-lookup"><span data-stu-id="e0375-127">Enforcing these restrictions is the responsibility of your application.</span></span>

> [!Note]  
> <span data-ttu-id="e0375-128">При выполнении экспорта Windows Media DRM в сжатом содержимом доступ к списку включения можно получить с помощью метода [**ивмдрмлиценсе:: жетинклусионлист**](iwmdrmlicense-getinclusionlist.md) .</span><span class="sxs-lookup"><span data-stu-id="e0375-128">When performing Windows Media DRM Export on compressed content, you access the inclusion list through the [**IWMDRMLicense::GetInclusionList**](iwmdrmlicense-getinclusionlist.md) method.</span></span> <span data-ttu-id="e0375-129">При выполнении экспорта Windows Media DRM на несжатое содержимое используйте метод [**IWMDRMReader3:: жетинклусионлист**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) .</span><span class="sxs-lookup"><span data-stu-id="e0375-129">When performing Windows Media DRM Export on uncompressed content, use the [**IWMDRMReader3::GetInclusionList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) method.</span></span>

 

<span data-ttu-id="e0375-130">Чтобы зарегистрировать новую систему защиты содержимого в качестве Windows Media DRM, разрешенной экспортом в правилах соответствия экспорта DRM Windows Media, обратитесь по адресу wmla@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="e0375-130">To register a new content protection system as a Windows Media DRM Permitted Export in the Windows Media DRM export compliance rules, please contact wmla@microsoft.com.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0375-131">См. также</span><span class="sxs-lookup"><span data-stu-id="e0375-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0375-132">**Экспорт DRM**</span><span class="sxs-lookup"><span data-stu-id="e0375-132">**DRM Export**</span></span>](drm-export.md)
</dt> </dl>

 

 




