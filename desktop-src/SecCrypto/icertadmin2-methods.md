---
description: Интерфейс ICertAdmin2 предоставляет следующие методы.
ms.assetid: F6E0D863-5A78-48D5-8AED-DAEF80101B7E
title: Методы ICertAdmin2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 619e2afc9ee8e5e2eeab91893394e21e6c33ba14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664112"
---
# <a name="icertadmin2-methods"></a><span data-ttu-id="7a679-103">Методы ICertAdmin2</span><span class="sxs-lookup"><span data-stu-id="7a679-103">ICertAdmin2 Methods</span></span>

<span data-ttu-id="7a679-104">Интерфейс [**ICertAdmin2**](/windows/desktop/api/Certadm/nn-certadm-icertadmin2) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7a679-104">The [**ICertAdmin2**](/windows/desktop/api/Certadm/nn-certadm-icertadmin2) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7a679-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="7a679-105">In this section</span></span>

-   [<span data-ttu-id="7a679-106">**Метод DeleteRow**</span><span class="sxs-lookup"><span data-stu-id="7a679-106">**DeleteRow Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-deleterow)
-   [<span data-ttu-id="7a679-107">**Метод Денирекуест**</span><span class="sxs-lookup"><span data-stu-id="7a679-107">**DenyRequest Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-denyrequest)
-   [<span data-ttu-id="7a679-108">**Метод Жетарчиведкэй**</span><span class="sxs-lookup"><span data-stu-id="7a679-108">**GetArchivedKey Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getarchivedkey)
-   [<span data-ttu-id="7a679-109">**Метод Жеткапроперти**</span><span class="sxs-lookup"><span data-stu-id="7a679-109">**GetCAProperty Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcaproperty)
-   [<span data-ttu-id="7a679-110">**Метод Жеткапропертидисплайнаме**</span><span class="sxs-lookup"><span data-stu-id="7a679-110">**GetCAPropertyDisplayName Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcapropertydisplayname)
-   [<span data-ttu-id="7a679-111">**Метод Жеткапропертифлагс**</span><span class="sxs-lookup"><span data-stu-id="7a679-111">**GetCAPropertyFlags Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcapropertyflags)
-   [<span data-ttu-id="7a679-112">**Метод Жетконфижентри**</span><span class="sxs-lookup"><span data-stu-id="7a679-112">**GetConfigEntry Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getconfigentry)
-   [<span data-ttu-id="7a679-113">**Метод Жеткрл**</span><span class="sxs-lookup"><span data-stu-id="7a679-113">**GetCRL Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-getcrl)
-   [<span data-ttu-id="7a679-114">**Метод Жетмиролес**</span><span class="sxs-lookup"><span data-stu-id="7a679-114">**GetMyRoles Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getmyroles)
-   [<span data-ttu-id="7a679-115">**Метод Жетревокатионреасон**</span><span class="sxs-lookup"><span data-stu-id="7a679-115">**GetRevocationReason Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-getrevocationreason)
-   [<span data-ttu-id="7a679-116">**Метод Импортцертификате**</span><span class="sxs-lookup"><span data-stu-id="7a679-116">**ImportCertificate Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-importcertificate)
-   [<span data-ttu-id="7a679-117">**Метод Импорткэй**</span><span class="sxs-lookup"><span data-stu-id="7a679-117">**ImportKey Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-importkey)
-   [<span data-ttu-id="7a679-118">**Метод Исвалидцертификате**</span><span class="sxs-lookup"><span data-stu-id="7a679-118">**IsValidCertificate Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-isvalidcertificate)
-   [<span data-ttu-id="7a679-119">**Метод Публишкрл**</span><span class="sxs-lookup"><span data-stu-id="7a679-119">**PublishCRL Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-publishcrl)
-   [<span data-ttu-id="7a679-120">**Метод Публишкрлс**</span><span class="sxs-lookup"><span data-stu-id="7a679-120">**PublishCRLs Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-publishcrls)
-   [<span data-ttu-id="7a679-121">**Метод Ресубмитрекуест**</span><span class="sxs-lookup"><span data-stu-id="7a679-121">**ResubmitRequest Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-resubmitrequest)
-   [<span data-ttu-id="7a679-122">**Метод Revokecertificate не удалось**</span><span class="sxs-lookup"><span data-stu-id="7a679-122">**RevokeCertificate Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-revokecertificate)
-   [<span data-ttu-id="7a679-123">**Метод Сеткапроперти**</span><span class="sxs-lookup"><span data-stu-id="7a679-123">**SetCAProperty Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-setcaproperty)
-   [<span data-ttu-id="7a679-124">**Метод Сетцертификатикстенсион**</span><span class="sxs-lookup"><span data-stu-id="7a679-124">**SetCertificateExtension Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-setcertificateextension)
-   [<span data-ttu-id="7a679-125">**Метод Сетконфижентри**</span><span class="sxs-lookup"><span data-stu-id="7a679-125">**SetConfigEntry Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-setconfigentry)
-   [<span data-ttu-id="7a679-126">**Метод Сетрекуестаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="7a679-126">**SetRequestAttributes Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-setrequestattributes)

 

 



