---
title: Компоненты EAPHost
description: Сведения о трех компонентах проверки подлинности EAPHost. Просмотрите дополнительные доступные ресурсы для использования проверки подлинности EAPHost.
ms.assetid: f875c3f8-d2fb-461e-b356-e1b2ccaf9981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ede2fc6a705ec77fe982778239a92c7ffb10ef9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488293"
---
# <a name="components-of-eaphost"></a><span data-ttu-id="7ed0b-104">Компоненты EAPHost</span><span class="sxs-lookup"><span data-stu-id="7ed0b-104">Components of EAPHost</span></span>

<span data-ttu-id="7ed0b-105">В этом разделе описаны три компонента проверки подлинности EAPHost.</span><span class="sxs-lookup"><span data-stu-id="7ed0b-105">This topic describes the three components of EAPHost authentication.</span></span>

## <a name="eaphost-components"></a><span data-ttu-id="7ed0b-106">Компоненты EAPHost</span><span class="sxs-lookup"><span data-stu-id="7ed0b-106">EAPHost Components</span></span>

<span data-ttu-id="7ed0b-107">В проверке подлинности EAPHost имеются следующие три компонента.</span><span class="sxs-lookup"><span data-stu-id="7ed0b-107">EAPHost authentication has the following three components.</span></span>

-   <span data-ttu-id="7ed0b-108">Запрашивающая сторона, которая делает запросы на проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="7ed0b-108">The supplicant, which makes the authentication requests.</span></span>
-   <span data-ttu-id="7ed0b-109">Методы EAP узла (или клиента), которые реализуют определенные методы EAP и управляют сеансом проверки подлинности на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="7ed0b-109">The peer (or client) EAP methods, which implement the specific EAP methods and manage the authentication session on the client side.</span></span>
-   <span data-ttu-id="7ed0b-110">Методы проверки подлинности (или сервера) EAP, реализующие серверную часть протокола EAP.</span><span class="sxs-lookup"><span data-stu-id="7ed0b-110">The authenticator (or server) EAP methods, which implement the server side of the EAP protocol.</span></span>

<span data-ttu-id="7ed0b-111">API-интерфейсы для запрашивающих сторона вызываются непосредственно из приложения, которое хочет пройти проверку подлинности с помощью EAPHost.</span><span class="sxs-lookup"><span data-stu-id="7ed0b-111">The supplicant APIs are called directly from an application that wants to authenticate via EAPHost.</span></span> <span data-ttu-id="7ed0b-112">Однако интерфейсы одноранговых методов и методов проверки подлинности — это прототипы функций, которые должны быть реализованы для конкретного типа метода проверки подлинности EAP, например протокол проверки подлинности Microsoft Challenge версии 2,0 (MS-CHAPv2).</span><span class="sxs-lookup"><span data-stu-id="7ed0b-112">The peer method and authenticator method APIs, however, are function prototypes that must be implemented for a specific EAP authentication method type - such as the Microsoft Challenge Handshake Authentication Protocol version 2.0 (MS-CHAPv2).</span></span>

<span data-ttu-id="7ed0b-113">Если вы создаете приложение, которое будет использовать EAPHost для проверки подлинности, обратитесь к [Справочнику по API](eap-host-supplicant-api-reference.md)для обращения к EAPHost.</span><span class="sxs-lookup"><span data-stu-id="7ed0b-113">If you are authoring an application that will use EAPHost for authentication, please refer to the [EAPHost Supplicant API Reference](eap-host-supplicant-api-reference.md).</span></span>

<span data-ttu-id="7ed0b-114">Если вы создаете новый метод проверки подлинности EAP для управления с помощью EAPHost, обратитесь к [Справочнику по API однорангового метода EAPHost](eap-host-peer-method-api-reference.md) и [интерфейсам API метода средства проверки подлинности EAPHost](eaphost-authenticator-method-apis.md).</span><span class="sxs-lookup"><span data-stu-id="7ed0b-114">If you are authoring a new EAP authentication method to be managed by EAPHost, please refer to the [EAPHost Peer Method API Reference](eap-host-peer-method-api-reference.md) and the [EAPHost Authenticator Method APIs](eaphost-authenticator-method-apis.md).</span></span> <span data-ttu-id="7ed0b-115">Обратите внимание, что вы создадите реализации этих интерфейсов API, предоставляемых в новой библиотеке DLL, которая загружается с помощью EAPHost, а не вызывает их напрямую.</span><span class="sxs-lookup"><span data-stu-id="7ed0b-115">Note that you will be creating implementations of these APIs exposed in a new DLL that EAPHost loads, rather than calling them directly.</span></span>

 

 




