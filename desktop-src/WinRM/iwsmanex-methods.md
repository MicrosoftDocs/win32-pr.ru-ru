---
title: Методы Ивсманекс
description: Интерфейс Ивсманекс предоставляет следующие методы.
ms.assetid: 609F5D75-879A-4681-B746-8C7A8757F062
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7279d15d98b3e534e57a83813cd9cbe75a09fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067256"
---
# <a name="iwsmanex-methods"></a><span data-ttu-id="e121d-103">Методы Ивсманекс</span><span class="sxs-lookup"><span data-stu-id="e121d-103">IWSManEx Methods</span></span>

<span data-ttu-id="e121d-104">Интерфейс [**ивсманекс**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e121d-104">The [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e121d-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="e121d-105">In this section</span></span>

-   [<span data-ttu-id="e121d-106">**Метод Креатересаурцелокатор**</span><span class="sxs-lookup"><span data-stu-id="e121d-106">**CreateResourceLocator Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator)
-   [<span data-ttu-id="e121d-107">**Метод Енумератионфлагхиерарчидип**</span><span class="sxs-lookup"><span data-stu-id="e121d-107">**EnumerationFlagHierarchyDeep Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep)
-   [<span data-ttu-id="e121d-108">**Метод Енумератионфлагхиерарчидипбасепропсонли**</span><span class="sxs-lookup"><span data-stu-id="e121d-108">**EnumerationFlagHierarchyDeepBasePropsOnly Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly)
-   [<span data-ttu-id="e121d-109">**Метод Енумератионфлагхиерарчишаллов**</span><span class="sxs-lookup"><span data-stu-id="e121d-109">**EnumerationFlagHierarchyShallow Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow)
-   [<span data-ttu-id="e121d-110">**Метод Енумератионфлагнонксмлтекст**</span><span class="sxs-lookup"><span data-stu-id="e121d-110">**EnumerationFlagNonXmlText Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext)
-   [<span data-ttu-id="e121d-111">**Метод Енумератионфлагретурнепр**</span><span class="sxs-lookup"><span data-stu-id="e121d-111">**EnumerationFlagReturnEPR Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr)
-   [<span data-ttu-id="e121d-112">**Метод Енумератионфлагретурнобжект**</span><span class="sxs-lookup"><span data-stu-id="e121d-112">**EnumerationFlagReturnObject Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject)
-   [<span data-ttu-id="e121d-113">**Метод Енумератионфлагретурнобжектандепр**</span><span class="sxs-lookup"><span data-stu-id="e121d-113">**EnumerationFlagReturnObjectAndEPR Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr)
-   [<span data-ttu-id="e121d-114">**Метод Жетеррормессаже**</span><span class="sxs-lookup"><span data-stu-id="e121d-114">**GetErrorMessage Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage)
-   [<span data-ttu-id="e121d-115">**Метод Сессионфлагкредусернамепассворд**</span><span class="sxs-lookup"><span data-stu-id="e121d-115">**SessionFlagCredUsernamePassword Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword)
-   [<span data-ttu-id="e121d-116">**Метод Сессионфлаженаблеспнсерверпорт**</span><span class="sxs-lookup"><span data-stu-id="e121d-116">**SessionFlagEnableSPNServerPort Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport)
-   [<span data-ttu-id="e121d-117">**Метод Сессионфлагноенкриптион**</span><span class="sxs-lookup"><span data-stu-id="e121d-117">**SessionFlagNoEncryption Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption)
-   [<span data-ttu-id="e121d-118">**Метод Сессионфлагскипкачекк**</span><span class="sxs-lookup"><span data-stu-id="e121d-118">**SessionFlagSkipCACheck Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck)
-   [<span data-ttu-id="e121d-119">**Метод Сессионфлагскипкнчекк**</span><span class="sxs-lookup"><span data-stu-id="e121d-119">**SessionFlagSkipCNCheck Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck)
-   [<span data-ttu-id="e121d-120">**Метод Сессионфлагусебасик**</span><span class="sxs-lookup"><span data-stu-id="e121d-120">**SessionFlagUseBasic Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic)
-   [<span data-ttu-id="e121d-121">**Метод Сессионфлагуседижест**</span><span class="sxs-lookup"><span data-stu-id="e121d-121">**SessionFlagUseDigest Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest)
-   [<span data-ttu-id="e121d-122">**Метод Сессионфлагусекерберос**</span><span class="sxs-lookup"><span data-stu-id="e121d-122">**SessionFlagUseKerberos Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos)
-   [<span data-ttu-id="e121d-123">**Метод Сессионфлагусенеготиате**</span><span class="sxs-lookup"><span data-stu-id="e121d-123">**SessionFlagUseNegotiate Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate)
-   [<span data-ttu-id="e121d-124">**Метод Сессионфлагусеноаусентикатион**</span><span class="sxs-lookup"><span data-stu-id="e121d-124">**SessionFlagUseNoAuthentication Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication)
-   [<span data-ttu-id="e121d-125">**Метод SessionFlagUTF8**</span><span class="sxs-lookup"><span data-stu-id="e121d-125">**SessionFlagUTF8 Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8)

 

 




