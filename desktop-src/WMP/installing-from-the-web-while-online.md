---
title: Установка из Интернета в режиме «в сети»
description: Установка из Интернета в режиме «в сети»
ms.assetid: 891483b0-6ba4-4ed4-b043-c6c109dc696b
keywords:
- Интернет-магазины проигрывателя Windows Media, установка из Интернета во время работы в сети
- Интернет-магазины, установка из Интернета во время работы в сети
- Тип 1 Интернет-магазины, установка из Интернета во время работы в сети
- Тип 2. Интернет-магазины, установка из Интернета во время работы в сети
- Интернет-магазины проигрывателя Windows Media, оперативная установка из Интернета
- Интернет-магазины, оперативная установка из Интернета
- Тип 1 Интернет-магазины, оперативная установка из Интернета
- Тип 2 Интернет-магазинов, оперативная установка из Интернета
- Установка Интернет-магазинов из Интернета во время работы в сети
- оперативная установка интернет-магазинов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd342d3fc79cf3012d5bc290561a9b63167e044f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681474"
---
# <a name="installing-from-the-web-while-online"></a><span data-ttu-id="9a5f8-113">Установка из Интернета в режиме «в сети»</span><span class="sxs-lookup"><span data-stu-id="9a5f8-113">Installing from the Web While Online</span></span>

<span data-ttu-id="9a5f8-114">Пользователи могут установить проигрыватель Windows Media в качестве загружаемого веб-файла при подключении к Интернету.</span><span class="sxs-lookup"><span data-stu-id="9a5f8-114">Users can install Windows Media Player as a Web download while connected to the Internet.</span></span> <span data-ttu-id="9a5f8-115">В этом случае Майкрософт может настроить указанное начальное Интернет-магазин.</span><span class="sxs-lookup"><span data-stu-id="9a5f8-115">In this case, Microsoft can configure the initial online store that you specify.</span></span>

<span data-ttu-id="9a5f8-116">Чтобы перераспределить проигрыватель Windows Media таким образом, используйте следующий URL-адрес:</span><span class="sxs-lookup"><span data-stu-id="9a5f8-116">To redistribute Windows Media Player in this manner, use the following URL:</span></span>

<span data-ttu-id="9a5f8-117"> https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*версия*&UserLocale =*localID*&Service =*ключ*</span><span class="sxs-lookup"><span data-stu-id="9a5f8-117">https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*version*&UserLocale=*localID*&Service=*key*</span></span>

<span data-ttu-id="9a5f8-118">В предыдущем URL-адресе задайте *ключ* в качестве имени ключа для Интернет-магазина и задайте для *LocaleID* идентификатор локали, в котором хранится служба.</span><span class="sxs-lookup"><span data-stu-id="9a5f8-118">In the preceding URL, set *key* to the key name for your online store, and set *localeID* to the identifier of the locale where your store provides service.</span></span> <span data-ttu-id="9a5f8-119">Задайте для параметра *версия* значение 2 для проигрывателя Windows Media 11 в Windows XP или 1 для проигрывателя Windows Media 10.</span><span class="sxs-lookup"><span data-stu-id="9a5f8-119">Set *version* to 2 for Windows Media Player 11 on Windows XP or 1 for Windows Media Player 10.</span></span> <span data-ttu-id="9a5f8-120">URL-адрес устанавливает проигрыватель Windows Media и устанавливает исходное активное хранилище в указанное значение *Key*.</span><span class="sxs-lookup"><span data-stu-id="9a5f8-120">The URL installs Windows Media Player and sets the initial active store to the one specified by *key*.</span></span>

<span data-ttu-id="9a5f8-121">В следующем примере показан URL-адрес, который устанавливает проигрыватель Windows Media 11 и задает Proseware в качестве первоначального активного хранилища.</span><span class="sxs-lookup"><span data-stu-id="9a5f8-121">The following example shows a URL that installs Windows Media Player 11 and sets Proseware as the initial active store.</span></span> <span data-ttu-id="9a5f8-122">Значение 409 для *LocaleID* указывает, что Proseware предоставляет службу в США.</span><span class="sxs-lookup"><span data-stu-id="9a5f8-122">The value of 409 for *localeID* indicates that Proseware provides service in the United States.</span></span>

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=2&UserLocale=409&Service=Proseware

<span data-ttu-id="9a5f8-123">Если документ ServiceInfo для Интернет-магазина содержит элемент install, программа установки проигрывателя Windows Media настроит процесс установки.</span><span class="sxs-lookup"><span data-stu-id="9a5f8-123">If the ServiceInfo document for the online store includes an Install element, Windows Media Player setup will customize the setup process.</span></span> <span data-ttu-id="9a5f8-124">Используя значения атрибутов, программа установки выводит лицензионное соглашение (EULA) и заявление о конфиденциальности, а также извлекает и устанавливает CAB-файл на компьютер пользователя.</span><span class="sxs-lookup"><span data-stu-id="9a5f8-124">Using the attribute values, setup displays your End User License Agreement (EULA) and your privacy statement, and also retrieves and installs your .cab file to the user's computer.</span></span> <span data-ttu-id="9a5f8-125">Например, эту функцию можно использовать для установки последней версии COM-объекта, который требуется вашему Интернет-магазину.</span><span class="sxs-lookup"><span data-stu-id="9a5f8-125">For example, you can use this feature to install the latest version of a COM object that your online store requires.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a5f8-126">См. также</span><span class="sxs-lookup"><span data-stu-id="9a5f8-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a5f8-127">**Сведения, общие для типа 1 и 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="9a5f8-127">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="9a5f8-128">**Элемент install**</span><span class="sxs-lookup"><span data-stu-id="9a5f8-128">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="9a5f8-129">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="9a5f8-129">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="9a5f8-130">**Настройка начального Интернет-магазина**</span><span class="sxs-lookup"><span data-stu-id="9a5f8-130">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> </dl>

 

 




