---
title: Добавление и изменение событий
description: Добавление и изменение событий
ms.assetid: 342b0592-67b7-4c13-bee8-48ac322d3d27
keywords:
- Подключаемые модули проигрывателя Windows Media, примеры страниц свойств Echo
- страницы свойств "подключаемые модули", "Эхо-примеры"
- подключаемые модули обработки цифровых сигналов, примеры страниц свойств
- Подключаемые модули DSP, примеры страниц свойств
- Пример подключаемого модуля "Echo DSP", страницы свойств
- Пример подключаемого модуля Echo DSP, события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c8e069c20dc2c953998b9e5c2a47f509166ca3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331131"
---
# <a name="adding-and-modifying-the-events"></a><span data-ttu-id="4be39-109">Добавление и изменение событий</span><span class="sxs-lookup"><span data-stu-id="4be39-109">Adding and Modifying the Events</span></span>

<span data-ttu-id="4be39-110">Необходимо предоставить обработчики событий для \_ событий изменения EN, происходящих при изменении пользователем текста в полях редактирования страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="4be39-110">You need to supply event handlers for the EN\_CHANGE events that occur when the user changes the text in the property page edit boxes.</span></span> <span data-ttu-id="4be39-111">Эти обработчики событий имеют простую реализацию, которая просто включает параметр **Применить** в диалоговом окне страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="4be39-111">These event handlers have a simple implementation that merely enables **Apply** in the property page dialog box.</span></span>

## <a name="modifying-the-scale-factor-event-handler"></a><span data-ttu-id="4be39-112">Изменение обработчика событий коэффициента масштабирования</span><span class="sxs-lookup"><span data-stu-id="4be39-112">Modifying the Scale Factor Event Handler</span></span>

<span data-ttu-id="4be39-113">Необходимо изменить имя существующего обработчика событий, предоставленного мастером подключаемых модулей для поля ввода коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="4be39-113">You need to change the name of the existing event handler that the plug-in wizard provided for the scale factor edit box.</span></span> <span data-ttu-id="4be39-114">Необходимо изменить имя с Ончанжескале на Ончанжеделай в трех местах:</span><span class="sxs-lookup"><span data-stu-id="4be39-114">You should change the name from OnChangeScale to OnChangeDelay in three locations:</span></span>

1.  <span data-ttu-id="4be39-115">В Ечопроппаже. h измените имя в разделе макроса схемы сообщения.</span><span class="sxs-lookup"><span data-stu-id="4be39-115">In EchoPropPage.h, change the name in the message map macro section.</span></span> <span data-ttu-id="4be39-116">Замените строку, которая сопоставляет событие изменения коэффициента масштабирования с методом Ончанжескале, следующим кодом:</span><span class="sxs-lookup"><span data-stu-id="4be39-116">Replace the line that maps the scale factor change event to the OnChangeScale method with the following code:</span></span>
    ```C++
    COMMAND_HANDLER(IDC_DELAYTIME, EN_CHANGE, OnChangeDelay)
    
    ```

    

2.  <span data-ttu-id="4be39-117">В Ечопроппаже. h измените имя в строке, которая прототипет функцию Ончанжескале:</span><span class="sxs-lookup"><span data-stu-id="4be39-117">In EchoPropPage.h, change the name in the line that prototypes the OnChangeScale function:</span></span>
    ```C++
    LRESULT (OnChangeDelay)(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled);
    
    ```

    

3.  <span data-ttu-id="4be39-118">В Ечопроппаже. cpp измените имя в заголовке функции:</span><span class="sxs-lookup"><span data-stu-id="4be39-118">In EchoPropPage.cpp, change the name in the function header:</span></span>
    ```C++
    LRESULT CEchoPropPage::OnChangeDelay(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled)
    
    ```

    

## <a name="adding-the-wet-mix-event-handler"></a><span data-ttu-id="4be39-119">Добавление обработчика событий со смешением</span><span class="sxs-lookup"><span data-stu-id="4be39-119">Adding the Wet Mix Event Handler</span></span>

<span data-ttu-id="4be39-120">Вы можете легко добавить обработчик событий для \_ события смены языка, присоединенного к \_ элементу управления "поле ввода" IDC ветмикс.</span><span class="sxs-lookup"><span data-stu-id="4be39-120">You can easily add the event handler for the EN\_CHANGE event that is attached to the IDC\_WETMIX edit box control.</span></span> <span data-ttu-id="4be39-121">В редакторе ресурсов диалогового окна:</span><span class="sxs-lookup"><span data-stu-id="4be39-121">From the dialog resource editor:</span></span>

