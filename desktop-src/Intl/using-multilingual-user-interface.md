---
description: Использование многоязыкового интерфейса пользователя
ms.assetid: caf167ad-f9a8-4093-9581-57bc507d1f6a
title: Использование многоязыкового интерфейса пользователя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287acc88d144c7775d2125cbb4a055784370d87f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272952"
---
# <a name="using-multilingual-user-interface"></a><span data-ttu-id="6ae65-103">Использование многоязыкового интерфейса пользователя</span><span class="sxs-lookup"><span data-stu-id="6ae65-103">Using Multilingual User Interface</span></span>

<span data-ttu-id="6ae65-104">В этом разделе описывается использование функций многоязыкового пользовательского интерфейса (MUI) для проектирования и реализации приложений.</span><span class="sxs-lookup"><span data-stu-id="6ae65-104">This section describes how to use Multilingual User Interface (MUI) functionality to design and implement your applications.</span></span> <span data-ttu-id="6ae65-105">Ниже приведены аспекты технологии MUI, которые будут воспроизводиться на большинстве этапов жизненного цикла приложения.</span><span class="sxs-lookup"><span data-stu-id="6ae65-105">The following are aspects of MUI technology that will come into play at most stages of the application lifecycle.</span></span>

-   <span data-ttu-id="6ae65-106">Разработка приложений, включая подготовку ресурсов, настройку языковых настроек приложения, Поиск и загрузку ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ae65-106">Application development, including resource preparation, setting of application language preferences, finding and loading of resources</span></span>
-   <span data-ttu-id="6ae65-107">Сборка и локализация приложения</span><span class="sxs-lookup"><span data-stu-id="6ae65-107">Building and localizing the application</span></span>
-   <span data-ttu-id="6ae65-108">Развертывание приложения</span><span class="sxs-lookup"><span data-stu-id="6ae65-108">Deploying the application</span></span>

<span data-ttu-id="6ae65-109">Ниже приведены некоторые вопросы, которые следует учитывать при проектировании и реализации приложения MUI.</span><span class="sxs-lookup"><span data-stu-id="6ae65-109">Here are some questions to consider when designing and implementing a MUI application.</span></span>

-   <span data-ttu-id="6ae65-110">Какие версии Windows будет поддерживать приложение?</span><span class="sxs-lookup"><span data-stu-id="6ae65-110">What are the versions of Windows that the application will support?</span></span>
-   <span data-ttu-id="6ae65-111">На каких языках будет локализовано приложение?</span><span class="sxs-lookup"><span data-stu-id="6ae65-111">In what languages will the application be localized?</span></span>
-   <span data-ttu-id="6ae65-112">Должны ли параметры языка приложения всегда соответствовать языковым параметрам операционной системы или пользователь приложения может устанавливать определенные языки?</span><span class="sxs-lookup"><span data-stu-id="6ae65-112">Should the application language settings always follow language settings for the operating system, or should the application user be able to set specific languages?</span></span>
-   <span data-ttu-id="6ae65-113">Какой тип ресурсов пользовательского интерфейса используется приложением и где они хранятся?</span><span class="sxs-lookup"><span data-stu-id="6ae65-113">What type of user interface resources does the application use and where are they stored?</span></span>

<span data-ttu-id="6ae65-114">Этот раздел содержит следующие темы.</span><span class="sxs-lookup"><span data-stu-id="6ae65-114">This section includes the following topics.</span></span> <span data-ttu-id="6ae65-115">В описаниях предполагается приложение MUI, предназначенное для Windows Vista и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="6ae65-115">The descriptions assume a MUI application targeted at Windows Vista and later.</span></span> <span data-ttu-id="6ae65-116">Ресурсы для этого приложения — это ресурсы Win32 с ресурсами, зависящими от языка, и исполняемым кодом, размещенным в отдельных файлах Win32 PE.</span><span class="sxs-lookup"><span data-stu-id="6ae65-116">The resources for this application are Win32 resources, with language-specific resources and executable code residing in separate Win32 PE files.</span></span> <span data-ttu-id="6ae65-117">При необходимости добавляются специальные рекомендации по поддержке операционных систем, предшествующих Windows Vista, или для различных типов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ae65-117">Special considerations for support of pre-Windows Vista operating systems or for different types of resources are added as appropriate.</span></span>

-   [<span data-ttu-id="6ae65-118">Подготовка ресурсов</span><span class="sxs-lookup"><span data-stu-id="6ae65-118">Preparing Resources</span></span>](preparing-resources.md)
-   [<span data-ttu-id="6ae65-119">Настройка языковых настроек приложения</span><span class="sxs-lookup"><span data-stu-id="6ae65-119">Setting Application Language Preferences</span></span>](setting-application-language-preferences.md)
-   [<span data-ttu-id="6ae65-120">Поиск ресурсов Win32 PE</span><span class="sxs-lookup"><span data-stu-id="6ae65-120">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
-   [<span data-ttu-id="6ae65-121">Поиск ресурсов, отличных от Win32 PE</span><span class="sxs-lookup"><span data-stu-id="6ae65-121">Locating Non-Win32 PE Resources</span></span>](locating-non-win32-pe-resources.md)
-   [<span data-ttu-id="6ae65-122">Локализация ресурсов и сборка приложения</span><span class="sxs-lookup"><span data-stu-id="6ae65-122">Localizing Resources and Building the Application</span></span>](localizing-resources-and-building-the-application.md)
-   [<span data-ttu-id="6ae65-123">MUI: пример приложения "Параметры системы"</span><span class="sxs-lookup"><span data-stu-id="6ae65-123">MUI: System Settings Application Sample</span></span>](mui-system-settings-application-sample.md)
-   [<span data-ttu-id="6ae65-124">MUI: пример параметров Application-Specific (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="6ae65-124">MUI: Application-Specific Settings Sample (Windows Vista)</span></span>](mui-application-specific-settings-sample-vista.md)
-   [<span data-ttu-id="6ae65-125">MUI: образец параметров Application-Specific (до Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="6ae65-125">MUI: Application-Specific Settings Sample (Pre-Windows Vista)</span></span>](mui-application-specific-settings-sample-pre-vista.md)

 

 



