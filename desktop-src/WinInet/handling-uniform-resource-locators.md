---
title: Обработка указателей универсальных ресурсов
description: Универсальный указатель ресурсов (URL) — это компактное представление расположения и метода доступа для ресурса, расположенного в Интернете.
ms.assetid: bb59ada6-f49f-412c-a32c-4fb9495b1222
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08157738d99e78ff4d458a3bdd1b1e2e661ce538
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "104552027"
---
# <a name="handling-uniform-resource-locators"></a><span data-ttu-id="f04d1-103">Обработка указателей универсальных ресурсов</span><span class="sxs-lookup"><span data-stu-id="f04d1-103">Handling Uniform Resource Locators</span></span>

<span data-ttu-id="f04d1-104">Универсальный указатель ресурсов (URL) — это компактное представление расположения и метода доступа для ресурса, расположенного в Интернете.</span><span class="sxs-lookup"><span data-stu-id="f04d1-104">A Uniform Resource Locator (URL) is a compact representation of the location and access method for a resource located on the Internet.</span></span> <span data-ttu-id="f04d1-105">Каждый URL-адрес состоит из схемы (HTTP, HTTPS или FTP) и строки, зависящей от схемы.</span><span class="sxs-lookup"><span data-stu-id="f04d1-105">Each URL consists of a scheme (HTTP, HTTPS, or FTP) and a scheme-specific string.</span></span> <span data-ttu-id="f04d1-106">Эта строка может также содержать сочетание пути к каталогу, строки поиска или имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="f04d1-106">This string can also include a combination of a directory path, search string, or name of the resource.</span></span> <span data-ttu-id="f04d1-107">Функции WinINet предоставляют возможность создавать, объединять, разбивать и канонизировать URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="f04d1-107">The WinINet functions provide the ability to create, combine, break down, and canonicalize URLs.</span></span> <span data-ttu-id="f04d1-108">Дополнительные сведения об URL-адресах см. в [документе RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) по универсальным указателям ресурсов (URL).</span><span class="sxs-lookup"><span data-stu-id="f04d1-108">For more information on URLs, see [RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) on Uniform Resource Locators (URL).</span></span>

<span data-ttu-id="f04d1-109">Функции URL-адреса работают в режиме, ориентированном на задачи.</span><span class="sxs-lookup"><span data-stu-id="f04d1-109">The URL functions operate in a task-oriented manner.</span></span> <span data-ttu-id="f04d1-110">Содержимое и формат URL-адреса, переданного функции, не проверяются.</span><span class="sxs-lookup"><span data-stu-id="f04d1-110">The content and format of the URL that is given to the function is not verified.</span></span> <span data-ttu-id="f04d1-111">Вызывающее приложение должно следить за использованием этих функций, чтобы убедиться, что данные имеют требуемый формат.</span><span class="sxs-lookup"><span data-stu-id="f04d1-111">The calling application should track the use of these functions to ensure that the data is in the intended format.</span></span> <span data-ttu-id="f04d1-112">Например, функция [**интернетканоникализеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) преобразует символ "%" в escape-последовательность "%25", если не использует флаги.</span><span class="sxs-lookup"><span data-stu-id="f04d1-112">For example, the [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) function would convert the character "%" into the escape sequence "%25" when using no flags.</span></span> <span data-ttu-id="f04d1-113">Если в каноническом URL-адресе используется [**интернетканоникализеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) , то управляющая последовательность "%25" будет преобразована в экранированную последовательность "%2525", которая не будет работать должным образом.</span><span class="sxs-lookup"><span data-stu-id="f04d1-113">If [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) is used on the canonicalized URL, the escape sequence "%25" would be converted into the escape sequence "%2525", which would not work properly.</span></span>

