---
title: Основы DRM
description: Основы DRM
ms.assetid: f36da29d-5f9d-441d-8061-eb50331a8e7a
keywords:
- Windows Media Format SDK, основы DRM
- Управление цифровыми правами (DRM), о
- DRM (Управление цифровыми правами), о программе
- Управление цифровыми правами (DRM), защита содержимого
- DRM (Управление цифровыми правами), защита содержимого
- Управление цифровыми правами (DRM), упаковка содержимого
- DRM (Управление цифровыми правами), упаковка содержимого
- Управление цифровыми правами (DRM), чтение защищенного содержимого
- DRM (Управление цифровыми правами), чтение защищенного содержимого
- Защита содержимого
- Упаковка содержимого
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c210fceb69174147dcb36a3e97b5591c2654a566
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411385"
---
# <a name="drm-basics"></a><span data-ttu-id="a00da-114">Основы DRM</span><span class="sxs-lookup"><span data-stu-id="a00da-114">DRM Basics</span></span>

<span data-ttu-id="a00da-115">Технологии DRM Windows Media очень просты с точки зрения пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="a00da-115">The Windows Media DRM technologies are fairly simple from the perspective of the Windows Media Format SDK.</span></span> <span data-ttu-id="a00da-116">Компоненты пакета SDK можно использовать для защиты содержимого и воспроизведения защищенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="a00da-116">Components of the SDK can be used to protect content and to play protected content.</span></span>

## <a name="protecting-content"></a><span data-ttu-id="a00da-117">Защита контента</span><span class="sxs-lookup"><span data-stu-id="a00da-117">Protecting Content</span></span>

<span data-ttu-id="a00da-118">Защита содержимого (также называемого упакованным содержимым) включает шифрование раздела данных файла и включение некоторых сведений в заголовок файла, позволяющий игрокам расшифровывать содержимое.</span><span class="sxs-lookup"><span data-stu-id="a00da-118">Protecting content (also called packaging content) involves encrypting the data section of the file and including some information in the file header that enables players to decrypt the content.</span></span>

<span data-ttu-id="a00da-119">Для шифрования содержимого необходим ключ, который является значением, используемым для заполнения алгоритмов шифрования.</span><span class="sxs-lookup"><span data-stu-id="a00da-119">To encrypt the content, you need a key, which is a value used to seed the encryption algorithms.</span></span> <span data-ttu-id="a00da-120">Ключ состоит из двух частей: начальное значение ключа (или закрытый ключ) и идентификатор ключа (или открытый ключ).</span><span class="sxs-lookup"><span data-stu-id="a00da-120">A key is made up of two pieces: a key seed (or private key), and a key identifier (or public key).</span></span> <span data-ttu-id="a00da-121">Начальное значение является секретным значением, с помощью которого кодируется содержимое.</span><span class="sxs-lookup"><span data-stu-id="a00da-121">The key seed is the secret value with which you encode content.</span></span> <span data-ttu-id="a00da-122">Идентификатор ключа — это открытое значение, включенное в заголовок защищенного файла.</span><span class="sxs-lookup"><span data-stu-id="a00da-122">The key identifier is a public value that is included in the header of a protected file.</span></span>

<span data-ttu-id="a00da-123">Если файл защищен, его нельзя расшифровать без лицензии.</span><span class="sxs-lookup"><span data-stu-id="a00da-123">When a file is protected, it cannot be decrypted without a license.</span></span> <span data-ttu-id="a00da-124">Лицензия включает сведения, указывающие условия использования защищенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="a00da-124">A license includes information that specifies the terms of use for the protected content.</span></span> <span data-ttu-id="a00da-125">Условия лицензии определяются владельцем содержимого и могут быть настроены в соответствии с различными потребностями.</span><span class="sxs-lookup"><span data-stu-id="a00da-125">The terms of a license are decided by the content owner and can be customized to meet a variety of needs.</span></span> <span data-ttu-id="a00da-126">Частью процесса упаковки файла является включение URL веб-страницы, на которой пользователи могут получить лицензию для доступа к содержимому.</span><span class="sxs-lookup"><span data-stu-id="a00da-126">Part of the process of packaging a file is to include the URL of a Web page where users can acquire a license to access the content.</span></span>

## <a name="reading-protected-content"></a><span data-ttu-id="a00da-127">Чтение защищенного содержимого</span><span class="sxs-lookup"><span data-stu-id="a00da-127">Reading Protected Content</span></span>

<span data-ttu-id="a00da-128">Для чтения защищенного содержимого лицензия на содержимое должна находиться на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="a00da-128">To read protected content, a license for the content must reside on the client computer.</span></span> <span data-ttu-id="a00da-129">Некоторые ограничения лицензии проверяются внутренне компонентами DRM пакета SDK Windows Media Format, а другие должны быть принудительно применены приложением.</span><span class="sxs-lookup"><span data-stu-id="a00da-129">Some license restrictions are checked internally by the DRM components of the Windows Media Format SDK, while others must be enforced by your application.</span></span>

<span data-ttu-id="a00da-130">Вы можете использовать объекты пакета SDK Windows Media Format, чтобы помочь пользователям получать лицензии на содержимое и выполнять другие административные задачи, такие как обновление компонентов DRM и резервное копирование лицензий.</span><span class="sxs-lookup"><span data-stu-id="a00da-130">You can use the objects of the Windows Media Format SDK to assist the user in acquiring licenses for content and to perform other administrative tasks, such as updating DRM components and backing up licenses.</span></span>

> [!Note]  
> <span data-ttu-id="a00da-131">DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="a00da-131">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a00da-132">См. также</span><span class="sxs-lookup"><span data-stu-id="a00da-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a00da-133">**Функции цифровых Rights Management**</span><span class="sxs-lookup"><span data-stu-id="a00da-133">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="a00da-134">**Включение поддержки DRM**</span><span class="sxs-lookup"><span data-stu-id="a00da-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




