---
title: Установка коммутируемого подключения к Интернету
description: Для управления подключениями через модем используются следующие функции.
ms.assetid: dd33ed4b-eb7c-449c-b309-8f5c290a5a93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce03ecc67e27c67bb9807f473aac5210b03f755
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070486"
---
# <a name="establishing-a-dial-up-connection-to-the-internet"></a><span data-ttu-id="696fe-103">Установка коммутируемого подключения к Интернету</span><span class="sxs-lookup"><span data-stu-id="696fe-103">Establishing a Dial-Up Connection to the Internet</span></span>

<span data-ttu-id="696fe-104">Для управления подключениями через модем используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="696fe-104">The following functions are used to handle modem connections.</span></span>

-   [<span data-ttu-id="696fe-105">**интернетаутодиал**</span><span class="sxs-lookup"><span data-stu-id="696fe-105">**InternetAutodial**</span></span>](/windows/win32/api/winineti/nf-winineti-internetautodial)
-   [<span data-ttu-id="696fe-106">**интернетаутодиалхангуп**</span><span class="sxs-lookup"><span data-stu-id="696fe-106">**InternetAutodialHangup**</span></span>](/windows/win32/api/winineti/nf-winineti-internetautodialhangup)
-   [<span data-ttu-id="696fe-107">**интернетдиал**</span><span class="sxs-lookup"><span data-stu-id="696fe-107">**InternetDial**</span></span>](/windows/win32/api/winineti/nf-winineti-internetdial)
-   [<span data-ttu-id="696fe-108">**интернетжетконнектедстате**</span><span class="sxs-lookup"><span data-stu-id="696fe-108">**InternetGetConnectedState**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstate)
-   [<span data-ttu-id="696fe-109">**интернетжетконнектедстатикс**</span><span class="sxs-lookup"><span data-stu-id="696fe-109">**InternetGetConnectedStateEx**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstateex)
-   [<span data-ttu-id="696fe-110">**интернесангуп**</span><span class="sxs-lookup"><span data-stu-id="696fe-110">**InternetHangUp**</span></span>](/windows/win32/api/winineti/nf-winineti-internethangup)
-   [<span data-ttu-id="696fe-111">**интернетгунлине**</span><span class="sxs-lookup"><span data-stu-id="696fe-111">**InternetGoOnline**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgoonline)

> [!Note]  
> <span data-ttu-id="696fe-112">Функции WinINet-подключения не поддерживают двойное соединение, проверку подлинности смарт-карты или соединения, требующие сертификации на основе реестра.</span><span class="sxs-lookup"><span data-stu-id="696fe-112">WinINet dial-up functions do not support double-dial connections, SmartCard authentication, or connections that require registry-based certification.</span></span>

 

> [!Note]  
> <span data-ttu-id="696fe-113">Начиная с Windows Vista и Windows Server 2008, функции удаленного доступа WinINet используют [функции RAS](/windows/desktop/RRAS/remote-access-service-functions) для установления коммутируемого подключения.</span><span class="sxs-lookup"><span data-stu-id="696fe-113">Starting on Windows Vista and Windows Server 2008, the WinINet dial-up functions use the [RAS functions](/windows/desktop/RRAS/remote-access-service-functions) to establish a dial-up connection.</span></span> <span data-ttu-id="696fe-114">WinINet поддерживает функциональные возможности, описанные в функции [**расдиалдлг**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) .</span><span class="sxs-lookup"><span data-stu-id="696fe-114">WinINet supports the functionality documented in the [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) function.</span></span>

 

> [!Note]  
> <span data-ttu-id="696fe-115">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="696fe-115">WinINet does not support server implementations.</span></span> <span data-ttu-id="696fe-116">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="696fe-116">In addition, it should not be used from a service.</span></span> <span data-ttu-id="696fe-117">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="696fe-117">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 