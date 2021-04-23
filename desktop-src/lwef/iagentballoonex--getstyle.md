---
title: Иажентбаллунекс
description: Иажентбаллунекс
ms.assetid: 7c6a7260-073b-4535-b8e7-a8cae9aae9ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e21ab22a9aa5a85fdbe1bc541f29df75313cdce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888763"
---
# <a name="iagentballoonexgetstyle"></a><span data-ttu-id="1df77-103">Иажентбаллунекс:: штриховка</span><span class="sxs-lookup"><span data-stu-id="1df77-103">IAgentBalloonEx::GetStyle</span></span>

<span data-ttu-id="1df77-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1df77-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetStyle(
   long * plStyle,  // address of style settings
);
```

<span data-ttu-id="1df77-105">Извлекает параметры стиля всплывающего окна символа.</span><span class="sxs-lookup"><span data-stu-id="1df77-105">Retrieves the character's word balloon style settings.</span></span>

-   <span data-ttu-id="1df77-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1df77-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1df77-107"><span id="plStyle"></span><span id="plstyle"></span><span id="PLSTYLE"></span>*плстиле*</span><span class="sxs-lookup"><span data-stu-id="1df77-107"><span id="plStyle"></span><span id="plstyle"></span><span id="PLSTYLE"></span>*plStyle*</span></span>
</dt> <dd>

<span data-ttu-id="1df77-108">Параметры стиля для всплывающей подсказки Word, которые могут быть комбинацией любого из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="1df77-108">Style settings for the word balloon, which can be a combination of any of the following values:</span></span>



| <span data-ttu-id="1df77-109">Значение</span><span class="sxs-lookup"><span data-stu-id="1df77-109">Value</span></span>                                                                           | <span data-ttu-id="1df77-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1df77-110">Description</span></span>                                                 |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="1df77-111">**const неподписанный короткий** **стиль всплывающего окна \_ \_ баллунон = 0x00000001;**</span><span class="sxs-lookup"><span data-stu-id="1df77-111">**const unsigned short** **BALLOON\_STYLE\_BALLOONON = 0x00000001;**</span></span><br/> | <span data-ttu-id="1df77-112">Всплывающее сообщение поддерживается для выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1df77-112">The balloon is supported for output.</span></span>                        |
| <span data-ttu-id="1df77-113">**const неподписанный короткий** **стиль всплывающего окна \_ \_ сизетотекст = 0x0000002;**</span><span class="sxs-lookup"><span data-stu-id="1df77-113">**const unsigned short** **BALLOON\_STYLE \_SIZETOTEXT = 0x0000002;**</span></span>           | <span data-ttu-id="1df77-114">Высота всплывающего окна изменяется в соответствии с выводом текста.</span><span class="sxs-lookup"><span data-stu-id="1df77-114">The balloon height is sized to accommodate the text output.</span></span> |
| <span data-ttu-id="1df77-115">**const неподписанный короткий** **стиль всплывающего окна \_ \_ : автоматическое скрытие = 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="1df77-115">**const unsigned short** **BALLOON\_STYLE \_AUTOHIDE = 0x00000004;**</span></span>            | <span data-ttu-id="1df77-116">Всплывающее сообщение автоматически скрывается.</span><span class="sxs-lookup"><span data-stu-id="1df77-116">The balloon is automatically hidden.</span></span>                        |
| <span data-ttu-id="1df77-117">**const неподписанный короткий** **стиль всплывающего окна \_ \_ : автоскорость = 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="1df77-117">**const unsigned short** **BALLOON\_STYLE \_AUTOPACE = 0x00000008;**</span></span>            | <span data-ttu-id="1df77-118">Вывод текста осуществляется в соответствии с частотой вывода.</span><span class="sxs-lookup"><span data-stu-id="1df77-118">The text output is paced based on the output rate.</span></span>          |



 

</dd> </dl>

<span data-ttu-id="1df77-119">Если задан бит стиля **баллунон** , всплывающее окно появляется при использовании метода [**говорите**](speak-method.md) или « [**подумать**](think-method.md) », если пользователь не переопределит его отображение на странице свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="1df77-119">When the **BalloonOn** style bit is set, the word balloon appears when the [**Speak**](speak-method.md) or [**Think**](think-method.md) method is used, unless the user overrides its display through the Microsoft Agent property sheet.</span></span> <span data-ttu-id="1df77-120">Если не задано, всплывающие окна не отображаются.</span><span class="sxs-lookup"><span data-stu-id="1df77-120">When not set, no balloon appears.</span></span>

<span data-ttu-id="1df77-121">Если задан бит стиля **сизетотекст** , всплывающая подсказка автоматически изменяет высоту всплывающего окна на текущий размер текста, указанного в методе [**говорите**](speak-method.md) или « [**подумать**](think-method.md) ».</span><span class="sxs-lookup"><span data-stu-id="1df77-121">When the **SizeToText** style bit is set, the word balloon automatically sizes the height of the balloon to the current size of the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method.</span></span> <span data-ttu-id="1df77-122">Если значение не задано, Высота всплывающего окна основывается на значении свойства "число строк" всплывающего окна.</span><span class="sxs-lookup"><span data-stu-id="1df77-122">When not set, the balloon's height is based on the balloon's number of lines property setting.</span></span> <span data-ttu-id="1df77-123">Этот бит стиля имеет значение 1, поэтому попытка использовать [**иажентбаллунекс:: сетнумлинес**](iagentballoonex--setnumlines.md) приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="1df77-123">This style bit is set to 1 and an attempt to use [**IAgentBalloonEx::SetNumLines**](iagentballoonex--setnumlines.md) will result in an error.</span></span>

<span data-ttu-id="1df77-124">Если задан бит **автоскрытия** , всплывающая подсказка Word автоматически скрывается по истечении короткого времени ожидания. Если этот параметр не задан, всплывающее сообщение отображается до появления нового вызова [**говорите**](speak-method.md) или [**обработки**](think-method.md) , если этот символ скрыт, либо пользователь щелкает или перетаскивает этот символ.</span><span class="sxs-lookup"><span data-stu-id="1df77-124">When the **AutoHide** style bit is set, the word balloon automatically hides after a short time-out. When not set, the balloon displays until a new [**Speak**](speak-method.md) or [**Think**](think-method.md) call, the character is hidden, or the user clicks or drags the character.</span></span>

<span data-ttu-id="1df77-125">Если задан бит **Автотемпа** , всплывающая подсказка выводит на экран результаты на основе текущей скорости вывода, например по одному слову за раз.</span><span class="sxs-lookup"><span data-stu-id="1df77-125">When the **AutoPace** style bit is set, the word balloon paces the output based on the current output rate, for example, one word at a time.</span></span> <span data-ttu-id="1df77-126">Когда вывод превышает размер всплывающего окна, первый текст автоматически прокручивается.</span><span class="sxs-lookup"><span data-stu-id="1df77-126">When output exceeds the size of the balloon, the former text is automatically scrolled.</span></span> <span data-ttu-id="1df77-127">Если не задано, весь текст, входящий в оператор [**говорите**](speak-method.md) или « [**подумать**](think-method.md) », отображается одновременно.</span><span class="sxs-lookup"><span data-stu-id="1df77-127">When not set, all text included in a [**Speak**](speak-method.md) or [**Think**](think-method.md) statement displays at once.</span></span>

<span data-ttu-id="1df77-128">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="1df77-128">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="1df77-129">Значения по умолчанию для этих битов стиля основаны на параметрах при компиляции символа с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="1df77-129">The defaults for these style bits are based on the settings when the character is compiled through the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="1df77-130">См. также:</span><span class="sxs-lookup"><span data-stu-id="1df77-130">See Also</span></span>

[<span data-ttu-id="1df77-131">**Иажентбаллунекс:: SetStyle**</span><span class="sxs-lookup"><span data-stu-id="1df77-131">**IAgentBalloonEx::SetStyle**</span></span>](iagentballoonex--setstyle.md)


 

 





