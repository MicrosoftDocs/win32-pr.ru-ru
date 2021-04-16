---
title: Совместимость клиентских и серверных Windows 8.1 и Windows Server 2012 R2
description: Совместимость клиентских и серверных Windows 8.1 и Windows Server 2012 R2
ms.assetid: 45C37E2D-3513-4708-A562-1426D2B832F0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c46647dd9ad0f0baeae1ffb98905740a37f9530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531991"
---
# <a name="windows-81-and-windows-server-2012-r2-client-and-server-compatibility"></a><span data-ttu-id="c2d56-103">Совместимость клиентских и серверных Windows 8.1 и Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c2d56-103">Windows 8.1 and Windows Server 2012 R2 client and server compatibility</span></span>

<span data-ttu-id="c2d56-104">В этом разделе описаны изменения в операционной системе, о которых следует уделить особое внимание из-за возможных влияния на существующие приложения и о том, как новые приложения должны разрабатываться на клиентах, на серверах или на клиентах и серверах.</span><span class="sxs-lookup"><span data-stu-id="c2d56-104">This section describes changes in the operating system that you should pay special attention to due to the potential impacts on existing apps and how new apps should be designed on clients, on servers, or on both clients and servers.</span></span> <span data-ttu-id="c2d56-105">Ниже приведен список разделов, рассмотренных в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="c2d56-105">Following is the list of topics covered in this section:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c2d56-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="c2d56-106">In this section</span></span>



| <span data-ttu-id="c2d56-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="c2d56-107">Topic</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="c2d56-108">Описание</span><span class="sxs-lookup"><span data-stu-id="c2d56-108">Description</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="c2d56-109">Изменения версии операционной системы в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c2d56-109">Operating system version changes in Windows 8.1</span></span>](operating-system-version-changes-in-windows-8-1.md)<br/>                                                                                                             |             |
| [<span data-ttu-id="c2d56-110">Компоненты Windows, установленные по запросу</span><span class="sxs-lookup"><span data-stu-id="c2d56-110">Windows components installed on demand</span></span>](windows-components-installed-on-demand.md)<br/>                                                                                                                               |             |
| [<span data-ttu-id="c2d56-111">Поведение отката шрифта HTML</span><span class="sxs-lookup"><span data-stu-id="c2d56-111">HTML font fallback behavior</span></span>](html-font-fallback-behavior.md)<br/>                                                                                                                                                     |             |
| [<span data-ttu-id="c2d56-112">Windows 8.1 допускает только URI HTTPS, а не URI HTTP</span><span class="sxs-lookup"><span data-stu-id="c2d56-112">Windows 8.1 allows only https URIs, not http URIs</span></span>](windows-8-1-allows-only-https-uris--not-http-uris.md)<br/>                                                                                                         |             |
| [<span data-ttu-id="c2d56-113">Входные данные маусевхил для Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c2d56-113">Mousewheel input for Windows 8.1</span></span>](mousewheel-input-for-windows-8-1.md)<br/>                                                                                                                                           |             |
| [<span data-ttu-id="c2d56-114">Сенсорные устройства Windows Precision</span><span class="sxs-lookup"><span data-stu-id="c2d56-114">Windows precision touchpad devices</span></span>](windows-precision-touchpad-devices.md)<br/>                                                                                                                                       |             |
| [<span data-ttu-id="c2d56-115">Высокое разрешение для настольных приложений в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c2d56-115">High DPI for desktop apps in Windows 8.1</span></span>](high-dpi-for-desktop-apps-in-windows-8-1.md)<br/>                                                                                                                           |             |
| [<span data-ttu-id="c2d56-116">Пользовательский интерфейс пограничной панели подавляется при включении и в сценариях инерции</span><span class="sxs-lookup"><span data-stu-id="c2d56-116">Edge UI is suppressed in  in-out-in  and  inertia  scenarios</span></span>](edge-ui-is-suppressed-in--in-out-in--and--inertia--scenarios.md)<br/>                                                                                   |             |
| [<span data-ttu-id="c2d56-117">Вызов Иммсетконверсионстатус () или Иммжетконверсионстатус () из приложений Магазина Windows не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c2d56-117">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from Windows Store apps is not supported</span></span>](calling-immsetconversionstatus---or-immgetconversionstatus---from-windows-store-apps-is-not-supported.md)<br/> |             |
| [<span data-ttu-id="c2d56-118">Модель режима IME изменена с "на пользователя" на "на поток"</span><span class="sxs-lookup"><span data-stu-id="c2d56-118">IME mode model changed from per-user to per-thread</span></span>](ime-mode-model-changed-from-per-user-to-per-thread.md)<br/>                                                                                                       |             |
| [<span data-ttu-id="c2d56-119">Интерфейсы API диспетчера методов ввода не поддерживаются в упрощенном китайском языке (IME)</span><span class="sxs-lookup"><span data-stu-id="c2d56-119">Input Method manager APIs are not supported by Simplified Chinese IME</span></span>](input-method-manager-apis-are-not-supported-by-simplified-chinese-ime.md)<br/>                                                                 |             |
| [<span data-ttu-id="c2d56-120">Некоторые панели ввода программного обеспечения IME для восточноазиатских языков теперь отправляют ключ</span><span class="sxs-lookup"><span data-stu-id="c2d56-120">Some East Asian IME software input panels now send vKey</span></span>](some-east-asian-ime-software-input-panels-now-send-vkey.md)<br/>                                                                                             |             |



 

 

 





