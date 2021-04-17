---
description: В Windows Vista и более поздних версиях можно использовать псевдо-национальные настройки для тестирования возможности локализации приложений. Этот раздел содержит процедуры для использования псевдо-кодов.
ms.assetid: 1eccdbb9-a1bd-443a-a5f6-d64c9e5c87b3
title: Использование псевдо-национальных настроек для тестирования возможности локализации
ms.topic: article
ms.date: 07/05/2018
ms.openlocfilehash: f8c6b435b85a5bef98eff9bf76681096779433e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684599"
---
# <a name="using-pseudo-locales-for-localizability-testing"></a><span data-ttu-id="cf30b-104">Использование псевдо-национальных настроек для тестирования возможности локализации</span><span class="sxs-lookup"><span data-stu-id="cf30b-104">Using pseudo-locales for localizability testing</span></span>

<span data-ttu-id="cf30b-105">[Псевдо-региональные стандарты](pseudo-locales.md) встроены в Windows Vista и более поздних версий, чтобы к ним можно было обращаться через API-интерфейсы поддержки национальных языков (NLS).</span><span class="sxs-lookup"><span data-stu-id="cf30b-105">[Pseudo-locales](pseudo-locales.md) are built in to Windows Vista and later, so that you can access them via National Language Support (NLS) APIs.</span></span> <span data-ttu-id="cf30b-106">Для проверки возможности [локализации](/windows/uwp/design/globalizing/globalizing-portal) приложений можно использовать псевдо-национальные настройки.</span><span class="sxs-lookup"><span data-stu-id="cf30b-106">You can use pseudo-locales to test the [localizability](/windows/uwp/design/globalizing/globalizing-portal) of your applications.</span></span> <span data-ttu-id="cf30b-107">Этот раздел содержит процедуры для использования псевдо-кодов.</span><span class="sxs-lookup"><span data-stu-id="cf30b-107">This topic includes procedures for using pseudo-codes.</span></span>

> [!NOTE]
> <span data-ttu-id="cf30b-108">Одна задача, требующая особого рассмотрения, когда речь идет о псевдолокализациих, заключается в их перечислении; как в коде, так и в области языковых и региональных параметров панели управления.</span><span class="sxs-lookup"><span data-stu-id="cf30b-108">One task that needs special consideration when it comes to pseudo-locales is enumerating them; whether in your code, or in the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="cf30b-109">Далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="cf30b-109">More on that later in this topic.</span></span>

<span data-ttu-id="cf30b-110">Имена псевдо-локалей: "QPS-Плок", "QPS-плока" и "QPS-плокм".</span><span class="sxs-lookup"><span data-stu-id="cf30b-110">The names of the pseudo-locales are "qps-ploc", "qps-ploca", and "qps-plocm".</span></span> <span data-ttu-id="cf30b-111">Начиная с Windows 10 также доступен псевдо-locale "QPS-ЛАТН-x-sh".</span><span class="sxs-lookup"><span data-stu-id="cf30b-111">As of Windows 10, the pseudo-locale "qps-Latn-x-sh" is also available.</span></span>

## <a name="retrieve-information-about-pseudo-locales"></a><span data-ttu-id="cf30b-112">Получение сведений о псевдо-национальных параметрах</span><span class="sxs-lookup"><span data-stu-id="cf30b-112">Retrieve information about pseudo-locales</span></span>

<span data-ttu-id="cf30b-113">[**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) можно использовать для получения сведений о псевдо-локале.</span><span class="sxs-lookup"><span data-stu-id="cf30b-113">You can use [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) to retrieve information about a pseudo-locale.</span></span> <span data-ttu-id="cf30b-114">Передайте в функцию имя определенного псевдо-локали (см. список имен выше).</span><span class="sxs-lookup"><span data-stu-id="cf30b-114">Pass into the function the name of the particular pseudo-locale (see the list of names above).</span></span> <span data-ttu-id="cf30b-115">Например, "QPS-плокм" для зеркально отображаемого псевдо-locale.</span><span class="sxs-lookup"><span data-stu-id="cf30b-115">For example, "qps-plocm" for the mirrored pseudo-locale.</span></span>

```cpp
wchar_t languageIdentifier[5];
int rc{ ::GetLocaleInfoEx(L"qps-plocm", LOCALE_ILANGUAGE, languageIdentifier, 5) };
```

## <a name="use-localenametolcid-with-pseudo-locales"></a><span data-ttu-id="cf30b-116">Использование ЛокаленаметолЦид с псевдо-языками</span><span class="sxs-lookup"><span data-stu-id="cf30b-116">Use LocaleNameToLCID with pseudo-locales</span></span>

<span data-ttu-id="cf30b-117">Вы можете вызвать функцию сопоставления NLS [**локаленаметолЦид**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) с именем псевдо-locale.</span><span class="sxs-lookup"><span data-stu-id="cf30b-117">You can call the NLS mapping function [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) with the name of a pseudo-locale.</span></span>

