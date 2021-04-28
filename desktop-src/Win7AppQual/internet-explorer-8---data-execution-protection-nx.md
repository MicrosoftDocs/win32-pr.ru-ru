---
description: Internet Explorer 8 — Защита выполнения данных/NX
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: Internet Explorer 8 — Защита выполнения данных/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb0208cc20e78c30f42b09af78460990be20b002
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088252"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a>Internet Explorer 8 — Защита выполнения данных/NX

## <a name="affected-platforms"></a>Затронутые платформы

 **Клиенты** — Windows XP, Windows Vista, Windows 7  
**Серверы** — windows Server 2003, windows Server 2008, windows Server 2008 R2  










> [!Note]  
> Internet Explorer 8 включит защиту DEP/NX при запуске в операционной системе с последним пакетом обновления. В Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1 и Windows Server 2008 по умолчанию DEP/NX включено в Internet Explorer 8.

 

## <a name="feature-impact"></a>Воздействие на функции

**Серьезность** — средний  
**Частота** -низкая  

> [!Note]  
> Как правило, любое приложение, работающее в Internet Explorer и несовместимое с DEP/NX, приведет к сбою при запуске и не будет работать. Internet Explorer может аварийно завершить работу при запуске, если установлены надстройки, несовместимые с DEP/NX.

 

## <a name="description"></a>Описание

DEP/NX — это функция безопасности, которая помогает устранить уязвимости, связанные с памятью. Начиная с Internet Explorer 8, все процессы Internet Explorer по умолчанию включают функцию DEP/NX.

## <a name="manifestation-of-impact"></a>Влияние на манифесты

Ядро Windows отслеживает выполнение программы. Если ядро обнаруживает попытку выполнить код на странице памяти, которая не помечена как исполняемый объект, ядро прерывает выполнение программы, что приводит к сбою. Это мера безопасности, позволяющая гарантировать, что уязвимости, связанные с памятью (например, переполнения буфера) в приложении, нельзя использовать для выполнения произвольного кода.

## <a name="end-user-mitigation"></a>Устранение End-User

-   Установите более позднюю версию надстройки или платформы, совместимую с DEP/NX.
-   Запустите Internet Explorer с правами администратора, а затем отключите DEP/NX с помощью флажка **включить защиту памяти для предотвращения атак** из Интернета на вкладке **Свойства обозревателя**  /  **Дополнительно** .

## <a name="developer-solution"></a>Решение для разработчиков

Скомпилируйте приложения с помощью последних версий платформ, совместимых с DEP.

## <a name="leveraging-feature-capabilities"></a>Использование возможностей функций

-   Использование параметра компоновщика/NXCOMPAT для указания совместимости DEP/NX
-   Применяйте свой код к другим доступным средствам защиты, таким как защита стека (/GS), защищенная обработка исключений (/SafeSEH) и ASLR (/DynamicBase)

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Совместимость, производительность, надежность и тестирование на удобство использования

-   Протестируйте код с включенной функцией DEP/NX с помощью последней выпущенной версии Internet Explorer в Windows Vista SP1 или более поздней версии.
-   Протестируйте Internet Explorer 7 в Windows Vista после включения параметра DEP/NX. Чтобы включить DEP/NX для Internet Explorer 7, запустите Internet Explorer от имени администратора, а затем установите соответствующий флажок в меню Сервис > свойства обозревателя > вкладка Дополнительно.
-   Запустите средство тестирования совместимости Internet Explorer (ИЕКТТ), входящее в состав набора средств для обеспечения совместимости приложений (ACT), для выявления потенциальных проблем, связанных с изменениями DEP/NX.

## <a name="links-to-other-resources"></a>Ссылки на другие ресурсы

-   [Internet Explorer 8 Security, часть I: защита памяти DEP/NX](/archive/blogs/ie/)
-   [Предотвращение выполнения данных](../memory/data-execution-prevention.md)
-   [Новые API-интерфейсы NX, добавленные в Windows Vista SP1, Windows XP SP3 и Windows Server 2008 R2](/archive/blogs/michael_howard/)
-   [Загрузка набора средств для обеспечения совместимости приложений](/windows-hardware/get-started/adk-install)
-   [Известные проблемы с функциями безопасности в Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
