---
description: Поддержка прокси-сервера для сетевых источников
ms.assetid: e739746d-2a09-4237-a7c1-0aed4e4516d7
title: Поддержка прокси-сервера для сетевых источников
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97bc1172c072a54f9f76cbcd3a297a972efbde29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692584"
---
# <a name="proxy-support-for-network-sources"></a><span data-ttu-id="564ec-103">Поддержка прокси-сервера для сетевых источников</span><span class="sxs-lookup"><span data-stu-id="564ec-103">Proxy Support for Network Sources</span></span>

<span data-ttu-id="564ec-104">Прокси-сервер — это промежуточный сервер между интрасетью и Интернетом, который направляет запросы от клиентского приложения на сервер мультимедиа и извлекает файлы с сервера мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="564ec-104">A proxy server is an intermediate server between your intranet and the Internet, which routes requests from the client application to the media server and retrieves files from the media server.</span></span>

<span data-ttu-id="564ec-105">Media Foundation неявно создает объект *-Локатор прокси* , когда клиентское приложение пытается получить доступ к URL-адресу источника.</span><span class="sxs-lookup"><span data-stu-id="564ec-105">Media Foundation implicitly creates a *proxy locator* object when a client application tries to access a source URL.</span></span> <span data-ttu-id="564ec-106">Объект-указатель прокси предоставляет интерфейс [**имфнетпроксилокатор**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="564ec-106">The proxy locator object exposes the [**IMFNetProxyLocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) interface.</span></span> <span data-ttu-id="564ec-107">Во время разрешения источника Media Foundation проверяет хранилище свойств, переданное в метод сопоставителя источника.</span><span class="sxs-lookup"><span data-stu-id="564ec-107">During source resolution, Media Foundation checks the property store passed to the source resolver method.</span></span>

<span data-ttu-id="564ec-108">Если хранилище свойств содержит свойство [мфнетсаурце \_ проксилокаторфактори](mfnetsource-proxylocatorfactory-property.md) , для которого задан объект фабрики локатора прокси-сервера, реализуемый приложением, то он вызывает метод [**имфнетпроксилокаторфактори:: креатепроксилокатор**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) , чтобы создать локатор прокси-сервера с настраиваемыми параметрами конфигурации.</span><span class="sxs-lookup"><span data-stu-id="564ec-108">If the property store contains the [MFNETSOURCE\_PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) property set to a proxy locator factory object implemented by the application then, it invokes the [**IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) method to create a proxy locator with custom configuration settings.</span></span>

<span data-ttu-id="564ec-109">Если хранилище свойств не задано, Media Foundation создает прокси-локатор с конфигурацией по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="564ec-109">If the property store is not set, then Media Foundation creates the proxy locator with default configuration.</span></span> <span data-ttu-id="564ec-110">Ниже приведены эти параметры.</span><span class="sxs-lookup"><span data-stu-id="564ec-110">These settings are as follows:</span></span>

-   <span data-ttu-id="564ec-111">Если задана политика пользователя, локатор прокси-сервера использует параметры, заданные в реестре.</span><span class="sxs-lookup"><span data-stu-id="564ec-111">If user policy is set, then the proxy locator uses settings specified in the registry.</span></span>

-   <span data-ttu-id="564ec-112">Для HTTP локатор прокси-сервера использует параметры прокси-сервера браузера.</span><span class="sxs-lookup"><span data-stu-id="564ec-112">For HTTP, the proxy locator uses browser proxy settings.</span></span>

-   <span data-ttu-id="564ec-113">В случае с протоколом RTSP локатор прокси-сервера настроен для обхода прокси-серверов при подключении к серверу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="564ec-113">For RTSP, the proxy locator is configured to bypass proxy servers when connecting to the media server.</span></span>

<span data-ttu-id="564ec-114">Эта конфигурация по умолчанию может быть изменена приложением.</span><span class="sxs-lookup"><span data-stu-id="564ec-114">This default configuration can be changed by the application.</span></span> <span data-ttu-id="564ec-115">Следующие разделы содержат сведения о параметрах конфигурации для локатора прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="564ec-115">The following topics contain information about the configuration settings for a proxy locator:</span></span>

-   [<span data-ttu-id="564ec-116">Параметры конфигурации локатора прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="564ec-116">Proxy Locator Configuration Settings</span></span>](proxy-locator-configuration-settings.md)

-   [<span data-ttu-id="564ec-117">Настройка локатора прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="564ec-117">How to Configure the Proxy Locator</span></span>](how-to-configure-the-proxy-locator.md)

<span data-ttu-id="564ec-118">Media Foundation инициализирует локатор прокси-сервера для URL-адреса источника, указанного для [сопоставителя источника](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="564ec-118">Media Foundation initializes the proxy locator for the source URL specified to the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="564ec-119">Локатор прокси-сервера обнаруживает используемый прокси-сервер на основе параметров конфигурации.</span><span class="sxs-lookup"><span data-stu-id="564ec-119">The proxy locator detects a proxy server to use based on configuration settings.</span></span> <span data-ttu-id="564ec-120">Когда локатор прокси-сервера пытается установить прокси-сервер, он записывает в реестр результаты успешного или неуспешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="564ec-120">When the proxy locator attempts the set a proxy server, it records the success or failure result in the registry.</span></span> <span data-ttu-id="564ec-121">Это значение проверяется во время следующего процесса обнаружения прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="564ec-121">This value is checked during the next proxy detection process.</span></span> <span data-ttu-id="564ec-122">Если известно, что на определенном прокси-сервере возникают сбои в прошлом, локатор прокси пропускает его.</span><span class="sxs-lookup"><span data-stu-id="564ec-122">If a certain proxy server is known to have caused failures in the past, the proxy locator skips it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="564ec-123">См. также</span><span class="sxs-lookup"><span data-stu-id="564ec-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="564ec-124">Атрибуты и свойства</span><span class="sxs-lookup"><span data-stu-id="564ec-124">Attributes and Properties</span></span>](attributes-and-properties.md)
</dt> <dt>

[<span data-ttu-id="564ec-125">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="564ec-125">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



