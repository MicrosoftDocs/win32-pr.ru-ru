---
title: Строки формата
description: Строка формата — это интерпретируемый токен, распознаваемый подсистемой NDR. Строки формата часто называются MOPs; в этой документации используется строка формата термина в пределах.
ms.assetid: 548283bd-023a-41dd-b1d0-661305d019e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563dd9e4145a7d83b2e49f180329c05c1d55155d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776964"
---
# <a name="format-strings"></a><span data-ttu-id="efbff-104">Строки формата</span><span class="sxs-lookup"><span data-stu-id="efbff-104">Format Strings</span></span>

<span data-ttu-id="efbff-105">Строка формата — это интерпретируемый токен, распознаваемый подсистемой NDR.</span><span class="sxs-lookup"><span data-stu-id="efbff-105">A format string is an interpreted token that the NDR engine understands.</span></span> <span data-ttu-id="efbff-106">Строки формата часто называются MOPs; в этой документации используется строка формата термина в пределах.</span><span class="sxs-lookup"><span data-stu-id="efbff-106">Format strings are often referred to as MOPs; this documentation uses the term format string throughout.</span></span>

<span data-ttu-id="efbff-107">Чтобы быть более точным, символ форматирования является отдельным (атомарным) интерпретируемым маркером.</span><span class="sxs-lookup"><span data-stu-id="efbff-107">To be more precise, a format character is an individual (atomic) interpretable token.</span></span> <span data-ttu-id="efbff-108">Каждый символ формата имеет размер в один байт.</span><span class="sxs-lookup"><span data-stu-id="efbff-108">Each format character is one byte in size.</span></span> <span data-ttu-id="efbff-109">Строка форматирования представляет собой последовательность символов формата или символов форматирования и числовых данных.</span><span class="sxs-lookup"><span data-stu-id="efbff-109">A format string is a sequence of format characters or format characters and numerical data.</span></span> <span data-ttu-id="efbff-110">Дескриптор термина также используется для именования общих последовательностей. Например, строка формата параметра или дескриптор параметра — это строка формата, используемая для описания параметра подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="efbff-110">The term descriptor is also used for naming common sequences; for example, a parameter format string or a parameter descriptor is a format string used to describe a parameter of a routine.</span></span>

<span data-ttu-id="efbff-111">Символы формата имеют предполагающее определенную символьные имена, такие как FC \_ длинная или FC \_ .</span><span class="sxs-lookup"><span data-stu-id="efbff-111">Format characters have suggestive symbolic names like FC\_LONG or FC\_STRUCT.</span></span> <span data-ttu-id="efbff-112">Все символы строки формата, используемые MIDL и подсистема NDR, определяются в файле Ндртипес. h.</span><span class="sxs-lookup"><span data-stu-id="efbff-112">All format string characters used by MIDL and the NDR engine are defined in the Ndrtypes.h file.</span></span>

## <a name="format-string-tables"></a><span data-ttu-id="efbff-113">Форматирование таблиц строк</span><span class="sxs-lookup"><span data-stu-id="efbff-113">Format String Tables</span></span>

<span data-ttu-id="efbff-114">Обработчик использует две первичные таблицы строк формата: таблицу строк формата процедур, **\_ \_ MIDL \_ прокформатстринг**, которая сохраняет дескрипторы процедур; и таблицу строкового формата, **\_ \_ MIDL \_ типеформатстринг**, которая хранит дескрипторы типов данных.</span><span class="sxs-lookup"><span data-stu-id="efbff-114">Two primary format string tables are used by the engine: the procedure format string table, **\_\_MIDL\_ProcFormatString**, that keeps the procedure descriptors; and the type format string table, **\_\_MIDL\_TypeFormatString**, that keeps the data type descriptors.</span></span> <span data-ttu-id="efbff-115">Компилятор создает и в основные файлы заглушки ( \* \_ c. c, \* \_ s. c, \* \_ p. c).</span><span class="sxs-lookup"><span data-stu-id="efbff-115">The compiler generates both into the main stub files (\*\_c.c, \*\_s.c, \*\_p.c).</span></span> <span data-ttu-id="efbff-116">Таблица строкового формата используется в основном для различных интерпретаторов, но она также используется для преобразования буфера независимо от режима компилятора.</span><span class="sxs-lookup"><span data-stu-id="efbff-116">The procedure format string table is used mostly by various interpreters but it is also used for the buffer conversion regardless of the compiler mode.</span></span> <span data-ttu-id="efbff-117">Таблица строкового формата используется при вызове основного механизма NDR для указания конкретных типов данных, с которыми необходимо работать.</span><span class="sxs-lookup"><span data-stu-id="efbff-117">The type format string table is used when calling the core NDR engine to indicate specific data types to be worked on.</span></span>

