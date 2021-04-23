---
description: Интерфейсы API цифровой подписи XPS
ms.assetid: 44244035-f7d5-47f1-b4d8-b895562be855
title: Интерфейсы API цифровой подписи XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160fc532ed90cb41e4d0cb524daba87f72edefd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684294"
---
# <a name="xps-digital-signature-api-interfaces"></a><span data-ttu-id="d01df-103">Интерфейсы API цифровой подписи XPS</span><span class="sxs-lookup"><span data-stu-id="d01df-103">XPS Digital Signature API Interfaces</span></span>

## <a name="contents"></a><span data-ttu-id="d01df-104">Содержимое</span><span class="sxs-lookup"><span data-stu-id="d01df-104">Contents</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d01df-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="d01df-105">In this section</span></span>



| <span data-ttu-id="d01df-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="d01df-106">Interface</span></span>                                                                           | <span data-ttu-id="d01df-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d01df-107">Description</span></span>                                                                                         |
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d01df-108">**икспссигнатуре**</span><span class="sxs-lookup"><span data-stu-id="d01df-108">**IXpsSignature**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature)<br/>                                   | <span data-ttu-id="d01df-109">Представляет одну цифровую подпись.</span><span class="sxs-lookup"><span data-stu-id="d01df-109">Represents a single digital signature.</span></span><br/>                                                   |
| [<span data-ttu-id="d01df-110">**икспссигнатуреблокк**</span><span class="sxs-lookup"><span data-stu-id="d01df-110">**IXpsSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)<br/>                         | <span data-ttu-id="d01df-111">Представляет блок запросов сигнатур, которые хранятся в Сигнатуредефинитионс части.</span><span class="sxs-lookup"><span data-stu-id="d01df-111">Represents a block of signature requests that are stored in a SignatureDefinitions part.</span></span><br/> |
| [<span data-ttu-id="d01df-112">**икспссигнатуреблоккколлектион**</span><span class="sxs-lookup"><span data-stu-id="d01df-112">**IXpsSignatureBlockCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)<br/>     | <span data-ttu-id="d01df-113">Коллекция интерфейсов [**икспссигнатуреблокк**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) .</span><span class="sxs-lookup"><span data-stu-id="d01df-113">A collection of [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) interfaces.</span></span><br/>             |
| [<span data-ttu-id="d01df-114">**икспссигнатуреколлектион**</span><span class="sxs-lookup"><span data-stu-id="d01df-114">**IXpsSignatureCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)<br/>               | <span data-ttu-id="d01df-115">Коллекция указателей интерфейса [**икспссигнатуре**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) .</span><span class="sxs-lookup"><span data-stu-id="d01df-115">A collection of [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) interface pointers.</span></span><br/>               |
| [<span data-ttu-id="d01df-116">**икспссигнатуреманажер**</span><span class="sxs-lookup"><span data-stu-id="d01df-116">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)<br/>                     | <span data-ttu-id="d01df-117">Управляет цифровыми подписями и запросами цифровых подписей документа XPS.</span><span class="sxs-lookup"><span data-stu-id="d01df-117">Manages the digital signatures and digital signature requests of an XPS document.</span></span><br/>        |
| [<span data-ttu-id="d01df-118">**икспссигнатуререкуест**</span><span class="sxs-lookup"><span data-stu-id="d01df-118">**IXpsSignatureRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)<br/>                     | <span data-ttu-id="d01df-119">Обращается к компонентам запроса подписи.</span><span class="sxs-lookup"><span data-stu-id="d01df-119">Accesses the components of a signature request.</span></span><br/>                                          |
| [<span data-ttu-id="d01df-120">**икспссигнатуререкуестколлектион**</span><span class="sxs-lookup"><span data-stu-id="d01df-120">**IXpsSignatureRequestCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)<br/> | <span data-ttu-id="d01df-121">Коллекция интерфейсов [**икспссигнатуререкуест**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) .</span><span class="sxs-lookup"><span data-stu-id="d01df-121">A collection of [**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) interfaces.</span></span><br/>         |
| [<span data-ttu-id="d01df-122">**икспссигнингоптионс**</span><span class="sxs-lookup"><span data-stu-id="d01df-122">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)<br/>                         | <span data-ttu-id="d01df-123">Предоставляет доступ к отдельным параметрам подписи, используемым новыми сигнатурами.</span><span class="sxs-lookup"><span data-stu-id="d01df-123">Provides access to the individual signing options that are used by new signatures.</span></span><br/>       |



 

 

 




