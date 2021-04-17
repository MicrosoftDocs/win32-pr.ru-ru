---
description: Объект Пенинпутпанел позволяет легко добавлять в приложения входные данные на месте.
ms.assetid: ad63302e-b386-4b32-95bf-be1129839c33
title: Класс Пенинпутпанел (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PenInputPanel
- PenInputPanel.IPenInputPanel
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 0564f758d47e516873b8df5020f3f03a5bcb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693725"
---
# <a name="peninputpanel-class"></a><span data-ttu-id="d4b6d-103">Класс Пенинпутпанел</span><span class="sxs-lookup"><span data-stu-id="d4b6d-103">PenInputPanel class</span></span>

<span data-ttu-id="d4b6d-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-104">\[Deprecated.</span></span> <span data-ttu-id="d4b6d-105">**Пенинпутпанел** был заменен [панелью ввода текста (TIP)](text-input-panel-reference.md).\]</span><span class="sxs-lookup"><span data-stu-id="d4b6d-105">**PenInputPanel** has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).\]</span></span>

<span data-ttu-id="d4b6d-106">Объект **пенинпутпанел** позволяет легко добавлять в приложения входные данные на месте.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-106">The **PenInputPanel** object enables you to easily add in-place pen input to your applications.</span></span>

<span data-ttu-id="d4b6d-107">Объект **пенинпутпанел** доступен в виде подключаемого объекта, который позволяет добавлять функциональность панели ввода Tablet PC в существующие элементы управления.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-107">The **PenInputPanel** object is available as an attachable object that allows you to add Tablet PC Input Panel functionality to existing controls.</span></span> <span data-ttu-id="d4b6d-108">Пользовательский интерфейс в основном определяется текущим языком ввода.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-108">The user interface is largely mandated by the current input language.</span></span> <span data-ttu-id="d4b6d-109">Можно выбрать метод ввода по умолчанию для объекта **пенинпутпанел** : рукописный ввод или клавиатура.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-109">You have the option of choosing the default input method for the **PenInputPanel** object, either handwriting or keyboard.</span></span> <span data-ttu-id="d4b6d-110">Конечный пользователь может переключаться между методами ввода с помощью кнопок пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-110">The end user can switch between input methods using buttons on the user interface.</span></span>

<span data-ttu-id="d4b6d-111">**Пенинпутпанел** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d4b6d-111">**PenInputPanel** has these types of members:</span></span>

