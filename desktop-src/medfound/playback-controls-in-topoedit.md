---
description: Элементы управления воспроизведением в Топоедит
ms.assetid: 36ebfa9e-7092-4a93-b633-8eefef8ac9e6
title: Элементы управления воспроизведением в Топоедит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174317fbf53dc6d2573414c60d5d4cde1a010f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555573"
---
# <a name="playback-controls-in-topoedit"></a><span data-ttu-id="64847-103">Элементы управления воспроизведением в Топоедит</span><span class="sxs-lookup"><span data-stu-id="64847-103">Playback Controls in TopoEdit</span></span>

<span data-ttu-id="64847-104">После разрешения топологии она помещается в очередь в сеансе мультимедиа для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="64847-104">After a topology is resolved, it is queued on the Media Session for playback.</span></span> <span data-ttu-id="64847-105">Топоедит предоставляет элемент управления транспортом для изменения состояния топологии в сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="64847-105">TopoEdit provides transport control for changing the state of topology on the Media Session.</span></span>

<span data-ttu-id="64847-106">В следующей таблице показана команда меню/панели инструментов и эквивалентный метод Media Foundation для каждой операции.</span><span class="sxs-lookup"><span data-stu-id="64847-106">The following table shows the menu/toolbar command and the equivalent Media Foundation method for each operation.</span></span>



| <span data-ttu-id="64847-107">Команда меню или панели инструментов</span><span class="sxs-lookup"><span data-stu-id="64847-107">Menu/Toolbar Command</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="64847-108">Метод Media Foundation</span><span class="sxs-lookup"><span data-stu-id="64847-108">Media Foundation Method</span></span>                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="64847-109">В меню **элементы управления** выберите команду **воспроизвести**. \[ Новая строка \] — или \[ Новая строка \] . Нажмите кнопку **Воспроизведение** на панели инструментов (как показано на следующем рисунке). \[ \] ![ снимок экрана новой строки кнопка воспроизведения](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)</span><span class="sxs-lookup"><span data-stu-id="64847-109">On the **Controls** menu, click **Play**.\[newline\] -or-\[newline\] click the **play** button on the toolbar (shown in the following image).\[newline\]![screen shot of the play button](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)</span></span>    | [<span data-ttu-id="64847-110">**Имфмедиасессион:: Start**</span><span class="sxs-lookup"><span data-stu-id="64847-110">**IMFMediaSession::Start**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) |
| <span data-ttu-id="64847-111">В меню **элементы управления** выберите команду **прерывать**. \[ Новая строка \] — или \[ Новая строка \] . Нажмите кнопку " **Закрыть** " на панели инструментов (как показано на следующем рисунке). \[ \] ![ снимок экрана новой строки кнопка "Закрыть"](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)</span><span class="sxs-lookup"><span data-stu-id="64847-111">On the **Controls** menu, click **Stop**.\[newline\] -or-\[newline\] click the **stop** button on the toolbar (shown in the following image).\[newline\]![screen shot of the stop button](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)</span></span>    | [<span data-ttu-id="64847-112">**Имфмедиасессион:: останавливаться**</span><span class="sxs-lookup"><span data-stu-id="64847-112">**IMFMediaSession::Stop**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)   |
| <span data-ttu-id="64847-113">В меню **элементы управления** выберите **приостановить**. \[ Новая строка \] или \[ Новая строка \] нажмите кнопку **приостановить** на панели инструментов (как показано на следующем рисунке). \[ \] ![ снимок экрана новой строки — кнопка приостановки](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg)</span><span class="sxs-lookup"><span data-stu-id="64847-113">On the **Controls** menu, click **Pause**.\[newline\] -or-\[newline\] click the **pause** button on the toolbar (shown in the following image).\[newline\]![screen shot of the pause button](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg)</span></span> | [<span data-ttu-id="64847-114">**Имфмедиасессион::P Аусе**</span><span class="sxs-lookup"><span data-stu-id="64847-114">**IMFMediaSession::Pause**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) |



 

<span data-ttu-id="64847-115">Сведения об управлении воспроизведением программным способом с помощью Media Foundation API см. [в разделе Управление состояниями представления](how-to-control-presentation-states.md).</span><span class="sxs-lookup"><span data-stu-id="64847-115">For information about controlling the playback programmatically by using Media Foundation APIs, see [How to Control Presentation States](how-to-control-presentation-states.md).</span></span>

## <a name="seeking"></a><span data-ttu-id="64847-116">Нужна</span><span class="sxs-lookup"><span data-stu-id="64847-116">Seeking</span></span>

<span data-ttu-id="64847-117">Если топология доступна для поиска, можно выполнить поиск с помощью панели поиска (как показано на рисунке ниже), чтобы указать место на временной шкале топологии для начала воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="64847-117">If the topology is seekable, you can seek by using the seek bar (shown in the following image) to specify a place in the topology's timeline to begin playback.</span></span>

![снимок экрана с панелью поиска](images/95a4e3ef-8489-4e26-9f02-436f81d8a96e.jpg)

> [!Note]  
> <span data-ttu-id="64847-119">Если источник мультимедиа доступен для поиска, команда «останавливает» также ищет топологию обратно в начало потока.</span><span class="sxs-lookup"><span data-stu-id="64847-119">If the media source is seekable, the Stop command also seeks the topology back to the start of the stream.</span></span>

 

## <a name="changing-the-playback-rate"></a><span data-ttu-id="64847-120">Изменение скорости воспроизведения</span><span class="sxs-lookup"><span data-stu-id="64847-120">Changing the Playback Rate</span></span>

<span data-ttu-id="64847-121">Если базовый источник носителя для топологии поддерживает несколько скоростей воспроизведения, можно использовать полосу скорости для изменения скорости воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="64847-121">If the underlying media source for the topology supports multiple playback rates, you can use the rate bar to change the playback rate.</span></span> <span data-ttu-id="64847-122">Чтобы быстро перемотать топологию в сеансе мультимедиа, увеличьте скорость, перетащив ползунок вправо, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="64847-122">To fast-forward a topology on the Media Session, increase the rate by dragging the slider to the right, as shown in the following image.</span></span>

![снимок экрана полосы скорости](images/6e094ecf-c87f-4f27-bca7-a53cc790f5c2.jpg)

> [!Note]  
> <span data-ttu-id="64847-124">В этой версии Топоедит поддерживает только положительные тарифы.</span><span class="sxs-lookup"><span data-stu-id="64847-124">In this version, TopoEdit only supports positive rates.</span></span> <span data-ttu-id="64847-125">Обратная воспроизведение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="64847-125">Reverse playback is not supported.</span></span>

 

<span data-ttu-id="64847-126">Дополнительные сведения об изменении частоты воспроизведения программным путем с помощью Media Foundation API см. в разделе [сведения об управлении скоростью](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="64847-126">For information about changing the playback rate programmatically by using Media Foundation APIs, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="64847-127">См. также</span><span class="sxs-lookup"><span data-stu-id="64847-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64847-128">Меню Топоедит</span><span class="sxs-lookup"><span data-stu-id="64847-128">TopoEdit Menus</span></span>](topoedit-menus.md)
</dt> <dt>

[<span data-ttu-id="64847-129">Панель инструментов Топоедит</span><span class="sxs-lookup"><span data-stu-id="64847-129">TopoEdit Toolbar</span></span>](topoedit-toolbar.md)
</dt> <dt>

[<span data-ttu-id="64847-130">топоедит</span><span class="sxs-lookup"><span data-stu-id="64847-130">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



