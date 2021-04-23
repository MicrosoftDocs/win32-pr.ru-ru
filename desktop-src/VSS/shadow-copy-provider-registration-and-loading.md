---
description: Регистрация и загрузка поставщика теневого копирования
ms.assetid: f9bb72ce-9a2b-43cd-9697-1f6598a46e3e
title: Регистрация и загрузка поставщика теневого копирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725613ff37450075c964b3c66fce3ffba1a70529
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345002"
---
# <a name="shadow-copy-provider-registration-and-loading"></a><span data-ttu-id="40824-103">Регистрация и загрузка поставщика теневого копирования</span><span class="sxs-lookup"><span data-stu-id="40824-103">Shadow Copy Provider Registration and Loading</span></span>

## <a name="provider-registration"></a><span data-ttu-id="40824-104">Регистрация поставщика</span><span class="sxs-lookup"><span data-stu-id="40824-104">Provider Registration</span></span>

<span data-ttu-id="40824-105">Только поставщики вызовов VSS.</span><span class="sxs-lookup"><span data-stu-id="40824-105">Only VSS calls providers.</span></span> <span data-ttu-id="40824-106">Поставщик регистрируется для вызовов, вызывая [**ивссадмин:: RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), передавая **\_ \_ оборудование VSS Prov** для параметра *епровидертипе* .</span><span class="sxs-lookup"><span data-stu-id="40824-106">The provider registers for calls by invoking [**IVssAdmin::RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), passing **VSS\_PROV\_HARDWARE** for the *eProviderType* parameter.</span></span> <span data-ttu-id="40824-107">После регистрации поставщик будет задействован в управлении теневыми копиями до отмены регистрации с помощью [**ивссадмин:: унрегистерпровидер**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).</span><span class="sxs-lookup"><span data-stu-id="40824-107">Once registered, the provider will be involved in shadow copy management until unregistering using [**IVssAdmin::UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).</span></span>

## <a name="provider-loading-and-unloading"></a><span data-ttu-id="40824-108">Загрузка и выгрузка поставщика</span><span class="sxs-lookup"><span data-stu-id="40824-108">Provider Loading and Unloading</span></span>

<span data-ttu-id="40824-109">Поставщики можно часто загружать и выгружать.</span><span class="sxs-lookup"><span data-stu-id="40824-109">Providers can be frequently loaded and unloaded.</span></span> <span data-ttu-id="40824-110">Поставщики могут реализовывать [**ивсспровидернотификатионс**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) , чтобы определить, когда служба VSS загружает или выгружает поставщик.</span><span class="sxs-lookup"><span data-stu-id="40824-110">Providers can implement [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) to determine when VSS is loading or unloading the provider.</span></span>

 

 