1.  <span data-ttu-id="4be39-122">Щелкните правой кнопкой мыши \_ поле ввода IDC ветмикс и выберите пункт **события**.</span><span class="sxs-lookup"><span data-stu-id="4be39-122">Right-click the IDC\_WETMIX edit box and choose **Events**.</span></span> <span data-ttu-id="4be39-123">Откроется диалоговое окно Новое сообщение Windows и обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="4be39-123">The New Windows Message and Event Handlers dialog box appears.</span></span>
2.  <span data-ttu-id="4be39-124">В поле **класс или объект для обработчика** щелкните имя ресурса поля редактирования, IDC \_ ветмикс.</span><span class="sxs-lookup"><span data-stu-id="4be39-124">In the **Class or object to handle** box, click the name of the edit box resource, IDC\_WETMIX.</span></span>
3.  <span data-ttu-id="4be39-125">В окне **новые сообщения или события Windows** щелкните EN Change (смена языка), \_ чтобы выбрать его.</span><span class="sxs-lookup"><span data-stu-id="4be39-125">In the **New Windows messages/events** box, click EN\_CHANGE to select it.</span></span>
4.  <span data-ttu-id="4be39-126">Нажмите кнопку **Добавить обработчик**.</span><span class="sxs-lookup"><span data-stu-id="4be39-126">Click **Add Handler**.</span></span> <span data-ttu-id="4be39-127">Откроется диалоговое окно Добавление функции члена.</span><span class="sxs-lookup"><span data-stu-id="4be39-127">The Add Member Function dialog box appears.</span></span>
5.  <span data-ttu-id="4be39-128">В поле **имя функции члена** введите имя ончанжеветмикс.</span><span class="sxs-lookup"><span data-stu-id="4be39-128">In the **Member function name** box, type the name OnChangeWetmix.</span></span>
6.  <span data-ttu-id="4be39-129">Нажмите кнопку **ОК** , чтобы закрыть диалоговое окно Добавление функции члена.</span><span class="sxs-lookup"><span data-stu-id="4be39-129">Click **OK** to close the Add Member Function dialog box.</span></span>
7.  <span data-ttu-id="4be39-130">Нажмите кнопку **ОК** , чтобы вернуться в редактор ресурсов диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4be39-130">Click **OK** to return to the dialog box resource editor.</span></span>

<span data-ttu-id="4be39-131">Visual C++ автоматически добавляет код для схемы сообщений и для функции обработчика событий в Ечопроппаже. h.</span><span class="sxs-lookup"><span data-stu-id="4be39-131">Visual C++ automatically adds the code for the message map and for the event handler function to EchoPropPage.h.</span></span> <span data-ttu-id="4be39-132">Код, который он вставляет, содержит комментарий TODO, в котором можно добавить реализацию в заголовок функции.</span><span class="sxs-lookup"><span data-stu-id="4be39-132">The code it inserts provides a TODO comment where you can add the implementation in the header for the function.</span></span> <span data-ttu-id="4be39-133">Этот стиль немного отличается от образца кода мастера подключаемого модуля проигрывателя Windows Media, но является приемлемым.</span><span class="sxs-lookup"><span data-stu-id="4be39-133">This is a slightly different style than the Windows Media Player Plug-in Wizard sample code uses, but is acceptable.</span></span>

<span data-ttu-id="4be39-134">Требуется ли писать реализацию в файле заголовка или переместить ее в Ечопроппаже. cpp.</span><span class="sxs-lookup"><span data-stu-id="4be39-134">Whether you want to write your implementation in the header file or move it to EchoPropPage.cpp is up to you.</span></span> <span data-ttu-id="4be39-135">В любом случае для реализации **необходимо включить в** диалоговом окне страницы свойств только одну дополнительную строку кода.</span><span class="sxs-lookup"><span data-stu-id="4be39-135">In either case, the implementation needs only a single additional line of code to enable **Apply** in the property page dialog.</span></span> <span data-ttu-id="4be39-136">Вставьте эту строку кода перед строкой, которая возвращает из функции:</span><span class="sxs-lookup"><span data-stu-id="4be39-136">Insert this line of code before the line that returns from the function:</span></span>


```C++
SetDirty(TRUE);  // Enable Apply.

```



## <a name="related-topics"></a><span data-ttu-id="4be39-137">См. также</span><span class="sxs-lookup"><span data-stu-id="4be39-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4be39-138">**Изменение страницы свойств «пример эха»**</span><span class="sxs-lookup"><span data-stu-id="4be39-138">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




