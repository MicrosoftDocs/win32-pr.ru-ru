---
title: Интерфейс Исофткбд (Софткбдк. h)
description: Интерфейс Исофткбд используется приложениями и текстовыми службами для реализации экранной клавиатуры.
ms.assetid: 804634bd-646e-459f-9fbb-cd6929b11fab
keywords:
- Платформа текстовых служб интерфейса Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, описание
topic_type:
- apiref
api_name:
- ISoftKbd
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e046964616fc564aa2e0c3d0098ee2186cdaf8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681755"
---
# <a name="isoftkbd-interface"></a><span data-ttu-id="a0fd4-105">Интерфейс Исофткбд</span><span class="sxs-lookup"><span data-stu-id="a0fd4-105">ISoftKbd interface</span></span>

<span data-ttu-id="a0fd4-106">Интерфейс **исофткбд** используется приложениями и текстовыми службами для реализации экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-106">The **ISoftKbd** interface is used by applications and text services to implement a soft keyboard.</span></span>

## <a name="members"></a><span data-ttu-id="a0fd4-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="a0fd4-107">Members</span></span>

<span data-ttu-id="a0fd4-108">Интерфейс **исофткбд** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a0fd4-108">The **ISoftKbd** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a0fd4-109">**Исофткбд** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a0fd4-109">**ISoftKbd** also has these types of members:</span></span>

