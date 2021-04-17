---
description: Использование платформа .NET Framework 4 с приложениями, созданными на основе более ранних версий
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: Использование платформа .NET Framework 4 с приложениями, созданными на основе более ранних версий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ef252d128ae5d3c8f5b85ef486828fb82e152d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703401"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a>Использование платформа .NET Framework 4 с приложениями, созданными на основе более ранних версий

## <a name="platform"></a>Платформа

 **Клиенты** — Windows XP Windows Vista, Windows \| \| 7  
**Серверы** — windows Server 2003 windows \| Server 2008 \| Windows Server 2008 R2  


## <a name="feature-impact"></a>Воздействие на функции

 **Серьезность** — низкая  
**Частота** — высокая  






## <a name="description"></a>Описание

Платформа .NET Framework 4 обеспечивает высокую совместимость с приложениями, созданными с помощью более ранних версий платформа .NET Framework. Основные изменения в платформа .NET Framework 4 предназначены для повышения безопасности, соответствия стандартам, правильности, надежности и производительности.

Однако платформа .NET Framework 4 не будет автоматически использовать свою версию среды CLR для запуска приложений, созданных с помощью более ранних версий платформа .NET Framework.

## <a name="manifestation"></a>Проявление

Если приложение создано с помощью более ранней платформа .NET Framework и пользователь открывает это приложение на компьютере, где установлены платформа .NET Framework 4 и более ранняя версия платформа .NET Framework, то приложение использует предыдущую версию среды CLR.

Однако если платформа .NET Framework 4 является единственной версией среды выполнения, установленной на компьютере, приложение создает исключение и предлагает пользователю установить версию среды выполнения, для которой было создано приложение.

## <a name="solution"></a>Решение

Для запуска приложений, созданных с помощью более ранних версий платформа .NET Framework с платформа .NET Framework 4, необходимо скомпилировать приложение для целевой версии платформа .NET Framework 4, указав его в свойствах проекта в Microsoft Visual Studio, или можно указать платформа .NET Framework 4 в [**<supportedRuntime> элементе**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) в файле конфигурации приложения.

Дополнительные сведения о переходе на платформа .NET Framework 4 см. в разделе [руководство по миграции по платформа .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) и [совместимости версий в платформа .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).

## <a name="compatibility-tests"></a>Тесты на совместимость

После внесения изменений проверьте приложение, чтобы убедиться, что оно выполняется правильно. Совместимость можно проверить, как описано в разделе о [совместимости приложений платформа .NET Framework 4](/previous-versions/dd889541(v=msdn.10)) .

Если приложение или компонент не работает после установки платформа .NET Framework 4, отправьте сообщение об ошибке через веб-сайт [Microsoft Connect](https://connect.microsoft.com/visualstudio) .

## <a name="links-to-other-resources"></a>Ссылки на другие ресурсы

-   [**<supportedRuntime> дерев**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))
-   [Руководство. Миграция в .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))
-   [Совместимость версий в .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))
-   **Пошаговое руководство по совместимости приложений платформа .NET Framework 4 RTM:**<https://msdn.microsoft.com/library/dd889541.aspx>
-   [Microsoft Connect](https://connect.microsoft.com/)

 

 
