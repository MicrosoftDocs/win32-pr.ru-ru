---
title: Регистрация службы
description: Чтобы добавить службу в список поставщиков в мастере веб-публикаций или мастере заказа отпечатков через Интернет, необходимо добавить соответствующий раздел и его значения в реестр Windows.
ms.assetid: 4a6f6df8-f850-4a80-9cf9-e62f3350915f
keywords:
- регистрация, службы
- Мастер веб-публикаций, регистрация
- Мастер заказа отпечатков в сети, регистрация
- регистрация, мастер веб-публикаций
- регистрация, мастер заказа принтера в сети
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497133d7f0a769fce987745a2341a2e501fe7a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "104273671"
---
# <a name="registering-a-service"></a><span data-ttu-id="c86ac-108">Регистрация службы</span><span class="sxs-lookup"><span data-stu-id="c86ac-108">Registering a Service</span></span>

<span data-ttu-id="c86ac-109">Чтобы добавить службу в список поставщиков в мастере веб-публикаций или мастере заказа отпечатков через Интернет, необходимо добавить соответствующий раздел и его значения в реестр Windows.</span><span class="sxs-lookup"><span data-stu-id="c86ac-109">To add your service to the list of providers in either the Web Publishing Wizard or the Online Print Ordering Wizard, you must add the appropriate key and its values to the Windows registry.</span></span>

## <a name="required-keys-and-values"></a><span data-ttu-id="c86ac-110">Обязательные ключи и значения</span><span class="sxs-lookup"><span data-stu-id="c86ac-110">Required Keys and Values</span></span>

<span data-ttu-id="c86ac-111">Чтобы добавить службу в список поставщиков для мастера веб-публикаций, добавьте ключ, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="c86ac-111">To add your service to the list of providers for the Web Publishing Wizard, add a key as shown below.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     PublishingWizard
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

<span data-ttu-id="c86ac-112">Чтобы добавить службу в список поставщиков для мастера заказа отпечатков в сети, добавьте ключ, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="c86ac-112">To add your service to the list of providers for the Online Print Ordering Wizard, add a key as shown below.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

<span data-ttu-id="c86ac-113">Каждое из значений является строкой типа REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="c86ac-113">Each of the values is a string of type REG\_SZ.</span></span> <span data-ttu-id="c86ac-114">Укажите данные, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c86ac-114">Provide its data as explained in the following table.</span></span> 

| <span data-ttu-id="c86ac-115">Имя значения</span><span class="sxs-lookup"><span data-stu-id="c86ac-115">Value Name</span></span>     | <span data-ttu-id="c86ac-116">Объяснение</span><span class="sxs-lookup"><span data-stu-id="c86ac-116">Explanation</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c86ac-117">IconPath</span><span class="sxs-lookup"><span data-stu-id="c86ac-117">IconPath</span></span>       | <span data-ttu-id="c86ac-118">Полный путь к файлу значка, включая имя файла.</span><span class="sxs-lookup"><span data-stu-id="c86ac-118">The full path to the icon file, including the file name.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c86ac-119">DisplayName</span><span class="sxs-lookup"><span data-stu-id="c86ac-119">DisplayName</span></span>    | <span data-ttu-id="c86ac-120">Имя, отображаемое для службы, в списке поставщиков мастера.</span><span class="sxs-lookup"><span data-stu-id="c86ac-120">The name displayed for your service in the wizard's providers list.</span></span>                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="c86ac-121">Описание</span><span class="sxs-lookup"><span data-stu-id="c86ac-121">Description</span></span>    | <span data-ttu-id="c86ac-122">Краткое описание службы.</span><span class="sxs-lookup"><span data-stu-id="c86ac-122">A short description for your service.</span></span> <span data-ttu-id="c86ac-123">Это описание также отображается в списке поставщики мастера непосредственно под именем службы.</span><span class="sxs-lookup"><span data-stu-id="c86ac-123">This description also displays in the wizard's providers list directly below the name of your service.</span></span>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="c86ac-124">ПОЛНЫЙ</span><span class="sxs-lookup"><span data-stu-id="c86ac-124">HREF</span></span>           | <span data-ttu-id="c86ac-125">URL-адрес первой страницы службы.</span><span class="sxs-lookup"><span data-stu-id="c86ac-125">The URL of the first page of your service.</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="c86ac-126">суппортедтипес</span><span class="sxs-lookup"><span data-stu-id="c86ac-126">SupportedTypes</span></span> | <span data-ttu-id="c86ac-127">Типы файлов, поддерживаемые службой.</span><span class="sxs-lookup"><span data-stu-id="c86ac-127">The file types supported by your service.</span></span> <span data-ttu-id="c86ac-128">Например, *\* . jpg*.</span><span class="sxs-lookup"><span data-stu-id="c86ac-128">For instance, *\*.jpg*.</span></span> <span data-ttu-id="c86ac-129">Указывая только определенные типы файлов, служба отображается, только если выбраны эти типы файлов.</span><span class="sxs-lookup"><span data-stu-id="c86ac-129">By specifying only certain file types, your service only appears when those file types have been selected.</span></span> <span data-ttu-id="c86ac-130">Если выбрано более одного типа файлов, служба будет отображаться, если служба поддерживает любой из этих типов файлов.</span><span class="sxs-lookup"><span data-stu-id="c86ac-130">If more than one file type has been selected, your service appears if any of those file types are supported by your service.</span></span> <span data-ttu-id="c86ac-131">Если необходимо указать несколько типов файлов, разделите их в списке точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="c86ac-131">If you want to specify multiple file types, separate them in the list with semicolons.</span></span> <span data-ttu-id="c86ac-132">Например, *\* JPG; \* . BMP*.</span><span class="sxs-lookup"><span data-stu-id="c86ac-132">For example, *\*.jpg; \*.bmp*.</span></span> |



 

