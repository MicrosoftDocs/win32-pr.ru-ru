---
description: Диалоговое окно ошибки представляет собой модальное диалоговое окно, в котором отображается сообщение об ошибке. В каждой установке может существовать более одного диалогового окна ошибки.
ms.assetid: 11d4fe8b-ec5f-4576-95e5-c86344f0195c
title: Диалоговое окно ошибки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a153f5e6ee38235f830937d794a9ca9b81314583
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543026"
---
# <a name="error-dialog"></a><span data-ttu-id="0e35e-104">Диалоговое окно ошибки</span><span class="sxs-lookup"><span data-stu-id="0e35e-104">Error Dialog</span></span>

<span data-ttu-id="0e35e-105">Диалоговое окно ошибки представляет собой модальное диалоговое окно, в котором отображается сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0e35e-105">An Error dialog box is a modal dialog box box that displays an error message.</span></span> <span data-ttu-id="0e35e-106">В каждой установке может существовать более одного диалогового окна ошибки.</span><span class="sxs-lookup"><span data-stu-id="0e35e-106">More than one Error dialog box can exist in each installation.</span></span>

<span data-ttu-id="0e35e-107">Необходимо задать свойство Еррордиалог, которое указывает, какое диалоговое окно следует использовать.</span><span class="sxs-lookup"><span data-stu-id="0e35e-107">An ErrorDialog property needs to be set that specifies which dialog box is to be used.</span></span> <span data-ttu-id="0e35e-108">Если это свойство не задано или не указывает на допустимое диалоговое окно ошибки, то сообщения об ошибках отображаться не будут.</span><span class="sxs-lookup"><span data-stu-id="0e35e-108">If this property is not set or does not point to a valid Error dialog box, then the error messages will not be displayed.</span></span> <span data-ttu-id="0e35e-109">В этом случае ошибка заносится в журнал только с предупреждением об отсутствующем диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="0e35e-109">In this case, the error is only logged with a warning about the missing dialog box.</span></span>

