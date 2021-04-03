---
description: API истории файлов
ms.assetid: 7488BA36-DEBE-42F1-8A12-A2DB1DE8B827
title: API истории файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb612a0bbbbd28b703a82bc65c5cd4d33640f760
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990473"
---
# <a name="file-history-api"></a><span data-ttu-id="18c76-103">API истории файлов</span><span class="sxs-lookup"><span data-stu-id="18c76-103">File History API</span></span>

## <a name="in-this-section"></a><span data-ttu-id="18c76-104">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="18c76-104">In this section</span></span>

-   [<span data-ttu-id="18c76-105">**\_Состояние резервного копирования FH \_**</span><span class="sxs-lookup"><span data-stu-id="18c76-105">**FH\_BACKUP\_STATUS**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_backup_status)
-   [<span data-ttu-id="18c76-106">**\_ \_ результат проверки устройства \_ FH**</span><span class="sxs-lookup"><span data-stu-id="18c76-106">**FH\_DEVICE\_VALIDATION\_RESULT**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_device_validation_result)
-   [<span data-ttu-id="18c76-107">**\_тип локальной \_ политики \_ FH**</span><span class="sxs-lookup"><span data-stu-id="18c76-107">**FH\_LOCAL\_POLICY\_TYPE**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_local_policy_type)
-   [<span data-ttu-id="18c76-108">**\_Категория защищенного \_ элемента FH \_**</span><span class="sxs-lookup"><span data-stu-id="18c76-108">**FH\_PROTECTED\_ITEM\_CATEGORY**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_protected_item_category)
-   [<span data-ttu-id="18c76-109">**\_типы хранения \_ FH**</span><span class="sxs-lookup"><span data-stu-id="18c76-109">**FH\_RETENTION\_TYPES**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_retention_types)
-   [<span data-ttu-id="18c76-110">**\_типы целевых \_ дисков \_ FH**</span><span class="sxs-lookup"><span data-stu-id="18c76-110">**FH\_TARGET\_DRIVE\_TYPES**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_target_drive_types)
-   [<span data-ttu-id="18c76-111">**\_тип целевого \_ свойства \_ FH**</span><span class="sxs-lookup"><span data-stu-id="18c76-111">**FH\_TARGET\_PROPERTY\_TYPE**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_target_property_type)
-   [<span data-ttu-id="18c76-112">**фхконфигмгр**</span><span class="sxs-lookup"><span data-stu-id="18c76-112">**FhConfigMgr**</span></span>](fhconfigmgr.md)
-   [<span data-ttu-id="18c76-113">FhManagew.exe</span><span class="sxs-lookup"><span data-stu-id="18c76-113">FhManagew.exe</span></span>](fhmanagew-exe.md)
-   [<span data-ttu-id="18c76-114">**фхреассоЦиатион**</span><span class="sxs-lookup"><span data-stu-id="18c76-114">**FhReassociation**</span></span>](fhreassociation.md)
-   [<span data-ttu-id="18c76-115">**фхсервицеклосепипе**</span><span class="sxs-lookup"><span data-stu-id="18c76-115">**FhServiceClosePipe**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceclosepipe)
-   [<span data-ttu-id="18c76-116">**фхсервицеопенпипе**</span><span class="sxs-lookup"><span data-stu-id="18c76-116">**FhServiceOpenPipe**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceopenpipe)
-   [<span data-ttu-id="18c76-117">**фхсервицерелоадконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="18c76-117">**FhServiceReloadConfiguration**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhservicereloadconfiguration)
-   [<span data-ttu-id="18c76-118">**фхсервицеблоккбаккуп**</span><span class="sxs-lookup"><span data-stu-id="18c76-118">**FhServiceBlockBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceblockbackup)
-   [<span data-ttu-id="18c76-119">**фхсервицестартбаккуп**</span><span class="sxs-lookup"><span data-stu-id="18c76-119">**FhServiceStartBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhservicestartbackup)
-   [<span data-ttu-id="18c76-120">**фхсервицестопбаккуп**</span><span class="sxs-lookup"><span data-stu-id="18c76-120">**FhServiceStopBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhservicestopbackup)
-   [<span data-ttu-id="18c76-121">**фхсервицеунблоккбаккуп**</span><span class="sxs-lookup"><span data-stu-id="18c76-121">**FhServiceUnblockBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceunblockbackup)
-   [<span data-ttu-id="18c76-122">**ифхконфигмгр**</span><span class="sxs-lookup"><span data-stu-id="18c76-122">**IFhConfigMgr**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr)
-   [<span data-ttu-id="18c76-123">**ифхреассоЦиатион**</span><span class="sxs-lookup"><span data-stu-id="18c76-123">**IFhReassociation**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation)
-   [<span data-ttu-id="18c76-124">**ифхскопеитератор**</span><span class="sxs-lookup"><span data-stu-id="18c76-124">**IFhScopeIterator**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhscopeiterator)
-   [<span data-ttu-id="18c76-125">**ифхтаржет**</span><span class="sxs-lookup"><span data-stu-id="18c76-125">**IFhTarget**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhtarget)

 

 



