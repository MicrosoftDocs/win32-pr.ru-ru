---
description: использование платформа .NET Framework 4 с приложениями, созданными на основе более ранних версий
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: использование платформа .NET Framework 4 с приложениями, созданными на основе более ранних версий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12eb34b00cfe14a18e83e7726f1ffa962ba03f8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884751"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a>использование платформа .NET Framework 4 с приложениями, созданными на основе более ранних версий

## <a name="platform"></a>Платформа

 **клиенты** — Windows XP, Windows Vista, Windows 7  
**серверы** — Windows server 2003, Windows server 2008, Windows server 2008 R2  


## <a name="feature-impact"></a>Воздействие на функции

 **Серьезность** — низкая  
**Частота** — высокая  






## <a name="description"></a>Описание

платформа .NET Framework 4 обеспечивает высокую совместимость с приложениями, созданными с помощью более ранних версий платформа .NET Framework. основные изменения в платформа .NET Framework 4 предназначены для повышения безопасности, соответствия стандартам, правильности, надежности и производительности.

однако платформа .NET Framework 4 не будет автоматически использовать свою версию среды clr для запуска приложений, созданных с помощью более ранних версий платформа .NET Framework.

## <a name="manifestation"></a>Проявление

если приложение создано с помощью более ранней платформа .NET Framework и пользователь открывает это приложение на компьютере, где установлены платформа .NET Framework 4 и более ранняя версия платформа .NET Framework, то приложение использует предыдущую версию среды CLR.

однако если платформа .NET Framework 4 является единственной версией среды выполнения, установленной на компьютере, приложение создает исключение и предлагает пользователю установить версию среды выполнения, для которой было создано приложение.

## <a name="solution"></a>Решение

для запуска приложений, созданных с помощью более ранних версий платформа .NET Framework с платформа .NET Framework 4, необходимо скомпилировать приложение для целевой версии платформа .NET Framework 4, указав его в свойствах проекта в Microsoft Visual Studio, или можно указать платформа .NET Framework 4 в [**&lt; &gt; элементе supportedRuntime**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) в файле конфигурации приложения.

дополнительные сведения о переходе на платформа .NET Framework 4 см. в разделе [руководство по миграции по платформа .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) и [совместимости версий в платформа .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).

## <a name="compatibility-tests"></a>Тесты на совместимость

После внесения изменений проверьте приложение, чтобы убедиться, что оно выполняется правильно. совместимость можно проверить, как описано в разделе о [совместимости приложений платформа .NET Framework 4](/previous-versions/dd889541(v=msdn.10)) .

если приложение или компонент не работает после установки платформа .NET Framework 4, отправьте ошибку на веб-сайт [Microsoft Подключение](https://connect.microsoft.com/visualstudio) .

## <a name="links-to-other-resources"></a>Ссылки на другие ресурсы

-   [**&lt;supportedRuntime, &gt; элемент**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))
-   [Руководство. Миграция в .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))
-   [Совместимость версий в .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))
-   **пошаговое руководство по совместимости приложений платформа .NET Framework 4 RTM:**<https://msdn.microsoft.com/library/dd889541.aspx>
-   [Microsoft Connect](https://connect.microsoft.com/)

 

 
