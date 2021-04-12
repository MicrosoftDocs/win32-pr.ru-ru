---
title: Создание WinSNMP Applications с несколькими потоками
description: Реализация Microsoft WinSNMP гарантирует, что операции WinSNMP одного процесса не изменяют параметры WinSNMP другого процесса.
ms.assetid: faa98704-f55f-4450-9f6e-d2bbbc7a50b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb6b7991968c5c5efafa898758c3c60cad1abb2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413268"
---
# <a name="writing-winsnmp-applications-with-multiple-threads"></a>Создание WinSNMP Applications с несколькими потоками

Реализация Microsoft WinSNMP гарантирует, что операции WinSNMP одного процесса не изменяют параметры WinSNMP другого процесса.

WinSNMP-приложение с несколькими потоками должно обеспечивать потокобезопасность операций WinSNMP, устанавливающих параметры уровня приложения. Функции, устанавливающие параметры уровня приложения, — [**снмпсеттранслатемоде**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) и [**снмпсетретрансмитмоде**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode). Эти функции изменяют параметры для режима преобразования сущностей и контекста и режим повторной передачи.

Дополнительные сведения см. в разделе [множественные потоки](/windows/desktop/ProcThread/multiple-threads) , [безопасность потоков и права доступа](/windows/desktop/ProcThread/thread-security-and-access-rights).

 

 