-   [<span data-ttu-id="f04d1-114">Что такое канонический URL-адрес?</span><span class="sxs-lookup"><span data-stu-id="f04d1-114">What Is a Canonicalized URL?</span></span>](#what-is-a-canonicalized-url)
-   [<span data-ttu-id="f04d1-115">Использование функций WinINet для управления URL-адресами</span><span class="sxs-lookup"><span data-stu-id="f04d1-115">Using the WinINet Functions to Handle URLs</span></span>](#using-the-wininet-functions-to-handle-urls)
-   [<span data-ttu-id="f04d1-116">URL-адреса канонизацию</span><span class="sxs-lookup"><span data-stu-id="f04d1-116">Canonicalizing URLs</span></span>](#what-is-a-canonicalized-url)
-   [<span data-ttu-id="f04d1-117">Объединение базового и относительного URL-адреса</span><span class="sxs-lookup"><span data-stu-id="f04d1-117">Combining Base and Relative URLs</span></span>](#combining-base-and-relative-urls)
-   [<span data-ttu-id="f04d1-118">Взлом URL-адресов</span><span class="sxs-lookup"><span data-stu-id="f04d1-118">Cracking URLs</span></span>](#cracking-urls)
-   [<span data-ttu-id="f04d1-119">Создание URL-адресов</span><span class="sxs-lookup"><span data-stu-id="f04d1-119">Creating URLs</span></span>](#creating-urls)
-   [<span data-ttu-id="f04d1-120">Прямой доступ к URL-адресам</span><span class="sxs-lookup"><span data-stu-id="f04d1-120">Accessing URLs Directly</span></span>](#accessing-urls-directly)

## <a name="what-is-a-canonicalized-url"></a><span data-ttu-id="f04d1-121">Что такое канонический URL-адрес?</span><span class="sxs-lookup"><span data-stu-id="f04d1-121">What Is a Canonicalized URL?</span></span>

<span data-ttu-id="f04d1-122">Формат всех URL-адресов должен соответствовать принятому синтаксису и семантике для доступа к ресурсам через Интернет.</span><span class="sxs-lookup"><span data-stu-id="f04d1-122">The format of all URLs must follow the accepted syntax and semantics in order to access resources through the Internet.</span></span> <span data-ttu-id="f04d1-123">Каноническая обработка — это процесс форматирования URL-адреса для соблюдения синтаксиса и семантики.</span><span class="sxs-lookup"><span data-stu-id="f04d1-123">Canonicalization is the process of formatting a URL to follow this accepted syntax and semantics.</span></span>

<span data-ttu-id="f04d1-124">Символы, которые должны быть закодированы, включают в себя любые символы, не имеющие соответствующих графических символов в кодировке US-ASCII (шестнадцатеричная 80-FF, которые не используются в кодировке US-ASCII, а также шестнадцатеричные 00-1F и 7F, представляющие собой управляющие символы), пробелы, "%" (используемые для кодирования других символов) и ненадежные символы (<, >, ", \# , {,}, \| , \\ , ^, ~,, \[ \] и").</span><span class="sxs-lookup"><span data-stu-id="f04d1-124">Characters that must be encoded include any characters that have no corresponding graphic character in the US-ASCII coded character set (hexadecimal 80-FF, which are not used in the US-ASCII coded character set, and hexadecimal 00-1F and 7F, which are control characters), blank spaces, "%" (which is used to encode other characters), and unsafe characters (<, >, ", \#, {, }, \|, \\, ^, ~, \[, \], and ').</span></span>

## <a name="using-the-wininet-functions-to-handle-urls"></a><span data-ttu-id="f04d1-125">Использование функций WinINet для управления URL-адресами</span><span class="sxs-lookup"><span data-stu-id="f04d1-125">Using the WinINet Functions to Handle URLs</span></span>

<span data-ttu-id="f04d1-126">В следующей таблице перечислены функции URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="f04d1-126">The following table summarizes the URL functions.</span></span>



| <span data-ttu-id="f04d1-127">Функция</span><span class="sxs-lookup"><span data-stu-id="f04d1-127">Function</span></span>                                                   | <span data-ttu-id="f04d1-128">Описание</span><span class="sxs-lookup"><span data-stu-id="f04d1-128">Description</span></span>                                        |
|------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="f04d1-129">**интернетканоникализеурл**</span><span class="sxs-lookup"><span data-stu-id="f04d1-129">**InternetCanonicalizeUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) | <span data-ttu-id="f04d1-130">Каноникализес URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="f04d1-130">Canonicalizes the URL.</span></span>                             |
| [<span data-ttu-id="f04d1-131">**интернеткомбинеурл**</span><span class="sxs-lookup"><span data-stu-id="f04d1-131">**InternetCombineUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla)           | <span data-ttu-id="f04d1-132">Объединяет базовый и относительный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="f04d1-132">Combines base and relative URLs.</span></span>                   |
| [<span data-ttu-id="f04d1-133">**интернеткраккурл**</span><span class="sxs-lookup"><span data-stu-id="f04d1-133">**InternetCrackUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)               | <span data-ttu-id="f04d1-134">Выполняет синтаксический анализ строки URL-адреса в компоненты.</span><span class="sxs-lookup"><span data-stu-id="f04d1-134">Parses a URL string into components.</span></span>               |
| [<span data-ttu-id="f04d1-135">**интернеткреатеурл**</span><span class="sxs-lookup"><span data-stu-id="f04d1-135">**InternetCreateUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla)             | <span data-ttu-id="f04d1-136">Создает строку URL-адреса из компонентов.</span><span class="sxs-lookup"><span data-stu-id="f04d1-136">Creates a URL string from components.</span></span>              |
| [<span data-ttu-id="f04d1-137">**интернетопенурл**</span><span class="sxs-lookup"><span data-stu-id="f04d1-137">**InternetOpenUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)                 | <span data-ttu-id="f04d1-138">Начинает получение ресурса FTP, HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f04d1-138">Begins retrieving an FTP, HTTP, or HTTPS resource.</span></span> |



 

## <a name="canonicalizing-urls"></a><span data-ttu-id="f04d1-139">URL-адреса канонизацию</span><span class="sxs-lookup"><span data-stu-id="f04d1-139">Canonicalizing URLs</span></span>

<span data-ttu-id="f04d1-140">Канонизацию URL-адрес — это процесс, который преобразует URL-адрес, который может содержать ненадежные символы, такие как пробелы, зарезервированные символы и т. д., в допустимый формат.</span><span class="sxs-lookup"><span data-stu-id="f04d1-140">Canonicalizing a URL is the process that converts a URL, which might contain unsafe characters such as blank spaces, reserved characters, and so on, into an accepted format.</span></span>

<span data-ttu-id="f04d1-141">Функцию [**интернетканоникализеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) можно использовать для канонизировать URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="f04d1-141">The [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) function can be used to canonicalize URLs.</span></span> <span data-ttu-id="f04d1-142">Эта функция ориентирована на задачи, поэтому приложение должно внимательно отслеживать его использование.</span><span class="sxs-lookup"><span data-stu-id="f04d1-142">This function is very task-oriented, so the application should track its use carefully.</span></span> <span data-ttu-id="f04d1-143">[**Интернетканоникализеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) не проверяет, что переданный в него URL-адрес уже каноническ и что возвращаемый им URL-адрес является допустимым.</span><span class="sxs-lookup"><span data-stu-id="f04d1-143">[**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) does not verify that the URL passed to it is already canonicalized and that the URL that it returns is valid.</span></span>

<span data-ttu-id="f04d1-144">Следующие пять флагов управляют тем, как [**интернетканоникализеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) обрабатывает конкретный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="f04d1-144">The following five flags control how [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) handles a particular URL.</span></span> <span data-ttu-id="f04d1-145">Флаги можно использовать в сочетании.</span><span class="sxs-lookup"><span data-stu-id="f04d1-145">The flags can be used in combination.</span></span> <span data-ttu-id="f04d1-146">Если флаги не используются, функция кодирует URL-адрес по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f04d1-146">If no flags are used, the function encodes the URL by default.</span></span>



| <span data-ttu-id="f04d1-147">Значение</span><span class="sxs-lookup"><span data-stu-id="f04d1-147">Value</span></span>                     | <span data-ttu-id="f04d1-148">Значение</span><span class="sxs-lookup"><span data-stu-id="f04d1-148">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f04d1-149">\_режим браузера \_ ICU</span><span class="sxs-lookup"><span data-stu-id="f04d1-149">ICU\_BROWSER\_MODE</span></span>        | <span data-ttu-id="f04d1-150">Не закодировать или декодировать символы после " \# " или "?" и не удалять конечные пробелы после "?".</span><span class="sxs-lookup"><span data-stu-id="f04d1-150">Do not encode or decode characters after "\#" or "?", and do not remove trailing white space after "?".</span></span> <span data-ttu-id="f04d1-151">Если это значение не указано, то кодируется весь URL-адрес, а конечные пробелы удаляются.</span><span class="sxs-lookup"><span data-stu-id="f04d1-151">If this value is not specified, the entire URL is encoded, and trailing white space is removed.</span></span> |
| <span data-ttu-id="f04d1-152">декодирование ICU \_</span><span class="sxs-lookup"><span data-stu-id="f04d1-152">ICU\_DECODE</span></span>               | <span data-ttu-id="f04d1-153">Преобразование всех последовательностей% XX в символы, включая escape-последовательности, перед синтаксическим анализом URL.</span><span class="sxs-lookup"><span data-stu-id="f04d1-153">Convert all %XX sequences to characters, including escape sequences, before the URL is parsed.</span></span>                                                                                                          |
| <span data-ttu-id="f04d1-154">ICU \_ \_ только символы \_ кодирования</span><span class="sxs-lookup"><span data-stu-id="f04d1-154">ICU\_ENCODE\_SPACES\_ONLY</span></span> | <span data-ttu-id="f04d1-155">Закодировать только пробелы.</span><span class="sxs-lookup"><span data-stu-id="f04d1-155">Encode spaces only.</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="f04d1-156">ICU \_ без \_ кодирования</span><span class="sxs-lookup"><span data-stu-id="f04d1-156">ICU\_NO\_ENCODE</span></span>           | <span data-ttu-id="f04d1-157">Не преобразуйте ненадежные символы в escape-последовательности.</span><span class="sxs-lookup"><span data-stu-id="f04d1-157">Do not convert unsafe characters to escape sequences.</span></span>                                                                                                                                                   |
| <span data-ttu-id="f04d1-158">ICU \_ нет \_ мета</span><span class="sxs-lookup"><span data-stu-id="f04d1-158">ICU\_NO\_META</span></span>             | <span data-ttu-id="f04d1-159">Не удаляйте в URL-адресе метаданные (например, "." и "..").</span><span class="sxs-lookup"><span data-stu-id="f04d1-159">Do not remove meta sequences (such as "." and "..") from the URL.</span></span>                                                                                                                                       |



 

<span data-ttu-id="f04d1-160">\_Флаг декодирования ICU должен использоваться только для канонических URL-адресов, так как предполагается, что все последовательности% XX являются управляющими кодами Escape-кодов и преобразуют их в символы, указанные в коде.</span><span class="sxs-lookup"><span data-stu-id="f04d1-160">The ICU\_DECODE flag should be used only on canonicalized URLs, because it assumes that all %XX sequences are escape codes and converts them into the characters indicated by the code.</span></span> <span data-ttu-id="f04d1-161">Если в URL-адресе есть символ "%", который не является частью Escape-кода, ICU \_ декодирование все еще обрабатывает его как один.</span><span class="sxs-lookup"><span data-stu-id="f04d1-161">If the URL has a "%" symbol in it that is not part of an escape code, ICU\_DECODE still treats it as one.</span></span> <span data-ttu-id="f04d1-162">Эта характеристика может привести к тому, что [**интернетканоникализеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) создаст недопустимый URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="f04d1-162">This characteristic might cause [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) to create an invalid URL.</span></span>

<span data-ttu-id="f04d1-163">Чтобы использовать [**интернетканоникализеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) для возврата полностью декодированного URL-адреса, \_ \_ \_ необходимо указать флаги декодирования ICU и ICU.</span><span class="sxs-lookup"><span data-stu-id="f04d1-163">To use [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) to return a completely decoded URL, the ICU\_DECODE and ICU\_NO\_ENCODE flags must be specified.</span></span> <span data-ttu-id="f04d1-164">Эта программа установки предполагает, что URL-адрес, передаваемый в [**интернетканоникализеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) , был ранее канонический.</span><span class="sxs-lookup"><span data-stu-id="f04d1-164">This setup assumes that the URL being passed to [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) has been previously canonicalized.</span></span>

## <a name="combining-base-and-relative-urls"></a><span data-ttu-id="f04d1-165">Объединение базового и относительного URL-адреса</span><span class="sxs-lookup"><span data-stu-id="f04d1-165">Combining Base and Relative URLs</span></span>

<span data-ttu-id="f04d1-166">Относительный URL-адрес — это компактное представление расположения ресурса относительно абсолютного базового URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="f04d1-166">A relative URL is a compact representation of the location of a resource relative to an absolute base URL.</span></span> <span data-ttu-id="f04d1-167">Базовый URL-адрес должен быть известен анализатору и обычно включает схему, сетевое расположение и части пути URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="f04d1-167">The base URL must be known to the parser and usually includes the scheme, network location, and parts of the URL path.</span></span> <span data-ttu-id="f04d1-168">Приложение может вызвать [**интернеткомбинеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) , чтобы объединить относительный URL-адрес с его базовым URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="f04d1-168">An application can call [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) to combine the relative URL with its base URL.</span></span> <span data-ttu-id="f04d1-169">[**Интернеткомбинеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) также каноникализес результирующий URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="f04d1-169">[**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) also canonicalizes the resultant URL.</span></span>

## <a name="cracking-urls"></a><span data-ttu-id="f04d1-170">Взлом URL-адресов</span><span class="sxs-lookup"><span data-stu-id="f04d1-170">Cracking URLs</span></span>

<span data-ttu-id="f04d1-171">Функция [**интернеткраккурл**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) разделяет URL-адрес на части его компонентов и возвращает компоненты, указанные в структуре [**\_ компонентов URL-адреса**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , которая передается в функцию.</span><span class="sxs-lookup"><span data-stu-id="f04d1-171">The [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) function separates a URL into its component parts and returns the components indicated by the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure that is passed to the function.</span></span>

<span data-ttu-id="f04d1-172">Компоненты, составляющие структуру [**\_ компонентов URL-адреса**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , — это номер схемы, имя узла, номер порта, имя пользователя, пароль, путь URL-адреса и дополнительные сведения (например, параметры поиска).</span><span class="sxs-lookup"><span data-stu-id="f04d1-172">The components that make up the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure are the scheme number, host name, port number, user name, password, URL path, and additional information (such as search parameters).</span></span> <span data-ttu-id="f04d1-173">Каждый компонент, за исключением схемы и номеров портов, имеет строковый элемент, содержащий сведения, и элемент, содержащий длину строкового элемента.</span><span class="sxs-lookup"><span data-stu-id="f04d1-173">Each component, except the scheme and port numbers, has a string member that holds the information, and a member that holds the length of the string member.</span></span> <span data-ttu-id="f04d1-174">В схеме и номерах портов имеется только элемент, в котором хранится соответствующее значение. они оба возвращаются для всех успешных вызовов [**интернеткраккурл**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla).</span><span class="sxs-lookup"><span data-stu-id="f04d1-174">The scheme and port numbers have only a member that stores the corresponding value; they are both returned on all successful calls to [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla).</span></span>

<span data-ttu-id="f04d1-175">Чтобы получить значение конкретного компонента в структуре [**\_ компонентов URL-адреса**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , элементу, в котором хранится длина строки этого компонента, должно быть присвоено ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f04d1-175">To get the value of a particular component in the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure, the member that stores the string length of that component must be set to a nonzero value.</span></span> <span data-ttu-id="f04d1-176">Строковый элемент может быть либо адресом буфера, либо **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="f04d1-176">The string member can be either the address of a buffer or **NULL**.</span></span>

<span data-ttu-id="f04d1-177">Если элемент указателя содержит адрес буфера, то элемент длины строки должен содержать размер этого буфера.</span><span class="sxs-lookup"><span data-stu-id="f04d1-177">If the pointer member contains the address of a buffer, the string length member must contain the size of that buffer.</span></span> <span data-ttu-id="f04d1-178">[**Интернеткраккурл**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) возвращает сведения о компоненте в виде строки в буфере и сохраняет длину строки в члене длины строки.</span><span class="sxs-lookup"><span data-stu-id="f04d1-178">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) returns the component information as a string in the buffer and stores the string length in the string length member.</span></span>

<span data-ttu-id="f04d1-179">Если элемент указателя имеет **значение NULL**, то элементу длины строки может быть присвоено любое ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f04d1-179">If the pointer member is **NULL**, the string length member can be set to any nonzero value.</span></span> <span data-ttu-id="f04d1-180">[**Интернеткраккурл**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) хранит адрес первого символа строки URL-адреса, содержащей сведения о компоненте, и задает длину строки, равную количеству символов в оставшейся части строки URL-адреса, относящейся к компоненту.</span><span class="sxs-lookup"><span data-stu-id="f04d1-180">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) stores the address of the first character of the URL string that contains the component information and sets the string length to the number of characters in the remaining part of the URL string that pertains to the component.</span></span>

<span data-ttu-id="f04d1-181">Все члены-указатели имеют **значение NULL** с ненулевой точкой члена, соответствующей отправной точке в строке URL.</span><span class="sxs-lookup"><span data-stu-id="f04d1-181">All pointer members set to **NULL** with a nonzero length member point to the appropriate starting point in the URL string.</span></span> <span data-ttu-id="f04d1-182">Длину, хранящуюся в члене length, необходимо использовать для определения конца данных отдельного компонента.</span><span class="sxs-lookup"><span data-stu-id="f04d1-182">The length stored in the length member must be used to determine the end of the individual component's information.</span></span>

<span data-ttu-id="f04d1-183">Чтобы правильно инициализировать структуру [**\_ компонентов URL-адресов**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , элементу **двструктсизе** должен быть присвоен размер структуры [**\_ компонентов URL-адреса**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) в байтах.</span><span class="sxs-lookup"><span data-stu-id="f04d1-183">To finish initializing the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure properly, the **dwStructSize** member must be set to the size of the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure, in bytes.</span></span>

<span data-ttu-id="f04d1-184">Следующий пример возвращает компоненты URL-адреса в поле ввода, IDC \_ PreOpen1 и возвращает компоненты в список, IDC \_ преопенлист.</span><span class="sxs-lookup"><span data-stu-id="f04d1-184">The following example returns the components of the URL in the edit box, IDC\_PreOpen1, and returns the components to the list box, IDC\_PreOpenList.</span></span> <span data-ttu-id="f04d1-185">Чтобы отобразить только сведения об отдельном компоненте, эта функция копирует символ непосредственно после сведений о компоненте в строке и временно заменяет его **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="f04d1-185">To display only the information for an individual component, this function copies the character immediately after the component's information in the string and temporarily replaces it with a **NULL**.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>
#include <wininet.h>
#include <stdlib.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  CRACKER_BUFFER_SIZE           MAX_PATH

// For sample source code implementing the InternetErrorOut( ) 
// function referenced below, see the "Handling Errors" topic  
// under "Using WinInet"
extern BOOL WINAPI InternetErrorOut( HWND hWnd, DWORD dwError,
                                     LPCTSTR szFailingFunctionName );

// Forward declaration of listUrlPart helper functions:
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength );
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, int partValue );

// Static list describing the URL Scheme types 
// enumerated in INTERNET_SCHEME:
TCHAR* schemeType[] =
{
  TEXT( "[Partial URL]" ),                //  0
  TEXT( "[Unknown scheme]" ),             //  1
  TEXT( "[Default scheme]" ),             //  2
  TEXT( "FTP" ),                          //  3
  TEXT( "Gopher" ),                       //  4
  TEXT( "HTTP" ),                         //  5
  TEXT( "HTTPS" ),                        //  6
  TEXT( "File" ),                         //  7
  TEXT( "News" ),                         //  8
  TEXT( "MailTo" ),                       //  9
  TEXT( "Socks" ),                        // 10
  TEXT( "JavaScript" ),                   // 11
  TEXT( "VBScript" )                      // 12
};
#define  CRACKER_SCHEME_TYPE_ARRAY_SIZE      13

BOOL WINAPI Cracker( HWND hDlg, int nURLtextBoxId, int nListBoxId )
{
   int i, j;
   TCHAR* failedFunctionName;
   TCHAR URL_buffer[CRACKER_BUFFER_SIZE];

   URL_COMPONENTS URLparts;

   URLparts.dwStructSize = sizeof( URLparts );

   // The following elements determine which components are displayed
   URLparts.dwSchemeLength    = 1;
   URLparts.dwHostNameLength  = 1;
   URLparts.dwUserNameLength  = 1;
   URLparts.dwPasswordLength  = 1;
   URLparts.dwUrlPathLength   = 1;
   URLparts.dwExtraInfoLength = 1;

   URLparts.lpszScheme     = NULL;
   URLparts.lpszHostName   = NULL;
   URLparts.lpszUserName   = NULL;
   URLparts.lpszPassword   = NULL;
   URLparts.lpszUrlPath    = NULL;
   URLparts.lpszExtraInfo  = NULL;

   SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
   if( !GetDlgItemText( hDlg, nURLtextBoxId, 
                        URL_buffer, CRACKER_BUFFER_SIZE ) )
   {
       failedFunctionName = TEXT( "GetDlgItemText" );
       goto CrackerError_01;
   }

   if( FAILED( StringCchLength( URL_buffer, CRACKER_BUFFER_SIZE, 
                                (size_t*) &i ) ) )
   {
       failedFunctionName = TEXT( "StringCchLength" );
       goto CrackerError_01;
   }

   if( !InternetCrackUrl( URL_buffer, (DWORD)_tcslen( URL_buffer ), 0, 
                          &URLparts ) )
   {
       failedFunctionName = TEXT( "InternetCrackUrl" );
       goto CrackerError_01;
   }

   failedFunctionName = TEXT( "listURLpart" );

   i = URLparts.nScheme + 2;
   if( ( i >= 0 ) && ( i < CRACKER_SCHEME_TYPE_ARRAY_SIZE ) )
   {
       StringCchLength( schemeType[i], 
                        CRACKER_BUFFER_SIZE, 
                        (size_t*) &j );
       if( !listURLpart( hDlg, nListBoxId, 
                         TEXT("Scheme type"), 
                         schemeType[i], j ))
           goto CrackerError_01;
   }

   if( !listURLpart( hDlg, nListBoxId, TEXT( "Scheme text" ), 
                     URLparts.lpszScheme, 
                     URLparts.dwSchemeLength ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Host name" ), 
                     URLparts.lpszHostName, 
                     URLparts.dwHostNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Port number" ), 
                     (int) URLparts.nPort ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "User name" ), 
                     URLparts.lpszUserName, 
                     URLparts.dwUserNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Password" ), 
                     URLparts.lpszPassword, 
                     URLparts.dwPasswordLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Path" ), 
                     URLparts.lpszUrlPath, 
                     URLparts.dwUrlPathLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Extra information"), 
                     URLparts.lpszExtraInfo, 
                     URLparts.dwExtraInfoLength))
           goto CrackerError_01;

   return( TRUE );

CrackerError_01:
// For sample source code of the InternetErrorOut( ) function 
// referenced below, see the "Handling Errors" 
// topic under "Using WinInet"
   InternetErrorOut( hDlg, GetLastError( ), failedFunctionName );
   return FALSE;
}

// listURLpart( ) helper function for string parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];
  LPTSTR nextStart;
  size_t nextSize;

  if( partLength == 0 )  // Just skip empty ones
    return( TRUE );

  if( FAILED( StringCchCopyEx( outputBuffer, 
                              (size_t) CRACKER_BUFFER_SIZE,
                               szPartName, &nextStart, 
                               &nextSize, 0 ) ) ||
      FAILED( StringCchCopyEx( nextStart, nextSize, TEXT( ": " ), 
                               &nextStart, &nextSize, 0 ) ) ||
      FAILED( StringCchCopyNEx( nextStart, nextSize, part, 
                                (size_t) partLength,
                                &nextStart, &nextSize, 0 ) ) )
    return( FALSE );

  *nextStart = 0;
  if( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                          (LPARAM)outputBuffer ) < 0 )
    return( FALSE );
  return( TRUE );
}

// listURLpart( ) helper function for numeric parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, int partValue )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];

  if( FAILED( StringCchPrintf( outputBuffer, 
                               (size_t) CRACKER_BUFFER_SIZE,
                               TEXT( "%s: %d" ), szPartName, 
                               partValue ) ) ||
      ( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                            (LPARAM)outputBuffer ) < 0 ) )
    return( FALSE );
  return( TRUE );
}
```



## <a name="creating-urls"></a><span data-ttu-id="f04d1-186">Создание URL-адресов</span><span class="sxs-lookup"><span data-stu-id="f04d1-186">Creating URLs</span></span>

<span data-ttu-id="f04d1-187">Функция [**интернеткреатеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) использует сведения в структуре [**\_ компонентов URL-адреса**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) для создания унифицированного указателя ресурса.</span><span class="sxs-lookup"><span data-stu-id="f04d1-187">The [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) function uses the information in the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure to create a Uniform Resource Locator.</span></span>

<span data-ttu-id="f04d1-188">Компонентами, которые составляют структуру [**\_ компонентов URL-адреса**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , являются схема, имя узла, номер порта, имя пользователя, пароль, URL-адрес и дополнительные сведения (например, параметры поиска).</span><span class="sxs-lookup"><span data-stu-id="f04d1-188">The components that make up the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure are the scheme, host name, port number, user name, password, URL path, and additional information (such as search parameters).</span></span> <span data-ttu-id="f04d1-189">Каждый компонент, за исключением номера порта, имеет строковый элемент, содержащий сведения, и элемент, содержащий длину строкового элемента.</span><span class="sxs-lookup"><span data-stu-id="f04d1-189">Each component, except the port number, has a string member that holds the information, and a member that holds the length of the string member.</span></span>

<span data-ttu-id="f04d1-190">Для каждого обязательного компонента член указателя должен содержать адрес буфера, содержащего данные.</span><span class="sxs-lookup"><span data-stu-id="f04d1-190">For each required component, the pointer member should contain the address of the buffer holding the information.</span></span> <span data-ttu-id="f04d1-191">Элемент length должен иметь нулевое значение, если элемент указателя содержит адрес строки, завершающейся нулем; элементу length должна быть присвоена длина строки, если элемент указателя содержит адрес строки, которая не завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="f04d1-191">The length member should be set to zero if the pointer member contains the address of a zero-terminated string; the length member should be set to the string length if the pointer member contains the address of a string that is not zero-terminated.</span></span> <span data-ttu-id="f04d1-192">Элемент указателя всех компонентов, которые не являются обязательными, должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f04d1-192">The pointer member of any components that are not required must be **NULL**.</span></span>

## <a name="accessing-urls-directly"></a><span data-ttu-id="f04d1-193">Прямой доступ к URL-адресам</span><span class="sxs-lookup"><span data-stu-id="f04d1-193">Accessing URLs Directly</span></span>

<span data-ttu-id="f04d1-194">Доступ к ресурсам FTP и HTTP в Интернете Возможен напрямую с помощью функций [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)и [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) .</span><span class="sxs-lookup"><span data-stu-id="f04d1-194">FTP, and HTTP resources on the Internet can be accessed directly by using the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), and [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) functions.</span></span> <span data-ttu-id="f04d1-195">[**Интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) открывает подключение к ресурсу по URL-адресу, переданному в функцию.</span><span class="sxs-lookup"><span data-stu-id="f04d1-195">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) opens a connection to the resource at the URL passed to the function.</span></span> <span data-ttu-id="f04d1-196">При установке этого соединения возможны два действия.</span><span class="sxs-lookup"><span data-stu-id="f04d1-196">When this connection is made, there are two possible steps.</span></span> <span data-ttu-id="f04d1-197">Во-первых, если ресурс является файлом, [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) может скачать его; Во-вторых, если ресурс является каталогом, [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) может перечислить файлы в каталоге (за исключением случаев использования прокси-серверов CERN).</span><span class="sxs-lookup"><span data-stu-id="f04d1-197">First, if the resource is a file, [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) can download it; second, if the resource is a directory, [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) can enumerate the files within the directory (except when using CERN proxies).</span></span> <span data-ttu-id="f04d1-198">Дополнительные сведения о [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)см. в разделе [чтение файлов](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f04d1-198">For more information on [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), see [Reading Files](common-functions.md).</span></span> <span data-ttu-id="f04d1-199">Дополнительные сведения о [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)см. [в разделе Поиск следующего файла](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f04d1-199">For more information on [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), see [Finding the Next File](common-functions.md).</span></span>

<span data-ttu-id="f04d1-200">Для приложений, которые должны работать через прокси-сервер CERN, [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) можно использовать для доступа к каталогам и файлам FTP.</span><span class="sxs-lookup"><span data-stu-id="f04d1-200">For applications that need to operate through a CERN proxy, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) can be used to access FTP directories and files.</span></span> <span data-ttu-id="f04d1-201">Запросы FTP упаковываются в виде HTTP-запроса, который будет принимать прокси-сервер CERN.</span><span class="sxs-lookup"><span data-stu-id="f04d1-201">The FTP requests are packaged to appear like an HTTP request, which the CERN proxy would accept.</span></span>

<span data-ttu-id="f04d1-202">[**Интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) использует обработчик [**хинтернет**](appendix-a-hinternet-handles.md) , созданный функцией [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) , и URL-адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="f04d1-202">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) uses the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function and the URL of the resource.</span></span> <span data-ttu-id="f04d1-203">URL-адрес должен включать схему (http:, FTP:, файл: \[ для локального файла \] или HTTPS: \[ для безопасного протокола гипертекста \] ) и сетевое расположение (например, `www.microsoft.com` ).</span><span class="sxs-lookup"><span data-stu-id="f04d1-203">The URL must include the scheme (http:, ftp:, file: \[for a local file\], or https: \[for hypertext protocol secure\]) and network location (such as `www.microsoft.com`).</span></span> <span data-ttu-id="f04d1-204">URL-адрес может также включать путь (например,/исапи/гомском.АСП? TARGET =/Виндовс/феатуре/) и имя ресурса (например, default.htm).</span><span class="sxs-lookup"><span data-stu-id="f04d1-204">The URL can also include a path (for example, /isapi/gomscom.asp?TARGET=/windows/feature/) and resource name (for example, default.htm).</span></span> <span data-ttu-id="f04d1-205">Для запросов HTTP или HTTPS можно включать дополнительные заголовки.</span><span class="sxs-lookup"><span data-stu-id="f04d1-205">For HTTP or HTTPS requests, additional headers can be included.</span></span>

<span data-ttu-id="f04d1-206">[**Интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), [**Интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)и [**интернетсетфилепоинтер**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (только URL-адреса HTTP или HTTPS) могут использовать для скачивания ресурса маркер, созданный с помощью [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="f04d1-206">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (HTTP or HTTPS URLs only) can use the handle that is created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) to download the resource.</span></span>

<span data-ttu-id="f04d1-207">На следующей схеме показано, какие дескрипторы используются для каждой функции.</span><span class="sxs-lookup"><span data-stu-id="f04d1-207">The following diagram illustrates which handles to use with each function.</span></span>

![дескрипторы для использования с функциями](images/ax-wnt02.png)

<span data-ttu-id="f04d1-209">Корневой обработчик [**хинтернет**](appendix-a-hinternet-handles.md) , созданный [**Интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) , используется [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="f04d1-209">The root [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) is used by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span> <span data-ttu-id="f04d1-210">Обработчик **хинтернет** , созданный [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) , может использоваться [**интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (не показано здесь) и [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (только URL-адреса HTTP или HTTPS).</span><span class="sxs-lookup"><span data-stu-id="f04d1-210">The **HINTERNET** handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) can be used by [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (not shown here), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (HTTP or HTTPS URLs only).</span></span>

<span data-ttu-id="f04d1-211">Дополнительные сведения см. в разделе [**Хинтернет Handles**](appendix-a-hinternet-handles.md).</span><span class="sxs-lookup"><span data-stu-id="f04d1-211">For more information, see [**HINTERNET Handles**](appendix-a-hinternet-handles.md).</span></span>

> [!Note]  
> <span data-ttu-id="f04d1-212">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="f04d1-212">WinINet does not support server implementations.</span></span> <span data-ttu-id="f04d1-213">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="f04d1-213">In addition, it should not be used from a service.</span></span> <span data-ttu-id="f04d1-214">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="f04d1-214">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 