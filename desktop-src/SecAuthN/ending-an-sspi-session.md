---
description: Когда клиент завершит взаимодействие с любым сервером или закончит использовать дополнительные учетные данные, переданные функции AcquireCredentialsHandle, клиент должен вызвать функцию Фрикредентиалшандле.
ms.assetid: fa943e9b-d379-441f-8c6e-f0a0f5f7f1a3
title: Завершение сеанса SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1fdc51ba1c31ae4ac8abb52c6d4c4372a9d161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809347"
---
# <a name="ending-an-sspi-session"></a>Завершение сеанса SSPI

После завершения взаимодействия между клиентом и сервером обе стороны вызывают функцию [**делетесекуритиконтекст**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) с соответствующими дескрипторами контекста. Когда клиент завершит взаимодействие с любым сервером или закончит использовать дополнительные учетные данные, переданные функции [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , клиент должен вызвать функцию [**фрикредентиалшандле**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) . Когда сервер готов к завершению работы и перед выгрузкой библиотеки DLL, сервер должен вызвать **делетесекуритиконтекст**.

 

 
