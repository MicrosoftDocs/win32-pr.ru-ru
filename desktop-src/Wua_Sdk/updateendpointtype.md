---
description: Определяет тип конечных точек, которые могут использоваться для подключения к службе.
ms.assetid: 50397D25-7C71-4AA2-89BF-F90CBDCFFA91
title: Перечисление Упдатиндпоинттипе (Упдатиндпоинтаус. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: 942bcb5275c6a4f39d6e2828025e5b9a40e52c46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540122"
---
# <a name="updateendpointtype-enumeration"></a><span data-ttu-id="25feb-103">Перечисление Упдатиндпоинттипе</span><span class="sxs-lookup"><span data-stu-id="25feb-103">UpdateEndpointType enumeration</span></span>

<span data-ttu-id="25feb-104">Определяет тип конечных точек, которые могут использоваться для подключения к службе.</span><span class="sxs-lookup"><span data-stu-id="25feb-104">Defines the type of endpoints that can be used to connect to a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="25feb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25feb-105">Syntax</span></span>


```C++
typedef enum tagEndpointType { 
  uetClientServer          = 0,
  uetReporting             = ( uetClientServer + 1 ),
  uetWuaSelfUpdate         = ( uetReporting + 1 ),
  uetRegulation            = ( uetWuaSelfUpdate + 1 ),
  uetSimpleTargeting       = ( uetRegulation + 1 ),
  uetSecuredClientServer   = ( uetSimpleTargeting + 1 ),
  uetSecondaryServiceAuth  = ( uetSecuredClientServer + 1 )
} UpdateEndpointType;
```



## <a name="constants"></a><span data-ttu-id="25feb-106">Константы</span><span class="sxs-lookup"><span data-stu-id="25feb-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="25feb-107"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**уетклиентсервер**</span><span class="sxs-lookup"><span data-stu-id="25feb-107"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span></span>
</dt> <dd>

<span data-ttu-id="25feb-108">Конечная точка клиент-сервер, используемая для подключения к службе обновления, например Центр обновления Windows, Центр обновления Майкрософт и WSUS-сервер в корпоративной среде, для поиска сведений об обновлениях, которые могут быть применимы к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="25feb-108">A client-server endpoint that is used to connect to the update service, such as Windows Update, Microsoft Update, and WSUS server in a corporate environment, to find information on updates that may be applicable to the computer.</span></span>

<span data-ttu-id="25feb-109">Служба обновления возвращает сведения об обновлениях, опубликованных, измененных или снятых с момента последнего выполнения синхронизации с сервером.</span><span class="sxs-lookup"><span data-stu-id="25feb-109">The update service returns information on updates that have been published, revised, or withdrawn since the last time that client performed a sync with the server.</span></span>

</dd> <dt>

<span data-ttu-id="25feb-110"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**уетрепортинг**</span><span class="sxs-lookup"><span data-stu-id="25feb-110"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span></span>
</dt> <dd>

<span data-ttu-id="25feb-111">Конечная точка отчетов, которая используется, когда клиент сообщает о результатах проверок, скачивается и устанавливается обратно в службу обновления.</span><span class="sxs-lookup"><span data-stu-id="25feb-111">A reporting endpoint that is used when the client reports the results of scans, downloads, and installs back to the update service.</span></span>

<span data-ttu-id="25feb-112">В случае общедоступных служб (Центр обновления Windows и Центр обновления Майкрософт) это делается для целей мониторинга качества.</span><span class="sxs-lookup"><span data-stu-id="25feb-112">In the case of public services (Windows Update and Microsoft Update), this is done for quality monitoring purposes.</span></span>

<span data-ttu-id="25feb-113">В случае с частными службами, такими как корпоративный сервер WSUS, СХИС тип конечной точки позволяет серверу получать данные инвентаризации и другие сведения о клиентских компьютерах под управлением.</span><span class="sxs-lookup"><span data-stu-id="25feb-113">In the case of private services, such as a corporate WSUS server, thhis type of endpoint also allows the server to collect inventory and other information about the client computers under management.</span></span>

</dd> <dt>

<span data-ttu-id="25feb-114"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**уетвуаселфупдате**</span><span class="sxs-lookup"><span data-stu-id="25feb-114"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="25feb-115">Конечная точка самообновления, которая используется, когда клиентский компьютер обращается к службе обновления, чтобы узнать, существует ли новая версия клиентского программного обеспечения агента Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="25feb-115">A self-update endpoint that is used when the client computer contacts an update service to see whether there is a new version of the Windows Update Agent client software.</span></span>

<span data-ttu-id="25feb-116">Конечная точка самообновления использует другой протокол, а затем конечную точку Client-Server, чтобы можно было распространять самостоятельное обновление, даже если возникает ошибка, которая может препятствовать работе обычной клиент-серверной синхронизации на определенном клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="25feb-116">The Self-update endpoint uses a different protocol then the Client-Server endpoint so that self-updates can be distributed even if there is an error condition that might be preventing the normal client-server sync from working on a particular client computer.</span></span>

</dd> <dt>

<span data-ttu-id="25feb-117"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**уетрегулатион**</span><span class="sxs-lookup"><span data-stu-id="25feb-117"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span></span>
</dt> <dd>

<span data-ttu-id="25feb-118">Регулируемая конечная точка, используемая, когда клиентский компьютер обращается к регламентированной службе для работы с определенным обновлением, применимым к целевому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="25feb-118">A regulation endpoint that is used when the client computer contacts the regulation service to act on a particular update that is applicable to the target computer.</span></span>

<span data-ttu-id="25feb-119">Служба регулирования может указать, является ли обновление "регулируемым" (также называемым "регулируемым"). Иными словами, служба регулирования может сообщить клиентскому компьютеру, что он не должен работать с определенным обновлением, несмотря на то, что это обновление является применимым.</span><span class="sxs-lookup"><span data-stu-id="25feb-119">The regulation service can indicate whether the update is “regulated” (also known as “throttled”) – in other words, the regulation service can tell the client computer that it should not act on a particular update, even though that update appears to be applicable.</span></span>

</dd> <dt>

<span data-ttu-id="25feb-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**уетсимплетаржетинг**</span><span class="sxs-lookup"><span data-stu-id="25feb-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span></span>
</dt> <dd>

<span data-ttu-id="25feb-121">Простая конечная точка, используемая только с частными службами (WSUS-серверы в корпоративных средах).</span><span class="sxs-lookup"><span data-stu-id="25feb-121">A simple-targeting endpoint that is used only with private services (WSUS servers in corporate environments).</span></span> <span data-ttu-id="25feb-122">В корпоративной среде клиентские компьютеры могут быть назначены определенным целевым группам, а обновления могут быть утверждены для установки на компьютерах в некоторых группах, но не в других.</span><span class="sxs-lookup"><span data-stu-id="25feb-122">In a corporate environment, client computers can be assigned to particular target groups, and updates can be approved for installation on computers in some groups but not others.</span></span>

<span data-ttu-id="25feb-123">Например, администратор WSUS может создать группу "тестирование" для компьютеров, которые используются для тестирования новых обновлений, а администратор может утверждать новые выпущенные обновления для установки на компьютерах в группе тестирования, не утверждая их для установки на других компьютерах в Организации.</span><span class="sxs-lookup"><span data-stu-id="25feb-123">For example, the WSUS administrator may create a “Testing” group for computers that are used to test new updates, and the administrator may approve newly-released updates for installation on computers in the Testing group without approving them for installation on other computers in the organization.</span></span> <span data-ttu-id="25feb-124">Простой нацеливание Exchange используется для того, чтобы клиентский компьютер зарегистрировался на сервере WSUS и позволял серверу сообщить клиентскому компьютеру, в какой группе он находится.</span><span class="sxs-lookup"><span data-stu-id="25feb-124">The simple targeting exchange is used to allow a client computer to register itself with the WSUS server, and to allow the server to tell the client computer what group it is in.</span></span>

</dd> <dt>

<span data-ttu-id="25feb-125"><span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**уетсекуредклиентсервер**</span><span class="sxs-lookup"><span data-stu-id="25feb-125"><span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**</span></span>
</dt> <dd>

<span data-ttu-id="25feb-126">Защищенная конечная точка Client-Server, которая позволяет клиенту получать сведения о приложениях, которым требуется лицензирование, чтобы их можно было использовать на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="25feb-126">A secured-client-server endpoint that allows a client to obtain info on apps that need licensing so they can be used on a client computer.</span></span> <span data-ttu-id="25feb-127">Эта платформа лицензирования в настоящее время используется Windows 8 для развертывания приложений и обновлений, полученных через Магазин Windows.</span><span class="sxs-lookup"><span data-stu-id="25feb-127">This licensing framework is currently only used by Windows 8 to deploy apps and updates that are obtained through the Windows Store.</span></span> <span data-ttu-id="25feb-128">В настоящее время конечная точка Secure-Client-Server не используется Центр обновления Windows, Центр обновления Майкрософт или WSUS.</span><span class="sxs-lookup"><span data-stu-id="25feb-128">The secured-client-server endpoint is currently not used by Windows Update, Microsoft Update, or WSUS.</span></span>

</dd> <dt>

<span data-ttu-id="25feb-129"><span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**уетсекондарисервицеаус**</span><span class="sxs-lookup"><span data-stu-id="25feb-129"><span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**</span></span>
</dt> <dd>

<span data-ttu-id="25feb-130">Конечная точка вторичной службы — Аутентификация используется клиентом для обеспечения проверки подлинности перед получением сведений о приложениях, которым требуется лицензирование, чтобы их можно было использовать на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="25feb-130">The secondary-service-authentication endpoint is used by a client to provide authentication before it obtains info on apps that need licensing so they can be used on a client computer.</span></span> <span data-ttu-id="25feb-131">Эта платформа лицензирования в настоящее время используется Windows 8 для развертывания приложений и обновлений, полученных через Магазин Windows.</span><span class="sxs-lookup"><span data-stu-id="25feb-131">This licensing framework is currently only utilized by Windows 8 to deploy apps and updates that are obtained through the Windows Store.</span></span> <span data-ttu-id="25feb-132">В настоящее время конечная точка вторичной службы проверки подлинности не используется Центр обновления Windows, Центр обновления Майкрософт или WSUS.</span><span class="sxs-lookup"><span data-stu-id="25feb-132">The secondary-service-authentication endpoint is currently not used by Windows Update, Microsoft Update, or WSUS.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25feb-133">Требования</span><span class="sxs-lookup"><span data-stu-id="25feb-133">Requirements</span></span>



| <span data-ttu-id="25feb-134">Требование</span><span class="sxs-lookup"><span data-stu-id="25feb-134">Requirement</span></span> | <span data-ttu-id="25feb-135">Значение</span><span class="sxs-lookup"><span data-stu-id="25feb-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25feb-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25feb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="25feb-137">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="25feb-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="25feb-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25feb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="25feb-139">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="25feb-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="25feb-140">Header</span><span class="sxs-lookup"><span data-stu-id="25feb-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="25feb-141"><dt>Упдатиндпоинтаус. h</dt></span><span class="sxs-lookup"><span data-stu-id="25feb-141"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="25feb-142">IDL</span><span class="sxs-lookup"><span data-stu-id="25feb-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="25feb-143"><dt>Упдатиндпоинтаус. idl</dt></span><span class="sxs-lookup"><span data-stu-id="25feb-143"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



 

 




