---
description: Работа с эрами японского календаря
ms.assetid: a1dabf7c-6521-492e-bdc0-27cfb07cfc20
title: Работа с эрами японского календаря
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eba757745bf0d90d119c821772c7fc23f3f8694b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912544"
---
# <a name="era-handling-for-the-japanese-calendar"></a><span data-ttu-id="86495-103">Работа с эрами японского календаря</span><span class="sxs-lookup"><span data-stu-id="86495-103">Era Handling for the Japanese Calendar</span></span>

<span data-ttu-id="86495-104">У многих календарей есть эры, например AD/BC или CE/–.</span><span class="sxs-lookup"><span data-stu-id="86495-104">Many calendars have eras, such as AD/BC or CE/BCE.</span></span> <span data-ttu-id="86495-105">В японском календаре годы описываются ненгō, сочетанием номера года и названия эры.</span><span class="sxs-lookup"><span data-stu-id="86495-105">In the Japanese Calendar, years are described by nengō, a combination of the year number and era name.</span></span> <span data-ttu-id="86495-106">Например, 2009 — Хэйсэй 21.</span><span class="sxs-lookup"><span data-stu-id="86495-106">For example, 2009 is Heisei 21.</span></span> <span data-ttu-id="86495-107">В прошлом названия эре в японском языке меняются часто, но теперь японские Эр меняются только в случае германской.</span><span class="sxs-lookup"><span data-stu-id="86495-107">In the past, Japanese era names changed frequently, but now the Japanese eras change only on imperial succession.</span></span> <span data-ttu-id="86495-108">Windows и Microsoft .NET исторически поддерживали четыре современные эры в этой политике: Меижи, Таишō, Шōва и Хэйсэй.</span><span class="sxs-lookup"><span data-stu-id="86495-108">Windows and Microsoft .NET have historically supported the four modern eras under this policy: Meiji, Taishō, Shōwa and Heisei.</span></span>

<span data-ttu-id="86495-109">В Windows 7, Windows Server 2008 R2 и платформа .NET Framework 4 корпорация Майкрософт распознает, что в будущем могут быть добавлены дополнительные Эр.</span><span class="sxs-lookup"><span data-stu-id="86495-109">With Windows 7, Windows Server 2008 R2, and the .NET Framework 4, Microsoft recognizes that additional eras may be added in the future.</span></span> <span data-ttu-id="86495-110">В этих версиях Windows данные эры хранятся в реестре с ключом:</span><span class="sxs-lookup"><span data-stu-id="86495-110">On these versions of Windows the era data is stored in the registry under the key:</span></span><dl> <span data-ttu-id="86495-111">HKEY \_ локальный \_ компьютер \\ система \\ CurrentControlSet \\ контроль \\ NLS \\ календари \\ японская \\ эры</span><span class="sxs-lookup"><span data-stu-id="86495-111">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Nls\\Calendars\\Japanese\\Eras</span></span>  
</dl>

