---
description: Политика автоматического входа в систему (автоматический вход в систему) определяет, когда служба WinHTTP может включать учетные данные по умолчанию в запрос к серверу.
ms.assetid: 4ED8B6BC-E52D-4DE9-A9AE-1FDF61A978A9
title: винхттпаутологонлевел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7760faa94e24b7fe5b33717c504b03e4de42c0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910671"
---
# <a name="winhttpautologonlevel"></a><span data-ttu-id="fafde-103">винхттпаутологонлевел</span><span class="sxs-lookup"><span data-stu-id="fafde-103">WinHttpAutoLogonLevel</span></span>

<span data-ttu-id="fafde-104">Политика автоматического входа в систему (автоматический вход в систему) определяет, когда служба *WinHTTP* может включать учетные данные по умолчанию в запрос к серверу.</span><span class="sxs-lookup"><span data-stu-id="fafde-104">The automatic logon (auto-logon) policy determines when it is acceptable for *WinHTTP* to include the default credentials in a request to the server.</span></span>

<span data-ttu-id="fafde-105">Для этого параметра можно задать значение **L** для **параметра \_ уровень безопасности автоматического входа WinHTTP \_ \_ \_ Low**, установить **значение M** для **\_ \_ \_ уровня безопасности \_ WinHTTP с автовходом** и установить значение **H** для **\_ уровня безопасности автоматического входа WinHTTP \_ \_ \_ High**.</span><span class="sxs-lookup"><span data-stu-id="fafde-105">You can set this value to **L** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW**, set to **M** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM**, and set to **H** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH**.</span></span> <span data-ttu-id="fafde-106">Уровень по умолчанию **— \_ \_ \_ \_ средний уровень безопасности службы WinHTTP с автовходом**.</span><span class="sxs-lookup"><span data-stu-id="fafde-106">The default level is **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM**.</span></span> <span data-ttu-id="fafde-107">Дополнительные сведения о политике автоматического входа в систему см. в разделе [Проверка подлинности в WinHTTP](../winhttp/authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="fafde-107">For more information about automatic logon policy, see the section for [Authentication in WinHTTP](../winhttp/authentication-in-winhttp.md).</span></span>

<span data-ttu-id="fafde-108">**Windows 8 и Windows Server 2012:** Эта политика требует установщик Windows, работающих в Windows 8 или Windows Server 2012 и недоступна во всех более ранних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="fafde-108">**Windows 8 and Windows Server 2012:** This policy requires Windows Installer running on the Windows 8 or Windows Server 2012 and is unavailable on all earlier versions of Windows.</span></span>

## <a name="registry-key"></a><span data-ttu-id="fafde-109">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="fafde-109">Registry Key</span></span>

<span data-ttu-id="fafde-110">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="fafde-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="fafde-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fafde-111">Data Type</span></span>

<span data-ttu-id="fafde-112">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="fafde-112">**REG\_SZ**</span></span>

 

 
