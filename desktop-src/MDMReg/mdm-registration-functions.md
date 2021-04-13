---
title: Функции регистрации MDM
description: Регистрация MDM используется для следующих функций.
ms.assetid: 1b063a56-f59f-4b02-949f-c8b6bbf45a13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821e08d9c6631bbb300a86ab6b9c480a3af0c25b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104339441"
---
# <a name="mdm-registration-functions"></a><span data-ttu-id="77b37-103">Функции регистрации MDM</span><span class="sxs-lookup"><span data-stu-id="77b37-103">MDM Registration Functions</span></span>

<span data-ttu-id="77b37-104">Регистрация MDM используется для следующих функций.</span><span class="sxs-lookup"><span data-stu-id="77b37-104">The following functions are used by MDM Registration.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="77b37-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="77b37-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="77b37-106">**дисковерманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="77b37-106">**DiscoverManagementService**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementservice)
</dt> <dd>

<span data-ttu-id="77b37-107">Обнаружение службы MDM.</span><span class="sxs-lookup"><span data-stu-id="77b37-107">Discovers the MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="77b37-108">**дисковерманажементсервицеекс**</span><span class="sxs-lookup"><span data-stu-id="77b37-108">**DiscoverManagementServiceEx**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex)
</dt> <dd>

<span data-ttu-id="77b37-109">Обнаружение службы MDM с помощью сервера-кандидата.</span><span class="sxs-lookup"><span data-stu-id="77b37-109">Discovers the MDM service using a candidate server.</span></span>

</dd> <dt>

[<span data-ttu-id="77b37-110">**жетдевицерегистратионинфо**</span><span class="sxs-lookup"><span data-stu-id="77b37-110">**GetDeviceRegistrationInfo**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo)
</dt> <dd>

<span data-ttu-id="77b37-111">Извлекает сведения о регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="77b37-111">Retrieves the device registration information.</span></span>

</dd> <dt>

[<span data-ttu-id="77b37-112">**жетманажементапфиперлинк**</span><span class="sxs-lookup"><span data-stu-id="77b37-112">**GetManagementAppHyperlink**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink)
</dt> <dd>

<span data-ttu-id="77b37-113">Извлекает гиперссылку приложения управления, связанной со службой MDM.</span><span class="sxs-lookup"><span data-stu-id="77b37-113">Retrieves the management app hyperlink associated with the MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="77b37-114">**исдевицерегистередвисманажемент**</span><span class="sxs-lookup"><span data-stu-id="77b37-114">**IsDeviceRegisteredWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement)
</dt> <dd>

<span data-ttu-id="77b37-115">Проверяет, зарегистрировано ли устройство в службе MDM.</span><span class="sxs-lookup"><span data-stu-id="77b37-115">Checks whether the device is registered with an MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="77b37-116">**исманажементрегистратионалловед**</span><span class="sxs-lookup"><span data-stu-id="77b37-116">**IsManagementRegistrationAllowed**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed)
</dt> <dd>

<span data-ttu-id="77b37-117">Проверяет, разрешена ли регистрация MDM локальной политикой.</span><span class="sxs-lookup"><span data-stu-id="77b37-117">Checks whether MDM registration is allowed by local policy.</span></span>

</dd> <dt>

[<span data-ttu-id="77b37-118">**регистердевицевисманажемент**</span><span class="sxs-lookup"><span data-stu-id="77b37-118">**RegisterDeviceWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement)
</dt> <dd>

<span data-ttu-id="77b37-119">Регистрирует устройство в службе MDM, используя [ \[ протокол MS-MDE \] : Mobile Device](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267)Register.</span><span class="sxs-lookup"><span data-stu-id="77b37-119">Registers a device with a MDM service, using the [\[MS-MDE\]: Mobile Device Enrollment Protocol](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267).</span></span>

</dd> <dt>

[<span data-ttu-id="77b37-120">**регистердевицевисманажементусингаадкредентиалс**</span><span class="sxs-lookup"><span data-stu-id="77b37-120">**RegisterDeviceWithManagementUsingAADCredentials**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials)
</dt> <dd>

<span data-ttu-id="77b37-121">Регистрирует устройство в службе MDM, используя учетные данные Azure Active Directory (AAD).</span><span class="sxs-lookup"><span data-stu-id="77b37-121">Registers a device with a MDM service, using Azure Active Directory (AAD) credentials.</span></span>

</dd> <dt>

[<span data-ttu-id="77b37-122">**сетманажедекстерналли**</span><span class="sxs-lookup"><span data-stu-id="77b37-122">**SetManagedExternally**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally)
</dt> <dd>

<span data-ttu-id="77b37-123">Указывает агенту MDM, что устройство управляется извне и не регистрируется в службе MDM.</span><span class="sxs-lookup"><span data-stu-id="77b37-123">Indicates to the MDM agent that the device is managed externally and is not to be registered with an MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="77b37-124">**унрегистердевицевисманажемент**</span><span class="sxs-lookup"><span data-stu-id="77b37-124">**UnregisterDeviceWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement)
</dt> <dd>

<span data-ttu-id="77b37-125">Отмена регистрации устройства в службе MDM</span><span class="sxs-lookup"><span data-stu-id="77b37-125">Unregisters a device with the MDM service</span></span>

</dd> </dl>

 

 