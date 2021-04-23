---
title: Установка с компакт-диска в режиме «в сети»
description: Установка с компакт-диска в режиме «в сети»
ms.assetid: 4cf34f0e-caa0-42d1-b99a-51bbb7f0a7df
keywords:
- Интернет-магазины проигрывателя Windows Media, установка с компакт-диска в режиме "в сети"
- Интернет-магазины, установка с компакт-диска в режиме «в сети»
- Тип 1 Интернет-магазины, установка с компакт-диска в режиме "в сети"
- Тип 2. Интернет-магазины, установка с компакт-диска в режиме "в сети"
- Интернет-магазины проигрывателя Windows Media, оперативная установка с компакт-диска
- Интернет-магазины, установка в сети с компакт-диска
- Тип 1 Интернет-магазины, оперативная установка с компакт-диска
- Тип 2 Интернет-магазинов, оперативная установка с компакт-диска
- Интернет-магазины проигрывателя Windows Media, установки с CD в сети
- Интернет-магазины, установка с CD при работе в сети
- Тип 1 Online Stores, установка с компакт-диска в сети
- Тип 2 Интернет-магазинов, установка с CD в режиме "в сети"
- Установка сетевых магазинов с компакт-диска в режиме «в сети»
- Установки компакт-дисков в Интернете
- оперативная установка интернет-магазинов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd57015e64dece444b1a91afebe3144bee117caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691266"
---
# <a name="installing-from-a-cd-while-online"></a><span data-ttu-id="57672-118">Установка с компакт-диска в режиме «в сети»</span><span class="sxs-lookup"><span data-stu-id="57672-118">Installing from a CD While Online</span></span>

<span data-ttu-id="57672-119">Пользователи могут установить проигрыватель Windows Media с компакт-диска при подключении к Интернету.</span><span class="sxs-lookup"><span data-stu-id="57672-119">Users can install Windows Media Player from a CD while connected to the Internet.</span></span> <span data-ttu-id="57672-120">В этом случае программа установки проигрывателя Windows Media находит документ ServiceInfo, указанный параметром командной строки *serviceInfo* .</span><span class="sxs-lookup"><span data-stu-id="57672-120">When this happens, Windows Media Player setup locates the ServiceInfo document specified by the *ServiceInfo* command line parameter.</span></span> <span data-ttu-id="57672-121">Если **ключевой** атрибут соответствует параметру командной строки *дефаултсервице* , программа установки проверяет элемент Install на необходимость настройки процесса установки.</span><span class="sxs-lookup"><span data-stu-id="57672-121">If the **Key** attribute matches the *DefaultService* command line parameter, setup inspects the Install element to customize the setup process.</span></span> <span data-ttu-id="57672-122">Используя значения атрибутов, программа установки выводит лицензионное соглашение (EULA) и заявление о конфиденциальности, а также извлекает и устанавливает CAB-файл на компьютер пользователя.</span><span class="sxs-lookup"><span data-stu-id="57672-122">Using the attribute values, setup displays your End User License Agreement (EULA) and your privacy statement, and also retrieves and installs your .cab file to the user's computer.</span></span> <span data-ttu-id="57672-123">Например, эту функцию можно использовать для установки последней версии COM-объекта, который требуется вашему Интернет-магазину.</span><span class="sxs-lookup"><span data-stu-id="57672-123">For example, you can use this feature to install the latest version of a COM object that your online store requires.</span></span>

<span data-ttu-id="57672-124">После установки проигрыватель Windows Media устанавливает начальное Интернет-хранилище с использованием имени ключа, указанного для параметра командной строки *дефаултсервице* .</span><span class="sxs-lookup"><span data-stu-id="57672-124">After it is installed, Windows Media Player sets the initial online store using the key name you specified for the *DefaultService* command line parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57672-125">См. также</span><span class="sxs-lookup"><span data-stu-id="57672-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57672-126">**Сведения, общие для типа 1 и 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="57672-126">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="57672-127">**Элемент install**</span><span class="sxs-lookup"><span data-stu-id="57672-127">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="57672-128">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="57672-128">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="57672-129">**Настройка начального Интернет-магазина**</span><span class="sxs-lookup"><span data-stu-id="57672-129">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> <dt>

[<span data-ttu-id="57672-130">**Параметры командной строки программы установки для Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="57672-130">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




