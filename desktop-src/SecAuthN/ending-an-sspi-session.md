---
description: Когда клиент завершит взаимодействие с любым сервером или закончит использовать дополнительные учетные данные, переданные функции AcquireCredentialsHandle, клиент должен вызвать функцию Фрикредентиалшандле.
ms.assetid: fa943e9b-d379-441f-8c6e-f0a0f5f7f1a3
title: Завершение сеанса SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4669d3143b480df20f1a5f1d76e73cc75802766d1db83da9b75d304e256ae4dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008272"
---
# <a name="ending-an-sspi-session"></a>Завершение сеанса SSPI

После завершения взаимодействия между клиентом и сервером обе стороны вызывают функцию [**делетесекуритиконтекст**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) с соответствующими дескрипторами контекста. Когда клиент завершит взаимодействие с любым сервером или закончит использовать дополнительные учетные данные, переданные функции [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , клиент должен вызвать функцию [**фрикредентиалшандле**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) . Когда сервер готов к завершению работы и перед выгрузкой библиотеки DLL, сервер должен вызвать **делетесекуритиконтекст**.

 

 
