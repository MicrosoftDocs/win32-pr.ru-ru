---
title: Иажентбаллунекс SetStyle
description: Иажентбаллунекс SetStyle
ms.assetid: 5be569b7-8a2d-437b-b5db-401af343bc78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d942cc8adaf454a7c5f1cd299581f917560c00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700721"
---
# <a name="iagentballoonexsetstyle"></a><span data-ttu-id="d05b4-103">Иажентбаллунекс:: SetStyle</span><span class="sxs-lookup"><span data-stu-id="d05b4-103">IAgentBalloonEx::SetStyle</span></span>

<span data-ttu-id="d05b4-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d05b4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetStyle(
   long lStyle,  // style settings
);
```

<span data-ttu-id="d05b4-105">Извлекает параметры стиля всплывающего окна символа.</span><span class="sxs-lookup"><span data-stu-id="d05b4-105">Retrieves the character's word balloon style settings.</span></span>

-   <span data-ttu-id="d05b4-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d05b4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d05b4-107"><span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*лстиле*</span><span class="sxs-lookup"><span data-stu-id="d05b4-107"><span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*lStyle*</span></span>
</dt> <dd>

<span data-ttu-id="d05b4-108">Параметры стиля для всплывающей подсказки Word, которые могут быть комбинацией любого из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="d05b4-108">Style settings for the word balloon, which can be a combination of any of the following values:</span></span>



| <span data-ttu-id="d05b4-109">Значение</span><span class="sxs-lookup"><span data-stu-id="d05b4-109">Value</span></span>                                                                            | <span data-ttu-id="d05b4-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d05b4-110">Description</span></span>                                                 |
|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d05b4-111">**const неподписанный короткий** **стиль всплывающего окна \_ \_ баллунон = 0x00000001;**</span><span class="sxs-lookup"><span data-stu-id="d05b4-111">**const unsigned short** **BALLOON\_STYLE\_BALLOONON = 0x00000001;**</span></span><br/>  | <span data-ttu-id="d05b4-112">Всплывающее сообщение поддерживается для выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d05b4-112">The balloon is supported for output.</span></span>                        |
| <span data-ttu-id="d05b4-113">**const неподписанный короткий** **стиль всплывающего окна \_ \_ сизетотекст = 0x0000002;**</span><span class="sxs-lookup"><span data-stu-id="d05b4-113">**const unsigned short** **BALLOON\_STYLE \_SIZETOTEXT = 0x0000002;**</span></span><br/> | <span data-ttu-id="d05b4-114">Высота всплывающего окна изменяется в соответствии с выводом текста.</span><span class="sxs-lookup"><span data-stu-id="d05b4-114">The balloon height is sized to accommodate the text output.</span></span> |
| <span data-ttu-id="d05b4-115">**const неподписанный короткий** **стиль всплывающего окна \_ \_ : автоматическое скрытие = 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="d05b4-115">**const unsigned short** **BALLOON\_STYLE \_AUTOHIDE = 0x00000004;**</span></span><br/>  | <span data-ttu-id="d05b4-116">Всплывающее сообщение автоматически скрывается.</span><span class="sxs-lookup"><span data-stu-id="d05b4-116">The balloon is automatically hidden.</span></span>                        |
| <span data-ttu-id="d05b4-117">**const неподписанный короткий** **стиль всплывающего окна \_ \_ : автоскорость = 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="d05b4-117">**const unsigned short** **BALLOON\_STYLE \_AUTOPACE = 0x00000008;**</span></span><br/>  | <span data-ttu-id="d05b4-118">Вывод текста осуществляется в соответствии с частотой вывода.</span><span class="sxs-lookup"><span data-stu-id="d05b4-118">The text output is paced based on the output rate.</span></span>          |



 

</dd> </dl>

<span data-ttu-id="d05b4-119">Если задан бит стиля **баллунон** , всплывающее окно появляется при использовании метода [**говорите**](speak-method.md) или « [**подумать**](think-method.md) », если пользователь не переопределит его отображение на странице свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d05b4-119">When the **BalloonOn** style bit is set, the word balloon appears when the [**Speak**](speak-method.md) or [**Think**](think-method.md) method is used, unless the user overrides its display in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="d05b4-120">Если не задано, всплывающие окна не отображаются.</span><span class="sxs-lookup"><span data-stu-id="d05b4-120">When not set, no balloon appears.</span></span>

<span data-ttu-id="d05b4-121">Если задан бит стиля **сизетотекст** , всплывающая подсказка автоматически изменяет высоту всплывающего окна на текущий размер текста, указанного в методе [**говорите**](speak-method.md) или « [**подумать**](think-method.md) ».</span><span class="sxs-lookup"><span data-stu-id="d05b4-121">When the **SizeToText** style bit is set, the word balloon automatically sizes the height of the balloon to the current size of the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method.</span></span> <span data-ttu-id="d05b4-122">Если значение не задано, Высота всплывающего окна основывается на значении свойства "число строк" всплывающего окна.</span><span class="sxs-lookup"><span data-stu-id="d05b4-122">When not set, the balloon's height is based on the balloon's number of lines property setting.</span></span> <span data-ttu-id="d05b4-123">Этот бит стиля имеет значение 1, поэтому попытка использовать [**иажентбаллунекс:: сетнумлинес**](iagentballoonex--setnumlines.md) приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="d05b4-123">This style bit is set to 1 and an attempt to use [**IAgentBalloonEx::SetNumLines**](iagentballoonex--setnumlines.md) will result in an error.</span></span>

<span data-ttu-id="d05b4-124">Если задан бит **автоскрытия** , всплывающая подсказка Word автоматически скрывается после короткого времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="d05b4-124">When the **AutoHide** style bit is set, the word balloon automatically hides after a short timeout.</span></span> <span data-ttu-id="d05b4-125">Если этот параметр не задан, всплывающее сообщение отображается до появления нового вызова [**говорите**](speak-method.md) или [**обработки**](think-method.md) , если этот символ скрыт, либо пользователь щелкает или перетаскивает этот символ.</span><span class="sxs-lookup"><span data-stu-id="d05b4-125">When not set, the balloon displays until a new [**Speak**](speak-method.md) or [**Think**](think-method.md) call, the character is hidden, or the user clicks or drags the character.</span></span>

<span data-ttu-id="d05b4-126">Если задан бит **Автотемпа** , всплывающая подсказка выводит на экран результаты на основе текущей скорости вывода, например по одному слову за раз.</span><span class="sxs-lookup"><span data-stu-id="d05b4-126">When the **AutoPace** style bit is set, the word balloon paces the output based on the current output rate, for example, one word at a time.</span></span> <span data-ttu-id="d05b4-127">Когда вывод превышает размер всплывающего окна, первый текст автоматически прокручивается.</span><span class="sxs-lookup"><span data-stu-id="d05b4-127">When output exceeds the size of the balloon, the former text is automatically scrolled.</span></span> <span data-ttu-id="d05b4-128">Если не задано, весь текст, входящий в оператор [**говорите**](speak-method.md) или « [**подумать**](think-method.md) », отображается одновременно.</span><span class="sxs-lookup"><span data-stu-id="d05b4-128">When not set, all text included in a [**Speak**](speak-method.md) or [**Think**](think-method.md) statement displays at once.</span></span>

<span data-ttu-id="d05b4-129">Свойство стиля всплывающего окна можно задать, даже если пользователь отключил отображение всплывающего окна с помощью вкладки свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d05b4-129">The Balloon's style property can be set even if the user has disabled display of the Balloon using the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="d05b4-130">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="d05b4-130">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="d05b4-131">Значения по умолчанию для этих битов стиля основываются на параметрах, когда символ компилируется с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d05b4-131">The defaults for these style bits are based on their settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="d05b4-132">См. также:</span><span class="sxs-lookup"><span data-stu-id="d05b4-132">See Also</span></span>

[<span data-ttu-id="d05b4-133">**Иажентбаллунекс:: штриховка**</span><span class="sxs-lookup"><span data-stu-id="d05b4-133">**IAgentBalloonEx::GetStyle**</span></span>](iagentballoonex--getstyle.md)


 

 





