---
title: Приложения DRM индивидуализинг
description: Приложения DRM индивидуализинг
ms.assetid: 8d87c663-bc54-4928-9eee-d09c358e61f8
keywords:
- Windows Media Format SDK, приложения индивидуализинг DRM
- Пакет SDK для Windows Media Format, индивидуализинг приложений
- Расширенный системный формат (ASF), индивидуализинг приложения DRM
- ASF (Расширенный системный формат), приложения DRM индивидуализинг
- Расширенный системный формат (ASF), индивидуализинг приложений
- ASF (Расширенный системный формат), индивидуализинг приложений
- Управление цифровыми правами (DRM), приложения индивидуализинг
- DRM (Управление цифровыми правами), приложения индивидуализинг
- Управление цифровыми правами (DRM), индивидуализинг приложений
- DRM (Управление цифровыми правами), индивидуализинг приложений
- индивидуализинг приложения
- приложения DRM индивидуализинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c3fc0166332c52e39fc0882238fa9009aa0cc1
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "103987266"
---
# <a name="individualizing-drm-applications"></a><span data-ttu-id="6ec19-115">Приложения DRM индивидуализинг</span><span class="sxs-lookup"><span data-stu-id="6ec19-115">Individualizing DRM Applications</span></span>

<span data-ttu-id="6ec19-116">Для повышения безопасности компонент DRM приложений может быть *индивидуальным*.</span><span class="sxs-lookup"><span data-stu-id="6ec19-116">To increase security, the DRM component of applications can be *individualized*.</span></span> <span data-ttu-id="6ec19-117">Отдельное приложение — это одно из приложений, которое получило обновление до компонентов DRM, которое отличает его от всех остальных копий того же приложения.</span><span class="sxs-lookup"><span data-stu-id="6ec19-117">An individualized application is one that has received an upgrade to its DRM components that differentiates it from all other copies of the same application.</span></span> <span data-ttu-id="6ec19-118">Владельцы содержимого могут потребовать, чтобы их защищенные файлы воспроизводились только в приложении, которое было индивидуальным.</span><span class="sxs-lookup"><span data-stu-id="6ec19-118">Content owners can require that their protected files be played only on an application that has been individualized.</span></span>

<span data-ttu-id="6ec19-119">Процесс индивидуализации начинается, когда приложение обращается к службе Microsoft индивидуализации, которая затем устанавливает обновление системы безопасности на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="6ec19-119">The individualization process starts when the application contacts the Microsoft Individualization Service, which then installs a security upgrade on the user's computer.</span></span> <span data-ttu-id="6ec19-120">Поскольку служба индивидуализации обрабатывает сведения от пользователя, необходимо отобразить политику конфиденциальности Майкрософт или указать ссылку на эту страницу на веб-сайте Майкрософт: <https://privacy.microsoft.com/privacystatement> .</span><span class="sxs-lookup"><span data-stu-id="6ec19-120">Because the Individualization Service handles information from the user, you must display the Microsoft privacy policy or provide a link to that page at the Microsoft Web site: <https://privacy.microsoft.com/privacystatement>.</span></span>

<span data-ttu-id="6ec19-121">Индивидуальная настройка может быть выполнена различными способами.</span><span class="sxs-lookup"><span data-stu-id="6ec19-121">Individualization can be accomplished in different ways.</span></span> <span data-ttu-id="6ec19-122">Например, если пользователь воспроизводит защищенный файл, может быть выполнена отдельная Индивидуальная защита.</span><span class="sxs-lookup"><span data-stu-id="6ec19-122">For example, individualization can take place when a user plays a protected file.</span></span> <span data-ttu-id="6ec19-123">Запрос лицензии отправляется в [*службу лицензирования Windows Media*](wmformat-glossary.md), которая проверяет сертификат приложения, запрашивающего [*лицензию*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="6ec19-123">The license request is sent to the [*Windows Media License Service*](wmformat-glossary.md), which inspects the certificate of the application requesting the [*license*](wmformat-glossary.md).</span></span> <span data-ttu-id="6ec19-124">Если компонент DRM приложения не является индивидуальным, служба лицензирования Windows Media отказывается выдавать лицензию, поскольку она является политикой службы лицензирования Windows Media, выдавать лицензии только отдельным игрокам.</span><span class="sxs-lookup"><span data-stu-id="6ec19-124">If the DRM component of the application has not been individualized, Windows Media License Service refuses to issue the license, because it is the policy of Windows Media License Service to issue licenses only to individualized players.</span></span> <span data-ttu-id="6ec19-125">Приложение может уведомить пользователя о необходимости обновления приложения.</span><span class="sxs-lookup"><span data-stu-id="6ec19-125">The application can then notify the user that the application must be upgraded.</span></span> <span data-ttu-id="6ec19-126">Если пользователь согласен, для индивидуализируйте компонента DRM приложения предоставляется обновление системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="6ec19-126">If the user agrees, a security upgrade is provided to individualize the DRM component of the application.</span></span>

<span data-ttu-id="6ec19-127">Для повышения удобства работы пользователей можно запустить процесс индивидуализации в качестве этапа обновления системы безопасности во время установки. После этого пользователь не прерывается для получения обновления системы безопасности при попытке воспроизведения защищенного файла.</span><span class="sxs-lookup"><span data-stu-id="6ec19-127">For a better user experience, you can initiate the individualization process as a security upgrade step during setup; then the user is not interrupted to get a security upgrade while trying to play a protected file.</span></span> <span data-ttu-id="6ec19-128">Кроме того, можно активно рекомендовать индивидуальную возможность, добавив к приложению команду меню **обновления безопасности** или кнопку.</span><span class="sxs-lookup"><span data-stu-id="6ec19-128">You can also actively encourage individualization by adding a **Security Upgrade** menu command or button to the application.</span></span>

> [!Note]  
> <span data-ttu-id="6ec19-129">DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="6ec19-129">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6ec19-130">См. также</span><span class="sxs-lookup"><span data-stu-id="6ec19-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ec19-131">**Функции цифровых Rights Management**</span><span class="sxs-lookup"><span data-stu-id="6ec19-131">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="6ec19-132">**Включение поддержки DRM**</span><span class="sxs-lookup"><span data-stu-id="6ec19-132">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