-   [<span data-ttu-id="d4b6d-112">Перечисления</span><span class="sxs-lookup"><span data-stu-id="d4b6d-112">Enumerations</span></span>](#enumerations)
-   [<span data-ttu-id="d4b6d-113">События</span><span class="sxs-lookup"><span data-stu-id="d4b6d-113">Events</span></span>](#events)
-   [<span data-ttu-id="d4b6d-114">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="d4b6d-114">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="d4b6d-115">Методы</span><span class="sxs-lookup"><span data-stu-id="d4b6d-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="d4b6d-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="d4b6d-116">Properties</span></span>](#properties)

### <a name="enumerations"></a><span data-ttu-id="d4b6d-117">Перечисления</span><span class="sxs-lookup"><span data-stu-id="d4b6d-117">Enumerations</span></span>

<span data-ttu-id="d4b6d-118">Класс **пенинпутпанел** содержит эти перечисления.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-118">The **PenInputPanel** class has these enumerations.</span></span>



| <span data-ttu-id="d4b6d-119">Перечисление</span><span class="sxs-lookup"><span data-stu-id="d4b6d-119">Enumeration</span></span>                    | <span data-ttu-id="d4b6d-120">Описание</span><span class="sxs-lookup"><span data-stu-id="d4b6d-120">Description</span></span>                                                                               |
|:-------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4b6d-121">**панелтипе**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-121">**PanelType**</span></span>](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) | <span data-ttu-id="d4b6d-122">Определяет тип входных данных, доступных в объекте **пенинпутпанел** в данный момент.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-122">Defines the type of input currently available in the **PenInputPanel** object.</span></span><br/> |



 

### <a name="events"></a><span data-ttu-id="d4b6d-123">События</span><span class="sxs-lookup"><span data-stu-id="d4b6d-123">Events</span></span>

<span data-ttu-id="d4b6d-124">Класс **пенинпутпанел** содержит следующие события.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-124">The **PenInputPanel** class has these events.</span></span>



| <span data-ttu-id="d4b6d-125">Событие</span><span class="sxs-lookup"><span data-stu-id="d4b6d-125">Event</span></span>                                                  | <span data-ttu-id="d4b6d-126">Описание</span><span class="sxs-lookup"><span data-stu-id="d4b6d-126">Description</span></span>                                                                                                                             |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4b6d-127">**инпутфаилед**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-127">**InputFailed**</span></span>](peninputpanel-inputfailed.md)       | <span data-ttu-id="d4b6d-128">Происходит при изменении фокуса ввода до того, как объект **пенинпутпанел** смог вставить входные данные пользователя в присоединенный элемент управления.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-128">Occurs when input focus changes before the **PenInputPanel** object was able to insert user input into the attached control.</span></span><br/> |
| [<span data-ttu-id="d4b6d-129">**панелчанжед**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-129">**PanelChanged**</span></span>](peninputpanel-panelchanged.md)     | <span data-ttu-id="d4b6d-130">Происходит при изменении объекта **пенинпутпанел** между макетами.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-130">Occurs when the **PenInputPanel** object changes between layouts.</span></span><br/>                                                            |
| [<span data-ttu-id="d4b6d-131">**панелмовинг**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-131">**PanelMoving**</span></span>](peninputpanel-panelmoving.md)       | <span data-ttu-id="d4b6d-132">Происходит при перемещении объекта **пенинпутпанел** .</span><span class="sxs-lookup"><span data-stu-id="d4b6d-132">Occurs when the **PenInputPanel** object is moving.</span></span><br/>                                                                          |
| [<span data-ttu-id="d4b6d-133">**висиблечанжед**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-133">**VisibleChanged**</span></span>](peninputpanel-visiblechanged.md) | <span data-ttu-id="d4b6d-134">Происходит при отображении или скрытии объекта **пенинпутпанел** .</span><span class="sxs-lookup"><span data-stu-id="d4b6d-134">Occurs when the **PenInputPanel** object has shown or hidden itself.</span></span><br/>                                                         |



 

### <a name="interfaces"></a><span data-ttu-id="d4b6d-135">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="d4b6d-135">Interfaces</span></span>

<span data-ttu-id="d4b6d-136">Класс **пенинпутпанел** определяет эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-136">The **PenInputPanel** class defines these interfaces.</span></span>



| <span data-ttu-id="d4b6d-137">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="d4b6d-137">Interface</span></span>          | <span data-ttu-id="d4b6d-138">Описание</span><span class="sxs-lookup"><span data-stu-id="d4b6d-138">Description</span></span>                                                             |
|:-------------------|:------------------------------------------------------------------------|
| <span data-ttu-id="d4b6d-139">**ипенинпутпанел**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-139">**IPenInputPanel**</span></span> | <span data-ttu-id="d4b6d-140">Этот объект реализует COM-интерфейс **ипенинпутпанел** .</span><span class="sxs-lookup"><span data-stu-id="d4b6d-140">This object implements the **IPenInputPanel** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="d4b6d-141">Методы</span><span class="sxs-lookup"><span data-stu-id="d4b6d-141">Methods</span></span>

<span data-ttu-id="d4b6d-142">Класс **пенинпутпанел** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-142">The **PenInputPanel** class has these methods.</span></span>



| <span data-ttu-id="d4b6d-143">Метод</span><span class="sxs-lookup"><span data-stu-id="d4b6d-143">Method</span></span>                                                         | <span data-ttu-id="d4b6d-144">Описание</span><span class="sxs-lookup"><span data-stu-id="d4b6d-144">Description</span></span>                                                                                                                                                                                             |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4b6d-145">**коммитпендингинпут**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-145">**CommitPendingInput**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) | <span data-ttu-id="d4b6d-146">Отправляет собранные рукописные данные распознавателю и отправляет результаты распознавания.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-146">Sends collected ink to the recognizer and posts the recognition result.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="d4b6d-147">**енаблетсф**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-147">**EnableTsf**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-enabletsf)                   | <span data-ttu-id="d4b6d-148">При передаче значения **true** **пенинпутпанел** пытается отправить текст в присоединенный элемент управления через ПЛАТФОРМУ текстовых служб (TSF) и позволяет использовать пользовательский интерфейс исправления.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-148">When passed **TRUE**, the **PenInputPanel** attempts to send text to the attached control through the Text Services Framework (TSF) and enables the use of the correction user interface.</span></span><br/>    |
| [<span data-ttu-id="d4b6d-149">**MoveTo**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-149">**MoveTo**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)                         | <span data-ttu-id="d4b6d-150">Устанавливает расположение объекта **пенинпутпанел** на статическое расположение экрана.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-150">Sets the position of the **PenInputPanel** object to a static screen position.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="d4b6d-151">**Обновить**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-151">**Refresh**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)                       | <span data-ttu-id="d4b6d-152">Обновляет и восстанавливает свойства **пенинпутпанел** на основе параметров панели ввода Tablet PC, автоматически позиционирует панель ввода пера и устанавливает пользовательский интерфейс на панель по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-152">Updates and restores the **PenInputPanel** properties based on Tablet PC Input Panel settings, automatically positions the pen input panel and sets the user interface to the default panel.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d4b6d-153">Свойства</span><span class="sxs-lookup"><span data-stu-id="d4b6d-153">Properties</span></span>

<span data-ttu-id="d4b6d-154">Класс **пенинпутпанел** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-154">The **PenInputPanel** class has these properties.</span></span>



| <span data-ttu-id="d4b6d-155">Свойство</span><span class="sxs-lookup"><span data-stu-id="d4b6d-155">Property</span></span>                                                                  | <span data-ttu-id="d4b6d-156">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="d4b6d-156">Access type</span></span>           | <span data-ttu-id="d4b6d-157">Описание</span><span class="sxs-lookup"><span data-stu-id="d4b6d-157">Description</span></span>                                                                                                                                                                    |
|:--------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4b6d-158">**аттачедедитвиндов**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-158">**AttachedEditWindow**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow)<br/> | <span data-ttu-id="d4b6d-159">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d4b6d-159">Read/write</span></span><br/> | <span data-ttu-id="d4b6d-160">Возвращает или задает описатель окна элемента управления, к которому присоединен объект **пенинпутпанел** .</span><span class="sxs-lookup"><span data-stu-id="d4b6d-160">Gets or sets the window handle of the control that the **PenInputPanel** object is attached to.</span></span><br/>                                                                     |
| [<span data-ttu-id="d4b6d-161">**Автоотображение**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-161">**AutoShow**</span></span>](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)<br/>                     | <span data-ttu-id="d4b6d-162">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d4b6d-162">Read/write</span></span><br/> | <span data-ttu-id="d4b6d-163">Возвращает или задает логическое значение, указывающее, отображается ли объект **пенинпутпанел** , когда фокус установлен с помощью пера.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-163">Gets or sets a Boolean value that specifies whether the **PenInputPanel** object appears when focus is set using the pen.</span></span><br/>                                           |
| [<span data-ttu-id="d4b6d-164">**Момент**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-164">**Busy**</span></span>](/windows/desktop/api/Peninputpanel/nf-peninputpanel-ipeninputpanel-get_busy)<br/>                             | <span data-ttu-id="d4b6d-165">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4b6d-165">Read-only</span></span><br/>  | <span data-ttu-id="d4b6d-166">Возвращает логическое значение, указывающее, обрабатывает ли объект **пенинпутпанел** в данный момент рукописный ввод.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-166">Gets a Boolean value that specifies whether the **PenInputPanel** object is currently processing ink.</span></span><br/>                                                               |
| [<span data-ttu-id="d4b6d-167">**куррентпанел**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-167">**CurrentPanel**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel)<br/>             | <span data-ttu-id="d4b6d-168">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d4b6d-168">Read/write</span></span><br/> | <span data-ttu-id="d4b6d-169">Возвращает или задает тип панели, используемый в данный момент для ввода в объекте **пенинпутпанел** .</span><span class="sxs-lookup"><span data-stu-id="d4b6d-169">Gets or sets which panel type is currently being used for input within the **PenInputPanel** object.</span></span><br/>                                                                |
| [<span data-ttu-id="d4b6d-170">**дефаултпанел**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-170">**DefaultPanel**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel)<br/>             | <span data-ttu-id="d4b6d-171">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d4b6d-171">Read/write</span></span><br/> | <span data-ttu-id="d4b6d-172">Возвращает или задает тип панели, используемый по умолчанию для входных данных в объекте **пенинпутпанел** .</span><span class="sxs-lookup"><span data-stu-id="d4b6d-172">Gets or sets which panel type is the default panel type used for input within the **PenInputPanel** object.</span></span><br/>                                                         |
| [<span data-ttu-id="d4b6d-173">**фактоид**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-173">**Factoid**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)<br/>                       | <span data-ttu-id="d4b6d-174">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d4b6d-174">Read/write</span></span><br/> | <span data-ttu-id="d4b6d-175">Возвращает или задает строковое имя фактоид, используемое в распознавании.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-175">Gets or sets the string name of the factoid used in recognition.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="d4b6d-176">**Высота**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-176">**Height**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height)<br/>                         | <span data-ttu-id="d4b6d-177">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4b6d-177">Read-only</span></span><br/>  | <span data-ttu-id="d4b6d-178">Возвращает высоту объекта **пенинпутпанел** в клиентских координатах.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-178">Gets the height of the **PenInputPanel** object in client coordinates.</span></span><br/>                                                                                              |
| [<span data-ttu-id="d4b6d-179">**HorizontalOffset**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-179">**HorizontalOffset**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset)<br/>     | <span data-ttu-id="d4b6d-180">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d4b6d-180">Read/write</span></span><br/> | <span data-ttu-id="d4b6d-181">Возвращает или задает смещение между левым ребром объекта **пенинпутпанел** и левым ребром элемента управления, к которому он присоединен.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-181">Gets or sets the offset between the left edge of the **PenInputPanel** object and the left edge of the control to which it is attached.</span></span><br/>                             |
| [<span data-ttu-id="d4b6d-182">**Слева**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-182">**Left**</span></span>](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left)<br/>                             | <span data-ttu-id="d4b6d-183">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4b6d-183">Read-only</span></span><br/>  | <span data-ttu-id="d4b6d-184">Возвращает горизонтальную или вертикальную ось, положение левого края объекта **пенинпутпанел** в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-184">Gets the horizontal, or x-axis, location of the left edge of the **PenInputPanel** object, in screen coordinates.</span></span><br/>                                                   |
| [<span data-ttu-id="d4b6d-185">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-185">**Top**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top)<br/>                               | <span data-ttu-id="d4b6d-186">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4b6d-186">Read-only</span></span><br/>  | <span data-ttu-id="d4b6d-187">Получает вертикальную (или ось y) расположение верхнего края объекта **пенинпутпанел** в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-187">Gets the vertical, or y-axis, location of the top edge of the **PenInputPanel** object, in screen coordinates.</span></span><br/>                                                      |
| [<span data-ttu-id="d4b6d-188">**VerticalOffset**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-188">**VerticalOffset**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset)<br/>         | <span data-ttu-id="d4b6d-189">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d4b6d-189">Read/write</span></span><br/> | <span data-ttu-id="d4b6d-190">Возвращает или задает смещение между ближайшим горизонтальным ребром объекта **пенинпутпанел** и ближайшим горизонтальным ребром элемента управления, к которому он присоединен.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-190">Gets or sets the offset between the closest horizontal edge of the **PenInputPanel** object and the closest horizontal edge of the control to which it is attached.</span></span><br/> |
| [<span data-ttu-id="d4b6d-191">**Visible**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-191">**Visible**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_visible)<br/>                       | <span data-ttu-id="d4b6d-192">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d4b6d-192">Read/write</span></span><br/> | <span data-ttu-id="d4b6d-193">Возвращает или задает значение, указывающее, является ли объект **пенинпутпанел** видимым.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-193">Gets or sets a value that indicates whether the **PenInputPanel** object is visible.</span></span><br/>                                                                                |
| [<span data-ttu-id="d4b6d-194">**Ширина**</span><span class="sxs-lookup"><span data-stu-id="d4b6d-194">**Width**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width)<br/>                           | <span data-ttu-id="d4b6d-195">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4b6d-195">Read-only</span></span><br/>  | <span data-ttu-id="d4b6d-196">Возвращает ширину объекта **пенинпутпанел** в клиентских координатах.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-196">Gets the width of the **PenInputPanel** object in client coordinates.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="d4b6d-197">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4b6d-197">Remarks</span></span>

<span data-ttu-id="d4b6d-198">Для создания экземпляра этого объекта можно вызвать метод [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) в C++.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-198">This object can be instantiated by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4b6d-199">Требования</span><span class="sxs-lookup"><span data-stu-id="d4b6d-199">Requirements</span></span>



| <span data-ttu-id="d4b6d-200">Требование</span><span class="sxs-lookup"><span data-stu-id="d4b6d-200">Requirement</span></span> | <span data-ttu-id="d4b6d-201">Значение</span><span class="sxs-lookup"><span data-stu-id="d4b6d-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4b6d-202">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4b6d-202">Minimum supported client</span></span><br/> | <span data-ttu-id="d4b6d-203">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d4b6d-203">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d4b6d-204">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4b6d-204">Minimum supported server</span></span><br/> | <span data-ttu-id="d4b6d-205">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d4b6d-205">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d4b6d-206">Header</span><span class="sxs-lookup"><span data-stu-id="d4b6d-206">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4b6d-207"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d4b6d-207"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d4b6d-208">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d4b6d-208">Library</span></span><br/>                  | <dl> <span data-ttu-id="d4b6d-209"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4b6d-209"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d4b6d-210">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4b6d-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4b6d-211">Программирование панели ввода с помощью класса Пенинпутпанел</span><span class="sxs-lookup"><span data-stu-id="d4b6d-211">Programming the Input Panel Using the PenInputPanel Class</span></span>](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
