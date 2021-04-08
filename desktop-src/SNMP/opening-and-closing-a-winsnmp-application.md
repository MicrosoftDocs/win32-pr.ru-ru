---
title: Открытие и закрытие WinSNMP приложения
description: Приложение WinSNMP должно успешно вызвать функцию Снмпстартуп перед вызовом любой другой функции WinSNMP.
ms.assetid: ff2b99c9-c2fd-4bb7-8fd5-799e72c4560d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f960a22a6155d3f3eeec770af361fac2c0eb036e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068300"
---
# <a name="opening-and-closing-a-winsnmp-application"></a><span data-ttu-id="c764e-103">Открытие и закрытие WinSNMP приложения</span><span class="sxs-lookup"><span data-stu-id="c764e-103">Opening and Closing a WinSNMP Application</span></span>

<span data-ttu-id="c764e-104">Приложение WinSNMP должно успешно вызвать функцию [**снмпстартуп**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) перед вызовом любой другой функции WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="c764e-104">The WinSNMP application must call the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function successfully before it calls any other WinSNMP function.</span></span> <span data-ttu-id="c764e-105">Функция **снмпстартуп** включает реализацию Microsoft WinSNMP для выполнения процедур инициализации.</span><span class="sxs-lookup"><span data-stu-id="c764e-105">The **SnmpStartup** function enables the Microsoft WinSNMP implementation to perform initialization procedures.</span></span> <span data-ttu-id="c764e-106">Функция также возвращает в приложение версию API-интерфейса WinSNMP, поддерживаемую реализацией, уровень поддерживаемой SNMP-связи и режимы преобразования и перепередачи по умолчанию для реализации.</span><span class="sxs-lookup"><span data-stu-id="c764e-106">The function also returns to the application the version of the WinSNMP API that the implementation supports, the level of SNMP communications it supports, and the implementation's default translation and retransmission modes.</span></span>

<span data-ttu-id="c764e-107">Если приложению больше не требуются службы реализации, то приложение WinSNMP должно вызывать функцию [**снмпклеануп**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) .</span><span class="sxs-lookup"><span data-stu-id="c764e-107">The WinSNMP application must call the [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) function when the application no longer requires the implementation's services.</span></span> <span data-ttu-id="c764e-108">Несмотря на то, что **снмпклеануп** позволяет реализовать освобождение всех ресурсов, выделенных для приложения, рекомендуется, чтобы приложение сначала вызывало функцию [**снмпклосе**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) по одному разу для каждого открытого сеанса WinSNMP, чтобы обеспечить максимальную производительность реализации.</span><span class="sxs-lookup"><span data-stu-id="c764e-108">Even though **SnmpCleanup** enables the implementation to deallocate all resources allocated to the application, it is recommended that the application first call the [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) function once for each open WinSNMP session, to maximize the implementation's performance.</span></span> <span data-ttu-id="c764e-109">После завершения функции WinSNMP приложение должно вызвать [**снмпклеануп**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) как последнюю функцию WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="c764e-109">The WinSNMP application must call [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) as the last WinSNMP function before it terminates.</span></span>

 

 




