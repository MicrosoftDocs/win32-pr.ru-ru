---
description: Вы ссылаетесь на распознаватель рукописного ввода с помощью маркера ХРЕКОГНИЗЕР и контекста распознавателя в качестве ХРЕКОКОНТЕКСТ-маркера. Библиотека динамической компоновки (DLL) распознавателя может реализовывать распознаватели для нескольких языков.
ms.assetid: 23002d02-cf8f-489b-a50f-4a18ac091825
title: ХРЕКОГНИЗЕР и ХРЕКОКОНТЕКСТ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12af1bb5569a22a612f0a3ed667a55aac81da2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711153"
---
# <a name="hrecognizer-and-hrecocontext"></a><span data-ttu-id="c37b0-103">ХРЕКОГНИЗЕР и ХРЕКОКОНТЕКСТ</span><span class="sxs-lookup"><span data-stu-id="c37b0-103">HRECOGNIZER and HRECOCONTEXT</span></span>

<span data-ttu-id="c37b0-104">Вы ссылаетесь на распознаватель рукописного ввода с помощью маркера [хрекогнизер](hrecognizer-handle.md) и контекста распознавателя в качестве [хрекоконтекст](hrecocontext-handle.md) -маркера.</span><span class="sxs-lookup"><span data-stu-id="c37b0-104">You reference an ink recognizer with an [HRECOGNIZER](hrecognizer-handle.md) handle and a recognizer context as an [HRECOCONTEXT](hrecocontext-handle.md) handle.</span></span>

<span data-ttu-id="c37b0-105">Библиотека динамической компоновки (DLL) распознавателя может реализовывать распознаватели для нескольких языков.</span><span class="sxs-lookup"><span data-stu-id="c37b0-105">A recognizer dynamic-link library (DLL) can implement recognizers for more than one language.</span></span> <span data-ttu-id="c37b0-106">В этом случае каждый язык выбирается идентификатором CLSID, который передается при создании объекта [**иинкрекогнизер**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) в приложении.</span><span class="sxs-lookup"><span data-stu-id="c37b0-106">If so, each language is selected by a CLSID that is passed in when creating the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object in the application.</span></span> <span data-ttu-id="c37b0-107">Кроме того, Библиотека DLL распознавателя может создать несколько дескрипторов распознавателя при их загрузке, один или несколько для каждого распознаваемого языка.</span><span class="sxs-lookup"><span data-stu-id="c37b0-107">In addition, a recognizer DLL can create multiple recognizer handles when it is loaded, one or more for each language recognized.</span></span>

<span data-ttu-id="c37b0-108">Создается контекст распознавателя, который представляет событие распознавания определенного фрагмента рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="c37b0-108">A recognizer context is created to represent the event of recognizing a specific piece of ink.</span></span> <span data-ttu-id="c37b0-109">При создании контекста соответствующий обработчик объектов распознавателя передается в функцию [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) .</span><span class="sxs-lookup"><span data-stu-id="c37b0-109">When the context is created, the associated recognizer objects handle is passed to the [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) function.</span></span> <span data-ttu-id="c37b0-110">Это связывает язык с контекстом распознавателя.</span><span class="sxs-lookup"><span data-stu-id="c37b0-110">This associates the language with the recognizer context.</span></span>

<span data-ttu-id="c37b0-111">Контекст распознавателя может представлять распознавание всех рукописных данных в тексте сообщения электронной почты, рукописного ввода одного поля в приложении или одной строки текста, записанной на панели ввода Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="c37b0-111">A recognizer context may represent the recognition of all the ink in the body of an email, the ink of a single field within an application, or a single line of text written in the Tablet PC Input Panel.</span></span> <span data-ttu-id="c37b0-112">Объем рукописного ввода в одном контексте распознавания может отличаться от одного штриха к целой странице или более.</span><span class="sxs-lookup"><span data-stu-id="c37b0-112">The volume of ink in a single recognizer context may vary from a single stroke to a whole page or more.</span></span>

<span data-ttu-id="c37b0-113">Контекст распознавателя определяется параметрами:</span><span class="sxs-lookup"><span data-stu-id="c37b0-113">The recognizer context is defined by the settings of:</span></span>

-   <span data-ttu-id="c37b0-114">Руководством по распознаванию.</span><span class="sxs-lookup"><span data-stu-id="c37b0-114">The recognition guide.</span></span>
-   <span data-ttu-id="c37b0-115">Любой фактоидс.</span><span class="sxs-lookup"><span data-stu-id="c37b0-115">Any factoids.</span></span>
-   <span data-ttu-id="c37b0-116">Любые флаги.</span><span class="sxs-lookup"><span data-stu-id="c37b0-116">Any flags.</span></span>
-   <span data-ttu-id="c37b0-117">Контекст текста.</span><span class="sxs-lookup"><span data-stu-id="c37b0-117">The text context.</span></span>
-   <span data-ttu-id="c37b0-118">Любой список слов.</span><span class="sxs-lookup"><span data-stu-id="c37b0-118">Any word list.</span></span>
-   <span data-ttu-id="c37b0-119">Режим автозаполнения символов.</span><span class="sxs-lookup"><span data-stu-id="c37b0-119">The character Autocomplete mode.</span></span>

