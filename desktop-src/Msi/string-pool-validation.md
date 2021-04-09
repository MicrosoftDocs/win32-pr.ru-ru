---
description: Установщик Windows сохраняет все строки базы данных в одном общем пуле строк, чтобы уменьшить размер базы данных и повысить производительность.
ms.assetid: b627f3da-3545-4c1a-85b0-d8845fdac621
title: Проверка String-Pool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb544b5c76026846f7e8b8f6f331195426ab55c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155123"
---
# <a name="string-pool-validation"></a><span data-ttu-id="26034-103">Проверка String-Pool</span><span class="sxs-lookup"><span data-stu-id="26034-103">String-Pool Validation</span></span>

<span data-ttu-id="26034-104">Установщик Windows сохраняет все строки базы данных в одном общем пуле строк, чтобы уменьшить размер базы данных и повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="26034-104">The Windows Installer stores all database strings in a single shared string pool to reduce the size of the database and to improve performance.</span></span> <span data-ttu-id="26034-105">Единственным средством проверки строкового пула является использование средства Мсиинфо, находящихся в пакете SDK для установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="26034-105">The only means of validating the string pool is to use the MsiInfo tool found in the Windows Installer SDK.</span></span>

<span data-ttu-id="26034-106">Проверка пула строк состоит из двух основных проверок:</span><span class="sxs-lookup"><span data-stu-id="26034-106">String pool verification consists of two main checks:</span></span>

-   [<span data-ttu-id="26034-107">Проверки строк DBCS</span><span class="sxs-lookup"><span data-stu-id="26034-107">DBCS string tests</span></span>](#dbcs-string-tests)
-   [<span data-ttu-id="26034-108">Проверка счетчика ссылок</span><span class="sxs-lookup"><span data-stu-id="26034-108">Reference count verification</span></span>](#reference-count-verification)

## <a name="dbcs-string-tests"></a><span data-ttu-id="26034-109">Проверки строк DBCS</span><span class="sxs-lookup"><span data-stu-id="26034-109">DBCS String Tests</span></span>

<span data-ttu-id="26034-110">Проверка строк DBCS проверяет каждую строку в базе данных на наличие двух критериев: для пакетов с нейтральной кодовой страницей, если какой-либо символ является расширенным символом (больше 127), строка помечается, и отображается сообщение о том, что кодовая страница базы данных является недопустимой, так как для этих символов требуется, чтобы конкретная кодовая страница была согласована на всех системах.</span><span class="sxs-lookup"><span data-stu-id="26034-110">The DBCS string tests scan each string in the database for two criteria: For packages with a neutral code page marked, if any character is an extended character (greater than 127), the string is flagged and a message is displayed saying that the code page of the database is invalid because these characters require a specific code page to be rendered consistently on all systems.</span></span>

<span data-ttu-id="26034-111">Если база данных содержит кодовую страницу, каждая строка сканируется на наличие недопустимого индикатора DBCS.</span><span class="sxs-lookup"><span data-stu-id="26034-111">If the database has a code page, each string is scanned for an invalid DBCS indicator.</span></span> <span data-ttu-id="26034-112">Если ненейтральная строка была неправильно помечена, символы не отображаются правильно.</span><span class="sxs-lookup"><span data-stu-id="26034-112">If a non-neutral string has been improperly marked, the characters will not render correctly.</span></span> <span data-ttu-id="26034-113">(Чаще всего это происходит из-за принудительного применения кодовой страницы к конкретному значению с помощью \_ Таблица Форцекодепаже с ненейтральными строками, уже наявляющимисяся в базе данных.) Обратите внимание, что эта проверка требует, чтобы кодовая страница базы данных была установлена в системе.</span><span class="sxs-lookup"><span data-stu-id="26034-113">(This is most commonly caused by forcing the code page to a particular value using the \_ForceCodepage table with non-neutral strings already in the database.) Note that this check requires that the code page of the database be installed on the system.</span></span>

<span data-ttu-id="26034-114">Если имеется проблема с кодовой страницей, пользователь может исправить ошибку с помощью \_ таблицы форцекодепаже, чтобы принудительно применить соответствующее значение для кодовой страницы базы данных.</span><span class="sxs-lookup"><span data-stu-id="26034-114">If there is a code page problem, the user may fix the error by using the \_ForceCodepage table to force the code page of the database to the appropriate value.</span></span> <span data-ttu-id="26034-115">Дополнительные сведения см. в разделе [Обработка кодовых страниц](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="26034-115">For more information, see [Code Page Handling](code-page-handling-windows-installer-.md).</span></span>

## <a name="reference-count-verification"></a><span data-ttu-id="26034-116">Проверка счетчика ссылок</span><span class="sxs-lookup"><span data-stu-id="26034-116">Reference Count Verification</span></span>

<span data-ttu-id="26034-117">Чтобы проверить счетчик ссылок всех строк, каждая таблица сканируется на наличие строковых значений, сохраняется количество каждой отдельной строки, а результат сравнивается с сохраненным числом ссылок в пуле строк базы данных.</span><span class="sxs-lookup"><span data-stu-id="26034-117">To verify the reference counts of all strings, every table is scanned for string values, a count of each distinct string is kept, and the result is compared to the stored reference count in the database string pool.</span></span>

<span data-ttu-id="26034-118">При наличии проблемы с числом ссылок на строки пользователь должен немедленно экспортировать каждую таблицу базы данных с помощью [**мсидатабасикспорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), создать новую базу данных и импортировать таблицы в новую базу данных с помощью [**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="26034-118">If there is a string reference count problem, the user should immediately export each table of the database using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), create a new database, and import the tables into the new database using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="26034-119">Новая база данных будет иметь то же содержимое, что и старая база данных, но счетчики ссылок на строки верны.</span><span class="sxs-lookup"><span data-stu-id="26034-119">The new database then has the same content as the old database, but the string reference counts are correct.</span></span> <span data-ttu-id="26034-120">Добавление или удаление данных из базы данных с поврежденным пулом строк может привести к повреждению базы данных и утрате данных, поэтому необходимо быстро выполнить эти действия, чтобы предотвратить дальнейшую потерю данных.</span><span class="sxs-lookup"><span data-stu-id="26034-120">Adding or deleting data from a database with a corrupt string pool can increase corruption of the database and loss of data, so taking these steps quickly is important to prevent further data loss.</span></span>

<span data-ttu-id="26034-121">При перестроении баз данных не забудьте внедрить все необходимые хранилища и потоки в новую базу данных ( [ \_ см. таблицу "таблицы и](-streams-table.md) [ \_ хранилища](-storages-table.md)таблиц") и знать о проблемах с кодовыми страницами.</span><span class="sxs-lookup"><span data-stu-id="26034-121">When rebuilding databases, remember to embed any necessary storages and streams in the new database (see [\_Streams Table](-streams-table.md) and [\_Storages Table](-storages-table.md)) and be aware of code page issues.</span></span> <span data-ttu-id="26034-122">Также не забудьте задать все необходимые свойства [потока сводных данных](summary-information-stream.md) .</span><span class="sxs-lookup"><span data-stu-id="26034-122">Also remember to set each of the necessary [Summary Information Stream](summary-information-stream.md) properties.</span></span>

 

 



