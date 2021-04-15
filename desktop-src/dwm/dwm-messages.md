---
title: Сообщения DWM
description: В этом разделе содержатся сведения о диспетчер окон рабочего стола (DWM) сообщений.
ms.assetid: FF251CDA-7D68-4dd0-A54B-50B07E11C7C1
keywords:
- Диспетчер окон рабочего стола (DWM), справочные материалы
- DWM (диспетчер окон рабочего стола), Справочник
- Диспетчер окон рабочего стола (DWM), сообщения
- DWM (диспетчер окон рабочего стола), сообщения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399db1399cfc7cb60d29f0fa554a2233dc75a279
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "105710229"
---
# <a name="dwm-messages"></a><span data-ttu-id="61ec3-107">Сообщения DWM</span><span class="sxs-lookup"><span data-stu-id="61ec3-107">DWM Messages</span></span>

<span data-ttu-id="61ec3-108">В этом разделе содержатся сведения о диспетчер окон рабочего стола (DWM) сообщений.</span><span class="sxs-lookup"><span data-stu-id="61ec3-108">This section contains information about the Desktop Window Manager (DWM) messages.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="61ec3-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="61ec3-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61ec3-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="61ec3-110">Topic</span></span></th>
<th><span data-ttu-id="61ec3-111">Описание</span><span class="sxs-lookup"><span data-stu-id="61ec3-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61ec3-112"><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="61ec3-112"><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="61ec3-113">Информирует все окна верхнего уровня о том, что цвет цветов изменился.</span><span class="sxs-lookup"><span data-stu-id="61ec3-113">Informs all top-level windows that the colorization color has changed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61ec3-114"><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="61ec3-114"><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="61ec3-115">Информирует все окна верхнего уровня, что композиция DWM включена или отключена.</span><span class="sxs-lookup"><span data-stu-id="61ec3-115">Informs all top-level windows that DWM composition has been enabled or disabled.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="61ec3-116">Начиная с Windows 8, композиция DWM всегда включена, поэтому это сообщение не отправляется независимо от изменения видеорежима.</span><span class="sxs-lookup"><span data-stu-id="61ec3-116">As of Windows 8, DWM composition is always enabled, so this message is not sent regardless of video mode changes.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61ec3-117"><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="61ec3-117"><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="61ec3-118">Посылается, когда изменилась политика отрисовки области, не являющейся клиентской.</span><span class="sxs-lookup"><span data-stu-id="61ec3-118">Sent when the non-client area rendering policy has changed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61ec3-119"><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a></span><span class="sxs-lookup"><span data-stu-id="61ec3-119"><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a></span></span><br/></td>
<td><span data-ttu-id="61ec3-120">Указывает окну указать статический точечный рисунок для использования в качестве <em>динамического предварительного просмотра</em> (также известного как <em>Предварительный просмотр</em>) этого окна.</span><span class="sxs-lookup"><span data-stu-id="61ec3-120">Instructs a window to provide a static bitmap to use as a <em>live preview</em> (also known as a <em>Peek preview</em>) of that window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61ec3-121"><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="61ec3-121"><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a></span></span><br/></td>
<td><span data-ttu-id="61ec3-122">Указывает окну указать статический точечный рисунок для использования в качестве эскиза этого окна.</span><span class="sxs-lookup"><span data-stu-id="61ec3-122">Instructs a window to provide a static bitmap to use as a thumbnail representation of that window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61ec3-123"><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="61ec3-123"><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a></span></span><br/></td>
<td><span data-ttu-id="61ec3-124">Посылается, когда оконное окно DWM разворачивается.</span><span class="sxs-lookup"><span data-stu-id="61ec3-124">Sent when a DWM composed window is maximized.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





