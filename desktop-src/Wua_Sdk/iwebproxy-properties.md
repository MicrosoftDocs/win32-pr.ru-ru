---
description: Интерфейс IWebProxy определяет следующие свойства.
ms.assetid: 449b19ec-dc95-40f7-87af-84fb7dacb328
title: Свойства IWebProxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96628e7c799232b741e1834964a3a8ef6f6264c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423666"
---
# <a name="iwebproxy-properties"></a><span data-ttu-id="1c2a7-103">Свойства IWebProxy</span><span class="sxs-lookup"><span data-stu-id="1c2a7-103">IWebProxy Properties</span></span>

<span data-ttu-id="1c2a7-104">Интерфейс [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1c2a7-104">The [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) interface defines the following properties.</span></span>



| <span data-ttu-id="1c2a7-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="1c2a7-105">Property</span></span>                                                   | <span data-ttu-id="1c2a7-106">Описание</span><span class="sxs-lookup"><span data-stu-id="1c2a7-106">Description</span></span>                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c2a7-107">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="1c2a7-107">**Address**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)                       | <span data-ttu-id="1c2a7-108">Возвращает и задает адрес и десятичный номер порта прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="1c2a7-108">Gets and sets the address and the decimal port number of the proxy server.</span></span>                                                |
| [<span data-ttu-id="1c2a7-109">**Автообнаружение**</span><span class="sxs-lookup"><span data-stu-id="1c2a7-109">**AutoDetect**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_autodetect)                 | <span data-ttu-id="1c2a7-110">Возвращает и задает логическое значение, указывающее, будет ли [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) автоматически определять параметры прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="1c2a7-110">Gets and sets a Boolean value that indicates whether [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) automatically detects proxy settings.</span></span> |
| [<span data-ttu-id="1c2a7-111">**бипасслист**</span><span class="sxs-lookup"><span data-stu-id="1c2a7-111">**BypassList**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_bypasslist)                 | <span data-ttu-id="1c2a7-112">Возвращает и задает коллекцию адресов, которые не используют прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="1c2a7-112">Gets and sets a collection of addresses that do not use the proxy server.</span></span>                                                 |
| [<span data-ttu-id="1c2a7-113">**бипасспроксйонлокал**</span><span class="sxs-lookup"><span data-stu-id="1c2a7-113">**BypassProxyOnLocal**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_bypassproxyonlocal) | <span data-ttu-id="1c2a7-114">Возвращает и задает логическое значение, указывающее, пропускает ли локальный адрес прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="1c2a7-114">Gets and sets a Boolean value that indicates whether local addresses bypass the proxy server.</span></span>                             |
| [<span data-ttu-id="1c2a7-115">**Доступно**</span><span class="sxs-lookup"><span data-stu-id="1c2a7-115">**ReadOnly**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_readonly)                     | <span data-ttu-id="1c2a7-116">Возвращает логическое значение, указывающее, доступен ли объект [**WebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1c2a7-116">Gets a Boolean value that indicates whether the [**WebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) object is read-only.</span></span>                        |
| [<span data-ttu-id="1c2a7-117">**Имен**</span><span class="sxs-lookup"><span data-stu-id="1c2a7-117">**UserName**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_username)                     | <span data-ttu-id="1c2a7-118">Возвращает и задает имя пользователя для отправки на прокси-сервер для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="1c2a7-118">Gets and sets the user name to submit to the proxy server for authentication.</span></span>                                             |



 

 

 