```cpp
LCID lcid{ ::LocaleNameToLCID(L"qps-plocm", 0) };
```

## <a name="enable-pseudo-locales-for-enumeration"></a><span data-ttu-id="cf30b-118">Включить псевдо-национальные настройки для перечисления</span><span class="sxs-lookup"><span data-stu-id="cf30b-118">Enable pseudo-locales for enumeration</span></span>

<span data-ttu-id="cf30b-119">В приложении можно вызвать [**енумсистемлокалесекс**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) , чтобы перечислить языковые стандарты, распознаваемые системой.</span><span class="sxs-lookup"><span data-stu-id="cf30b-119">In your application, you can call [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) to enumerate the locales that the system recognizes.</span></span> <span data-ttu-id="cf30b-120">Региональные и языковые параметры панели управления также вызывают **енумсистемлокалесекс** для создания списка отображаемых языковых стандартов.</span><span class="sxs-lookup"><span data-stu-id="cf30b-120">The regional and language options portion of the Control Panel also calls **EnumSystemLocalesEx** to build the list of locales that it displays.</span></span> <span data-ttu-id="cf30b-121">Однако по умолчанию четыре псевдо-локали, перечисленные выше, не распознаются системой, поэтому они не будут возвращены функцией **енумсистемлокалесекс**.</span><span class="sxs-lookup"><span data-stu-id="cf30b-121">However, by default, the four pseudo-locales listed above are not recognized by the system, so they won't be returned by **EnumSystemLocalesEx**.</span></span> <span data-ttu-id="cf30b-122">Для систем с Windows Vista вплоть до Windows 10 версии 1709, решение заключается в том, чтобы включить псевдо-национальные настройки, добавив ключи в реестр Windows.</span><span class="sxs-lookup"><span data-stu-id="cf30b-122">For systems from Windows Vista up to and including Windows 10, version 1709, the solution is to enable pseudo-locales by adding keys to the Windows Registry.</span></span>

<span data-ttu-id="cf30b-123">Изменения вносятся в \_ Раздел HKEY Local \_ Machine \\ System \\ CurrentControlSet \\ управления \\ ключами NLS для языков, установленных в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="cf30b-123">The edits are made under the HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Nls key for the languages installed on the operating system.</span></span> <span data-ttu-id="cf30b-124">Эти параметры можно использовать, чтобы включить псевдо-национальные настройки.</span><span class="sxs-lookup"><span data-stu-id="cf30b-124">You can make these settings to enable the pseudo-locales.</span></span> <span data-ttu-id="cf30b-125">Каждый ключ, показанный ниже, представляет собой шестнадцатеричный код, соответствующий включенному параметру псевдо-locale.</span><span class="sxs-lookup"><span data-stu-id="cf30b-125">Each key shown below is the hexadecimal LCID corresponding to the pseudo-locale being enabled.</span></span> <span data-ttu-id="cf30b-126">Каждое значение имеет тип String (REG \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="cf30b-126">Each value is of type string (REG\_SZ).</span></span>

```
[HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Nls\Locale]
"00000501"="1" // qps-ploc (Windows Vista and later)
"000005fe"="7" // qps-ploca (Windows Vista and later)
"00000901"="1" // qps-Latn-x-sh (Windows 10 and later)
"000009ff"="d" // qps-plocm (Windows Vista and later)
```

<span data-ttu-id="cf30b-127">В Windows 10, версия 1803, изменение реестра Windows не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="cf30b-127">For Windows 10, version 1803, editing the Windows Registry like this has no effect.</span></span> <span data-ttu-id="cf30b-128">Но вы по-прежнему можете вызывать интерфейсы API NLS без перечисления с именами псевдо-языков (см. Приведенные выше примеры кода) для заполнения пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cf30b-128">But you can still call the non-enumerating NLS APIs with the names of the pseudo-locales (see the code examples above) to populate your user interface (UI).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf30b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="cf30b-129">Related topics</span></span>

* [<span data-ttu-id="cf30b-130">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="cf30b-130">Using National Language Support</span></span>](using-national-language-support.md)
* [<span data-ttu-id="cf30b-131">Псевдо-языковые стандарты</span><span class="sxs-lookup"><span data-stu-id="cf30b-131">Pseudo-Locales</span></span>](pseudo-locales.md)
* [<span data-ttu-id="cf30b-132">енумсистемлокалесекс</span><span class="sxs-lookup"><span data-stu-id="cf30b-132">EnumSystemLocalesEx</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)
* [<span data-ttu-id="cf30b-133">GetLocaleInfoEx</span><span class="sxs-lookup"><span data-stu-id="cf30b-133">GetLocaleInfoEx</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
* [<span data-ttu-id="cf30b-134">локаленаметолЦид</span><span class="sxs-lookup"><span data-stu-id="cf30b-134">LocaleNameToLCID</span></span>](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
