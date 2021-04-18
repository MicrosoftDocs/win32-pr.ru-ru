---
description: Все распознавание для элементов управления с поддержкой рукописного ввода осуществляется через объект Рекогнизерконтекст. Интерфейсы API технологии Tablet PC позволяют задать свойство фактоид объекта Рекогнизерконтекст.
ms.assetid: 453993a7-f055-4d84-870c-256d1ec17731
title: Настройка контекста для элементов управления Ink-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6776978834f030353a84c04f03e5ecf05ba060cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348625"
---
# <a name="setting-context-for-ink-enabled-controls"></a><span data-ttu-id="da491-104">Настройка контекста для элементов управления Ink-Enabled</span><span class="sxs-lookup"><span data-stu-id="da491-104">Setting Context for Ink-Enabled Controls</span></span>

<span data-ttu-id="da491-105">Все распознавание для элементов управления с поддержкой рукописного ввода осуществляется через объект [**рекогнизерконтекст**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="da491-105">All recognition for ink-enabled controls occurs through a [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span> <span data-ttu-id="da491-106">Интерфейсы API технологии Tablet PC позволяют задать свойство [**фактоид**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) объекта **рекогнизерконтекст** .</span><span class="sxs-lookup"><span data-stu-id="da491-106">The Tablet PC Technology APIs enable you to set the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property on a **RecognizerContext** object.</span></span>

<span data-ttu-id="da491-107">При создании приложения с поддержкой рукописного ввода используйте свойства [**фактоид**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) и [**список слов**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) объекта [**рекогнизерконтекст**](inkrecognizercontext-class.md) для установки контекстов.</span><span class="sxs-lookup"><span data-stu-id="da491-107">If you are creating an ink-enabled application, use the [**RecognizerContext**](inkrecognizercontext-class.md) object's [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) and [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) properties to set contexts.</span></span>

<span data-ttu-id="da491-108">Можно передать строковые значения имен во входных областях, определенных в перечислении [**инпутскопе**](/windows/win32/api/inputscope/ne-inputscope-inputscope) , в свойство [**фактоид**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) , разделенное на открывающий объект (!</span><span class="sxs-lookup"><span data-stu-id="da491-108">You may pass in the string values of the names in the input scopes defined in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration to the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property, delimited with an opening (!</span></span> <span data-ttu-id="da491-109">и заключение).</span><span class="sxs-lookup"><span data-stu-id="da491-109">and a closing ).</span></span> <span data-ttu-id="da491-110">Например, чтобы задать для контекста объекта [**рекогнизерконтекст**](inkrecognizercontext-class.md) смещение к символам, используемым в URL-адресе, используйте синтаксис, показанный в следующих \# примерах на языке C:</span><span class="sxs-lookup"><span data-stu-id="da491-110">For example, to set the context for a [**RecognizerContext**](inkrecognizercontext-class.md) object to bias toward characters used in a URL, use the syntax shown in the following C\# examples:</span></span>


```C++
theRecoContext.Factoid = "(!IS_URL)";
```



> [!Note]  
> <span data-ttu-id="da491-111">Области ввода, как определено в перечислении [**инпутскопе**](/windows/win32/api/inputscope/ne-inputscope-inputscope) , заменяют фактоидс, которые были доступны в предыдущих версиях пакета SDK для Windows XP Tablet PC Edition, хотя эти фактоидс продолжат работать для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="da491-111">The input scopes as defined in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration supersede the factoids that were available in previous versions of the Windows XP Tablet PC Edition SDK, although these factoids will continue to work in order to provide backward compatibility.</span></span>

 

<span data-ttu-id="da491-112">В следующем \# примере на языке C задается свойство [**фактоид**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) для почтовых индексов:</span><span class="sxs-lookup"><span data-stu-id="da491-112">The following C\# example sets the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property for postal codes:</span></span>


```C++
theRecognizerContext.Factoid = "(!IS_ADDRESS_POSTALCODE)";
```



<span data-ttu-id="da491-113">Вы можете комбинировать области ввода, используя синтаксис регулярных выражений для рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="da491-113">You can combine input scopes by using the handwriting regular expression syntax.</span></span> <span data-ttu-id="da491-114">Дополнительные сведения об использовании синтаксиса регулярных выражений см. [в разделе Пользовательские области ввода с регулярными выражениями](custom-input-scopes-with-regular-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="da491-114">For more details about using regular expression syntax, see [Custom Input Scopes with Regular Expressions](custom-input-scopes-with-regular-expressions.md).</span></span>

<span data-ttu-id="da491-115">Можно установить флаги распознавания для объекта [**рекогнизерконтекст**](inkrecognizercontext-class.md) , чтобы влиять на поведение распознавателя.</span><span class="sxs-lookup"><span data-stu-id="da491-115">You can set recognition flags on the [**RecognizerContext**](inkrecognizercontext-class.md) object to affect the behavior of the recognizer.</span></span> <span data-ttu-id="da491-116">Одним из таких флагов является флаг **приведения** в [](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) перечислении инкрекогнитионмодес **рекогнизерконтекст**.</span><span class="sxs-lookup"><span data-stu-id="da491-116">One such flag is the **Coerce** flag in the [**InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) enumeration of the **RecognizerContext**.</span></span> <span data-ttu-id="da491-117">Флаг **приведение** заставляет распознаватель вернуть результат, соответствующий определению фактоид, который задан.</span><span class="sxs-lookup"><span data-stu-id="da491-117">The **Coerce** flag forces the recognizer to return a result that matches the definition of the factoid that is set.</span></span> <span data-ttu-id="da491-118">Например, если у вас есть форма, для которой пользователь должен ввести числовое количество, может быть полезно задать **значение фактоид, \_** а также задать для свойства [**рекогнитионфлагс**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) значение **приведение**.</span><span class="sxs-lookup"><span data-stu-id="da491-118">For example, if you have a form that requires the user to enter a numerical quantity, it may be useful to set the **IS\_NUMBER** factoid and also set the [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) property to **Coerce**.</span></span> <span data-ttu-id="da491-119">В этом экземпляре флаг **приведения** гарантирует, что распознаватель возвращает только числа.</span><span class="sxs-lookup"><span data-stu-id="da491-119">In that instance, the **Coerce** flag guarantees that the recognizer returns only numbers.</span></span>

<span data-ttu-id="da491-120">В следующем \# примере на языке C задается свойство [**Рекогнитионфлагс**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) для **приведения**:</span><span class="sxs-lookup"><span data-stu-id="da491-120">The following C\# example sets the [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) property to **Coerce**:</span></span>


```C++
theRecognizerContext.RecognitionFlags = RecognitionModes.Coerce;
```



<span data-ttu-id="da491-121">Однако при принятии решения о задании флага **приведение** следует соблюдать осторожность.</span><span class="sxs-lookup"><span data-stu-id="da491-121">However, use caution when deciding to set the **Coerce** flag.</span></span> <span data-ttu-id="da491-122">Флаг заставляет распознаватель соответствовать только определению фактоид.</span><span class="sxs-lookup"><span data-stu-id="da491-122">The flag forces the recognizer to match only the definition of the factoid.</span></span> <span data-ttu-id="da491-123">Например, если задать для параметра значение — \_ Телефон \_ фуллтелефоненумбер ввода и флаг **приведение** , то распознаватель возвращает результаты, точно соответствующие определению \_ только для телефонной \_ фуллтелефоненумбер входной области.</span><span class="sxs-lookup"><span data-stu-id="da491-123">For example, if you set the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope and the **Coerce** flag, the recognizer returns results that exactly match the definition of the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope only.</span></span> <span data-ttu-id="da491-124">Если пользователь записывает "911" с \_ \_ входной областью фуллтелефоненумбер телефона и установленным флагом **приведение** , распознаватель может вернуть пустую строку или случайную строку в формате (XXX) XXX-XXXX (где X — цифра).</span><span class="sxs-lookup"><span data-stu-id="da491-124">If a user writes "911" with the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope and the **Coerce** flag set, the recognizer may return either an empty string or a random string in the format of (XXX) XXX-XXXX (where X is a digit).</span></span> <span data-ttu-id="da491-125">Формат XXX не соответствует определению параметра — \_ \_ Phone фуллтелефоненумбер фактоид, хотя это допустимый номер телефона.</span><span class="sxs-lookup"><span data-stu-id="da491-125">The format of XXX does not match the definition of the IS\_TELEPHONE\_FULLTELEPHONENUMBER factoid, even though it is a valid phone number.</span></span>

<span data-ttu-id="da491-126">Список поддерживаемых форматов для каждой области ввода см. в справочнике по [**инпутскопе**](/windows/win32/api/inputscope/ne-inputscope-inputscope) .</span><span class="sxs-lookup"><span data-stu-id="da491-126">For lists of the supported formats for each input scope, see the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) reference.</span></span>

<span data-ttu-id="da491-127">Чтобы вернуть поле в значение по умолчанию для распознавателя, установите для параметра фактоид значение \_ по умолчанию, как показано в следующем примере на языке C \# :</span><span class="sxs-lookup"><span data-stu-id="da491-127">To return a field to the default setting for the recognizer, set the factoid to IS\_DEFAULT , as in the following C\# example:</span></span>


```C++
theRecgonizerContext.Factoid = "(!IS_DEFAULT)";
```



<span data-ttu-id="da491-128">Для приложений, использующих элемент управления [InkEdit](inkedit-control-reference.md) , задайте тип фактоид для элемента управления, указав:</span><span class="sxs-lookup"><span data-stu-id="da491-128">For applications that use the [InkEdit](inkedit-control-reference.md) control, set the factoid type for the control by specifying:</span></span>


```C++
InkEdit1.Factoid = "(!IS_INPUTSCOPE)"
```



<span data-ttu-id="da491-129">Где `IS_INPUTSCOPE` — имя области ввода, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="da491-129">Where `IS_INPUTSCOPE` is the name of the input scope you want to apply.</span></span>

<span data-ttu-id="da491-130">Элемент управления [InkEdit](inkedit-control-reference.md) не предоставляет объект [**рекогнизерконтекст**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="da491-130">The [InkEdit](inkedit-control-reference.md) control does not expose a [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span> <span data-ttu-id="da491-131">Вы по-прежнему можете назначить контекст с помощью свойства [**фактоид**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) элемента управления InkEdit, но нельзя установить флаг **вордмоде** .</span><span class="sxs-lookup"><span data-stu-id="da491-131">You can still assign context by using the [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) property of the InkEdit control, but you cannot set the **WORDMODE** flag.</span></span>

 

 
