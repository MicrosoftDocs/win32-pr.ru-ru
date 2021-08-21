---
title: Открытие и закрытие WinSNMP приложения
description: Приложение WinSNMP должно успешно вызвать функцию Снмпстартуп перед вызовом любой другой функции WinSNMP.
ms.assetid: ff2b99c9-c2fd-4bb7-8fd5-799e72c4560d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4aa18f437f8b1a430ad27b40b838859d2e00641bcb4532602715548b370acce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009252"
---
# <a name="opening-and-closing-a-winsnmp-application"></a>Открытие и закрытие WinSNMP приложения

Приложение WinSNMP должно успешно вызвать функцию [**снмпстартуп**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) перед вызовом любой другой функции WinSNMP. Функция **снмпстартуп** включает реализацию Microsoft WinSNMP для выполнения процедур инициализации. Функция также возвращает в приложение версию API-интерфейса WinSNMP, поддерживаемую реализацией, уровень поддерживаемой SNMP-связи и режимы преобразования и перепередачи по умолчанию для реализации.

Если приложению больше не требуются службы реализации, то приложение WinSNMP должно вызывать функцию [**снмпклеануп**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) . Несмотря на то, что **снмпклеануп** позволяет реализовать освобождение всех ресурсов, выделенных для приложения, рекомендуется, чтобы приложение сначала вызывало функцию [**снмпклосе**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) по одному разу для каждого открытого сеанса WinSNMP, чтобы обеспечить максимальную производительность реализации. После завершения функции WinSNMP приложение должно вызвать [**снмпклеануп**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) как последнюю функцию WinSNMP.

 

 




