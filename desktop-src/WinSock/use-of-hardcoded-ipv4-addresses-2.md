---
description: Долговременное написание IPv4 привело к жесткому кодированию множества известных IPv4-адресов, таких как адреса замыканий на себя (127. x. x. x), целочисленных констант, таких как декодирование \_ замыканий на себя, а также других.
ms.assetid: adb39f27-c219-43cd-9e86-b2d3b663c79c
title: Использование жестко закодированных IPv4-адресов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8205840b1c79afcaf375b81f3223a1c780cc03d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343455"
---
# <a name="use-of-hardcoded-ipv4-addresses"></a><span data-ttu-id="fa0bc-103">Использование жестко закодированных IPv4-адресов</span><span class="sxs-lookup"><span data-stu-id="fa0bc-103">Use of Hardcoded IPv4 Addresses</span></span>

<span data-ttu-id="fa0bc-104">Долговременное написание IPv4 привело к жесткому кодированию множества известных IPv4-адресов, таких как адреса замыканий на себя (127. x. x. x), целочисленных констант, таких как декодирование \_ замыканий на себя, а также других.</span><span class="sxs-lookup"><span data-stu-id="fa0bc-104">The longevity of IPv4 resulted in hard coding many well-known IPv4 addresses, such as loopback addresses (127.x.x.x), integer constants such as INADDR\_LOOPBACK, among others.</span></span> <span data-ttu-id="fa0bc-105">При использовании жесткого кодирования эти адреса представляют очевидные проблемы при изменении и существующем приложении для поддержки протокола IPv6 или создании новых программ, независимых от использования версий.</span><span class="sxs-lookup"><span data-stu-id="fa0bc-105">The practice of hard coding these addresses presents obvious problems when modifying and existing application to support IPv6 or creating new IP version-independent programs.</span></span>

<span data-ttu-id="fa0bc-106">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="fa0bc-106">Best Practice</span></span>

-   <span data-ttu-id="fa0bc-107">Лучший подход заключается в том, чтобы не прописано никаких адресов.</span><span class="sxs-lookup"><span data-stu-id="fa0bc-107">The best approach is to avoid hardcoding any addresses.</span></span>

<span data-ttu-id="fa0bc-108">Код, чтобы избежать</span><span class="sxs-lookup"><span data-stu-id="fa0bc-108">Code To Avoid</span></span>

-   <span data-ttu-id="fa0bc-109">Избегайте использования жестко зафиксированных адресов в коде.</span><span class="sxs-lookup"><span data-stu-id="fa0bc-109">Avoid using hardcoded addresses in code.</span></span>

<span data-ttu-id="fa0bc-110">**Изменение существующей базы кода с IPv4 на IPv4 и взаимодействие с IPv6**</span><span class="sxs-lookup"><span data-stu-id="fa0bc-110">**To modify your existing code base from IPv4 to IPv4- and IPv6-interoperability**</span></span>

1.  <span data-ttu-id="fa0bc-111">Получите служебную программу *Checkv4.exe* .</span><span class="sxs-lookup"><span data-stu-id="fa0bc-111">Acquire the *Checkv4.exe* utility.</span></span> <span data-ttu-id="fa0bc-112">Программа *Checkv4.exe* устанавливается в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK), выпущенного для Windows Vista и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="fa0bc-112">The *Checkv4.exe* utility is installed as part of the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later.</span></span> <span data-ttu-id="fa0bc-113">Windows SDK доступен по подписке MSDN. ее также можно загрузить с веб-сайта Майкрософт ( https://msdn.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="fa0bc-113">The Windows SDK is available through an MSDN subscription and can also be downloaded from the Microsoft website (https://msdn.microsoft.com).</span></span>
2.  <span data-ttu-id="fa0bc-114">Запустите служебную программу *Checkv4.exe* для своего кода.</span><span class="sxs-lookup"><span data-stu-id="fa0bc-114">Run the *Checkv4.exe* utility against your code.</span></span> <span data-ttu-id="fa0bc-115">Узнайте, как запустить служебную программу *Checkv4.exe* для файлов в разделе об [использовании служебной программы Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="fa0bc-115">Learn about how to run the *Checkv4.exe* utility against your files in the section on [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>
3.  <span data-ttu-id="fa0bc-116">Служебная программа *Checkv4.exe* предупреждает о наличии общих определений для IPv4-адресов, таких как деадрес \_ замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="fa0bc-116">The *Checkv4.exe* utility alerts you to the presence of common defines for IPv4 addresses, such as INADDR\_LOOPBACK.</span></span> <span data-ttu-id="fa0bc-117">Измените код, который использует строковые литералы, с кодом, который не зависит от версии протокола.</span><span class="sxs-lookup"><span data-stu-id="fa0bc-117">Modify any code that uses literal strings with code that is protocol-version agnostic.</span></span>
4.  <span data-ttu-id="fa0bc-118">Найдите в базе кода другие возможные строковые литералы, если это уместно.</span><span class="sxs-lookup"><span data-stu-id="fa0bc-118">Search your code base for other potential literal strings, as appropriate.</span></span>

<span data-ttu-id="fa0bc-119">Служебная программа *Checkv4.exe* может помочь найти общие строковые литералы, но могут быть другие, характерные для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="fa0bc-119">The *Checkv4.exe* utility can help you find common literal strings, but there may be others that are specific to your application.</span></span> <span data-ttu-id="fa0bc-120">Необходимо выполнить тщательный поиск и тестирование, чтобы гарантировать, что база кода ерадикатед потенциальные проблемы, связанные со строковыми строками.</span><span class="sxs-lookup"><span data-stu-id="fa0bc-120">You should perform thorough searching and testing to ensure your code base has eradicated potential problems associated with literal strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa0bc-121">См. также</span><span class="sxs-lookup"><span data-stu-id="fa0bc-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa0bc-122">Рекомендации по IPv6 для приложений Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="fa0bc-122">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="fa0bc-123">Изменение структур данных для IPv6 Winsock Аппикатионс</span><span class="sxs-lookup"><span data-stu-id="fa0bc-123">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="fa0bc-124">Сокеты с двумя стеками для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="fa0bc-124">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="fa0bc-125">Вызовы функций для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="fa0bc-125">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="fa0bc-126">Проблемы с пользовательским интерфейсом для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="fa0bc-126">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="fa0bc-127">Базовые протоколы для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="fa0bc-127">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 



