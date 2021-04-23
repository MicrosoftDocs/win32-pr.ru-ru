---
description: Термин &\# 0034; language&\# 0034; указывает коллекцию свойств, используемых при взаимодействии и написании сообщений.
ms.assetid: 8214c00d-4ec6-4597-8088-7819a160f0dc
title: Языковые стандарты и языки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2c0d0fa41b9186b2135d9497d52de24577bbae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683004"
---
# <a name="locales-and-languages"></a><span data-ttu-id="ed296-103">Языковые стандарты и языки</span><span class="sxs-lookup"><span data-stu-id="ed296-103">Locales and Languages</span></span>

<span data-ttu-id="ed296-104">Термин "язык" обозначает коллекцию свойств, используемых для речевого и записанного обмена данными.</span><span class="sxs-lookup"><span data-stu-id="ed296-104">The term "language" indicates a collection of properties used in spoken and written communication.</span></span> <span data-ttu-id="ed296-105">Каждый язык имеет название языка и идентификатор языка, который указывает на конкретную [кодовую страницу](code-pages.md) (ANSI, DOS, Macintosh), используемую для представления [географического расположения](table-of-geographical-locations.md) языка в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="ed296-105">Each language has a language name and a language identifier that indicate the particular [code page](code-pages.md) (ANSI, DOS, Macintosh) used to represent the [geographical location](table-of-geographical-locations.md) for the language on the operating system.</span></span> <span data-ttu-id="ed296-106">Нейтральный язык обозначается именем, например en, для английского языка.</span><span class="sxs-lookup"><span data-stu-id="ed296-106">A neutral language is indicated by a name such as "en" for English.</span></span> <span data-ttu-id="ed296-107">Более географически конкретный язык может быть обозначен именем, включающим как региональные стандарты, так и сведения о стране или регионе.</span><span class="sxs-lookup"><span data-stu-id="ed296-107">A more geographically specific language can be indicated by a name that includes both locale and country/region information.</span></span> <span data-ttu-id="ed296-108">Например, языковой стандарт Английский (США) имеет название «en-US».</span><span class="sxs-lookup"><span data-stu-id="ed296-108">For example, the locale English (United States) has the language name "en-US".</span></span>

<span data-ttu-id="ed296-109">"Языковой стандарт" — это коллекция данных о предпочтениях пользователей, связанных с языком, представленная в виде списка значений.</span><span class="sxs-lookup"><span data-stu-id="ed296-109">A "locale" is a collection of language-related user preference information represented as a list of values.</span></span> <span data-ttu-id="ed296-110">Windows XP поддерживает более 150 языковых стандартов, а Windows Vista поддерживает около 200.</span><span class="sxs-lookup"><span data-stu-id="ed296-110">Windows XP supports more than 150 locales, and Windows Vista supports about 200.</span></span> <span data-ttu-id="ed296-111">Каждый языковой стандарт определяется языком и порядком сортировки и содержит как имя локали, так и идентификатор локали.</span><span class="sxs-lookup"><span data-stu-id="ed296-111">Each locale is defined by a language and a sort order, and has both a locale name and a locale identifier.</span></span> <span data-ttu-id="ed296-112">Примером имени локали для немецкого языка (Германия) является «de-DE \_ телефония».</span><span class="sxs-lookup"><span data-stu-id="ed296-112">An example of a locale name for German (Germany) is "de-DE\_phonebook".</span></span>