<span data-ttu-id="86495-112">При необходимости к этому ключу можно добавить дополнительные Эр с помощью обычного Центр обновления Windows процесса.</span><span class="sxs-lookup"><span data-stu-id="86495-112">If necessary, additional eras can be added to that key through the normal Windows Update process.</span></span> <span data-ttu-id="86495-113">Этот ключ можно просмотреть с помощью редактора реестра (Regedit.exe).</span><span class="sxs-lookup"><span data-stu-id="86495-113">This key can be viewed using the registry editor (Regedit.exe).</span></span> <span data-ttu-id="86495-114">Пример ключа и значений, поставляемых в Windows 7:</span><span class="sxs-lookup"><span data-stu-id="86495-114">An example of the key and values shipped in Windows 7 is:</span></span>

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"1868 01 01"="明治_明_Meiji_M"
"1912 07 30"="大正_大_Taisho_T"
"1926 12 25"="昭和_昭_Showa_S"
"1989 01 08"="平成_平_Heisei_H"
```

<span data-ttu-id="86495-115">Название каждого значения эры — это дата начала эры в григорианском календаре.</span><span class="sxs-lookup"><span data-stu-id="86495-115">The name of each era value is the date the era begins in the Gregorian calendar.</span></span> <span data-ttu-id="86495-116">Значение содержит название эры в японском, сокращенное имя на японском языке, имя на английском и сокращенное название на английском языке:</span><span class="sxs-lookup"><span data-stu-id="86495-116">The value contains the era name in Japanese, the abbreviated name in Japanese, the name in English, and an abbreviated name in English:</span></span><dl> <span data-ttu-id="86495-117">"гггг мм дд" = "JE \_ аже \_ ee \_ АИ"</span><span class="sxs-lookup"><span data-stu-id="86495-117">"YYYY MM DD"="JE\_AJE\_EE\_AEE"</span></span>  
</dl>where

-   <span data-ttu-id="86495-118">"Гггг мм дд" — это дата начала эры в году, месяц, день, где год состоит из 4 цифр, день — 2 цифры, а месяц — также 2 цифры.</span><span class="sxs-lookup"><span data-stu-id="86495-118">"YYYY MM DD" is the Gregorian date of the start of the era in year, month, day form where year is 4 digits, day is 2 digits and month is also 2 digits.</span></span> <span data-ttu-id="86495-119">Каждая часть даты отделяется пробелом.</span><span class="sxs-lookup"><span data-stu-id="86495-119">A space separates each part of the date.</span></span>
-   <span data-ttu-id="86495-120">"JE" — это японское название эры, за которым следует символ подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="86495-120">"JE" is the Japanese name of the era, and is followed by an underscore.</span></span>
-   <span data-ttu-id="86495-121">"Аже" — это сокращенное название эры в японском языке, за которым следует символ подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="86495-121">"AJE" is the abbreviated name of the era, in Japanese, and is followed by an underscore.</span></span>
-   <span data-ttu-id="86495-122">"EE" — это английское название японской эры, за которым следует символ подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="86495-122">"EE" is the English name of the Japanese era, and is followed by an underscore.</span></span>
-   <span data-ttu-id="86495-123">"АИ" — это сокращенное название японской эры в японском языке.</span><span class="sxs-lookup"><span data-stu-id="86495-123">"AEE" is the abbreviated English name of the Japanese era.</span></span>

<span data-ttu-id="86495-124">Одним из соображений для разработчиков приложений является возможность добавления дополнительных Эр с помощью Центр обновления Windows или других средств.</span><span class="sxs-lookup"><span data-stu-id="86495-124">One consideration for application developers is the possibility that additional eras will be added by Windows Update or other means.</span></span> <span data-ttu-id="86495-125">В этом случае приложение может столкнуться с более чем ожидаемой четырьмя Эр для японского календаря.</span><span class="sxs-lookup"><span data-stu-id="86495-125">In that case the application may encounter more than the expected four eras for the Japanese calendar.</span></span> <span data-ttu-id="86495-126">Тест-инженеры тестирования могут добавлять в реестр дополнительную эру; Однако он должен быть ограничен только тестовыми компьютерами, так как он влияет на поведение всего компьютера.</span><span class="sxs-lookup"><span data-stu-id="86495-126">For testing purposes testers may add an additional era to the registry; however, that should be restricted to test machines only, as it impacts the behavior of the entire machine.</span></span>

<span data-ttu-id="86495-127">Ниже приведен пример такого ключа, который можно использовать для тестирования.</span><span class="sxs-lookup"><span data-stu-id="86495-127">An example of such a key that could be used for test follows.</span></span> <span data-ttu-id="86495-128">Это изменение можно выполнить с помощью редактора реестра.</span><span class="sxs-lookup"><span data-stu-id="86495-128">This change can be made with the registry editor.</span></span> <span data-ttu-id="86495-129">(Это пример только для тестового использования и не предназначен для прогнозирования будущих добавлений.)</span><span class="sxs-lookup"><span data-stu-id="86495-129">(This is an example for test use only, and is not intended to predict any future additions.)</span></span>

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"2020 09 01"="仮名_仮_Test Era_X"
```

<span data-ttu-id="86495-130">Обратите внимание, что это касается только компьютеров под Windows 7 и более поздних версий или платформа .NET Framework 4 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="86495-130">Note that this only impacts machines running Windows 7 and later or .NET Framework 4 and later.</span></span> <span data-ttu-id="86495-131">Разработчикам приложений рекомендуется протестировать свои приложения с помощью таких дополнительных тестовых Эр, чтобы гарантировать, что их приложения будут продолжать работать при добавлении дополнительных эр в будущем.</span><span class="sxs-lookup"><span data-stu-id="86495-131">Application developers are encouraged to test their applications with such additional test eras to ensure that their applications will continue to work if additional eras are added at some future date.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86495-132">См. также</span><span class="sxs-lookup"><span data-stu-id="86495-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86495-133">Получение сведений о времени и дате</span><span class="sxs-lookup"><span data-stu-id="86495-133">Retrieving Time and Date Information</span></span>](retrieving-time-and-date-information.md)
</dt> <dt>

[<span data-ttu-id="86495-134">Идентификаторы календаря</span><span class="sxs-lookup"><span data-stu-id="86495-134">Calendar Identifiers</span></span>](calendar-identifiers.md)
</dt> </dl>

 

 



