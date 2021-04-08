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
# <a name="opening-and-closing-a-winsnmp-application"></a>Открытие и закрытие WinSNMP приложения

Приложение WinSNMP должно успешно вызвать функцию [**снмпстартуп**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) перед вызовом любой другой функции WinSNMP. Функция **снмпстартуп** включает реализацию Microsoft WinSNMP для выполнения процедур инициализации. Функция также возвращает в приложение версию API-интерфейса WinSNMP, поддерживаемую реализацией, уровень поддерживаемой SNMP-связи и режимы преобразования и перепередачи по умолчанию для реализации.

Если приложению больше не требуются службы реализации, то приложение WinSNMP должно вызывать функцию [**снмпклеануп**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) . Несмотря на то, что **снмпклеануп** позволяет реализовать освобождение всех ресурсов, выделенных для приложения, рекомендуется, чтобы приложение сначала вызывало функцию [**снмпклосе**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) по одному разу для каждого открытого сеанса WinSNMP, чтобы обеспечить максимальную производительность реализации. После завершения функции WinSNMP приложение должно вызвать [**снмпклеануп**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) как последнюю функцию WinSNMP.

 

 




