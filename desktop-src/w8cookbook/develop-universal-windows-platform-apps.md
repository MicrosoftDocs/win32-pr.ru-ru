---
title: Разработка приложений универсальная платформа Windows (UWP)
description: Разработка приложений универсальная платформа Windows (UWP)
ms.assetid: 215256D7-CBBA-43B0-A99C-490A25D1F82C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3654c1c8773a813fcc7f88b21a86c2ef6049184
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "105710245"
---
# <a name="develop-universal-windows-platform-uwp-apps"></a><span data-ttu-id="0f02c-103">Разработка приложений универсальная платформа Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="0f02c-103">Develop Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="0f02c-104">Мы рекомендуем поставщикам программных продуктов для настольных систем (Win32) переносить классические приложения в [универсальная платформа Windows (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) через мост рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="0f02c-104">We encourage all desktop (Win32) app ISVs to bring your desktop apps to the [Universal Windows Platform (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) via the Desktop Bridge.</span></span> <span data-ttu-id="0f02c-105">Приложения UWP также поддерживаются [Магазином Windows](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/), чтобы вы могли предоставлять пользователям обновленные версии приложений в автоматическом режиме, снижая расходы на поддержку.</span><span class="sxs-lookup"><span data-stu-id="0f02c-105">UWP apps are also supported in the [Windows Store](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/), so it’s easier for you to update your users to a consistent version automatically, lowering your support costs.</span></span>

<span data-ttu-id="0f02c-106">Если классические приложения нельзя преобразовать с помощью моста для настольных систем, настоятельно рекомендуется использовать установщик, который следует рекомендациям, и убедиться, что он полностью протестирован.</span><span class="sxs-lookup"><span data-stu-id="0f02c-106">If your desktop apps cannot be converted using the Desktop Bridge, we highly recommend that you use an installer that follows best practices, and ensure this is fully tested.</span></span> <span data-ttu-id="0f02c-107">Установщик — это ваш пользователь или первый интерфейс пользователя в приложении.</span><span class="sxs-lookup"><span data-stu-id="0f02c-107">An installer is your user or customer's first experience with your app.</span></span> <span data-ttu-id="0f02c-108">Слишком часто он работает некорректно или тестируется недостаточно тщательно и не для всех случаев использования.</span><span class="sxs-lookup"><span data-stu-id="0f02c-108">All too often, this doesn’t work well or it hasn’t been fully tested for all scenarios.</span></span> <span data-ttu-id="0f02c-109">[Комплект сертификации приложений для Windows](https://dev.windows.com/develop/app-certification-kit) поможет вам протестировать установку и удаление приложения Win32 и помочь вам определить использование недокументированных API, а также другие основные проблемы, связанные с производительностью, прежде чем пользователи будут работать.</span><span class="sxs-lookup"><span data-stu-id="0f02c-109">The [Windows App Certification Kit](https://dev.windows.com/develop/app-certification-kit) can help you test install and uninstall of your Win32 app and help you identify use of undocumented APIs, as well as other basic performance-related best-practice issues before your users do.</span></span>

## <a name="best-practices"></a><span data-ttu-id="0f02c-110">Рекомендации.</span><span class="sxs-lookup"><span data-stu-id="0f02c-110">Best practices:</span></span>

-   <span data-ttu-id="0f02c-111">Используйте установщики, которые работают в среде как 32-, так и 64-разрядных версий Windows.</span><span class="sxs-lookup"><span data-stu-id="0f02c-111">Use installers that work for both 32-bit and 64-bit versions of Windows.</span></span>
-   <span data-ttu-id="0f02c-112">Проектируйте установщики с учетом возможности их запуска разными способами (пользователем или в автоматическом режиме).</span><span class="sxs-lookup"><span data-stu-id="0f02c-112">Design your installers to run on multiple scenarios (user or machine level).</span></span>
-   <span data-ttu-id="0f02c-113">Храните все распространяемые компоненты Windows в исходном пакете — в случае перепаковки этих компонентов установщик может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="0f02c-113">Keep all Windows redistributables in the original packaging – if you repackage these, it’s possible that this will break the installer.</span></span>
-   <span data-ttu-id="0f02c-114">Разрабатывайте установщики в соответствии с расписанием — разработчики часто забывают добавлять установщики в состав пакета поставки программного продукта в ходе жизненного цикла разработки ПО.</span><span class="sxs-lookup"><span data-stu-id="0f02c-114">Schedule development time for your installers—these are often overlooked as a deliverable during the software development lifecycle.</span></span>

 

 




