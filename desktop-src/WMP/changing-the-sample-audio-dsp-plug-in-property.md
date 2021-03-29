---
title: Изменение примера свойства подключаемого модуля DSP аудиоподсистемы
description: Изменение примера свойства подключаемого модуля DSP аудиоподсистемы
ms.assetid: 9e742bcd-cff8-422f-ad91-d8d46f15bdc4
keywords:
- Подключаемые модули проигрывателя Windows Media, DSP аудиоподсистемы
- подключаемые модули, DSP аудиоподсистемы
- подключаемые модули обработки цифровых сигналов, свойства аудио
- Подключаемые модули DSP, звуковые свойства
- подключаемые модули DSP аудио, свойства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc27f58fa8c8903b54f9903797dcc32a7795841
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777720"
---
# <a name="changing-the-sample-audio-dsp-plug-in-property"></a><span data-ttu-id="a822c-108">Изменение примера свойства подключаемого модуля DSP аудиоподсистемы</span><span class="sxs-lookup"><span data-stu-id="a822c-108">Changing the Sample Audio DSP Plug-in Property</span></span>

<span data-ttu-id="a822c-109">Возможно, потребуется изменить свойство, создаваемое мастером подключаемых модулей проигрывателя Windows Media по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a822c-109">You will probably want to change the property that the Windows Media Player Plug-in Wizard creates by default.</span></span> <span data-ttu-id="a822c-110">В следующем списке приведены элементы, которые могут потребоваться изменить:</span><span class="sxs-lookup"><span data-stu-id="a822c-110">The following list details the items that might require changing:</span></span>

-   <span data-ttu-id="a822c-111">**Ресурс диалогового окна.**</span><span class="sxs-lookup"><span data-stu-id="a822c-111">**The dialog resource.**</span></span> <span data-ttu-id="a822c-112">Перейдите на вкладку **ресаурцевиев** в окне рабочей области проекта.</span><span class="sxs-lookup"><span data-stu-id="a822c-112">Click the **ResourceView** tab in the Project Workspace window.</span></span> <span data-ttu-id="a822c-113">Разверните список папок, чтобы открыть папку диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a822c-113">Expand the folder list to open the Dialog folder.</span></span> <span data-ttu-id="a822c-114">Дважды щелкните ресурс диалогового окна, чтобы открыть редактор ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a822c-114">Double-click the dialog resource to open the resource editor.</span></span> <span data-ttu-id="a822c-115">Вы можете внести изменения в диалоговое окно страницы свойств, чтобы удовлетворить ваши потребности.</span><span class="sxs-lookup"><span data-stu-id="a822c-115">You can make changes to the property page dialog to fulfill your needs.</span></span> <span data-ttu-id="a822c-116">Например, можно изменить текст в метке или заменить элемент управления "поле ввода" флажком.</span><span class="sxs-lookup"><span data-stu-id="a822c-116">For instance, you could change the text in the label or replace the edit control with a checkbox.</span></span>
-   <span data-ttu-id="a822c-117">**Объектный код страницы свойств.**</span><span class="sxs-lookup"><span data-stu-id="a822c-117">**The property page object code.**</span></span> <span data-ttu-id="a822c-118">Реализация по умолчанию использует переменную типа Double для хранения коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="a822c-118">The default implementation uses a variable of type double to store the scale factor.</span></span> <span data-ttu-id="a822c-119">Может потребоваться другой тип данных.</span><span class="sxs-lookup"><span data-stu-id="a822c-119">You might require a different type of data.</span></span> <span data-ttu-id="a822c-120">Это также потребует изменения кода, сохраняющего данные в реестре, и считывания данных из реестра (включая код, считывающий данные из реестра в *кпрожектнаме*::**финалконструкт**).</span><span class="sxs-lookup"><span data-stu-id="a822c-120">This would also require you to change the code that persists the data to the registry and reads the data from the registry (including the code that reads from the registry in *CProjectName*::**FinalConstruct**).</span></span>
-   <span data-ttu-id="a822c-121">**Переменная члена, в которой хранится значение свойства.**</span><span class="sxs-lookup"><span data-stu-id="a822c-121">**The member variable that stores the property value.**</span></span> <span data-ttu-id="a822c-122">Эта переменная называется "m \_ фскалефактор" и объявлена как тип Double.</span><span class="sxs-lookup"><span data-stu-id="a822c-122">This variable is named "m\_fScaleFactor" and is declared as type double.</span></span> <span data-ttu-id="a822c-123">Может потребоваться изменить имя и тип этой переменной по всему проекту.</span><span class="sxs-lookup"><span data-stu-id="a822c-123">You may want to change the name and type of this variable throughout the project.</span></span>
-   <span data-ttu-id="a822c-124">**Методы get и Property.**</span><span class="sxs-lookup"><span data-stu-id="a822c-124">**The property get and property put methods.**</span></span> <span data-ttu-id="a822c-125">Может потребоваться изменить имена, параметры и реализации этих методов.</span><span class="sxs-lookup"><span data-stu-id="a822c-125">You might want to change the names, parameters, and implementations of these methods.</span></span> <span data-ttu-id="a822c-126">Не забывайте также отражать эти изменения в других местах проекта.</span><span class="sxs-lookup"><span data-stu-id="a822c-126">Don't forget to also reflect those changes elsewhere in the project.</span></span> <span data-ttu-id="a822c-127">Например, страница свойств **Apply** вызывает метод *кпрожектнаме*:: Where **\_ Scale**.</span><span class="sxs-lookup"><span data-stu-id="a822c-127">For instance, the property page **Apply** method calls *CProjectName*::**put\_scale**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a822c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a822c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a822c-129">**Реализация подключаемого модуля DSP аудиоподсистемы**</span><span class="sxs-lookup"><span data-stu-id="a822c-129">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




