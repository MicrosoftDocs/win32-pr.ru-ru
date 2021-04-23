---
description: Объект-разделитель использует Рекогнизерконтекст для улучшения его анализа сегментов распознавания и создания текста распознавания для элементов рукописного ввода.
ms.assetid: 33d9abc4-151e-47b4-b66f-ff6adfe21222
title: Работа с контекстом распознавателя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdea8c59bc894a6962e8bbe7e58f316327a548e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072825"
---
# <a name="working-with-a-recognizer-context"></a><span data-ttu-id="7db4c-103">Работа с контекстом распознавателя</span><span class="sxs-lookup"><span data-stu-id="7db4c-103">Working with a Recognizer Context</span></span>

<span data-ttu-id="7db4c-104">Объект- [**Разделитель**](inkdivider-class.md) использует [**рекогнизерконтекст**](inkrecognizercontext-class.md) для улучшения его анализа сегментов распознавания и создания текста распознавания для элементов рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="7db4c-104">The [**Divider**](inkdivider-class.md) object uses a [**RecognizerContext**](inkrecognizercontext-class.md) to improve its analysis of recognition segments and to generate recognition text for handwriting elements.</span></span>

<span data-ttu-id="7db4c-105">Контекст распознавателя можно задать с помощью свойства [**рекогнизерконтекст**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) объекта- [**разделителя**](inkdivider-class.md) или путем указания контекста распознавателя в вызове конструктора [разделителя](/previous-versions/ms839465(v=msdn.10)) (в управляемом коде).</span><span class="sxs-lookup"><span data-stu-id="7db4c-105">You can set the recognizer context by using the [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property of the [**Divider**](inkdivider-class.md) object or by supplying the recognizer context in the call to the [Divider](/previous-versions/ms839465(v=msdn.10)) constructor (in managed code).</span></span> <span data-ttu-id="7db4c-106">Если для свойства **рекогнизерконтекст** назначается контекст распознавателя для распознавателя, не поддерживающего рукописного ввода, или для распознавателя, который не поддерживает функцию свободного ввода, создается исключение.</span><span class="sxs-lookup"><span data-stu-id="7db4c-106">If a recognizer context for a non-handwriting recognizer or for a recognizer that does not support the free input capability is assigned to the **RecognizerContext** property, then an exception is thrown.</span></span>

<span data-ttu-id="7db4c-107">Если распознаватели не установлены или контекст распознавателя не назначен объекту- [**разделителю**](inkdivider-class.md) , то объект- **Разделитель** не использует контекст распознавателя.</span><span class="sxs-lookup"><span data-stu-id="7db4c-107">If recognizers are not installed or a recognizer context is not assigned to the [**Divider**](inkdivider-class.md) object, the **Divider** object does not use a recognizer context.</span></span> <span data-ttu-id="7db4c-108">В этом случае функция анализа макета выполняет подразделение сегментов, и ни один текст не связан с объектом [**дивисионресулт**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="7db4c-108">In this case, the layout analysis feature performs the segment division, and no text is associated with the [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

> [!Note]  
> <span data-ttu-id="7db4c-109">Свойство [**рекогнизерконтекст**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) нельзя изменить после того, как штрихи были назначены объекту [**разделителя**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="7db4c-109">The [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property cannot be changed after strokes have been assigned to the [**Divider**](inkdivider-class.md) object.</span></span> <span data-ttu-id="7db4c-110">Объект **разделителя** использует значения свойств по умолчанию объекта [**рекогнизерконтекст**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="7db4c-110">The **Divider** object uses the default property values of the [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

 

<span data-ttu-id="7db4c-111">Объект [**разделителя**](inkdivider-class.md) применяет контекст распознавателя к рукописным элементам во время анализа макета.</span><span class="sxs-lookup"><span data-stu-id="7db4c-111">The [**Divider**](inkdivider-class.md) object applies the recognizer context to handwritten elements during layout analysis.</span></span> <span data-ttu-id="7db4c-112">Все штрихи, назначаемые непосредственно контексту распознавателя, игнорируются объектом **разделителя** .</span><span class="sxs-lookup"><span data-stu-id="7db4c-112">Any strokes you assign directly to the recognizer context are ignored by the **Divider** object.</span></span> <span data-ttu-id="7db4c-113">Дополнительные сведения о распознавании текста см. в разделе [о распознавании рукописного ввода](about-handwriting-recognition.md).</span><span class="sxs-lookup"><span data-stu-id="7db4c-113">For more information about text recognition, see [About Handwriting Recognition](about-handwriting-recognition.md).</span></span>

 

 