<span data-ttu-id="c86ac-133">Ниже приведен полный пример для службы обработки фотографий, озаглавленной "Мипровидер".</span><span class="sxs-lookup"><span data-stu-id="c86ac-133">The following is a complete example for a photo processing service entitled "MyProvider."</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProvider
                              IconPath = C:\MyProviderFiles\MyIcon.ico
                              DisplayName = My Photo Processing Provider
                              Description = 24 hour processing guaranteed!
                              HREF = https://www.MyProvider.com/Intro.htm
                              SupportedTypes = *.jpg; *.gif; *.bmp
```

<span data-ttu-id="c86ac-134">При вызове URL-адреса службы в конец URL-адреса добавляются два значения — LCID и LangID.</span><span class="sxs-lookup"><span data-stu-id="c86ac-134">When the URL of your service is called, two values are added to the end of the URL—lcid and langid.</span></span> <span data-ttu-id="c86ac-135">Например, строка URL-адреса для приведенного выше примера может быть HTTPS: \/ /www.MyProvider.com/Intro.htm? LCID = 1033&LangID = 1033.</span><span class="sxs-lookup"><span data-stu-id="c86ac-135">For example, the URL string for the example above might be https:\//www.MyProvider.com/Intro.htm?lcid=1033&langid=1033.</span></span> <span data-ttu-id="c86ac-136">Эти переменные используются для сведений о языке и локализации.</span><span class="sxs-lookup"><span data-stu-id="c86ac-136">These variables are used for language and localization information.</span></span>

-   <span data-ttu-id="c86ac-137">**LCID** используется для информирования сервера о стране или регионе клиента и языковых параметрах.</span><span class="sxs-lookup"><span data-stu-id="c86ac-137">**lcid** is used to inform the server of the client's country/region and language settings.</span></span> <span data-ttu-id="c86ac-138">Он не используется для определения языка пользовательского интерфейса клиента, но используется для определения правильного формата валюты, даты и времени и других данных, зависящих от региона.</span><span class="sxs-lookup"><span data-stu-id="c86ac-138">It is not used to determine the language of the client's UI, but is used to determine the proper format for currency, date and time, and other region-specific data.</span></span>
-   <span data-ttu-id="c86ac-139">**LangID** используется для информирования сервера о параметре языка клиента по умолчанию, чтобы он мог использовать нужный язык в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="c86ac-139">**langid** is used to inform the server of the client's default language setting so that it can use the proper language in the UI.</span></span>

 

 




