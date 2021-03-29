---
description: Схемы Интернета, поддерживаемые WinHTTP.
ms.assetid: 31e45879-807e-4dd5-9f99-94a46011e55e
title: INTERNET_SCHEME (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7b73dcc13b2623e3a6f28d2d49d1965464070f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912411"
---
# <a name="internet_scheme"></a><span data-ttu-id="e466a-103">\_схема Интернета</span><span class="sxs-lookup"><span data-stu-id="e466a-103">INTERNET\_SCHEME</span></span>

<span data-ttu-id="e466a-104">Схемы Интернета, поддерживаемые WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="e466a-104">Internet schemes supported by WinHTTP.</span></span>

<dl> <dt>

<span data-ttu-id="e466a-105"><span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**\_ \_ http-схема Интернета**</span><span class="sxs-lookup"><span data-stu-id="e466a-105"><span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**INTERNET\_SCHEME\_HTTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e466a-106">1</span><span class="sxs-lookup"><span data-stu-id="e466a-106">1</span></span>
</dt> <dt>



<span data-ttu-id="e466a-107">Интернет-схема HTTP.</span><span class="sxs-lookup"><span data-stu-id="e466a-107">An HTTP internet scheme.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e466a-108"><span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**\_HTTPS схемы \_ Интернета**</span><span class="sxs-lookup"><span data-stu-id="e466a-108"><span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**INTERNET\_SCHEME\_HTTPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e466a-109">2</span><span class="sxs-lookup"><span data-stu-id="e466a-109">2</span></span>
</dt> <dt>



<span data-ttu-id="e466a-110">Схема Интернета HTTPS (SSL).</span><span class="sxs-lookup"><span data-stu-id="e466a-110">An HTTPS (SSL) internet scheme.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e466a-111"><span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**\_ \_ FTP-схема Интернета**</span><span class="sxs-lookup"><span data-stu-id="e466a-111"><span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**INTERNET\_SCHEME\_FTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e466a-112">3</span><span class="sxs-lookup"><span data-stu-id="e466a-112">3</span></span>
</dt> <dt>



<span data-ttu-id="e466a-113">Интернет-схема FTP.</span><span class="sxs-lookup"><span data-stu-id="e466a-113">An FTP internet scheme.</span></span> <span data-ttu-id="e466a-114">Эта схема поддерживается только в [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) и [**винхттпжетпроксифорурлекс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="e466a-114">This scheme is only supported for use in [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) and [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e466a-115"><span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**Интернет \_ схемы \_ SOCKS**</span><span class="sxs-lookup"><span data-stu-id="e466a-115"><span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**INTERNET\_SCHEME\_SOCKS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e466a-116">4</span><span class="sxs-lookup"><span data-stu-id="e466a-116">4</span></span>
</dt> <dt>



<span data-ttu-id="e466a-117">Интернет-схема SOCKS.</span><span class="sxs-lookup"><span data-stu-id="e466a-117">A SOCKS internet scheme.</span></span> <span data-ttu-id="e466a-118">Эта схема поддерживается только в [**\_ \_ \_ записи результата прокси-сервера WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry).</span><span class="sxs-lookup"><span data-stu-id="e466a-118">This scheme is only supported for use in [**WINHTTP\_PROXY\_RESULT\_ENTRY**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e466a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e466a-119">Requirements</span></span>



| <span data-ttu-id="e466a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e466a-120">Requirement</span></span> | <span data-ttu-id="e466a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e466a-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e466a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e466a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e466a-123">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e466a-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="e466a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e466a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e466a-125">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e466a-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>   |
| <span data-ttu-id="e466a-126">Header</span><span class="sxs-lookup"><span data-stu-id="e466a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e466a-127"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="e466a-127"><dt>Winhttp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e466a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e466a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e466a-129">**\_запись результата прокси-сервера WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e466a-129">**WINHTTP\_PROXY\_RESULT\_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> </dl>

 

 




