---
title: Справочник по API EAPHost
description: Узнайте об API-интерфейсах EAPHost и их компонентах. См. справочные сведения по различным темам API, таким как схема EAPHost XML.
ms.assetid: ac2f074f-b525-42a2-8637-c96a08d77714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c4d80c402f963a05bbcfb79ca451541603489e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413700"
---
# <a name="eaphost-api-reference"></a><span data-ttu-id="e2904-104">Справочник по API EAPHost</span><span class="sxs-lookup"><span data-stu-id="e2904-104">EAPHost API Reference</span></span>

<span data-ttu-id="e2904-105">API-интерфейсы EAPHost делятся на три компонента: интерфейсы API, которые непосредственно вызываются из приложения с поддержкой EAP; API однорангового метода EAP, которые управляют запросами на отправитель для конкретного типа проверки подлинности EAP и вызывают Интерактивные элементы на клиенте; и API-интерфейсы проверки подлинности EAP, которые выполняют аутентификацию на стороне сервера для запрашивающей стороны.</span><span class="sxs-lookup"><span data-stu-id="e2904-105">The EAPHost APIs are divided into three components: the supplicant APIs, which are directly callable from an EAP-enabled application; the EAP peer method APIs, which manage supplicant requests for a specific EAP authentication type and raise interactive elements on the client; and the EAP authenticator APIS, which perform the server-side authentication of a supplicant.</span></span>

<span data-ttu-id="e2904-106">Последние два компонента API — метод однорангового узла EAP и API метода проверки подлинности EAP — требуются пользовательские и согласованные реализации в библиотеках DLL, которые предоставляют их службе EAPHost.</span><span class="sxs-lookup"><span data-stu-id="e2904-106">The latter two API components -- the EAP Peer Method and EAP Authenticator Method APIs -- require custom and conformant implementation in DLLs that expose them to the EAPHost service.</span></span> <span data-ttu-id="e2904-107">Их нельзя вызывать непосредственно из кода приложения; Вместо этого они вызываются с помощью EAPHost (на стороне клиента для методов соединения EAP и на стороне сервера для методов проверки подлинности EAP), если реализация соответствует сигнатурам API, указанным в соответствующей документации.</span><span class="sxs-lookup"><span data-stu-id="e2904-107">They cannot be called directly from application code; instead, they are called by EAPHost (on client side for EAP peer methods, and on the server side for EAP authenticator methods) if the implementation matches the API signatures specified in the corresponding documentation.</span></span> <span data-ttu-id="e2904-108">Конкретная информация о реализации API предоставляется на каждой странице справки по функциям.</span><span class="sxs-lookup"><span data-stu-id="e2904-108">API implementation specific information is provided on each function reference page.</span></span>

## <a name="eaphost-registry-settings"></a><span data-ttu-id="e2904-109">Параметры реестра EAPHost</span><span class="sxs-lookup"><span data-stu-id="e2904-109">EAPHost Registry Settings</span></span>



| <span data-ttu-id="e2904-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="e2904-110">Topic</span></span>                                                      | <span data-ttu-id="e2904-111">Описание</span><span class="sxs-lookup"><span data-stu-id="e2904-111">Description</span></span>                                      |
|------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="e2904-112">Параметры реестра EAPHost</span><span class="sxs-lookup"><span data-stu-id="e2904-112">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md) | <span data-ttu-id="e2904-113">Описывает разделы реестра, используемые EAPHost.</span><span class="sxs-lookup"><span data-stu-id="e2904-113">Describes the registry keys consumed by EAPHost.</span></span> |



 

## <a name="eaphost-xml-schema"></a><span data-ttu-id="e2904-114">Схема XML EAPHost</span><span class="sxs-lookup"><span data-stu-id="e2904-114">EAPHost XML Schema</span></span>



| <span data-ttu-id="e2904-115">Раздел</span><span class="sxs-lookup"><span data-stu-id="e2904-115">Topic</span></span>                                            | <span data-ttu-id="e2904-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e2904-116">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2904-117">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="e2904-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md) | <span data-ttu-id="e2904-118">Описывает схему EAPHost и устаревшую схему для создания XML-кода конфигурации и XML-кода учетных данных.</span><span class="sxs-lookup"><span data-stu-id="e2904-118">Describes the EAPHost schema and legacy schema for creating configuration XML and credential XML.</span></span> |



 