## <a name="format-string-notation"></a><span data-ttu-id="efbff-118">Нотация строки формата</span><span class="sxs-lookup"><span data-stu-id="efbff-118">Format String Notation</span></span>

<span data-ttu-id="efbff-119">Нотация, используемая в этом документе, соответствует стандартным рекомендациям по созданию описания программирования, а строка ( \| ) используется для обозначения альтернативных конструкций и квадратных скобок ( \[ \] ), используемых для указания необязательных элементов.</span><span class="sxs-lookup"><span data-stu-id="efbff-119">The notation used in this document follows common programming description guidelines, with a bar ( \| ) used to denote alternative constructs and square brackets ( \[ \] ) used to indicate optional elements.</span></span> <span data-ttu-id="efbff-120">Строки формата часто размещаются в стеке для удобства чтения (отчетности).</span><span class="sxs-lookup"><span data-stu-id="efbff-120">Format strings are frequently stacked up for readability (accountability).</span></span> <span data-ttu-id="efbff-121">В этом документе FC обозначает один символ формата.</span><span class="sxs-lookup"><span data-stu-id="efbff-121">Throughout this document, FC denotes a single format character.</span></span> <span data-ttu-id="efbff-122">Символы формата представляются во всех ПРОПИСных буквах с использованием их фактических символьных имен.</span><span class="sxs-lookup"><span data-stu-id="efbff-122">Format characters are presented in all CAPS, using their actual symbolic names.</span></span> <span data-ttu-id="efbff-123">Другие произвольные поля представлены именем и размером.</span><span class="sxs-lookup"><span data-stu-id="efbff-123">Other arbitrary fields are represented by a name and a size.</span></span>

<span data-ttu-id="efbff-124">Угловые скобки ( <> ) используются для обозначения размеров дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="efbff-124">Angle brackets ( <> ) are used to denote sizes of the descriptors.</span></span> <span data-ttu-id="efbff-125">Соглашения, приведенные в следующей таблице, используются.</span><span class="sxs-lookup"><span data-stu-id="efbff-125">The conventions shown in the following table are employed.</span></span>



| <span data-ttu-id="efbff-126">Notation</span><span class="sxs-lookup"><span data-stu-id="efbff-126">Notation</span></span>     | <span data-ttu-id="efbff-127">Значение</span><span class="sxs-lookup"><span data-stu-id="efbff-127">Meaning</span></span>                                                   |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="efbff-128"><*\n*></span><span class="sxs-lookup"><span data-stu-id="efbff-128"><*n*></span></span>  | <span data-ttu-id="efbff-129">Размер дескриптора составляет n байт.</span><span class="sxs-lookup"><span data-stu-id="efbff-129">The size of descriptor is n bytes.</span></span>                        |
| <>     | <span data-ttu-id="efbff-130">Размер дескриптора меняется.</span><span class="sxs-lookup"><span data-stu-id="efbff-130">The size of descriptor varies.</span></span>                            |
| <span data-ttu-id="efbff-131">{<>}\*</span><span class="sxs-lookup"><span data-stu-id="efbff-131">{<>}\*</span></span> | <span data-ttu-id="efbff-132">Дескриптор повторяется любое количество раз (0, 1, 2...).</span><span class="sxs-lookup"><span data-stu-id="efbff-132">The descriptor is repeated any number of times (0,1,2 …).</span></span> |



 

<span data-ttu-id="efbff-133">Следующие символы формата имеют специальное значение.</span><span class="sxs-lookup"><span data-stu-id="efbff-133">The following format characters have a special meaning.</span></span>



| <span data-ttu-id="efbff-134">Знак</span><span class="sxs-lookup"><span data-stu-id="efbff-134">Character</span></span> | <span data-ttu-id="efbff-135">Значение</span><span class="sxs-lookup"><span data-stu-id="efbff-135">Meaning</span></span>                                   |
|-----------|-------------------------------------------|
| <span data-ttu-id="efbff-136">\_Завершение FC</span><span class="sxs-lookup"><span data-stu-id="efbff-136">FC\_END</span></span>   | <span data-ttu-id="efbff-137">Указывает конец некоторых строк формата.</span><span class="sxs-lookup"><span data-stu-id="efbff-137">Indicates the end of some format strings.</span></span> |
| <span data-ttu-id="efbff-138">\_Клавиатура FC</span><span class="sxs-lookup"><span data-stu-id="efbff-138">FC\_PAD</span></span>   | <span data-ttu-id="efbff-139">Неинтерпретируемый символ панели.</span><span class="sxs-lookup"><span data-stu-id="efbff-139">Uninterpreted pad character.</span></span>              |



 

 

 




