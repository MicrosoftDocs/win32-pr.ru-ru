---
description: Определяет профиль WLAN, используемый собственной службой автонастройки WiFi.
ms.assetid: 8312d213-1d01-4bd0-a8d9-65ca23560888
title: Схема WLAN_profile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d484215ca53ddcd97dbef4adf4aac17cd8457b3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144536"
---
# <a name="wlan_profile-schema"></a><span data-ttu-id="8d8ed-103">\_Схема профиля WLAN</span><span class="sxs-lookup"><span data-stu-id="8d8ed-103">WLAN\_profile Schema</span></span>

<span data-ttu-id="8d8ed-104">\_Схема профиля WLAN определяет профиль WLAN, используемый собственной службой автонастройки WiFi.</span><span class="sxs-lookup"><span data-stu-id="8d8ed-104">The WLAN\_profile Schema defines a WLAN profile used by the Native Wifi AutoConfig service.</span></span>

<span data-ttu-id="8d8ed-105">Служба автонастройки принимает профили беспроводной связи от агента групповая политика, интерфейса сценариев (**netsh**), пользовательского интерфейса или интерфейса USB Flash.</span><span class="sxs-lookup"><span data-stu-id="8d8ed-105">The AutoConfig service accepts wireless profiles from the Group Policy Agent, the scripting interface (**netsh**), the user interface, or from the USB flash configuration interface.</span></span>

<span data-ttu-id="8d8ed-106">Профиль, полученный от одной из этих систем, сопоставляется со \_ схемой профиля WLAN и хранится в хранилище профилей.</span><span class="sxs-lookup"><span data-stu-id="8d8ed-106">A profile received from one of these systems is mapped to the WLAN\_profile schema and stored in the profile store.</span></span> <span data-ttu-id="8d8ed-107">Профили можно экспортировать из хранилища профилей с помощью команд netsh или с помощью таких элементов API, как [**вланжетпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).</span><span class="sxs-lookup"><span data-stu-id="8d8ed-107">Profiles can be exported from the profile store using netsh commands or using API elements such as [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).</span></span>

<span data-ttu-id="8d8ed-108">Корневым элементом профиля WLAN является элемент [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8d8ed-108">The root element of a WLAN profile is the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span> <span data-ttu-id="8d8ed-109">Каждый профиль будет иметь только один корневой элемент.</span><span class="sxs-lookup"><span data-stu-id="8d8ed-109">Each profile will have exactly one root element.</span></span> <span data-ttu-id="8d8ed-110">Элемент **вланпрофиле** находится в пространстве имен `https://www.microsoft.com/networking/WLAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="8d8ed-110">The **WLANProfile** element is in the namespace `https://www.microsoft.com/networking/WLAN/profile/v1`.</span></span>

<span data-ttu-id="8d8ed-111">Чтобы просмотреть примеры профилей WLAN, см. раздел [образцы профилей беспроводной связи](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="8d8ed-111">To view sample WLAN profiles, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

-   [<span data-ttu-id="8d8ed-112">\_Элементы схемы профиля WLAN</span><span class="sxs-lookup"><span data-stu-id="8d8ed-112">WLAN\_profile Schema Elements</span></span>](wlan-profileschema-elements.md)
-   [<span data-ttu-id="8d8ed-113">\_Простые типы схемы профиля WLAN</span><span class="sxs-lookup"><span data-stu-id="8d8ed-113">WLAN\_profile Schema Simple Types</span></span>](wlan-profileschema-simple-types.md)

## <a name="related-topics"></a><span data-ttu-id="8d8ed-114">См. также</span><span class="sxs-lookup"><span data-stu-id="8d8ed-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8d8ed-115">[Команды Netsh для беспроводной локальной сети (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="8d8ed-115">[Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))</span></span>
</dt> </dl>

 

 