## <a name="common-eaphost-api-reference"></a><span data-ttu-id="e2904-119">Общая ссылка на API EAPHost</span><span class="sxs-lookup"><span data-stu-id="e2904-119">Common EAPHost API Reference</span></span>



| <span data-ttu-id="e2904-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="e2904-120">Topic</span></span>                                                                   | <span data-ttu-id="e2904-121">Описание</span><span class="sxs-lookup"><span data-stu-id="e2904-121">Description</span></span>                                  |
|-------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="e2904-122">Распространенные перечисления API EAPHost</span><span class="sxs-lookup"><span data-stu-id="e2904-122">Common EAPHost API Enumerations</span></span>](common-eap-host-api-enumerations.md) | <span data-ttu-id="e2904-123">Перечисляет константы, общие для всех API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="e2904-123">Lists constants common to all EAPHost APIs.</span></span>  |
| [<span data-ttu-id="e2904-124">Общие структуры API EAPHost</span><span class="sxs-lookup"><span data-stu-id="e2904-124">Common EAPHost API Structures</span></span>](common-eap-host-api-structures.md)     | <span data-ttu-id="e2904-125">Содержит структуры, общие для всех API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="e2904-125">Lists structures common to all EAPHost APIs.</span></span> |
| [<span data-ttu-id="e2904-126">Общие константы API EAPHost</span><span class="sxs-lookup"><span data-stu-id="e2904-126">Common EAPHost API Constants</span></span>](common-eap-host-error-constants.md)     | <span data-ttu-id="e2904-127">Перечисляет константы, общие для всех API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="e2904-127">Lists constants common to all EAPHost APIs.</span></span>  |



 

## <a name="eaphost-api-reference"></a><span data-ttu-id="e2904-128">Справочник по API EAPHost</span><span class="sxs-lookup"><span data-stu-id="e2904-128">EAPHost API Reference</span></span>



| <span data-ttu-id="e2904-129">Раздел</span><span class="sxs-lookup"><span data-stu-id="e2904-129">Topic</span></span>                                                                       | <span data-ttu-id="e2904-130">Описание</span><span class="sxs-lookup"><span data-stu-id="e2904-130">Description</span></span>                                                                                                                                      |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2904-131">Справочник по API для запрашивающей сторона EAPHost</span><span class="sxs-lookup"><span data-stu-id="e2904-131">EAPHost Supplicant API Reference</span></span>](eap-host-supplicant-api-reference.md)   | <span data-ttu-id="e2904-132">Описывает элементы API, доступные для поддержки вызовов вызывающей сторона к EAPHost.</span><span class="sxs-lookup"><span data-stu-id="e2904-132">Describes the API elements available to enable supplicant calls to EAPHost.</span></span>                                                                      |
| [<span data-ttu-id="e2904-133">Справочник по API однорангового метода EAPHost</span><span class="sxs-lookup"><span data-stu-id="e2904-133">EAPHost Peer Method API Reference</span></span>](eap-host-peer-method-api-reference.md) | <span data-ttu-id="e2904-134">Описывает элементы API, которые должны быть реализованы для создания библиотеки DLL однорангового метода EAP, которая может быть загружена и вызвана клиентом EAPHost.</span><span class="sxs-lookup"><span data-stu-id="e2904-134">Describes the API elements that must be implemented to create an EAP peer method DLL that can be loaded and called by a client EAPHost.</span></span>          |
| [<span data-ttu-id="e2904-135">API-интерфейсы метода проверки подлинности EAPHost</span><span class="sxs-lookup"><span data-stu-id="e2904-135">EAPHost Authenticator Method APIs</span></span>](eaphost-authenticator-method-apis.md)  | <span data-ttu-id="e2904-136">Описывает элементы API, которые должны быть реализованы для создания DLL метода проверки подлинности EAP, который может быть загружен и вызван сервером EAPHost.</span><span class="sxs-lookup"><span data-stu-id="e2904-136">Describes the API elements that must be implemented to create an EAP authenticator method DLL that can be loaded and called by a server EAPHost.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e2904-137">См. также</span><span class="sxs-lookup"><span data-stu-id="e2904-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2904-138">Об EAPHost</span><span class="sxs-lookup"><span data-stu-id="e2904-138">About EAPHost</span></span>](about-eap-host.md)
</dt> <dt>

[<span data-ttu-id="e2904-139">Использование EAPHost</span><span class="sxs-lookup"><span data-stu-id="e2904-139">Using EAPHost</span></span>](using-eap-host.md)
</dt> </dl>

 

 