<span data-ttu-id="ed296-113">Каждая операционная система имеет по крайней мере один установленный языковой стандарт и часто имеет множество языков, из которых пользователь может выбрать.</span><span class="sxs-lookup"><span data-stu-id="ed296-113">Each operating system has at least one installed locale and often has many locales from which the user can select.</span></span> <span data-ttu-id="ed296-114">С каждым языковым стандартом связаны различные сведения, отличные от его имени и идентификатора.</span><span class="sxs-lookup"><span data-stu-id="ed296-114">Each locale has a variety of information associated with it, other than its name and identifier.</span></span> <span data-ttu-id="ed296-115">Типы сведений о языковых стандартах описаны в разделе [константы сведений о языке](locale-information-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ed296-115">Locale information types are described in [Locale Information Constants](locale-information-constants.md).</span></span>

<span data-ttu-id="ed296-116">Операционная система назначает языковой стандарт для каждого потока, первоначально присваивая параметру "системный язык по умолчанию", определяемый [ \_ \_ по умолчанию системой национальной настройки](locale-system-default.md).</span><span class="sxs-lookup"><span data-stu-id="ed296-116">The operating system assigns a locale to each thread, initially assigning the "system default locale," defined by [LOCALE\_SYSTEM\_DEFAULT](locale-system-default.md).</span></span> <span data-ttu-id="ed296-117">Этот языковой стандарт задается при установке операционной системы или при его выборе пользователем с помощью языковых и региональных параметров панели управления.</span><span class="sxs-lookup"><span data-stu-id="ed296-117">This locale is set when the operating system is installed or when the user selects it using the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="ed296-118">При выполнении потока в процессе, принадлежащем пользователю, операционная система назначает потоку "язык по умолчанию для пользователя".</span><span class="sxs-lookup"><span data-stu-id="ed296-118">When running a thread in a process belonging to the user, the operating system assigns the "user default locale" to the thread.</span></span> <span data-ttu-id="ed296-119">Этот языковой стандарт определяется [пользователем языкового стандарта \_ \_ по умолчанию](locale-user-default.md).</span><span class="sxs-lookup"><span data-stu-id="ed296-119">This locale is defined by [LOCALE\_USER\_DEFAULT](locale-user-default.md).</span></span> <span data-ttu-id="ed296-120">Приложение может переопределить значение по умолчанию с помощью функции [**сетсреадлокале**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) , чтобы явно задать языковой стандарт для потока.</span><span class="sxs-lookup"><span data-stu-id="ed296-120">An application can override either default by using the [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) function to explicitly set the locale for a thread.</span></span>

<span data-ttu-id="ed296-121">Для реализации языка требуется соответствующий языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="ed296-121">Implementation of a language requires a corresponding locale.</span></span> <span data-ttu-id="ed296-122">Операционная система реализует нейтральный язык, выбирая данные для языкового стандарта, связанного с определенной версией языка (обычно это наиболее распространенный языковой стандарт).</span><span class="sxs-lookup"><span data-stu-id="ed296-122">The operating system implements a neutral language by selecting the data for the locale associated with a specific version of the language, usually the most widespread locale.</span></span>

<span data-ttu-id="ed296-123">Начиная с Windows Vista, определенный язык может соответствовать дополнительному языковому стандарту, который является типом пользовательского языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="ed296-123">Starting with Windows Vista, it is possible for a particular language to correspond to a supplemental locale, which is a type of custom locale.</span></span> <span data-ttu-id="ed296-124">Так как дополнительные языковые стандарты имеют один идентификатор локали, приложения должны работать с этими языками и соответствующими языками по имени, а не по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="ed296-124">Since supplemental locales all share a single locale identifier, your applications should handle these locales and the corresponding languages by name instead of by identifier.</span></span>

<span data-ttu-id="ed296-125">Понятия языка тесно связаны с основными понятиями языкового стандарта, но эти два термина не взаимозаменяемы.</span><span class="sxs-lookup"><span data-stu-id="ed296-125">Language concepts are closely related to locale concepts, but the two terms are not interchangeable.</span></span> <span data-ttu-id="ed296-126">Как правило, функции, связанные с [многоязычным пользовательским интерфейсом](multilingual-user-interface.md) , работают с языками, а функции многоязыковой поддержки — по языкам.</span><span class="sxs-lookup"><span data-stu-id="ed296-126">As a general rule, functions related to the [Multilingual User Interface](multilingual-user-interface.md) deal with languages, while the NLS functions act upon locales.</span></span>

<span data-ttu-id="ed296-127">В этом разделе рассматриваются следующие темы.</span><span class="sxs-lookup"><span data-stu-id="ed296-127">The following topics are covered in this section:</span></span>

-   [<span data-ttu-id="ed296-128">Пользовательские языковые стандарты</span><span class="sxs-lookup"><span data-stu-id="ed296-128">Custom Locales</span></span>](custom-locales.md)
-   [<span data-ttu-id="ed296-129">Идентификаторы языка</span><span class="sxs-lookup"><span data-stu-id="ed296-129">Language Identifiers</span></span>](language-identifiers.md)
-   [<span data-ttu-id="ed296-130">Имена языков</span><span class="sxs-lookup"><span data-stu-id="ed296-130">Language Names</span></span>](language-names.md)
-   [<span data-ttu-id="ed296-131">Идентификаторы языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="ed296-131">Locale Identifiers</span></span>](locale-identifiers.md)
-   [<span data-ttu-id="ed296-132">Имена языковых стандартов</span><span class="sxs-lookup"><span data-stu-id="ed296-132">Locale Names</span></span>](locale-names.md)
-   [<span data-ttu-id="ed296-133">Псевдо-языковые стандарты</span><span class="sxs-lookup"><span data-stu-id="ed296-133">Pseudo-Locales</span></span>](pseudo-locales.md)

## <a name="related-topics"></a><span data-ttu-id="ed296-134">См. также</span><span class="sxs-lookup"><span data-stu-id="ed296-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed296-135">Сведения о поддержке национальных языков</span><span class="sxs-lookup"><span data-stu-id="ed296-135">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="ed296-136">Кодовые страницы</span><span class="sxs-lookup"><span data-stu-id="ed296-136">Code Pages</span></span>](code-pages.md)
</dt> <dt>

[<span data-ttu-id="ed296-137">Константы сведений о языковых стандартах</span><span class="sxs-lookup"><span data-stu-id="ed296-137">Locale Information Constants</span></span>](locale-information-constants.md)
</dt> <dt>

[<span data-ttu-id="ed296-138">Многоязыковой интерфейс пользователя</span><span class="sxs-lookup"><span data-stu-id="ed296-138">Multilingual User Interface</span></span>](multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="ed296-139">Таблица геолокаций</span><span class="sxs-lookup"><span data-stu-id="ed296-139">Table of Geographical Locations</span></span>](table-of-geographical-locations.md)
</dt> <dt>

[<span data-ttu-id="ed296-140">Управление языком пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="ed296-140">User Interface Language Management</span></span>](user-interface-language-management.md)
</dt> <dt>

[<span data-ttu-id="ed296-141">**сетсреадлокале**</span><span class="sxs-lookup"><span data-stu-id="ed296-141">**SetThreadLocale**</span></span>](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)
</dt> </dl>

 

 