<span data-ttu-id="c37b0-120">Маркер для контекста распознавателя передается всем функциям, использующим эти параметры.</span><span class="sxs-lookup"><span data-stu-id="c37b0-120">The handle for the recognizer context is passed to all functions that use these settings.</span></span> <span data-ttu-id="c37b0-121">Изменение параметра изменяет контекст распознавателя.</span><span class="sxs-lookup"><span data-stu-id="c37b0-121">Changing a setting changes the recognizer context.</span></span>

<span data-ttu-id="c37b0-122">Приложение может использовать несколько контекстов для распознавания рукописного ввода из разных частей экрана.</span><span class="sxs-lookup"><span data-stu-id="c37b0-122">The application may use several contexts to recognize ink from different parts of the screen.</span></span> <span data-ttu-id="c37b0-123">Отдельный контекст может распознать несколько строк текста.</span><span class="sxs-lookup"><span data-stu-id="c37b0-123">An individual context can recognize multiple lines of text.</span></span> <span data-ttu-id="c37b0-124">Однако отдельный контекст не может обрабатывать два абзаца параллельно, например несколько столбцов в газетной статье.</span><span class="sxs-lookup"><span data-stu-id="c37b0-124">However, an individual context cannot process two paragraphs written side by side, such as multiple columns in a newspaper article.</span></span>

<span data-ttu-id="c37b0-125">Чтобы распознать новый рукописный ввод, создайте новый контекст.</span><span class="sxs-lookup"><span data-stu-id="c37b0-125">To recognize new ink, create a new context.</span></span> <span data-ttu-id="c37b0-126">В качестве альтернативы можно использовать функцию [**клонеконтекст**](/windows/desktop/api/recapis/nf-recapis-clonecontext) для создания копии контекста, не имеющего рукописных данных и результатов, или функции [**ресетконтекст**](/windows/desktop/api/recapis/nf-recapis-resetcontext) для очистки контекста рукописного ввода и результатов.</span><span class="sxs-lookup"><span data-stu-id="c37b0-126">As an alternative, use the [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) function to make a copy of a context that does not have the ink and results, or the [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) function to clear a context of its ink and results.</span></span> <span data-ttu-id="c37b0-127">С помощью этих подходов приложение рукописного ввода может повторно использовать контекст.</span><span class="sxs-lookup"><span data-stu-id="c37b0-127">With these approaches, an ink application can reuse a context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c37b0-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c37b0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c37b0-129">**Функция Сетгуиде**</span><span class="sxs-lookup"><span data-stu-id="c37b0-129">**SetGuide Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setguide)
</dt> <dt>

[<span data-ttu-id="c37b0-130">**Функция onguide**</span><span class="sxs-lookup"><span data-stu-id="c37b0-130">**GetGuide Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getguide)
</dt> <dt>

[<span data-ttu-id="c37b0-131">**Функция Сетфактоид**</span><span class="sxs-lookup"><span data-stu-id="c37b0-131">**SetFactoid Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setfactoid)
</dt> <dt>

[<span data-ttu-id="c37b0-132">**Функция Сетфлагс**</span><span class="sxs-lookup"><span data-stu-id="c37b0-132">**SetFlags Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setflags)
</dt> <dt>

[<span data-ttu-id="c37b0-133">**Функция Сетенабледуникодеранжес**</span><span class="sxs-lookup"><span data-stu-id="c37b0-133">**SetEnabledUnicodeRanges Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)
</dt> <dt>

[<span data-ttu-id="c37b0-134">**Функция Жетенабледуникодеранжес**</span><span class="sxs-lookup"><span data-stu-id="c37b0-134">**GetEnabledUnicodeRanges Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)
</dt> <dt>

[<span data-ttu-id="c37b0-135">**Функция Сеткакмоде**</span><span class="sxs-lookup"><span data-stu-id="c37b0-135">**SetCACMode Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setcacmode)
</dt> <dt>

[<span data-ttu-id="c37b0-136">**Функция Сеттекстконтекст**</span><span class="sxs-lookup"><span data-stu-id="c37b0-136">**SetTextContext Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-settextcontext)
</dt> <dt>

[<span data-ttu-id="c37b0-137">**Функция Сетвордлист**</span><span class="sxs-lookup"><span data-stu-id="c37b0-137">**SetWordList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 



