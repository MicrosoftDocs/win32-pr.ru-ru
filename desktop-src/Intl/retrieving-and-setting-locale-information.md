---
description: Извлечение и установка сведений о языковых стандартах
ms.assetid: 7675f826-76be-4361-a82c-9573040a7e72
title: Извлечение и установка сведений о языковых стандартах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f9faa8749073016862587330776f32e65749b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682622"
---
# <a name="retrieving-and-setting-locale-information"></a><span data-ttu-id="b8b05-103">Извлечение и установка сведений о языковых стандартах</span><span class="sxs-lookup"><span data-stu-id="b8b05-103">Retrieving and Setting Locale Information</span></span>

<span data-ttu-id="b8b05-104">Приложение должно иметь возможность извлекать и задавать конкретные сведения о доступных языковых [стандартах и языках](locales-and-languages.md).</span><span class="sxs-lookup"><span data-stu-id="b8b05-104">The application must be able to retrieve and set specific information about available [locales and languages](locales-and-languages.md).</span></span> <span data-ttu-id="b8b05-105">Каждый элемент сведений о языковых стандартах, например название определенного дня недели или символ, используемый в качестве десятичного разделителя, имеет соответствующую константу.</span><span class="sxs-lookup"><span data-stu-id="b8b05-105">Each element of locale information, such as the name of a particular day of the week or the character used as a decimal separator, has a corresponding constant.</span></span> <span data-ttu-id="b8b05-106">Доступные константы определяются в [константах сведений о языковых стандартах](locale-information-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b8b05-106">The available constants are defined in [Locale Information Constants](locale-information-constants.md).</span></span>

<span data-ttu-id="b8b05-107">Приложение всегда хранит сведения о языковых стандартах и управляет ими в виде строки, завершающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="b8b05-107">Your application always stores and manipulates locale information as a null-terminated string.</span></span> <span data-ttu-id="b8b05-108">Двоичные данные не допускаются, и любые числовые значения должны быть указаны как текст.</span><span class="sxs-lookup"><span data-stu-id="b8b05-108">No binary data is allowed, and any numeric values must be specified as text.</span></span> <span data-ttu-id="b8b05-109">Каждый тип данных имеет определенный формат.</span><span class="sxs-lookup"><span data-stu-id="b8b05-109">Each type of information has a particular format.</span></span> <span data-ttu-id="b8b05-110">Кроме того, несколько типов связаны друг с другом, так что изменение одного типа также изменяет значение другого типа.</span><span class="sxs-lookup"><span data-stu-id="b8b05-110">Also, several types are linked together so that changing one type changes the value of the other type as well.</span></span>

<span data-ttu-id="b8b05-111">Чтобы получить сведения о языковых стандартах, приложение вызывает [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) или [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) с константой, соответствующей требуемой информации.</span><span class="sxs-lookup"><span data-stu-id="b8b05-111">To retrieve locale information, the application calls [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) with the constant that corresponds to the required information.</span></span> <span data-ttu-id="b8b05-112">Приложение может вызвать [**сетлокалеинфо**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) , чтобы задать элемент сведений о языковых стандартах.</span><span class="sxs-lookup"><span data-stu-id="b8b05-112">The application can call [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) to set an item of locale information.</span></span>

> [!Note]  
> <span data-ttu-id="b8b05-113">Хотя [идентификатор локали](locale-identifiers.md) может поддерживаться, он недоступен для использования приложением, если также не установлен соответствующий языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="b8b05-113">Although a [locale identifier](locale-identifiers.md) might be supported, it is not available for use by an application unless the corresponding locale is also installed.</span></span>

 

<span data-ttu-id="b8b05-114">Так как большинство констант сведений о языковых стандартах являются взаимоисключающими, в каждый момент времени может обрабатываться только один тип информации.</span><span class="sxs-lookup"><span data-stu-id="b8b05-114">Since most locale information constants are mutually exclusive, only one type of information can be handled at a time.</span></span> <span data-ttu-id="b8b05-115">Исключениями из этого правила являются [языковой стандарт. \_ используйте параметр \_ CP \_ ACP](locale-use-cp-acp.md), [ \_ \_ номер возврата языкового стандарта](locale-return-constants.md)и [языковой стандарт \_ наусероверриде](locale-nouseroverride.md), который можно сочетать с другими константами с помощью двоичного файла или.</span><span class="sxs-lookup"><span data-stu-id="b8b05-115">The exceptions to this rule are [LOCALE\_USE\_CP\_ACP](locale-use-cp-acp.md), [LOCALE\_RETURN\_NUMBER](locale-return-constants.md), and [LOCALE\_NOUSEROVERRIDE](locale-nouseroverride.md), which can be combined with other constants using a binary OR.</span></span>

> [!Caution]  
> <span data-ttu-id="b8b05-116">Использовать ЯЗЫКовой стандарт \_ наусероверриде настоятельно не рекомендуется, так как он отключает предпочтения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b8b05-116">Use of LOCALE\_NOUSEROVERRIDE is strongly discouraged as it disables user preferences.</span></span>

 

<span data-ttu-id="b8b05-117">Как и в ряде приложений, например Microsoft Active Directory, приложение может поддерживать свои строки в базе данных, поддерживающей сортировку.</span><span class="sxs-lookup"><span data-stu-id="b8b05-117">Like a number of applications, for example Microsoft Active Directory, your application can maintain its strings in a sortable database.</span></span> <span data-ttu-id="b8b05-118">Дополнительные сведения см. [в разделе Обработка сортировки в приложениях](handling-sorting-in-your-applications.md).</span><span class="sxs-lookup"><span data-stu-id="b8b05-118">For more information, see [Handling Sorting in Your Applications](handling-sorting-in-your-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8b05-119">См. также</span><span class="sxs-lookup"><span data-stu-id="b8b05-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8b05-120">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="b8b05-120">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="b8b05-121">Константы сведений о языковых стандартах</span><span class="sxs-lookup"><span data-stu-id="b8b05-121">Locale Information Constants</span></span>](locale-information-constants.md)
</dt> <dt>

[<span data-ttu-id="b8b05-122">Обработка сортировки в приложениях</span><span class="sxs-lookup"><span data-stu-id="b8b05-122">Handling Sorting in Your Applications</span></span>](handling-sorting-in-your-applications.md)
</dt> <dt>

[<span data-ttu-id="b8b05-123">Работа с пользовательскими языками</span><span class="sxs-lookup"><span data-stu-id="b8b05-123">Working with Custom Locales</span></span>](working-with-custom-locales.md)
</dt> </dl>

 

 



