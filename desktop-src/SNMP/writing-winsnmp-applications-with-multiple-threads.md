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
# <a name="writing-winsnmp-applications-with-multiple-threads"></a><span data-ttu-id="f51a9-103">Создание WinSNMP Applications с несколькими потоками</span><span class="sxs-lookup"><span data-stu-id="f51a9-103">Writing WinSNMP Applications with Multiple Threads</span></span>

<span data-ttu-id="f51a9-104">Реализация Microsoft WinSNMP гарантирует, что операции WinSNMP одного процесса не изменяют параметры WinSNMP другого процесса.</span><span class="sxs-lookup"><span data-stu-id="f51a9-104">The Microsoft WinSNMP implementation ensures that the WinSNMP operations of one process do not modify the WinSNMP settings of another process.</span></span>

<span data-ttu-id="f51a9-105">WinSNMP-приложение с несколькими потоками должно обеспечивать потокобезопасность операций WinSNMP, устанавливающих параметры уровня приложения.</span><span class="sxs-lookup"><span data-stu-id="f51a9-105">A WinSNMP application with multiple threads must ensure that WinSNMP operations that set application-level parameters are thread-safe.</span></span> <span data-ttu-id="f51a9-106">Функции, устанавливающие параметры уровня приложения, — [**снмпсеттранслатемоде**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) и [**снмпсетретрансмитмоде**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode).</span><span class="sxs-lookup"><span data-stu-id="f51a9-106">The functions that set application-level parameters are [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) and [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode).</span></span> <span data-ttu-id="f51a9-107">Эти функции изменяют параметры для режима преобразования сущностей и контекста и режим повторной передачи.</span><span class="sxs-lookup"><span data-stu-id="f51a9-107">These functions modify settings for the entity and context translation mode and the retransmission mode.</span></span>

<span data-ttu-id="f51a9-108">Дополнительные сведения см. в разделе [множественные потоки](/windows/desktop/ProcThread/multiple-threads) , [безопасность потоков и права доступа](/windows/desktop/ProcThread/thread-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="f51a9-108">For more information, see [Multiple Threads](/windows/desktop/ProcThread/multiple-threads) and [Thread Security and Access Rights](/windows/desktop/ProcThread/thread-security-and-access-rights).</span></span>

 

 