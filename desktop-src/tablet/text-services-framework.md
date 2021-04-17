---
description: Общие сведения о платформе текстовых служб для планшетных ПК.
ms.assetid: f77fe77a-8625-47c5-bfc7-b473c8e8a8c6
title: Платформа текстовых служб (планшетный ПК)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25eb3e635ae7394502ed203cb9ea31e115dc09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684510"
---
# <a name="text-services-framework-tablet-pc"></a><span data-ttu-id="6b84d-103">Платформа текстовых служб (планшетный ПК)</span><span class="sxs-lookup"><span data-stu-id="6b84d-103">Text Services Framework (Tablet PC)</span></span>

<span data-ttu-id="6b84d-104">Если [Платформа текстовых служб (TSF)](../tsf/text-services-framework.md) включена для элемента управления с присоединенным объектом [Пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) , объект пенинпутпанел может вставлять текст напрямую.</span><span class="sxs-lookup"><span data-stu-id="6b84d-104">When the [Text Services Framework (TSF)](../tsf/text-services-framework.md) is enabled on a control with a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object attached, the PenInputPanel object can insert text directly.</span></span> <span data-ttu-id="6b84d-105">Если элемент управления не поддерживает платформу текстовых служб (TSF), то объект Пенинпутпанел должен использовать [функцию SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) для вставки текста.</span><span class="sxs-lookup"><span data-stu-id="6b84d-105">If the control does not support Text Services Framework (TSF), the PenInputPanel object must resort to using the [SendInput function](/windows/win32/api/winuser/nf-winuser-sendinput) to insert text.</span></span>

<span data-ttu-id="6b84d-106">Возможность вставки текста напрямую очень важна для тех, кто помещает знаки восточно-азиатских языков, где использование [функции SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) может привести к неправильным символам.</span><span class="sxs-lookup"><span data-stu-id="6b84d-106">The ability to insert text directly becomes very important for those inputting East Asian characters, where using the [SendInput function](/windows/win32/api/winuser/nf-winuser-sendinput) can produce incorrect characters.</span></span>

<span data-ttu-id="6b84d-107">TSF предоставляет интерфейс для исправления ошибок распознавания, позволяющий конечному пользователю исправлять, переписывать или даже диктовать нужный текст.</span><span class="sxs-lookup"><span data-stu-id="6b84d-107">TSF provides an interface for correcting recognition errors enabling the end user to correct, rewrite, or even dictate the proper text.</span></span>

<span data-ttu-id="6b84d-108">TSF включается путем вызова метода [енаблетсф](/previous-versions/ms569656(v=vs.100)) с параметром *Enable* , установленным в **значение true**.</span><span class="sxs-lookup"><span data-stu-id="6b84d-108">TSF is enabled by calling the [EnableTsf](/previous-versions/ms569656(v=vs.100)) method with the *enable* parameter set to **TRUE**.</span></span>

<span data-ttu-id="6b84d-109">\[C\#\]</span><span class="sxs-lookup"><span data-stu-id="6b84d-109">\[C\#\]</span></span>


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(theControl);
//...
thePenInputPanel.EnableTsf(true);
```



<span data-ttu-id="6b84d-110">Объект [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) , присоединенный к элементу управления [InkEdit](/previous-versions/ms552265(v=vs.100)) , обеспечивает надежный пользовательский интерфейс, так как InkEdit поддерживает TSF.</span><span class="sxs-lookup"><span data-stu-id="6b84d-110">A [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object attached to a [InkEdit](/previous-versions/ms552265(v=vs.100)) control provides a robust user experience because the InkEdit supports TSF.</span></span> <span data-ttu-id="6b84d-111">Однако обязательно задайте для свойства [инкмоде](/previous-versions/ms835850(v=msdn.10)) значение [Microsoft. Ink. инкмоде. Ink](/previous-versions/ms827399(v=msdn.10)) в элементе управления InkEdit, как указано в разделе [рекомендации](best-practices.md) .</span><span class="sxs-lookup"><span data-stu-id="6b84d-111">However, be sure to set the [InkMode](/previous-versions/ms835850(v=msdn.10)) property to [Microsoft.Ink.InkMode.Ink](/previous-versions/ms827399(v=msdn.10)) on the InkEdit control as mentioned in the [Best Practices](best-practices.md) topic.</span></span>

<span data-ttu-id="6b84d-112">В примере [пенинпутпанел](peninputpanel-sample.md) приведен пример включения TSF.</span><span class="sxs-lookup"><span data-stu-id="6b84d-112">The [PenInputPanel Sample](peninputpanel-sample.md) provides an example of enabling TSF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b84d-113">См. также</span><span class="sxs-lookup"><span data-stu-id="6b84d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b84d-114">инфраструктуры текстовых служб (TSF)</span><span class="sxs-lookup"><span data-stu-id="6b84d-114">Text Services Framework</span></span>](../tsf/text-services-framework.md)
</dt> </dl>

 

 
