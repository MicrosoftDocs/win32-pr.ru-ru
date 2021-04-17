---
description: ICE44 проверяет, что Невдиалог, Спавндиалог и Спавнваитдиалог Контролевентс ссылаются на допустимые диалоговые окна в таблице диалоговых окон.
ms.assetid: 401bae25-a361-45f6-af3f-0f31be463c84
title: ICE44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16354ac435979d830ff14c33a846e97757b64962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663658"
---
# <a name="ice44"></a><span data-ttu-id="c2af1-103">ICE44</span><span class="sxs-lookup"><span data-stu-id="c2af1-103">ICE44</span></span>

<span data-ttu-id="c2af1-104">ICE44 проверяет, что [невдиалог](newdialog-controlevent.md), [спавндиалог](spawndialog-controlevent.md)и [спавнваитдиалог](spawnwaitdialog-controlevent.md) контролевентс ссылаются на допустимые диалоговые окна в [таблице диалоговых](dialog-table.md)окон.</span><span class="sxs-lookup"><span data-stu-id="c2af1-104">ICE44 validates that the [NewDialog](newdialog-controlevent.md), [SpawnDialog](spawndialog-controlevent.md), and [SpawnWaitDialog](spawnwaitdialog-controlevent.md) ControlEvents reference valid dialog boxes in the [Dialog table](dialog-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="c2af1-105">Результат</span><span class="sxs-lookup"><span data-stu-id="c2af1-105">Result</span></span>

<span data-ttu-id="c2af1-106">ICE44 отправляет сообщение об ошибке, если имеется событие элемента управления диалогового окна, которое не ссылается на диалоговое окно, указанное в таблице диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="c2af1-106">ICE44 posts an error message if there is a dialog control event that does not reference a dialog box listed in the Dialog table.</span></span>

## <a name="example"></a><span data-ttu-id="c2af1-107">Пример</span><span class="sxs-lookup"><span data-stu-id="c2af1-107">Example</span></span>

<span data-ttu-id="c2af1-108">ICE44 сообщит о следующих ошибках в приведенном примере.</span><span class="sxs-lookup"><span data-stu-id="c2af1-108">ICE44 would report the following errors for the example shown.</span></span>



| <span data-ttu-id="c2af1-109">ICE44, ошибка</span><span class="sxs-lookup"><span data-stu-id="c2af1-109">ICE44 error</span></span>                                                                                                                               | <span data-ttu-id="c2af1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c2af1-110">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2af1-111">Событие элемента управления для элемента управления "Dialog1". Control1 имеет тип Спавндиалог, но его аргумент Dialog2 не является допустимой записью в диалоговой таблице.</span><span class="sxs-lookup"><span data-stu-id="c2af1-111">Control Event for Control 'Dialog1'.'Control1' is of type SpawnDialog, but its argument Dialog2 is not a valid entry in the Dialog Table.</span></span> | <span data-ttu-id="c2af1-112">Существуют действия Спавндиалог, Спавнваитдиалог или Невдиалог с аргументом, который не ссылается на диалоговое окно в таблице диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="c2af1-112">There is a SpawnDialog, SpawnWaitDialog, or NewDialog actions that has an argument that does not refer to a dialog box in the Dialog table.</span></span> <span data-ttu-id="c2af1-113">Чтобы устранить эту ошибку, добавьте аргумент, который является ключом в таблице диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="c2af1-113">To fix this error, add an argument that is a key in the Dialog Table.</span></span><br/> |



 

<span data-ttu-id="c2af1-114">[Таблица диалоговых окон](dialog-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="c2af1-114">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="c2af1-115">Диалог</span><span class="sxs-lookup"><span data-stu-id="c2af1-115">Dialog</span></span>  | <span data-ttu-id="c2af1-116">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c2af1-116">Title</span></span> |
|---------|-------|
| <span data-ttu-id="c2af1-117">Dialog1</span><span class="sxs-lookup"><span data-stu-id="c2af1-117">Dialog1</span></span> |       |



 

<span data-ttu-id="c2af1-118">[Таблица таблице ControlEvent событие](controlevent-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="c2af1-118">[ControlEvent Table](controlevent-table.md) (partial)</span></span>



| <span data-ttu-id="c2af1-119">Диалог\_</span><span class="sxs-lookup"><span data-stu-id="c2af1-119">Dialog\_</span></span> | <span data-ttu-id="c2af1-120">элементом управления\_</span><span class="sxs-lookup"><span data-stu-id="c2af1-120">Control\_</span></span> | <span data-ttu-id="c2af1-121">Тип</span><span class="sxs-lookup"><span data-stu-id="c2af1-121">Type</span></span>        | <span data-ttu-id="c2af1-122">Аргумент</span><span class="sxs-lookup"><span data-stu-id="c2af1-122">Argument</span></span> |
|----------|-----------|-------------|----------|
| <span data-ttu-id="c2af1-123">Dialog1</span><span class="sxs-lookup"><span data-stu-id="c2af1-123">Dialog1</span></span>  | <span data-ttu-id="c2af1-124">Control1</span><span class="sxs-lookup"><span data-stu-id="c2af1-124">Control1</span></span>  | <span data-ttu-id="c2af1-125">спавндиалог</span><span class="sxs-lookup"><span data-stu-id="c2af1-125">SpawnDialog</span></span> | <span data-ttu-id="c2af1-126">Dialog2</span><span class="sxs-lookup"><span data-stu-id="c2af1-126">Dialog2</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="c2af1-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c2af1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2af1-128">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="c2af1-128">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




