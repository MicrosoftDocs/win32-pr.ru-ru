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
# <a name="call-less-asynchronous-operations"></a><span data-ttu-id="6914b-103">Асинхронные операции без вызова</span><span class="sxs-lookup"><span data-stu-id="6914b-103">Call-less Asynchronous Operations</span></span>

<span data-ttu-id="6914b-104">Существует пять асинхронных операций, которые не связаны с каким бы то ни было определенным вызовом.</span><span class="sxs-lookup"><span data-stu-id="6914b-104">There are five asynchronous operations that are not related to any particular call.</span></span> <span data-ttu-id="6914b-105">Функции TAPI 2. x [**линедевспеЦифик**](/windows/win32/api/tapi/nf-tapi-linedevspecific), [**линедевспеЦификфеатуре**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature), [**линефорвард**](/windows/win32/api/tapi/nf-tapi-lineforward), [**линесеттерминал**](/windows/win32/api/tapi/nf-tapi-linesetterminal)и [**линеункомплетекалл**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall) инициируют эти операции.</span><span class="sxs-lookup"><span data-stu-id="6914b-105">The TAPI 2.x [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific), [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature), [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward), [**lineSetTerminal**](/windows/win32/api/tapi/nf-tapi-linesetterminal), and [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall) functions initiate these operations.</span></span> <span data-ttu-id="6914b-106">Если приложение инициирует одну из этих асинхронных операций и вызывает [**линеклосе**](/windows/win32/api/tapi/nf-tapi-lineclose), поставщик услуг может не получить указания о том, что приложение отказало от функции.</span><span class="sxs-lookup"><span data-stu-id="6914b-106">If an application initiates one of these asynchronous operations and calls [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose), the service provider may receive no indication that the application has abandoned the function.</span></span> <span data-ttu-id="6914b-107">Это может произойти, если приложение не было единственным приложением для открытия строки.</span><span class="sxs-lookup"><span data-stu-id="6914b-107">This can occur if the application was not the only application to have the line open.</span></span> <span data-ttu-id="6914b-108">Если приложение вызывает **линеклосе** с одной из этих операций в ожидании и это единственное приложение с маркером строки, TAPI вызывает функцию [**тспи \_ линеклосе**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) , и поставщик услуг должен завершить асинхронную операцию, вызывая функцию обратного вызова [*\_ процесса завершения*](/windows/win32/api/tspi/nc-tspi-async_completion) для каждой такой незавершенной операции с помощью \_ значения ошибки линирр оператионфаилед.</span><span class="sxs-lookup"><span data-stu-id="6914b-108">If the application calls **lineClose** with one of these operations pending, and it is the only application with a handle to the line, TAPI calls the [**TSPI\_lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) function and the service provider should terminate the asynchronous operation, calling the [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) callback function for each such outstanding operation with the LINEERR\_OPERATIONFAILED error value.</span></span>

 

 
