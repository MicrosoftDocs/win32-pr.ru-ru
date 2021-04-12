---
description: Существует пять асинхронных операций, которые не связаны с каким бы то ни было определенным вызовом.
ms.assetid: d7107834-07e4-40ed-91ea-2e6127597c13
title: Асинхронные операции без вызова
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f4a246ab4a9022ce01d9707a7c5dc5cdc6e9e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345695"
---
# <a name="call-less-asynchronous-operations"></a>Асинхронные операции без вызова

Существует пять асинхронных операций, которые не связаны с каким бы то ни было определенным вызовом. Функции TAPI 2. x [**линедевспеЦифик**](/windows/win32/api/tapi/nf-tapi-linedevspecific), [**линедевспеЦификфеатуре**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature), [**линефорвард**](/windows/win32/api/tapi/nf-tapi-lineforward), [**линесеттерминал**](/windows/win32/api/tapi/nf-tapi-linesetterminal)и [**линеункомплетекалл**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall) инициируют эти операции. Если приложение инициирует одну из этих асинхронных операций и вызывает [**линеклосе**](/windows/win32/api/tapi/nf-tapi-lineclose), поставщик услуг может не получить указания о том, что приложение отказало от функции. Это может произойти, если приложение не было единственным приложением для открытия строки. Если приложение вызывает **линеклосе** с одной из этих операций в ожидании и это единственное приложение с маркером строки, TAPI вызывает функцию [**тспи \_ линеклосе**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) , и поставщик услуг должен завершить асинхронную операцию, вызывая функцию обратного вызова [*\_ процесса завершения*](/windows/win32/api/tspi/nc-tspi-async_completion) для каждой такой незавершенной операции с помощью \_ значения ошибки линирр оператионфаилед.

 

 
