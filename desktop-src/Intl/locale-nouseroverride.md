---
description: наусероверриде ЛОКАЛи \_
ms.assetid: ab68d16b-5e1e-4af3-b048-43975cded00a
title: LOCALE_NOUSEROVERRIDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28c2f59358bf71936e3a812c10e061d7a169387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650814"
---
# <a name="locale_nouseroverride"></a><span data-ttu-id="b98ad-103">наусероверриде ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="b98ad-103">LOCALE\_NOUSEROVERRIDE</span></span>

> [!Caution]  
> <span data-ttu-id="b98ad-104">Так как ЯЗЫКовой стандарт \_ наусероверриде отключает параметры пользователя, его использование настоятельно не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="b98ad-104">Since LOCALE\_NOUSEROVERRIDE disables user preferences, its use is strongly discouraged.</span></span> <span data-ttu-id="b98ad-105">Эта константа не гарантирует стабильность данных, поскольку [пользовательские языковые стандарты](custom-locales.md), обновления служб, различные версии операционных систем и другие сценарии могут изменять данные непредвиденным образом.</span><span class="sxs-lookup"><span data-stu-id="b98ad-105">This constant does not guarantee data stability since [custom locales](custom-locales.md), service updates, different operating system versions, and other scenarios can change data in unexpected ways.</span></span> <span data-ttu-id="b98ad-106">Дополнительные сведения см. [в разделе Использование постоянных данных языкового стандарта](using-persistent-locale-data.md).</span><span class="sxs-lookup"><span data-stu-id="b98ad-106">For more information, see [Using Persistent Locale Data](using-persistent-locale-data.md).</span></span>

 

<span data-ttu-id="b98ad-107">Нет переопределений пользователей.</span><span class="sxs-lookup"><span data-stu-id="b98ad-107">No user override.</span></span> <span data-ttu-id="b98ad-108">В некоторых функциях, например [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) и [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex), эта константа заставляет функцию обходить любые переопределяемые пользователем переопределения и использовать Системное значение по умолчанию для любой другой константы, указанной в вызове функции.</span><span class="sxs-lookup"><span data-stu-id="b98ad-108">In several functions, for example, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) and [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex), this constant causes the function to bypass any user override and use the system default value for any other constant specified in the function call.</span></span> <span data-ttu-id="b98ad-109">Сведения извлекаются из базы данных языкового стандарта, даже если идентификатор указывает текущий языковой стандарт, а пользователь изменил некоторые значения с помощью панели управления или если приложение изменило эти значения с помощью [**сетлокалеинфо**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="b98ad-109">The information is retrieved from the locale database, even if the identifier indicates the current locale and the user has changed some of the values using the Control Panel, or if an application has changed these values by using [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span></span> <span data-ttu-id="b98ad-110">Если эта константа не указана, любые значения, настроенные пользователем на панели управления или настроенные с помощью [**сетлокалеинфо**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) , имеют приоритет над параметрами базы данных для текущего языкового стандарта по умолчанию системы.</span><span class="sxs-lookup"><span data-stu-id="b98ad-110">If this constant is not specified, any values that the user has configured from the Control Panel or that an application has configured using [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) take precedence over the database settings for the current system default locale.</span></span>

 

 



