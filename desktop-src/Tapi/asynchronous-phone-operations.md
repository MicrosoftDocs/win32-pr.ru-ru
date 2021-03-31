---
description: Есть девять асинхронных операций, связанных с телефонами.
ms.assetid: b255bdde-1677-401f-b02d-4850e0e98dc4
title: Асинхронные операции на телефоне
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4a70a1d980c4f0d42d5160ee020531b538f488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911216"
---
# <a name="asynchronous-phone-operations"></a><span data-ttu-id="7605a-103">Асинхронные операции на телефоне</span><span class="sxs-lookup"><span data-stu-id="7605a-103">Asynchronous Phone Operations</span></span>

<span data-ttu-id="7605a-104">Есть девять асинхронных операций, связанных с телефонами.</span><span class="sxs-lookup"><span data-stu-id="7605a-104">There are nine asynchronous operations related to phones.</span></span> <span data-ttu-id="7605a-105">Они инициируются функциями [**тспи \_ фонедевспеЦифик**](/windows/win32/api/tspi/nf-tspi-tspi_phonedevspecific), [**тспи \_ фонесетбуттонинфо**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo), [**тспи \_ фонесетдата**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdata), [**тспи \_ фонесетдисплай**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdisplay), [**TSPI \_ phoneSetGain**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetgain), [**TSPI \_ phoneSetHookSwitch**](/windows/win32/api/tspi/nf-tspi-tspi_phonesethookswitch), [**TSPI \_ phoneSetLamp**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetlamp), [**TSPI \_ phoneSetRing**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetring)и [**TSPI \_ phoneSetVolume**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetvolume) .</span><span class="sxs-lookup"><span data-stu-id="7605a-105">These are initiated by the [**TSPI\_phoneDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_phonedevspecific), [**TSPI\_phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo), [**TSPI\_phoneSetData**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdata), [**TSPI\_phoneSetDisplay**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdisplay), [**TSPI\_phoneSetGain**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetgain), [**TSPI\_phoneSetHookSwitch**](/windows/win32/api/tspi/nf-tspi-tspi_phonesethookswitch), [**TSPI\_phoneSetLamp**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetlamp), [**TSPI\_phoneSetRing**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetring), and [**TSPI\_phoneSetVolume**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetvolume) functions.</span></span> <span data-ttu-id="7605a-106">Если приложение вызывает функцию TAPI [**фонеклосе**](/windows/win32/api/tapi/nf-tapi-phoneclose) и имеет единственный маркер телефона, TAPI вызывает функцию [**тспи \_ фонеклосе**](/windows/win32/api/tspi/nf-tspi-tspi_phoneclose) , чтобы направить поставщику услуг на завершение асинхронных операций и вызвать функцию обратного вызова [*\_ процедуры завершения*](/windows/win32/api/tspi/nc-tspi-async_completion) , если это уместно.</span><span class="sxs-lookup"><span data-stu-id="7605a-106">If an application calls the TAPI [**phoneClose**](/windows/win32/api/tapi/nf-tapi-phoneclose) function and has the only handle to the phone, TAPI calls the [**TSPI\_phoneClose**](/windows/win32/api/tspi/nf-tspi-tspi_phoneclose) function to direct the service provider to terminate the asynchronous operations and call the [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) callback function as appropriate.</span></span> <span data-ttu-id="7605a-107">Если у приложения нет единственного маркера для телефона, поставщик услуг не получает уведомления о запросе, а все необработанные асинхронные операции остаются активными.</span><span class="sxs-lookup"><span data-stu-id="7605a-107">If the application does not have the only handle to the phone, the service provider receives no notification of the request and any outstanding asynchronous operations remain active.</span></span>

 

 
