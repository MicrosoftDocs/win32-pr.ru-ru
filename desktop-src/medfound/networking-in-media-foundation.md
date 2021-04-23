---
description: Сетевые подключения в Media Foundation
ms.assetid: 59eec612-3b6d-400c-8190-1ae8675a2e1b
title: Сетевые подключения в Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3aff68ee1f9e124cda5dd01e82192078b41b0de
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914044"
---
# <a name="networking-in-media-foundation"></a><span data-ttu-id="d1e80-103">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d1e80-103">Networking in Media Foundation</span></span>

<span data-ttu-id="d1e80-104">Приложения на основе Media Foundation могут воспроизводить источники мультимедиа по сети.</span><span class="sxs-lookup"><span data-stu-id="d1e80-104">Applications based on Media Foundation can play media sources over a network.</span></span> <span data-ttu-id="d1e80-105">Для приложения процесс аналогичен воспроизведению из локального файла.</span><span class="sxs-lookup"><span data-stu-id="d1e80-105">For the application, the process is similar to playing from a local file.</span></span>



| <span data-ttu-id="d1e80-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="d1e80-106">Topic</span></span>                                                                                      | <span data-ttu-id="d1e80-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d1e80-107">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1e80-108">Компоненты сетевого источника</span><span class="sxs-lookup"><span data-stu-id="d1e80-108">Network Source Features</span></span>](network-source-features.md)                                     | <span data-ttu-id="d1e80-109">Описание функций, поддерживаемых сетевым источником и связанными параметрами конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d1e80-109">Describes the features supported by the network source and the associated configuration options.</span></span>                                        |
| [<span data-ttu-id="d1e80-110">Поддержка прокси-сервера для сетевых источников</span><span class="sxs-lookup"><span data-stu-id="d1e80-110">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)                 | <span data-ttu-id="d1e80-111">Предоставляет сведения об использовании объекта локатора прокси-сервера, определяющего прокси-сервер, используемый при соединении с сервером.</span><span class="sxs-lookup"><span data-stu-id="d1e80-111">Provides information about using the proxy locator object that determines the proxy to use when connecting to a server.</span></span>                 |
| [<span data-ttu-id="d1e80-112">Проверка подлинности источника сети</span><span class="sxs-lookup"><span data-stu-id="d1e80-112">Network Source Authentication</span></span>](network-source-authentication.md)                         | <span data-ttu-id="d1e80-113">Предоставляет сведения об использовании компонентов проверки подлинности, таких как кэш учетных данных и диспетчер учетных данных.</span><span class="sxs-lookup"><span data-stu-id="d1e80-113">Provides information about using the authentication components such as the credential cache and the credential manager.</span></span>                 |
| [<span data-ttu-id="d1e80-114">Получение событий из сетевого источника</span><span class="sxs-lookup"><span data-stu-id="d1e80-114">How to Get Events from the Network Source</span></span>](how-to-get-events-from-the-network-source.md) | <span data-ttu-id="d1e80-115">Содержит сведения о получении Media Foundation событий во время открытия соединения и перед созданием сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="d1e80-115">Provides information about getting Media Foundation events during the opening of a connection and before the network source is created.</span></span> |
| [<span data-ttu-id="d1e80-116">Поддерживаемые протоколы</span><span class="sxs-lookup"><span data-stu-id="d1e80-116">Supported Protocols</span></span>](supported-protocols.md)                                             | <span data-ttu-id="d1e80-117">Описание протоколов, поддерживаемых сетевым источником.</span><span class="sxs-lookup"><span data-stu-id="d1e80-117">Describes the protocols that are supported by the network source.</span></span> <span data-ttu-id="d1e80-118">Кроме того, предоставляет сведения о процедуре смены протокола.</span><span class="sxs-lookup"><span data-stu-id="d1e80-118">Also, provides information about the protocol rollover procedure.</span></span>     |
| [<span data-ttu-id="d1e80-119">Ведение журнала клиента</span><span class="sxs-lookup"><span data-stu-id="d1e80-119">Client Logging</span></span>](client-logging.md)                                                       | <span data-ttu-id="d1e80-120">Описывает поля ведения журнала клиента, которые может настроить приложение, и способ получения сетевой статистики.</span><span class="sxs-lookup"><span data-stu-id="d1e80-120">Describes the client logging fields that the application can configure and how it can retrieve network statistics.</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="d1e80-121">См. также</span><span class="sxs-lookup"><span data-stu-id="d1e80-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1e80-122">Media Foundationое программное руководством</span><span class="sxs-lookup"><span data-stu-id="d1e80-122">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="d1e80-123">Источники мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d1e80-123">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="d1e80-124">Использование источников мультимедиа с сеансом мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d1e80-124">Using Media Sources with the Media Session</span></span>](using-media-sources-with-the-media-session.md)
</dt> </dl>

 

 



