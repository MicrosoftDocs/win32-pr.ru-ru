---
title: Функции DirectComposition
description: В этом разделе описываются функции, предоставляемые Microsoft DirectComposition \ 32; API.
ms.assetid: 750FDFD5-ADD5-43B3-A596-ECDB82C2EF73
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 934e0b7e32f22faaefdf625e0af2a42a03e469d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134050"
---
# <a name="directcomposition-functions"></a><span data-ttu-id="a0b3e-103">Функции DirectComposition</span><span class="sxs-lookup"><span data-stu-id="a0b3e-103">DirectComposition functions</span></span>

<span data-ttu-id="a0b3e-104">В этом разделе описываются функции, предоставляемые API Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="a0b3e-104">This section describes the functions provided by the Microsoft DirectComposition API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a0b3e-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="a0b3e-105">In this section</span></span>



| <span data-ttu-id="a0b3e-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="a0b3e-106">Topic</span></span>                                                                                       | <span data-ttu-id="a0b3e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a0b3e-107">Description</span></span>                                                                                                                                          |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0b3e-108">**дкомпоситионаттачмауседрагтохвнд**</span><span class="sxs-lookup"><span data-stu-id="a0b3e-108">**DCompositionAttachMouseDragToHwnd**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositionattachmousedragtohwnd)<br/>   | <span data-ttu-id="a0b3e-109">Создает взаимодействие или Инпутсинк для перенаправления кнопки мыши вниз и всех последующих событий перемещения и вверх в заданный HWND.</span><span class="sxs-lookup"><span data-stu-id="a0b3e-109">Creates an Interaction/InputSink to route mouse button down and any subsequent move and up events to the given HWND.</span></span><br/>                      |
| [<span data-ttu-id="a0b3e-110">**дкомпоситионаттачмаусевхилтохвнд**</span><span class="sxs-lookup"><span data-stu-id="a0b3e-110">**DCompositionAttachMouseWheelToHwnd**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositionattachmousewheeltohwnd)<br/> | <span data-ttu-id="a0b3e-111">Создает взаимодействие или Инпутсинк для направления сообщений колесика мыши в заданный HWND.</span><span class="sxs-lookup"><span data-stu-id="a0b3e-111">Creates an Interaction/InputSink to route mouse wheel messages to the given HWND.</span></span> <br/>                                                        |
| [<span data-ttu-id="a0b3e-112">**дкомпоситионкреатедевице**</span><span class="sxs-lookup"><span data-stu-id="a0b3e-112">**DCompositionCreateDevice**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice)<br/>                     | <span data-ttu-id="a0b3e-113">Создает новый объект устройства, который можно использовать для создания других объектов DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="a0b3e-113">Creates a new device object that can be used to create other DirectComposition objects.</span></span><br/>                                                   |
| [<span data-ttu-id="a0b3e-114">**DCompositionCreateDevice2**</span><span class="sxs-lookup"><span data-stu-id="a0b3e-114">**DCompositionCreateDevice2**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice2)<br/>                   | <span data-ttu-id="a0b3e-115">Создает новый объект устройства, который можно использовать для создания других объектов DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="a0b3e-115">Creates a new device object that can be used to create other DirectComposition objects.</span></span><br/>                                                   |
| [<span data-ttu-id="a0b3e-116">**DCompositionCreateDevice3**</span><span class="sxs-lookup"><span data-stu-id="a0b3e-116">**DCompositionCreateDevice3**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositioncreatedevice3)<br/>                   | <span data-ttu-id="a0b3e-117">Создает новый объект устройства DirectComposition, который можно использовать для создания других объектов DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="a0b3e-117">Creates a new DirectComposition device object, which can be used to create other DirectComposition objects.</span></span><br/>                               |
| [<span data-ttu-id="a0b3e-118">**дкомпоситионкреатесурфацехандле**</span><span class="sxs-lookup"><span data-stu-id="a0b3e-118">**DCompositionCreateSurfaceHandle**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatesurfacehandle)<br/>       | <span data-ttu-id="a0b3e-119">Создает новый объект области композиции, который можно привязать к цепочке буфера обмена Microsoft DirectX или буферу обмена и связать с визуальным объектом.</span><span class="sxs-lookup"><span data-stu-id="a0b3e-119">Creates a new composition surface object that can be bound to a Microsoft DirectX swap chain or swap buffer and associated with a visual.</span></span><br/> |
| <span data-ttu-id="a0b3e-120">[**дкомпоситионжетфраместатистикс**](/previous-versions/windows/desktop/legacy/mt589902(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0b3e-120">[**DCompositionGetFrameStatistics**](/previous-versions/windows/desktop/legacy/mt589902(v=vs.85))</span></span><br/>         | <span data-ttu-id="a0b3e-121">Получает сведения о статистике композиции.</span><span class="sxs-lookup"><span data-stu-id="a0b3e-121">Retrieves composition statistics information.</span></span><br/>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="a0b3e-122">См. также</span><span class="sxs-lookup"><span data-stu-id="a0b3e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0b3e-123">Справочник по DirectComposition</span><span class="sxs-lookup"><span data-stu-id="a0b3e-123">DirectComposition Reference</span></span>](reference.md)
</dt> </dl>

 

