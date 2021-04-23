---
description: Если этот бит задан, диалоговое окно является диалоговым окном ошибки.
ms.assetid: a8a95f6a-6465-433b-98a4-95281cddedd3
title: Бит стиля диалогового окна ошибки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ff3e4868cf1941f80be4f7b2d70068ec949a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650596"
---
# <a name="error-dialog-style-bit"></a><span data-ttu-id="c26d7-103">Бит стиля диалогового окна ошибки</span><span class="sxs-lookup"><span data-stu-id="c26d7-103">Error Dialog Style Bit</span></span>

<span data-ttu-id="c26d7-104">Если этот бит задан, диалоговое окно является диалоговым окном ошибки.</span><span class="sxs-lookup"><span data-stu-id="c26d7-104">If this bit is set, the dialog box is an error dialog.</span></span>

<span data-ttu-id="c26d7-105">В этом стиле может быть несколько диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="c26d7-105">There can be more than one dialog with this style.</span></span> <span data-ttu-id="c26d7-106">Свойство **еррордиалог** определяет, какое диалоговое окно используется в качестве диалогового окна сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c26d7-106">The **ErrorDialog** property determines which dialog is used as an error dialog.</span></span> <span data-ttu-id="c26d7-107">Выбранное диалоговое окно может быть только одним из тех, для которых задан этот бит стиля.</span><span class="sxs-lookup"><span data-stu-id="c26d7-107">The selected dialog can be only one of those that have this style bit set.</span></span> <span data-ttu-id="c26d7-108">В диалоговом окне ошибки должен быть статический текстовый элемент управления с именем ErrorText.</span><span class="sxs-lookup"><span data-stu-id="c26d7-108">The error dialog must have a static text control named ErrorText.</span></span> <span data-ttu-id="c26d7-109">Этот элемент управления получает текст сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c26d7-109">This control receives the text of the error message.</span></span> <span data-ttu-id="c26d7-110">В диалоговом окне также должны быть семь кнопок push-уведомлений, соответствующих возможным возвращаемым значениям.</span><span class="sxs-lookup"><span data-stu-id="c26d7-110">The dialog should also have the seven push buttons corresponding to the possible return values.</span></span> <span data-ttu-id="c26d7-111">Сообщение об ошибке определяет, какие из этих кнопок отображаются на самом деле.</span><span class="sxs-lookup"><span data-stu-id="c26d7-111">The error message determines which of these buttons are actually displayed.</span></span> <span data-ttu-id="c26d7-112">Отображаемые кнопки переупорядочиваются, чтобы равномерно распределять их по диалоговому окну.</span><span class="sxs-lookup"><span data-stu-id="c26d7-112">The displayed buttons are rearranged so they are evenly distributed on the dialog.</span></span> <span data-ttu-id="c26d7-113">Это изменение расстановки изменяет координату X кнопок, но не другие три координаты.</span><span class="sxs-lookup"><span data-stu-id="c26d7-113">This rearrangement changes the X coordinate of the buttons, but not the other three coordinates.</span></span> <span data-ttu-id="c26d7-114">Поэтому рекомендуется, чтобы никакие другие элементы управления не были созданы в той же горизонтальной области диалогового окна, что и кнопки.</span><span class="sxs-lookup"><span data-stu-id="c26d7-114">Therefore it is advisable that no other control should be authored in the same horizontal region of the dialog as the buttons.</span></span> <span data-ttu-id="c26d7-115">Если в сообщении об ошибке не указано ни одной кнопки, отображается кнопка **ОК** .</span><span class="sxs-lookup"><span data-stu-id="c26d7-115">If the error message specifies no button, the **OK** button is displayed.</span></span> <span data-ttu-id="c26d7-116">Кнопка **по умолчанию** первый активный элемент управления и кнопка **Отмена** значения игнорируются в диалоговом окне ошибки.</span><span class="sxs-lookup"><span data-stu-id="c26d7-116">The **Default** button, First active control and **Cancel** button values are ignored for an error dialog.</span></span> <span data-ttu-id="c26d7-117">Кнопка **по умолчанию** , определенная в сообщении об ошибке, будет назначена всем трем значениям.</span><span class="sxs-lookup"><span data-stu-id="c26d7-117">The **Default** button defined in the error message will be assigned to all three values.</span></span> <span data-ttu-id="c26d7-118">Результат отправки этих кнопок должен быть определен в [таблице таблице ControlEvent событие](controlevent-table.md) , как и для всех остальных кнопок.</span><span class="sxs-lookup"><span data-stu-id="c26d7-118">The effect of pushing these buttons have to be defined in the [ControlEvent table](controlevent-table.md) just like for all other buttons.</span></span> <span data-ttu-id="c26d7-119">Заголовок диалогового окна создается таким же образом, как и другие диалоговые окна.</span><span class="sxs-lookup"><span data-stu-id="c26d7-119">The title of the dialog is authored in a way similar to other dialogs.</span></span> <span data-ttu-id="c26d7-120">Оно может быть перезаписано сообщением об ошибке, если оно указывает текст заголовка после списка кнопок.</span><span class="sxs-lookup"><span data-stu-id="c26d7-120">It can get overwritten by the error message if it specifies a header text after the button list.</span></span>

## <a name="value"></a><span data-ttu-id="c26d7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c26d7-121">Value</span></span>



| <span data-ttu-id="c26d7-122">Decimal</span><span class="sxs-lookup"><span data-stu-id="c26d7-122">Decimal</span></span> | <span data-ttu-id="c26d7-123">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="c26d7-123">Hexadecimal</span></span> | <span data-ttu-id="c26d7-124">Константа</span><span class="sxs-lookup"><span data-stu-id="c26d7-124">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="c26d7-125">65536</span><span class="sxs-lookup"><span data-stu-id="c26d7-125">65536</span></span>   | <span data-ttu-id="c26d7-126">0x00010000</span><span class="sxs-lookup"><span data-stu-id="c26d7-126">0x00010000</span></span>  | <span data-ttu-id="c26d7-127">**мсидбдиалогаттрибутесеррор**</span><span class="sxs-lookup"><span data-stu-id="c26d7-127">**msidbDialogAttributesError**</span></span> |



 

 

 



