---
description: Internet Explorer 8 — Защита выполнения данных/NX
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: Internet Explorer 8 — Защита выполнения данных/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1f969aa2e934f36142995150b6484dad2fa5067f6cbb5ab3a947055af375ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998894"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a>Internet Explorer 8 — Защита выполнения данных/NX

## <a name="affected-platforms"></a>Затронутые платформы

 **клиенты** — Windows XP, Windows Vista, Windows 7  
**серверы** — Windows server 2003, Windows server 2008, Windows server 2008 R2  










> [!Note]  
> Internet Explorer 8 включит защиту DEP/NX при запуске в операционной системе с последним пакетом обновления. Windows в XP sp3, Windows server 2003 SP3, Windows Vista с пакетом обновления 1 (SP1) и Windows Server 2008 по умолчанию DEP/NX включены в Internet Explorer 8.

 

## <a name="feature-impact"></a>Воздействие на функции

**Серьезность** — средний  
**Частота** -низкая  

> [!Note]  
> Как правило, любое приложение, работающее в Internet Explorer и несовместимое с DEP/NX, приведет к сбою при запуске и не будет работать. Internet Explorer может аварийно завершить работу при запуске, если установлены надстройки, несовместимые с DEP/NX.

 

## <a name="description"></a>Описание

DEP/NX — это функция безопасности, которая помогает устранить уязвимости, связанные с памятью. Начиная с Internet Explorer 8, все процессы Internet Explorer по умолчанию включают функцию DEP/NX.

## <a name="manifestation-of-impact"></a>Влияние на манифесты

ядро Windows отслеживает выполнение программы. Если ядро обнаруживает попытку выполнить код на странице памяти, которая не помечена как исполняемый объект, ядро прерывает выполнение программы, что приводит к сбою. Это мера безопасности, позволяющая гарантировать, что уязвимости, связанные с памятью (например, переполнения буфера) в приложении, нельзя использовать для выполнения произвольного кода.

## <a name="end-user-mitigation"></a>Устранение End-User

-   Установите более позднюю версию надстройки или платформы, совместимую с DEP/NX.
-   Запустите Internet Explorer с правами администратора, а затем отключите DEP/NX с помощью флажка **включить защиту памяти для предотвращения атак** из Интернета на вкладке **Свойства обозревателя**  /  **Дополнительно** .

## <a name="developer-solution"></a>Решение для разработчиков

Скомпилируйте приложения с помощью последних версий платформ, совместимых с DEP.

## <a name="leveraging-feature-capabilities"></a>Использование возможностей функций

-   Использование параметра компоновщика/NXCOMPAT для указания совместимости DEP/NX
-   Применяйте свой код к другим доступным средствам защиты, таким как защита стека (/GS), защищенная обработка исключений (/SafeSEH) и ASLR (/DynamicBase)

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Совместимость, производительность, надежность и тестирование на удобство использования

-   протестируйте код с включенной функцией DEP/NX с помощью последней выпущенной версии Internet Explorer в Windows Vista SP1 или более поздней версии.
-   протестируйте Internet Explorer 7 в Windows Vista после включения параметра DEP/NX. Чтобы включить DEP/NX для Internet Explorer 7, запустите Internet Explorer от имени администратора, а затем установите соответствующий флажок в меню Сервис > свойства обозревателя > вкладка Дополнительно.
-   запустите средство тестирования совместимости Internet Explorer (иектт), поставляемое вместе с набор средств совместимости приложений (акт), чтобы узнать о возможных проблемах, связанных с изменениями DEP/NX.

## <a name="links-to-other-resources"></a>Ссылки на другие ресурсы

-   [Internet Explorer 8 Security, часть I: защита памяти DEP/NX](/archive/blogs/ie/)
-   [Предотвращение выполнения данных](../memory/data-execution-prevention.md)
-   [добавлены новые api-интерфейсы NX для Windows Vista с пакетом обновления 1 (SP1), Windows XP SP3 и Windows Server 2008 R2](/archive/blogs/michael_howard/)
-   [загрузка набор средств совместимости приложений](/windows-hardware/get-started/adk-install)
-   [Известные проблемы с функциями безопасности в Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
