---
title: Специальные возможности элемента управления ActiveX без окон
description: В этом разделе описывается использование интерфейса API специальных возможностей Windows для обеспечения доступности элементов управления Microsoft ActiveX без окон.
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb0489cdd5de3ac34df361bfa3e7b3624ee18f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413351"
---
# <a name="windowless-activex-control-accessibility"></a><span data-ttu-id="d70af-103">Специальные возможности элемента управления ActiveX без окон</span><span class="sxs-lookup"><span data-stu-id="d70af-103">Windowless ActiveX Control Accessibility</span></span>

<span data-ttu-id="d70af-104">В этом разделе описывается использование интерфейса API специальных возможностей Windows для обеспечения доступности элементов управления Microsoft ActiveX без окон.</span><span class="sxs-lookup"><span data-stu-id="d70af-104">This section describes how to use the Windows Accessibility API to ensure that windowless Microsoft ActiveX controls are accessible.</span></span>

<span data-ttu-id="d70af-105">В Windows 8 включены новые интерфейсы API специальных возможностей Windows, упрощающие задачу реализации специальных возможностей для элементов управления ActiveX без окон.</span><span class="sxs-lookup"><span data-stu-id="d70af-105">Windows 8 includes new Windows Accessibility API interfaces that simplify the task of implementing accessibility for windowless ActiveX controls.</span></span> <span data-ttu-id="d70af-106">API включает интерфейсы, реализованные в безоконном элементе управления и в контейнере элемента управления, что позволяет без оконного контроля и его контейнера работать вместе, чтобы предоставить сведения о специальных возможностях для безоконного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d70af-106">The API includes interfaces that are implemented on a windowless control and on the control container, enabling the windowless control and its container to work together to provide accessibility information about the windowless control.</span></span> <span data-ttu-id="d70af-107">API поддерживает следующие сценарии.</span><span class="sxs-lookup"><span data-stu-id="d70af-107">The API supports the following scenarios:</span></span>

-   <span data-ttu-id="d70af-108">Microsoft Active Accessibility безоконные элементы управления, размещенные в контейнере элемента управления Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="d70af-108">Microsoft Active Accessibility windowless controls hosted in a Microsoft Active Accessibility control container.</span></span>
-   <span data-ttu-id="d70af-109">Microsoft Active Accessibility безоконные элементы управления, размещенные в контейнере элементов управления Microsoft UI Automation.</span><span class="sxs-lookup"><span data-stu-id="d70af-109">Microsoft Active Accessibility windowless controls hosted in a Microsoft UI Automation control container.</span></span>
-   <span data-ttu-id="d70af-110">Элементы управления без окон модели автоматизации пользовательского интерфейса, размещенные в контейнере элемента управления Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="d70af-110">UI Automation windowless controls hosted in a Microsoft Active Accessibility control container.</span></span>
-   <span data-ttu-id="d70af-111">Элементы управления без окон модели автоматизации пользовательского интерфейса, размещенные в контейнере элементов управления модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d70af-111">UI Automation windowless controls hosted in a UI Automation control container.</span></span>

<span data-ttu-id="d70af-112">В следующей таблице перечислены интерфейсы, которые поддерживают элементы управления ActiveX без окон и идентифицируются объекты, реализующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="d70af-112">The following table lists the interfaces that support windowless ActiveX controls and identifies the objects that implement the interfaces.</span></span>



| <span data-ttu-id="d70af-113">Объект</span><span class="sxs-lookup"><span data-stu-id="d70af-113">Object</span></span>              | <span data-ttu-id="d70af-114">MSAA</span><span class="sxs-lookup"><span data-stu-id="d70af-114">MSAA</span></span>                                                                             | <span data-ttu-id="d70af-115">автоматизация пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="d70af-115">UI automation</span></span>                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d70af-116">Управляющий объект</span><span class="sxs-lookup"><span data-stu-id="d70af-116">Control object</span></span>      | [<span data-ttu-id="d70af-117">**иакцессиблехандлер**</span><span class="sxs-lookup"><span data-stu-id="d70af-117">**IAccessibleHandler**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| <span data-ttu-id="d70af-118">Сайт управления</span><span class="sxs-lookup"><span data-stu-id="d70af-118">Control site</span></span>        | [<span data-ttu-id="d70af-119">**иакцессиблевиндовлесссите**</span><span class="sxs-lookup"><span data-stu-id="d70af-119">**IAccessibleWindowlessSite**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [<span data-ttu-id="d70af-120">**иравелементпровидервиндовлесссите**</span><span class="sxs-lookup"><span data-stu-id="d70af-120">**IRawElementProviderWindowlessSite**</span></span>](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| <span data-ttu-id="d70af-121">Корневой элемент главного окна</span><span class="sxs-lookup"><span data-stu-id="d70af-121">Root of host window</span></span> | [<span data-ttu-id="d70af-122">**иакцессиблехостинжелементпровидерс**</span><span class="sxs-lookup"><span data-stu-id="d70af-122">**IAccessibleHostingElementProviders**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [<span data-ttu-id="d70af-123">**иравелементпровидерхостингакцессиблес**</span><span class="sxs-lookup"><span data-stu-id="d70af-123">**IRawElementProviderHostingAccessibles**</span></span>](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a><span data-ttu-id="d70af-124">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="d70af-124">In this section</span></span>

-   [<span data-ttu-id="d70af-125">Использование модели автоматизации пользовательского интерфейса для обеспечения доступа к безоконному элементу управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="d70af-125">How to Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [<span data-ttu-id="d70af-126">Как использовать MSAA, чтобы сделать безоконный элемент управления ActiveX доступным</span><span class="sxs-lookup"><span data-stu-id="d70af-126">How to Use MSAA to Make a Windowless ActiveX Control Accessible</span></span>](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [<span data-ttu-id="d70af-127">Размещение элемента управления ActiveX без окон UI Automation</span><span class="sxs-lookup"><span data-stu-id="d70af-127">How to Host a UI Automation Windowless ActiveX Control</span></span>](host-a-ui-automation-windowless-activex-control.md)
-   [<span data-ttu-id="d70af-128">Размещение элемента управления ActiveX без окна MSAA</span><span class="sxs-lookup"><span data-stu-id="d70af-128">How to Host an MSAA Windowless ActiveX Control</span></span>](host-an-msaa-windowless-activex-control.md)

 

 