<span data-ttu-id="0e35e-110">В диалоговом окне ошибки должен быть установлен [бит стиля диалогового окна](error-dialog-style-bit.md) ошибки.</span><span class="sxs-lookup"><span data-stu-id="0e35e-110">An Error dialog box must have the [Error Dialog style bit](error-dialog-style-bit.md) set.</span></span> <span data-ttu-id="0e35e-111">Диалоговое окно должно содержать [элемент управления "текст](text-control.md) " с именем ErrorText.</span><span class="sxs-lookup"><span data-stu-id="0e35e-111">The dialog box must have a [Text control](text-control.md) named ErrorText.</span></span> <span data-ttu-id="0e35e-112">Запись для диалогового окна ошибки в [таблице диалоговых окон](dialog-table.md) должна содержать элемент управления ErrorText, введенный в \_ первое поле элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0e35e-112">The record for the Error dialog box in the [Dialog table](dialog-table.md) must have the ErrorText control entered into the Control\_First field.</span></span>

<span data-ttu-id="0e35e-113">Диалоговое окно должно содержать семь [кнопок](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="0e35e-113">The dialog box must contain seven [PushButtons](pushbutton-control.md).</span></span> <span data-ttu-id="0e35e-114">Все эти кнопки указывают таблице ControlEvent событие [EndDialog](enddialog-controlevent.md) в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="0e35e-114">All of these buttons specify the [EndDialog](enddialog-controlevent.md) ControlEvent in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="0e35e-115">Каждая кнопка задает один из следующих атрибутов: **еррораборт**, **еррорканцел**, **ерроригноре**, **еррорно**, **ерророк**, **еррорретри**, **еррорес**.</span><span class="sxs-lookup"><span data-stu-id="0e35e-115">Each button specifies one of the following attributes: **ErrorAbort**, **ErrorCancel**, **ErrorIgnore**, **ErrorNo**, **ErrorOk**, **ErrorRetry**, **ErrorYes**.</span></span>

> [!Note]  
> <span data-ttu-id="0e35e-116">Фокус этих элементов управления не должен быть связан с использованием элемента управления \_ следующий столбец в [таблице управления](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="0e35e-116">The focus of these controls should not be linked through the use of the Control\_Next column in the [Control table](control-table.md).</span></span>

 

<span data-ttu-id="0e35e-117">Эти кнопки должны размещаться примерно в том же положении в диалоговом окне, поскольку при их создании создается только подмножество этих семи кнопок в зависимости от сообщения.</span><span class="sxs-lookup"><span data-stu-id="0e35e-117">These buttons should be placed in approximately the same position in the dialog box because when it is created, only a subset of these seven buttons is created, depending on the message.</span></span> <span data-ttu-id="0e35e-118">Координата X кнопок изменяется таким образом, чтобы отображаемые кнопки были пробелом.</span><span class="sxs-lookup"><span data-stu-id="0e35e-118">The X coordinate of the buttons is modified so the buttons that are displayed are evenly spaced.</span></span> <span data-ttu-id="0e35e-119">Координаты Y, высота и ширина кнопок не меняются.</span><span class="sxs-lookup"><span data-stu-id="0e35e-119">The Y coordinate, height, and width of the buttons are unchanged.</span></span> <span data-ttu-id="0e35e-120">Так как кнопки располагаются горизонтально, другие элементы управления не могут быть помещены в одну и ту же горизонтальную область диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0e35e-120">Because the buttons are arranged horizontally, no other control can be placed in the same horizontal region of the dialog box.</span></span>

<span data-ttu-id="0e35e-121">В диалоговом окне ошибки поля элементов управления \_ по умолчанию и отмены элемента управления \_ в [таблице](dialog-table.md) не учитываются.</span><span class="sxs-lookup"><span data-stu-id="0e35e-121">For an Error dialog box, the Control\_Default and Control\_Cancel fields in the [Dialog table](dialog-table.md) are ignored.</span></span> <span data-ttu-id="0e35e-122">В \_ первом поле элемента управления для диалогового окна ошибки должен быть указан элемент управления ErrorText.</span><span class="sxs-lookup"><span data-stu-id="0e35e-122">The Control\_First field for an Error dialog box must specify the ErrorText control.</span></span>

<span data-ttu-id="0e35e-123">Если в этом диалоговом окне включен [элемент управления значком](icon-control.md) с именем еррорикон, отображаются следующие стандартные значки Windows:</span><span class="sxs-lookup"><span data-stu-id="0e35e-123">If an [Icon control](icon-control.md) named ErrorIcon is included on this dialog, the following standard Windows icons are displayed:</span></span>

-   <span data-ttu-id="0e35e-124">Иди \_ Ошибка в ответ на сообщения имтфаталексит.</span><span class="sxs-lookup"><span data-stu-id="0e35e-124">IDI\_ERROR in response to imtFatalExit messages.</span></span>
-   <span data-ttu-id="0e35e-125">Иди \_ предупреждение в ответ на сообщения имтеррор и имтварнинг.</span><span class="sxs-lookup"><span data-stu-id="0e35e-125">IDI\_WARNING in response to imtError and imtWarning messages.</span></span>
-   <span data-ttu-id="0e35e-126">Иди \_ сведения в ответ на сообщения имтаутофдискспаце.</span><span class="sxs-lookup"><span data-stu-id="0e35e-126">IDI\_INFORMATION in response to imtOutOfDiskSpace messages.</span></span>

<span data-ttu-id="0e35e-127">Элемент управления Еррорикон должен быть создан с помощью [атрибута элемента управления FixedSize](fixedsize-control-attribute.md) , чтобы избежать неправильного изменения размеров стандартных значков Windows.</span><span class="sxs-lookup"><span data-stu-id="0e35e-127">The ErrorIcon control should be created with the [FixedSize control attribute](fixedsize-control-attribute.md) set to avoid improper sizing of the standard Windows icons.</span></span>

 

 



