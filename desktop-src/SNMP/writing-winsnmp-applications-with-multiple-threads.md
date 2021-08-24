---
title: Создание WinSNMP Applications с несколькими потоками
description: Реализация Microsoft WinSNMP гарантирует, что операции WinSNMP одного процесса не изменяют параметры WinSNMP другого процесса.
ms.assetid: faa98704-f55f-4450-9f6e-d2bbbc7a50b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33ee400009204a1117eb54b8166ade2c10f3d1dd3317a8316d70fc8c2d606d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142737"
---
# <a name="writing-winsnmp-applications-with-multiple-threads"></a>Создание WinSNMP Applications с несколькими потоками

Реализация Microsoft WinSNMP гарантирует, что операции WinSNMP одного процесса не изменяют параметры WinSNMP другого процесса.

WinSNMP-приложение с несколькими потоками должно обеспечивать потокобезопасность операций WinSNMP, устанавливающих параметры уровня приложения. Функции, устанавливающие параметры уровня приложения, — [**снмпсеттранслатемоде**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) и [**снмпсетретрансмитмоде**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode). Эти функции изменяют параметры для режима преобразования сущностей и контекста и режим повторной передачи.

Дополнительные сведения см. в разделе [множественные потоки](/windows/desktop/ProcThread/multiple-threads) , [безопасность потоков и права доступа](/windows/desktop/ProcThread/thread-security-and-access-rights).

 

 