-   [<span data-ttu-id="a0fd4-110">Методы</span><span class="sxs-lookup"><span data-stu-id="a0fd4-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a0fd4-111">Методы</span><span class="sxs-lookup"><span data-stu-id="a0fd4-111">Methods</span></span>

<span data-ttu-id="a0fd4-112">Интерфейс **исофткбд** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-112">The **ISoftKbd** interface has these methods.</span></span>



| <span data-ttu-id="a0fd4-113">Метод</span><span class="sxs-lookup"><span data-stu-id="a0fd4-113">Method</span></span>                                                                                        | <span data-ttu-id="a0fd4-114">Описание</span><span class="sxs-lookup"><span data-stu-id="a0fd4-114">Description</span></span>                                                                                                   |
|:----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0fd4-115">**адвисесофткэйбоардевентсинк**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-115">**AdviseSoftKeyboardEventSink**</span></span>](isoftkbd-advisesoftkeyboardeventsink.md)                   | <span data-ttu-id="a0fd4-116">Устанавливает приемник событий программируемой клавиатуры для работы с Онкэйселектион уведомлениями с помощью экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-116">Installs a soft keyboard event sink to handle OnKeySelection notifications from the soft keyboard.</span></span><br/> |
| [<span data-ttu-id="a0fd4-117">**креатесофткэйбоардлайаутфромресаурце**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-117">**CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md) | <span data-ttu-id="a0fd4-118">Создает раскладку экранной клавиатуры из указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-118">Creates a soft keyboard layout from the specified resource.</span></span><br/>                                        |
| [<span data-ttu-id="a0fd4-119">**креатесофткэйбоардлайаутфромксмлфиле**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-119">**CreateSoftKeyboardLayoutFromXMLFile**</span></span>](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)   | <span data-ttu-id="a0fd4-120">Создает раскладку экранной клавиатуры из указанного XML-файла.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-120">Creates a soft keyboard layout from the specified XML file.</span></span><br/>                                        |
| [<span data-ttu-id="a0fd4-121">**креатесофткэйбоардвиндов**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-121">**CreateSoftKeyboardWindow**</span></span>](isoftkbd-createsoftkeyboardwindow.md)                         | <span data-ttu-id="a0fd4-122">Создает окно с экранной клавиатурой.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-122">Creates a soft keyboard window.</span></span><br/>                                                                    |
| [<span data-ttu-id="a0fd4-123">**дестройсофткэйбоардвиндов**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-123">**DestroySoftKeyboardWindow**</span></span>](isoftkbd-destroysoftkeyboardwindow.md)                       | <span data-ttu-id="a0fd4-124">Уничтожает окно с экранной клавиатурой.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-124">Destroys a soft keyboard window.</span></span><br/>                                                                   |
| [<span data-ttu-id="a0fd4-125">**енумсофткэйбоард**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-125">**EnumSoftKeyboard**</span></span>](isoftkbd-enumsoftkeyboard.md)                                         | <span data-ttu-id="a0fd4-126">Перечисляет возможные мягкие клавиатуры, поддерживающие указанный язык.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-126">Enumerates the possible soft keyboards that support the specified language.</span></span><br/>                        |
| [<span data-ttu-id="a0fd4-127">**жетсофткэйбоардколорс**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-127">**GetSoftKeyboardColors**</span></span>](isoftkbd-getsoftkeyboardcolors.md)                               | <span data-ttu-id="a0fd4-128">Получает цвет экранной клавиатуры, соответствующий заданному типу цвета.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-128">Retrieves the soft keyboard color corresponding to the supplied color type.</span></span><br/>                        |
| [<span data-ttu-id="a0fd4-129">**жетсофткэйбоардпоссизе**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-129">**GetSoftKeyboardPosSize**</span></span>](isoftkbd-getsoftkeyboardpossize.md)                             | <span data-ttu-id="a0fd4-130">Извлекает начальную точку и размер экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-130">Retrieves the starting position and size of a soft keyboard.</span></span><br/>                                       |
| [<span data-ttu-id="a0fd4-131">**жетсофткэйбоардтекстфонт**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-131">**GetSoftKeyboardTextFont**</span></span>](isoftkbd-getsoftkeyboardtextfont.md)                           | <span data-ttu-id="a0fd4-132">Извлекает шрифт текста, используемый мягкой клавиатурой.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-132">Retrieves the text font used by a soft keyboard.</span></span><br/>                                                   |
| [<span data-ttu-id="a0fd4-133">**жетсофткэйбоардтипемоде**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-133">**GetSoftKeyboardTypeMode**</span></span>](isoftkbd-getsoftkeyboardtypemode.md)                           | <span data-ttu-id="a0fd4-134">Получает режим типа для экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-134">Retrieves the type mode for a soft keyboard.</span></span><br/>                                                       |
| [<span data-ttu-id="a0fd4-135">**Инициализация**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-135">**Initialize**</span></span>](isoftkbd-initialize.md)                                                     | <span data-ttu-id="a0fd4-136">Инициализирует все необходимые поля для мягкой клавиатуры и создает стандартные раскладки клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-136">Initializes all necessary fields for a soft keyboard and generates standard soft keyboard layouts.</span></span><br/> |
| [<span data-ttu-id="a0fd4-137">**селектсофткэйбоард**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-137">**SelectSoftKeyboard**</span></span>](isoftkbd-selectsoftkeyboard.md)                                     | <span data-ttu-id="a0fd4-138">Выбирает указанную мягкую клавиатуру.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-138">Selects the specified soft keyboard.</span></span><br/>                                                               |
| [<span data-ttu-id="a0fd4-139">**сеткэйбоардлабелтекст**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-139">**SetKeyboardLabelText**</span></span>](isoftkbd-setkeyboardlabeltext.md)                                 | <span data-ttu-id="a0fd4-140">Задает текст метки для экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-140">Sets the label text from the layout for a soft keyboard.</span></span><br/>                                           |
| [<span data-ttu-id="a0fd4-141">**сеткэйбоардлабелтексткомбинатион**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-141">**SetKeyboardLabelTextCombination**</span></span>](isoftkbd-setkeyboardlabeltextcombination.md)           | <span data-ttu-id="a0fd4-142">Задает сочетание метки и текста, используемого для описания экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-142">Sets a combination of label and text used to describe a soft keyboard.</span></span><br/>                             |
| [<span data-ttu-id="a0fd4-143">**сетсофткэйбоардколорс**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-143">**SetSoftKeyboardColors**</span></span>](isoftkbd-setsoftkeyboardcolors.md)                               | <span data-ttu-id="a0fd4-144">Задает цвет экранной клавиатуры, соответствующий заданному типу цвета.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-144">Sets the soft keyboard color corresponding to the supplied color type.</span></span><br/>                             |
| [<span data-ttu-id="a0fd4-145">**сетсофткэйбоардпоссизе**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-145">**SetSoftKeyboardPosSize**</span></span>](isoftkbd-setsoftkeyboardpossize.md)                             | <span data-ttu-id="a0fd4-146">Задает начальное расположение и размер экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-146">Sets the starting position and size of a soft keyboard.</span></span><br/>                                            |
| [<span data-ttu-id="a0fd4-147">**сетсофткэйбоардтекстфонт**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-147">**SetSoftKeyboardTextFont**</span></span>](isoftkbd-setsoftkeyboardtextfont.md)                           | <span data-ttu-id="a0fd4-148">Задает шрифт текста, используемый мягкой клавиатурой.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-148">Sets the text font used by a soft keyboard.</span></span><br/>                                                        |
| [<span data-ttu-id="a0fd4-149">**сетсофткэйбоардтипемоде**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-149">**SetSoftKeyboardTypeMode**</span></span>](isoftkbd-setsoftkeyboardtypemode.md)                           | <span data-ttu-id="a0fd4-150">Задает режим типа для экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-150">Sets the type mode for a soft keyboard.</span></span><br/>                                                            |
| [<span data-ttu-id="a0fd4-151">**шовкэйсфоркэйсканмоде**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-151">**ShowKeysForKeyScanMode**</span></span>](isoftkbd-showkeysforkeyscanmode.md)                             | <span data-ttu-id="a0fd4-152">Отображает ключи, используемые для режима сканирования ключа для экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-152">Displays the keys used for the key scan mode for a soft keyboard.</span></span><br/>                                  |
| [<span data-ttu-id="a0fd4-153">**шовсофткэйбоард**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-153">**ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)                                         | <span data-ttu-id="a0fd4-154">Отображает экранную клавиатуру.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-154">Displays a soft keyboard.</span></span><br/>                                                                          |
| [<span data-ttu-id="a0fd4-155">**унадвисесофткэйбоардевентсинк**</span><span class="sxs-lookup"><span data-stu-id="a0fd4-155">**UnadviseSoftKeyboardEventSink**</span></span>](isoftkbd-unadvisesoftkeyboardeventsink.md)               | <span data-ttu-id="a0fd4-156">Удаляет многофункциональный приемник событий клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a0fd4-156">Removes a soft keyboard event sink.</span></span><br/>                                                                |



 

## <a name="requirements"></a><span data-ttu-id="a0fd4-157">Требования</span><span class="sxs-lookup"><span data-stu-id="a0fd4-157">Requirements</span></span>



| <span data-ttu-id="a0fd4-158">Требование</span><span class="sxs-lookup"><span data-stu-id="a0fd4-158">Requirement</span></span> | <span data-ttu-id="a0fd4-159">Значение</span><span class="sxs-lookup"><span data-stu-id="a0fd4-159">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0fd4-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0fd4-160">Minimum supported client</span></span><br/> | <span data-ttu-id="a0fd4-161">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a0fd4-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a0fd4-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0fd4-162">Minimum supported server</span></span><br/> | <span data-ttu-id="a0fd4-163">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a0fd4-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a0fd4-164">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a0fd4-164">Redistributable</span></span><br/>          | <span data-ttu-id="a0fd4-165">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="a0fd4-165">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="a0fd4-166">Header</span><span class="sxs-lookup"><span data-stu-id="a0fd4-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0fd4-167"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0fd4-167"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="a0fd4-168">IDL</span><span class="sxs-lookup"><span data-stu-id="a0fd4-168">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a0fd4-169"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a0fd4-169"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="a0fd4-170">DLL</span><span class="sxs-lookup"><span data-stu-id="a0fd4-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0fd4-171"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0fd4-171"><dt>Softkbd.dll</dt></span></span> </dl> |



 

