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
# <a name="using-pseudo-locales-for-localizability-testing"></a>Использование псевдо-национальных настроек для тестирования возможности локализации

[Псевдо-региональные стандарты](pseudo-locales.md) встроены в Windows Vista и более поздних версий, чтобы к ним можно было обращаться через API-интерфейсы поддержки национальных языков (NLS). Для проверки возможности [локализации](/windows/uwp/design/globalizing/globalizing-portal) приложений можно использовать псевдо-национальные настройки. Этот раздел содержит процедуры для использования псевдо-кодов.

> [!NOTE]
> Одна задача, требующая особого рассмотрения, когда речь идет о псевдолокализациих, заключается в их перечислении; как в коде, так и в области языковых и региональных параметров панели управления. Далее в этом разделе.

Имена псевдо-локалей: "QPS-Плок", "QPS-плока" и "QPS-плокм". Начиная с Windows 10 также доступен псевдо-locale "QPS-ЛАТН-x-sh".

## <a name="retrieve-information-about-pseudo-locales"></a>Получение сведений о псевдо-национальных параметрах

[**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) можно использовать для получения сведений о псевдо-локале. Передайте в функцию имя определенного псевдо-локали (см. список имен выше). Например, "QPS-плокм" для зеркально отображаемого псевдо-locale.

```cpp
wchar_t languageIdentifier[5];
int rc{ ::GetLocaleInfoEx(L"qps-plocm", LOCALE_ILANGUAGE, languageIdentifier, 5) };
```

## <a name="use-localenametolcid-with-pseudo-locales"></a>Использование ЛокаленаметолЦид с псевдо-языками

Вы можете вызвать функцию сопоставления NLS [**локаленаметолЦид**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) с именем псевдо-locale.

```cpp
LCID lcid{ ::LocaleNameToLCID(L"qps-plocm", 0) };
```

## <a name="enable-pseudo-locales-for-enumeration"></a>Включить псевдо-национальные настройки для перечисления

В приложении можно вызвать [**енумсистемлокалесекс**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) , чтобы перечислить языковые стандарты, распознаваемые системой. Региональные и языковые параметры панели управления также вызывают **енумсистемлокалесекс** для создания списка отображаемых языковых стандартов. Однако по умолчанию четыре псевдо-локали, перечисленные выше, не распознаются системой, поэтому они не будут возвращены функцией **енумсистемлокалесекс**. Для систем с Windows Vista вплоть до Windows 10 версии 1709, решение заключается в том, чтобы включить псевдо-национальные настройки, добавив ключи в реестр Windows.

Изменения вносятся в \_ Раздел HKEY Local \_ Machine \\ System \\ CurrentControlSet \\ управления \\ ключами NLS для языков, установленных в операционной системе. Эти параметры можно использовать, чтобы включить псевдо-национальные настройки. Каждый ключ, показанный ниже, представляет собой шестнадцатеричный код, соответствующий включенному параметру псевдо-locale. Каждое значение имеет тип String (REG \_ SZ).

```
[HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Nls\Locale]
"00000501"="1" // qps-ploc (Windows Vista and later)
"000005fe"="7" // qps-ploca (Windows Vista and later)
"00000901"="1" // qps-Latn-x-sh (Windows 10 and later)
"000009ff"="d" // qps-plocm (Windows Vista and later)
```

В Windows 10, версия 1803, изменение реестра Windows не оказывает никакого влияния. Но вы по-прежнему можете вызывать интерфейсы API NLS без перечисления с именами псевдо-языков (см. Приведенные выше примеры кода) для заполнения пользовательского интерфейса.

## <a name="related-topics"></a>См. также

* [Поддержка национальных языков](using-national-language-support.md)
* [Псевдо-языковые стандарты](pseudo-locales.md)
* [енумсистемлокалесекс](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)
* [GetLocaleInfoEx](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
* [локаленаметолЦид](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
