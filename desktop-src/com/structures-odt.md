---
title: Структуры (OLE и Передача данных)
description: Следующие структуры используются для реализации составных документов и выполнения обмена данными между приложениями.
ms.assetid: 76fef2dd-4cfb-4526-a1e0-8e3218aa6145
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa9dde7f81d388943dbc05b2d38065be262d7f29
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070966"
---
# <a name="structures-ole-and-data-transfer"></a><span data-ttu-id="d8198-103">Структуры (OLE и Передача данных)</span><span class="sxs-lookup"><span data-stu-id="d8198-103">Structures (OLE and Data Transfer)</span></span>

<span data-ttu-id="d8198-104">Следующие структуры используются для реализации составных документов и выполнения обмена данными между приложениями.</span><span class="sxs-lookup"><span data-stu-id="d8198-104">The following structures are used to implement compound documents and perform data transfer between applications.</span></span>

-   [<span data-ttu-id="d8198-105">**дваспектинфо**</span><span class="sxs-lookup"><span data-stu-id="d8198-105">**DVASPECTINFO**</span></span>](/windows/win32/api/ocidl/ne-ocidl-dvaspectinfoflag)
-   [<span data-ttu-id="d8198-106">**двекстентинфо**</span><span class="sxs-lookup"><span data-stu-id="d8198-106">**DVEXTENTINFO**</span></span>](/windows/win32/api/ocidl/ns-ocidl-dvextentinfo)
-   [<span data-ttu-id="d8198-107">**двтаржетдевице**</span><span class="sxs-lookup"><span data-stu-id="d8198-107">**DVTARGETDEVICE**</span></span>](/windows/win32/api/objidl/ns-objidl-dvtargetdevice)
-   [<span data-ttu-id="d8198-108">**форматетк**</span><span class="sxs-lookup"><span data-stu-id="d8198-108">**FORMATETC**</span></span>](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc)
-   [<span data-ttu-id="d8198-109">**обжектдескриптор**</span><span class="sxs-lookup"><span data-stu-id="d8198-109">**OBJECTDESCRIPTOR**</span></span>](/windows/win32/api/oleidl/ns-oleidl-objectdescriptor)
-   [<span data-ttu-id="d8198-110">**олекмд**</span><span class="sxs-lookup"><span data-stu-id="d8198-110">**OLECMD**</span></span>](/windows/desktop/api/DocObj/ns-docobj-olecmd)
-   [<span data-ttu-id="d8198-111">**олекмдтекст**</span><span class="sxs-lookup"><span data-stu-id="d8198-111">**OLECMDTEXT**</span></span>](/windows/desktop/api/DocObj/ns-docobj-olecmdtext)
-   [<span data-ttu-id="d8198-112">**олеинплацефрамеинфо**</span><span class="sxs-lookup"><span data-stu-id="d8198-112">**OLEINPLACEFRAMEINFO**</span></span>](/windows/win32/api/oleidl/ns-oleidl-oleinplaceframeinfo)
-   [<span data-ttu-id="d8198-113">**олеменуграупвидсс**</span><span class="sxs-lookup"><span data-stu-id="d8198-113">**OLEMENUGROUPWIDTHS**</span></span>](/windows/win32/api/oleidl/ns-oleidl-olemenugroupwidths)
-   [<span data-ttu-id="d8198-114">**олеуибуси**</span><span class="sxs-lookup"><span data-stu-id="d8198-114">**OLEUIBUSY**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuibusya)
-   [<span data-ttu-id="d8198-115">**олеуичанжеикон**</span><span class="sxs-lookup"><span data-stu-id="d8198-115">**OLEUICHANGEICON**</span></span>](/windows/win32/api/oledlg/nf-oledlg-oleuichangeicona)
-   [<span data-ttu-id="d8198-116">**олеуичанжесаурце**</span><span class="sxs-lookup"><span data-stu-id="d8198-116">**OLEUICHANGESOURCE**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuichangesourcea)
-   [<span data-ttu-id="d8198-117">**олеуиконверт**</span><span class="sxs-lookup"><span data-stu-id="d8198-117">**OLEUICONVERT**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuiconverta)
-   [<span data-ttu-id="d8198-118">**олеуиедитлинкс**</span><span class="sxs-lookup"><span data-stu-id="d8198-118">**OLEUIEDITLINKS**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuieditlinksa)
-   [<span data-ttu-id="d8198-119">**олеуигнрлпропс**</span><span class="sxs-lookup"><span data-stu-id="d8198-119">**OLEUIGNRLPROPS**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuignrlpropsa)
-   [<span data-ttu-id="d8198-120">**олеуиинсертобжект**</span><span class="sxs-lookup"><span data-stu-id="d8198-120">**OLEUIINSERTOBJECT**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuiinsertobjecta)
-   [<span data-ttu-id="d8198-121">**олеуилинкпропс**</span><span class="sxs-lookup"><span data-stu-id="d8198-121">**OLEUILINKPROPS**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuilinkpropsa)
-   [<span data-ttu-id="d8198-122">**олеуиобжектпропс**</span><span class="sxs-lookup"><span data-stu-id="d8198-122">**OLEUIOBJECTPROPS**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuiobjectpropsa)
-   [<span data-ttu-id="d8198-123">**олеуипастинтри**</span><span class="sxs-lookup"><span data-stu-id="d8198-123">**OLEUIPASTEENTRY**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuipasteentrya)
-   [<span data-ttu-id="d8198-124">**олеуипастеспеЦиал**</span><span class="sxs-lookup"><span data-stu-id="d8198-124">**OLEUIPASTESPECIAL**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuipastespeciala)
-   [<span data-ttu-id="d8198-125">**олеуивиевпропс**</span><span class="sxs-lookup"><span data-stu-id="d8198-125">**OLEUIVIEWPROPS**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuiviewpropsa)
-   [<span data-ttu-id="d8198-126">**олеверб**</span><span class="sxs-lookup"><span data-stu-id="d8198-126">**OLEVERB**</span></span>](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
-   [<span data-ttu-id="d8198-127">**POINTF**</span><span class="sxs-lookup"><span data-stu-id="d8198-127">**POINTF**</span></span>](/windows/win32/api/ocidl/ns-ocidl-pointf)
-   [<span data-ttu-id="d8198-128">**статдата**</span><span class="sxs-lookup"><span data-stu-id="d8198-128">**STATDATA**</span></span>](/windows/desktop/api/ObjIdl/nn-objidl-ienumstatdata)
-   [<span data-ttu-id="d8198-129">**стгмедиум**</span><span class="sxs-lookup"><span data-stu-id="d8198-129">**STGMEDIUM**</span></span>](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)

 

 




