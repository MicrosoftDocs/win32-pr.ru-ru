---
title: Чтение защищенных файлов
description: Чтение защищенных файлов
ms.assetid: 24f839f1-ce57-4d06-b1a5-a6bea7b5b7bb
keywords:
- Windows Media Format SDK, чтение защищенных файлов
- Windows Media Format SDK, защищенные файлы
- Расширенный формат систем (ASF), чтение защищенных файлов
- ASF (Расширенный системный формат), чтение защищенных файлов
- Расширенный формат систем (ASF), защищенные файлы
- ASF (Расширенный системный формат), защищенные файлы
- Расширенный системный формат (ASF), Вмстубдрм. lib
- ASF (Расширенный системный формат), Вмстубдрм. lib
- Вмстубдрм. lib, чтение защищенных файлов
- Вмстубдрм. lib, защищенные файлы
- Управление цифровыми правами (DRM), Вмстубдрм. lib
- DRM (Управление цифровыми правами), Вмстубдрм. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b2110708a28daae1e86ba3dac2ea1f18ad16fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788695"
---
# <a name="reading-protected-files"></a><span data-ttu-id="09548-115">Чтение защищенных файлов</span><span class="sxs-lookup"><span data-stu-id="09548-115">Reading Protected Files</span></span>

<span data-ttu-id="09548-116">Чтение защищенного с помощью DRM файла или сетевого потока, по сути, включает в себя попытку открыть файл (или подключиться к потоку), а затем обработать все события, которые могут быть отправлены из компонентов DRM.</span><span class="sxs-lookup"><span data-stu-id="09548-116">Reading a DRM-protected file or network stream basically involves attempting to open the file (or connect to the stream) and then handling any events that might be sent from the DRM components.</span></span>

<span data-ttu-id="09548-117">Если проигрыватель не поддерживает DRM (не имеет ссылки на допустимую библиотеку вмстубдрм. lib), вызов [**ивмреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) завершается ошибкой, когда пытается открыть защищенный файл и возвращает \_ содержимое, защищенное с помощью NS E, \_ \_ или связанная ошибка.</span><span class="sxs-lookup"><span data-stu-id="09548-117">If a player is not DRM-enabled (does not link to a valid wmstubdrm.lib library) the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) call fails when it tries to open a protected file and returns NS\_E\_PROTECTED\_CONTENT or some related error.</span></span>

<span data-ttu-id="09548-118">Когда приложение с поддержкой DRM пытается открыть защищенный DRM файл, компонент DRM автоматически выполняет поиск действительной лицензии в локальной системе.</span><span class="sxs-lookup"><span data-stu-id="09548-118">When a DRM-enabled application attempts to open a DRM-protected file, the DRM component automatically searches the local system for a valid license.</span></span> <span data-ttu-id="09548-119">Если он найден, компонент DRM автоматически расшифровывает файл способом, который полностью прозрачен для приложения.</span><span class="sxs-lookup"><span data-stu-id="09548-119">If one is found, the DRM component automatically decrypts the file in a way that is completely transparent to the application.</span></span> <span data-ttu-id="09548-120">Действие, которое приложение может выполнить в расшифрованном файле, зависит от прав, указанных в лицензии.</span><span class="sxs-lookup"><span data-stu-id="09548-120">The action that an application may perform on the decrypted file depends on the rights specified in the license.</span></span> <span data-ttu-id="09548-121">Полное описание возможных прав см. в документации по пакету SDK для диспетчера прав Windows Media.</span><span class="sxs-lookup"><span data-stu-id="09548-121">For a full description of possible rights, see the Windows Media Rights Manager SDK documentation.</span></span>

<span data-ttu-id="09548-122">Если у приложения нет действительной лицензии для файла, проигрыватель получает уведомление о состоянии от компонента DRM.</span><span class="sxs-lookup"><span data-stu-id="09548-122">If the application does not have a valid license for a file, the player receives a status notification from the DRM component.</span></span> <span data-ttu-id="09548-123">Затем приложение проигрывателя может инициировать процесс [*получения лицензии*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="09548-123">The player application can then initiate the [*license acquisition*](wmformat-glossary.md) process.</span></span> <span data-ttu-id="09548-124">После получения действительной лицензии файл доступен.</span><span class="sxs-lookup"><span data-stu-id="09548-124">After a valid license has been received, the file can be accessed.</span></span> <span data-ttu-id="09548-125">В следующих разделах описаны основные задачи, которые необходимо выполнить приложению при реализации процесса получения лицензии.</span><span class="sxs-lookup"><span data-stu-id="09548-125">The following sections describe the basic tasks that an application must perform in implementing the license acquisition process:</span></span>

-   [<span data-ttu-id="09548-126">Указание действий для выполнения</span><span class="sxs-lookup"><span data-stu-id="09548-126">Specifying the Actions To Be Performed</span></span>](specifying-the-actions-to-be-performed.md)
-   [<span data-ttu-id="09548-127">Обработка событий приобретения лицензий</span><span class="sxs-lookup"><span data-stu-id="09548-127">Handling License Acquisition Events</span></span>](handling-license-acquisition-events.md)
-   [<span data-ttu-id="09548-128">Приложения DRM индивидуализинг</span><span class="sxs-lookup"><span data-stu-id="09548-128">Individualizing DRM Applications</span></span>](individualizing-drm-applications.md)
-   [<span data-ttu-id="09548-129">Обработка событий индивидуализации</span><span class="sxs-lookup"><span data-stu-id="09548-129">Handling Individualization Events</span></span>](handling-individualization-events.md)

> [!Note]  
> <span data-ttu-id="09548-130">DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="09548-130">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="09548-131">См. также</span><span class="sxs-lookup"><span data-stu-id="09548-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09548-132">**Функции цифровых Rights Management**</span><span class="sxs-lookup"><span data-stu-id="09548-132">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="09548-133">**Список атрибутов DRM**</span><span class="sxs-lookup"><span data-stu-id="09548-133">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="09548-134">**Свойства DRM**</span><span class="sxs-lookup"><span data-stu-id="09548-134">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="09548-135">**Включение поддержки DRM**</span><span class="sxs-lookup"><span data-stu-id="09548-135">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




