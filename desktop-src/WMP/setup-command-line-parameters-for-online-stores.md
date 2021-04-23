---
title: Параметры командной строки программы установки для Интернет-магазинов
description: Параметры командной строки программы установки для Интернет-магазинов
ms.assetid: 26224d7c-ca12-43b9-9150-3d39bccb85d3
keywords:
- Интернет-магазины проигрывателя Windows Media, параметры командной строки программы установки
- Интернет-магазины, параметры командной строки программы установки
- Введите 1 Интернет-магазины, параметры командной строки программы установки
- Тип 2 Интернет-магазинов, параметры командной строки программы установки
- параметры командной строки программы установки
- Интернет-магазины проигрывателя Windows Media, параметры командной строки
- Интернет-магазины, параметры командной строки
- Тип 1 Интернет-магазины, параметры командной строки
- Тип 2 Интернет-магазинов, параметры командной строки
- параметры командной строки
- Интернет-магазины проигрывателя Windows Media, параметры
- Интернет-магазины, параметры
- Тип 1 Интернет-магазины, параметры
- Тип 2 Интернет-магазинов, параметры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0605814d3f8ce5e3015cf67d38f213a6b6f07500
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067907"
---
# <a name="setup-command-line-parameters-for-online-stores"></a><span data-ttu-id="eda37-117">Параметры командной строки программы установки для Интернет-магазинов</span><span class="sxs-lookup"><span data-stu-id="eda37-117">Setup Command-line Parameters for Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="eda37-118">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="eda37-118">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="eda37-119">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="eda37-119">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="eda37-120">При установке проигрывателя Windows Media 10 или Windows Media Player 11 в Windows XP можно добавить параметры командной строки, чтобы указать первое Интернет-хранилище, которое видит пользователь.</span><span class="sxs-lookup"><span data-stu-id="eda37-120">When installing Windows Media Player 10 or Windows Media Player 11 on Windows XP, you can append command-line parameters to specify the first online store that the user sees.</span></span>

<span data-ttu-id="eda37-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eda37-121">Syntax</span></span>


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:serviceKey /ServiceInfo:documentPath /ServiceExtra:queryString"
```



<span data-ttu-id="eda37-122">Параметры</span><span class="sxs-lookup"><span data-stu-id="eda37-122">Parameters</span></span>

<span data-ttu-id="eda37-123">Дефаултсервице (обязательно)</span><span class="sxs-lookup"><span data-stu-id="eda37-123">DefaultService (required)</span></span>

<span data-ttu-id="eda37-124">Имя ключа для Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="eda37-124">The key name for the online store.</span></span> <span data-ttu-id="eda37-125">Это значение должно совпадать с именем ключа в **ключевом** атрибуте элемента **serviceInfo** документа serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="eda37-125">This value must match the key name in the **Key** attribute of the **ServiceInfo** element of the ServiceInfo document.</span></span>

<span data-ttu-id="eda37-126">ServiceInfo (обязательно)</span><span class="sxs-lookup"><span data-stu-id="eda37-126">ServiceInfo (required)</span></span>

<span data-ttu-id="eda37-127">Полный путь к документу ServiceInfo, установленному на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="eda37-127">The fully qualified path to a ServiceInfo document installed on the user's computer.</span></span>

<span data-ttu-id="eda37-128">Сервицеекстра (необязательно)</span><span class="sxs-lookup"><span data-stu-id="eda37-128">ServiceExtra (optional)</span></span>

<span data-ttu-id="eda37-129">Строка запроса, которую проигрыватель Windows Media 10 будет добавлять к URL-адресу документа ServiceInfo при извлечении документа в режиме в сети.</span><span class="sxs-lookup"><span data-stu-id="eda37-129">A query string that Windows Media Player 10 will append to the URL for the ServiceInfo document when it retrieves the document online.</span></span>

## <a name="remarks"></a><span data-ttu-id="eda37-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eda37-130">Remarks</span></span>

<span data-ttu-id="eda37-131">Дополнительные сведения о распространении программного обеспечения проигрывателя Windows Media с помощью приложения см. в разделе [распространение программного обеспечения проигрывателя Windows Media](redistributing-windows-media-player-software.md).</span><span class="sxs-lookup"><span data-stu-id="eda37-131">For details about redistributing Windows Media Player software with your application, see [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md).</span></span>

<span data-ttu-id="eda37-132">Если компьютер пользователя не подключен к Интернету, сведения, содержащиеся в локальном документе ServiceInfo, используются для настройки проигрывателя Windows Media для начальной активной службы.</span><span class="sxs-lookup"><span data-stu-id="eda37-132">When the user's computer is not connected to the Internet, the information contained in the local ServiceInfo document is used to configure Windows Media Player for the initial active service.</span></span>

<span data-ttu-id="eda37-133">Параметры командной строки чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="eda37-133">Command-line parameters are case sensitive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eda37-134">См. также</span><span class="sxs-lookup"><span data-stu-id="eda37-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eda37-135">**Совместное фирменная символика Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="eda37-135">**Co-Branding Online Stores**</span></span>](co-branding-online-stores.md)
</dt> <dt>

[<span data-ttu-id="eda37-136">**Сведения, общие для типа 1 и 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="eda37-136">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="eda37-137">**Элемент install**</span><span class="sxs-lookup"><span data-stu-id="eda37-137">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="eda37-138">**Настройка начального Интернет-магазина**</span><span class="sxs-lookup"><span data-stu-id="eda37-138">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> </dl>

 

 




