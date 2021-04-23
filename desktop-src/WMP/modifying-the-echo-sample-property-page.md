---
title: Изменение страницы свойств «пример эха»
description: Изменение страницы свойств «пример эха»
ms.assetid: a7ebf7d7-1f70-421f-862f-bc60655bb242
keywords:
- Подключаемые модули проигрывателя Windows Media, примеры страниц свойств Echo
- страницы свойств "подключаемые модули", "Эхо-примеры"
- подключаемые модули обработки цифровых сигналов, примеры страниц свойств
- Подключаемые модули DSP, примеры страниц свойств
- Пример подключаемого модуля "Echo DSP", страницы свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f16c623f833d8d9c107c00e96fed92bab28e8b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410826"
---
# <a name="modifying-the-echo-sample-property-page"></a><span data-ttu-id="786d6-108">Изменение страницы свойств «пример эха»</span><span class="sxs-lookup"><span data-stu-id="786d6-108">Modifying the Echo Sample Property Page</span></span>

<span data-ttu-id="786d6-109">Реализация страницы свойств по умолчанию, предоставляемая в примере подключаемого модуля поставщика DSP для проигрывателя Windows Media, содержит один элемент управления "поле ввода", который получает коэффициент масштабирования от пользователя.</span><span class="sxs-lookup"><span data-stu-id="786d6-109">The default property page implementation provided by the Windows Media Player Plug-in Wizard DSP plug-in sample contains a single edit box control that receives the scale factor from the user.</span></span> <span data-ttu-id="786d6-110">Необходимо изменить страницу свойств для получения двух значений свойств, используемых образцом Echo.</span><span class="sxs-lookup"><span data-stu-id="786d6-110">You need to modify the property page to receive the two property values used by the Echo sample.</span></span>

<span data-ttu-id="786d6-111">Общие сведения о страницах свойств подключаемого модуля DSP см. [в разделе Реализация подключаемого модуля DSP для аудио](implementing-an-audio-dsp-plug-in.md).</span><span class="sxs-lookup"><span data-stu-id="786d6-111">For an overview of DSP plug-in property pages, see [Implementing an Audio DSP Plug-in](implementing-an-audio-dsp-plug-in.md).</span></span>

<span data-ttu-id="786d6-112">В следующих разделах приводится пошаговое руководство по изменению страницы свойств Sample.</span><span class="sxs-lookup"><span data-stu-id="786d6-112">The following sections step you through the process of modifying the sample property page:</span></span>

-   [<span data-ttu-id="786d6-113">Изменение ресурса диалогового окна Echo</span><span class="sxs-lookup"><span data-stu-id="786d6-113">Modifying the Echo Dialog Resource</span></span>](modifying-the-echo-dialog-resource.md)
-   [<span data-ttu-id="786d6-114">Добавление и изменение событий</span><span class="sxs-lookup"><span data-stu-id="786d6-114">Adding and Modifying the Events</span></span>](adding-and-modifying-the-events.md)
-   [<span data-ttu-id="786d6-115">Как образец Echo сохраняет данные</span><span class="sxs-lookup"><span data-stu-id="786d6-115">How the Echo Sample Persists Data</span></span>](how-the-echo-sample-persists-data.md)
-   [<span data-ttu-id="786d6-116">Реализация Цечопроппаже:: Онинитдиалог</span><span class="sxs-lookup"><span data-stu-id="786d6-116">Implementing CEchoPropPage::OnInitDialog</span></span>](implementing-cechoproppage--oninitdialog.md)
-   [<span data-ttu-id="786d6-117">Реализация Цечопроппаже:: Apply</span><span class="sxs-lookup"><span data-stu-id="786d6-117">Implementing CEchoPropPage::Apply</span></span>](implementing-cechoproppage--apply.md)
-   [<span data-ttu-id="786d6-118">Реализация Цечо:: Финалконструкт</span><span class="sxs-lookup"><span data-stu-id="786d6-118">Implementing CEcho::FinalConstruct</span></span>](implementing-cecho--finalconstruct.md)

## <a name="related-topics"></a><span data-ttu-id="786d6-119">См. также</span><span class="sxs-lookup"><span data-stu-id="786d6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="786d6-120">**Пример эха**</span><span class="sxs-lookup"><span data-stu-id="786d6-120">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




