---
title: Direct2D не поддерживает отрисовку в насыщенных метафайлах в Internet Explorer 9
description: Direct2D не поддерживает отрисовку в насыщенных метафайлах в Internet Explorer 9
ms.assetid: D106FBD6-F05E-41A6-B8F8-569EB9810E2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f51ae6d098c08c0a18656aae2adf3d79d68652
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314827"
---
# <a name="direct2d-does-not-support-rendering-to-rich-metafiles-in-internet-explorer-9"></a><span data-ttu-id="48aac-103">Direct2D не поддерживает отрисовку в насыщенных метафайлах в Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="48aac-103">Direct2D does not support rendering to rich metafiles in Internet Explorer 9</span></span>

## <a name="platforms"></a><span data-ttu-id="48aac-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="48aac-104">Platforms</span></span>

<span data-ttu-id="48aac-105">**Клиенты** — Windows Vista, Windows 7, Windows 8</span><span class="sxs-lookup"><span data-stu-id="48aac-105">**Clients** – Windows Vista, Windows 7, Windows 8</span></span>  
<span data-ttu-id="48aac-106">**Серверы** — windows Server 2008, windows Server 2008 R2, windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="48aac-106">**Servers** – Windows Server 2008, Windows Server 2008 R2, Windows Server 2012</span></span>  




## <a name="description"></a><span data-ttu-id="48aac-107">Описание</span><span class="sxs-lookup"><span data-stu-id="48aac-107">Description</span></span>

<span data-ttu-id="48aac-108">Благодаря внутренним изменениям отрисовки в Internet Explorer 9 интерфейсы API [ихтмлелементрендер::D равтодк](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) и [ивиевобжект::D RAW](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) теперь создают метафайл, содержащий один точечный рисунок, представляющий веб-содержимое, а не расширенный метафайл, содержащий сведения о тексте и векторе.</span><span class="sxs-lookup"><span data-stu-id="48aac-108">Due to internal rendering changes in Internet Explorer 9, the [IHTMLElementRender::DrawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) and [IViewObject::Draw](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) APIs will now create a metafile containing a single bitmap that represents the web content instead of a rich metafile containing text and vector info.</span></span> <span data-ttu-id="48aac-109">Это изменение было вызвано переходом с рендеринга GDI на аппаратное ускорение Direct2D (D2D).</span><span class="sxs-lookup"><span data-stu-id="48aac-109">This change was due to the move from GDI rendering to hardware-accelerated Direct2D (D2D) rendering.</span></span>

<span data-ttu-id="48aac-110">Это изменение влияет на приложения, использующие эти API, и использует текстовые или векторные сведения в метафайле.</span><span class="sxs-lookup"><span data-stu-id="48aac-110">This change affects apps that use these APIs and rely on text or vector info in the metafile.</span></span>

## <a name="manifestation"></a><span data-ttu-id="48aac-111">Проявление</span><span class="sxs-lookup"><span data-stu-id="48aac-111">Manifestation</span></span>

<span data-ttu-id="48aac-112">В зависимости от приложения, на которое влияет это изменение, пользователи могут столкнуться с поврежденным или неправильным поведением в своих приложениях.</span><span class="sxs-lookup"><span data-stu-id="48aac-112">Depending on the app that is affected by this change, users might see broken or incorrect behavior in their apps.</span></span>

## <a name="mitigation"></a><span data-ttu-id="48aac-113">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="48aac-113">Mitigation</span></span>

<span data-ttu-id="48aac-114">Приложения, для которых требуется извлечь текстовые данные из веб-документа (без сведений о размещении), могут использовать свойство [InnerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) для извлечения текста.</span><span class="sxs-lookup"><span data-stu-id="48aac-114">Apps that only need to extract text info from a web document (without positioning info) can use the [innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) property to extract text.</span></span>

<span data-ttu-id="48aac-115">Приложения, использующие Ивиевобжект::D RAW, могут использовать [функцию \_ ивиевобжектдрав \_ DMLT9 \_ с \_ ](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) ключом управления функциями GDI для возврата к отрисовке GDI, если режим документа:</span><span class="sxs-lookup"><span data-stu-id="48aac-115">Apps that use IViewObject::Draw can use the [FEATURE\_IVIEWOBJECTDRAW\_DMLT9\_WITH\_GDI](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) feature control key to revert to GDI rendering if the document mode:</span></span>

-   <span data-ttu-id="48aac-116">Меньше или равно 8</span><span class="sxs-lookup"><span data-stu-id="48aac-116">Is less or equal to 8</span></span>
-   <span data-ttu-id="48aac-117">ФКК разрешает этому узлу использовать GDI</span><span class="sxs-lookup"><span data-stu-id="48aac-117">The FCK authorizes that host to use GDI</span></span>
-   <span data-ttu-id="48aac-118">И в API передается метафайл DC</span><span class="sxs-lookup"><span data-stu-id="48aac-118">And a metafile DC is passed to the API</span></span>

## <a name="resources"></a><span data-ttu-id="48aac-119">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="48aac-119">Resources</span></span>

-   <span data-ttu-id="48aac-120">[Ихтмлелементрендер::D Равтодк](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="48aac-120">[IHTMLElementRender::DrawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))</span></span>
-   [<span data-ttu-id="48aac-121">Ивиевобжект::D RAW</span><span class="sxs-lookup"><span data-stu-id="48aac-121">IViewObject::Draw</span></span>](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw)
-   <span data-ttu-id="48aac-122">[Свойство Ихтмлелемент:: innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="48aac-122">[IHTMLElement::innerText Property](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))</span></span>
-   <span data-ttu-id="48aac-123">[Элементы управления функциями Интернета (I. Н](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="48aac-123">[Internet Feature Controls (I..L)](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))</span></span>

 

 