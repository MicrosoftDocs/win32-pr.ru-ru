---
title: Работа со списками отзыва
description: Работа со списками отзыва
ms.assetid: 4463abb5-f48f-484f-b837-512313572c0a
keywords:
- Пакет Windows Media Format SDK, списки отзыва
- Расширенный формат систем (ASF), списки отзыва
- ASF (Расширенный системный формат), списки отзыва
- списки отзыва
- Управление цифровыми правами (DRM), списки отзыва
- DRM (Управление цифровыми правами), списки отзыва
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f4eca82dd82c9225406a85034ff2a6df227fce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104532963"
---
# <a name="working-with-revocation-lists"></a><span data-ttu-id="165e4-109">Работа со списками отзыва</span><span class="sxs-lookup"><span data-stu-id="165e4-109">Working with Revocation Lists</span></span>

<span data-ttu-id="165e4-110">Для реагирования на нарушения безопасности и обеспечения того, что приложения проигрывателя, которые должны быть повреждены или скомпрометированы, не могут воспроизводить или использовать защищенные файлы, каждая выданная лицензия содержит список отзыва.</span><span class="sxs-lookup"><span data-stu-id="165e4-110">To respond to security breaches and to ensure that player applications known to be broken or compromised cannot play or use protected files, each license that is issued contains a revocation list.</span></span> <span data-ttu-id="165e4-111">Список отзыва содержит сертификаты приложений для всех приложений проигрывателя, известных для нарушения или повреждения.</span><span class="sxs-lookup"><span data-stu-id="165e4-111">A revocation list contains the application certificates of all those player applications known to be broken or corrupted.</span></span> <span data-ttu-id="165e4-112">При получении новой лицензии компонент DRM приложения Player проверяет список отзыва.</span><span class="sxs-lookup"><span data-stu-id="165e4-112">When a new license is received, the DRM component of the player application checks for a revocation list.</span></span> <span data-ttu-id="165e4-113">Если найден один из более новых версий, чем тот, который находится на компьютере, будет сохранен новый список.</span><span class="sxs-lookup"><span data-stu-id="165e4-113">If one is found that is newer than the one currently on the computer, the newer list is stored.</span></span> <span data-ttu-id="165e4-114">В следующий раз, когда потребитель воспроизводит защищенный ASF-файл, компонент DRM сравнивает приложение проигрывателя со списком отзыва.</span><span class="sxs-lookup"><span data-stu-id="165e4-114">The next time the consumer plays a protected ASF file, the DRM component compares the player application to the revocation list.</span></span> <span data-ttu-id="165e4-115">Если приложение проигрывателя отменяется, компонент DRM отправляет приложению сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="165e4-115">If the player application is revoked, the DRM component sends an error message to the application.</span></span>

<span data-ttu-id="165e4-116">Приложения проигрывателя могут получить сообщение об ошибке отзыва в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="165e4-116">Player applications can receive a revocation error message in the following scenarios:</span></span>

-   <span data-ttu-id="165e4-117">Сообщение об ошибке получается после того, как приложение вызовет метод [**ивмдрмреадер:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) для защищенного файла.</span><span class="sxs-lookup"><span data-stu-id="165e4-117">The error message is received after the application calls the [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) method for a protected file.</span></span> <span data-ttu-id="165e4-118">Вызов завершается ошибкой с кодом **HRESULT** NS \_ E \_ DRM \_ аппцерт \_ , который предоставляется функции обратного вызова **OnStatus** с ВМТ \_ получения \_ состояния лицензии.</span><span class="sxs-lookup"><span data-stu-id="165e4-118">The call fails with the **HRESULT** code NS\_E\_DRM\_APPCERT\_REVOKED, which is supplied to the **OnStatus** callback function with WMT\_ACQUIRE\_LICENSE status.</span></span> <span data-ttu-id="165e4-119">Если этот код **HRESULT** не учитывается, то ошибки продолжают возникать.</span><span class="sxs-lookup"><span data-stu-id="165e4-119">If this **HRESULT** code is ignored, errors will continue to occur.</span></span>
-   <span data-ttu-id="165e4-120">Сообщение об ошибке получается, когда приложение создает модуль чтения с поддержкой DRM и вызывает метод [**ивмреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) для защищенного файла.</span><span class="sxs-lookup"><span data-stu-id="165e4-120">The error message is received when the application creates the DRM-enabled reader and calls the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method for a protected file.</span></span> <span data-ttu-id="165e4-121">Вызов завершается ошибкой с кодом **HRESULT** NS \_ E \_ DRM \_ аппцерт \_ REVOKE, который передается в метод обратного вызова [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) с \_ состоянием ВМТ Opened.</span><span class="sxs-lookup"><span data-stu-id="165e4-121">The call fails with the **HRESULT** code NS\_E\_DRM\_APPCERT\_REVOKED, which is supplied to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method with WMT\_OPENED status.</span></span> <span data-ttu-id="165e4-122">Когда приложение Player получает это сообщение об ошибке, оно должно уведомлять пользователей и предоставить способ восстановления функций проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="165e4-122">When a player application receives this error message, the application should notify end users and provide a way for them to restore functionality to their player.</span></span> <span data-ttu-id="165e4-123">Например, приложение может открыть URL-адрес, по которому конечные пользователи могут загрузить обновление для скомпрометированного приложения.</span><span class="sxs-lookup"><span data-stu-id="165e4-123">For example, the application can open a URL where end users can download an upgrade for the compromised application.</span></span>

<span data-ttu-id="165e4-124">**Примечание** . DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="165e4-124">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="165e4-125">См. также</span><span class="sxs-lookup"><span data-stu-id="165e4-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="165e4-126">**Функции цифровых Rights Management**</span><span class="sxs-lookup"><span data-stu-id="165e4-126">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="165e4-127">**Обработка событий приобретения лицензий**</span><span class="sxs-lookup"><span data-stu-id="165e4-127">**Handling License Acquisition Events**</span></span>](handling-license-acquisition-events.md)
</dt> </dl>

 

 




