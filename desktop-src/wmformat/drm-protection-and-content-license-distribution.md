---
title: Распространение лицензий с защитой DRM и содержимым
description: Распространение лицензий с защитой DRM и содержимым
ms.assetid: 147fef8c-7298-450d-a1a9-345c03c49bec
keywords:
- Windows Media Format SDK, защита содержимого DRM
- Windows Media Format SDK, лицензии DRM
- Улучшенный системный формат (ASF), защита содержимого DRM
- ASF (расширенный формат систем), защита содержимого DRM
- Расширенный формат систем (ASF), распространение лицензий DRM
- ASF (расширенный формат систем), распространение лицензий DRM
- Управление цифровыми правами (DRM), защита содержимого
- DRM (Управление цифровыми правами), защита содержимого
- Управление цифровыми правами (DRM), распространение лицензий
- DRM (Управление цифровыми правами), распространение лицензий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25af13947828885d70f3e0fd9fe8bf035eb8c5e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332563"
---
# <a name="drm-protection-and-content-license-distribution"></a><span data-ttu-id="2ac3c-113">Распространение лицензий с защитой DRM и содержимым</span><span class="sxs-lookup"><span data-stu-id="2ac3c-113">DRM Protection and Content License Distribution</span></span>

<span data-ttu-id="2ac3c-114">На стороне создания технология управления цифровыми правами включает в себя два основных процесса: (1) Защита содержимого и (2) предоставление лицензий для содержимого.</span><span class="sxs-lookup"><span data-stu-id="2ac3c-114">On the creation side, digital rights management technology involves two main processes: (1) protecting the content and (2) providing licenses for the content.</span></span> <span data-ttu-id="2ac3c-115">Защита файла, по сути, включает шифрование содержимого и включает URL-адрес в заголовок файла, указывающий, где можно получить лицензию на содержимое.</span><span class="sxs-lookup"><span data-stu-id="2ac3c-115">Protecting a file basically involves encrypting the content, and including a URL in the file header that specifies where a license for the content may be obtained.</span></span> <span data-ttu-id="2ac3c-116">Если требуется защитить файлы с помощью, а затем распространить их на другие компьютеры или устройства, можно использовать пакет SDK Windows Media Format или пакет SDK диспетчера прав Windows Media для защиты файла.</span><span class="sxs-lookup"><span data-stu-id="2ac3c-116">If you want to protect files with and then distribute the files to other computers or devices, you can use either the Windows Media Format SDK or the Windows Media Rights Manager SDK to protect the file.</span></span> <span data-ttu-id="2ac3c-117">Для сценариев Live DRM необходимо использовать пакет SDK Windows Media Format для защиты содержимого при кодировании.</span><span class="sxs-lookup"><span data-stu-id="2ac3c-117">For live-DRM scenarios, you must use the Windows Media Format SDK to protect the content as it is being encoded.</span></span>

<span data-ttu-id="2ac3c-118">Чтобы создать и выдать лицензии для защищенного содержимого, можно создать собственное пользовательское решение с помощью объектов пакета SDK Windows Media Rights Manager или использовать службу, запущенную третьим лицом.</span><span class="sxs-lookup"><span data-stu-id="2ac3c-118">To create and issue licenses for protected content, you can create your own custom solution using the objects of the Windows Media Rights Manager SDK, or you can use a service run by a third party.</span></span>

<span data-ttu-id="2ac3c-119">Независимо от используемого метода, создаваемые защищенные файлы будут содержать в объекте заголовка DRM URL-адрес, указывающий клиентским приложениям, где можно получить лицензию на содержимое.</span><span class="sxs-lookup"><span data-stu-id="2ac3c-119">Whichever method you use, the protected files that you create will contain, in the DRM header object, a URL that tells client applications where to obtain a license for the content.</span></span>

> [!Note]  
> <span data-ttu-id="2ac3c-120">Пакет SDK для формата Windows Media не поддерживает создание или выдачу лицензий.</span><span class="sxs-lookup"><span data-stu-id="2ac3c-120">The Windows Media Format SDK does not provide support for creating or issuing licenses.</span></span>

 

<span data-ttu-id="2ac3c-121">На стороне воспроизведения приложение с поддержкой DRM должно иметь возможность получать лицензии для защищенного содержимого, расшифровывать его с помощью ключа, содержащегося в лицензии, и применять ограничения лицензии, например, сколько раз может быть воспроизведен файл, а также можно ли копировать файл на другое устройство.</span><span class="sxs-lookup"><span data-stu-id="2ac3c-121">On the playback side, a DRM-enabled application must be able to obtain licenses for protected content, to decrypt that content using the key contained in the license, and to enforce the license restrictions, such as the number of times a file may be played, or whether the file can be copied to another device.</span></span> <span data-ttu-id="2ac3c-122">Пакет Windows Media Format SDK предоставляет всю поддержку, необходимую для создания полностью включенного приложения для воспроизведения DRM.</span><span class="sxs-lookup"><span data-stu-id="2ac3c-122">The Windows Media Format SDK provides all the support required to create a fully enabled DRM playback application.</span></span>

> [!Note]  
> <span data-ttu-id="2ac3c-123">DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="2ac3c-123">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2ac3c-124">См. также</span><span class="sxs-lookup"><span data-stu-id="2ac3c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ac3c-125">**Функции цифровых Rights Management**</span><span class="sxs-lookup"><span data-stu-id="2ac3c-125">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="2ac3c-126">**Включение поддержки DRM**</span><span class="sxs-lookup"><span data-stu-id="2ac3c-126">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




