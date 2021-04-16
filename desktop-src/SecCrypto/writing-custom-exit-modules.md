---
description: Пользовательские модули выхода должны реализовывать интерфейс Ицертексит, который вызывается ядром сервера.
ms.assetid: 509e7945-b656-4c4c-b5eb-45fbe80377c7
title: Написание пользовательских модулей выхода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81798996059e878ef11dbcdf290298094d0849cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664228"
---
# <a name="writing-custom-exit-modules"></a><span data-ttu-id="36e4b-103">Написание пользовательских модулей выхода</span><span class="sxs-lookup"><span data-stu-id="36e4b-103">Writing Custom Exit Modules</span></span>

<span data-ttu-id="36e4b-104">Пользовательские модули выхода должны реализовывать интерфейс [**ицертексит**](/windows/desktop/api/Certexit/nn-certexit-icertexit) , который вызывается ядром сервера.</span><span class="sxs-lookup"><span data-stu-id="36e4b-104">Custom exit modules must implement the [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) interface, which is called by the server engine.</span></span> <span data-ttu-id="36e4b-105">Метод [**ицертексит:: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) вызывается ядром сервера при загрузке модуля Exit.</span><span class="sxs-lookup"><span data-stu-id="36e4b-105">The [**ICertExit::Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) method is called by the server engine when the exit module is loaded.</span></span> <span data-ttu-id="36e4b-106">Он позволяет модулю Exit выполнять инициализацию и возвращать значение, которое информирует серверный механизм о том, для каких событий требуется уведомление.</span><span class="sxs-lookup"><span data-stu-id="36e4b-106">It allows the exit module to perform initialization and returns a value that informs the server engine of the kinds of events for which it wants notification.</span></span> <span data-ttu-id="36e4b-107">Метод [**ицертексит::-Description**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) должен возвращать строку описания, когда подсистема сервера запрашивает его.</span><span class="sxs-lookup"><span data-stu-id="36e4b-107">The [**ICertExit::GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) method must return a description string when the server engine requests it.</span></span> <span data-ttu-id="36e4b-108">Метод [**ицертексит:: notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) вызывается ядром сервера для уведомления модуля выхода о том, что произошло событие.</span><span class="sxs-lookup"><span data-stu-id="36e4b-108">The [**ICertExit::Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) method is called by the server engine to notify the exit module that an event has occurred.</span></span>

<span data-ttu-id="36e4b-109">Модули выхода могут вызывать интерфейс [**ицертсерверексит**](/windows/desktop/api/Certif/nn-certif-icertserverexit) , который поддерживает многие из тех же методов, что и интерфейс [**ицертсерверполици**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) , за исключением методов [**сетцертификатикстенсион**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) и [**сетцертификатепроперти**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) .</span><span class="sxs-lookup"><span data-stu-id="36e4b-109">Exit modules can call the [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) interface, which supports many of the same methods as the [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) interface, with the exception of the [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) and [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) methods.</span></span>

<span data-ttu-id="36e4b-110">Сведения об удалении существующего модуля Exit и установке нового см. в разделе о настройке модуля выхода в справке.</span><span class="sxs-lookup"><span data-stu-id="36e4b-110">For information about removing the existing exit module and installing a new one, see the Exit Module Customization topic in Help.</span></span>

 

 



