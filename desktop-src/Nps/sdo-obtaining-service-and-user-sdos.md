---
title: Получение службы и пользователя Сдос
description: Чтобы получить Сдос для NPS (IAS) или определенного пользователя, вызовите методы Исдомачине Жетсервицесдо или Исдомачине Жетусерсдо.
ms.assetid: 23e23fb3-0102-4c36-b30f-18604131ee32
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c7562c3b7c6aa1150ba3ce6581441064eb386f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338244"
---
# <a name="obtaining-service-and-user-sdos"></a><span data-ttu-id="6461f-103">Получение службы и пользователя Сдос</span><span class="sxs-lookup"><span data-stu-id="6461f-103">Obtaining Service and User SDOs</span></span>

> [!Note]  
> <span data-ttu-id="6461f-104">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6461f-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

<span data-ttu-id="6461f-105">Чтобы получить Сдос для NPS (IAS) или определенного пользователя, вызовите методы [**исдомачине:: жетсервицесдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) или [**Исдомачине:: жетусерсдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) .</span><span class="sxs-lookup"><span data-stu-id="6461f-105">To obtain SDOs for NPS (IAS) or a particular user, call the [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) or [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) methods.</span></span> <span data-ttu-id="6461f-106">Эти методы возвращают указатели на интерфейсы [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) для этих объектов.</span><span class="sxs-lookup"><span data-stu-id="6461f-106">These methods return pointers to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interfaces for these objects.</span></span> <span data-ttu-id="6461f-107">Для пользователя SDO используйте метод [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) , чтобы получить интерфейс [**исдо**](/windows/desktop/api/sdoias/nn-sdoias-isdo) для объекта.</span><span class="sxs-lookup"><span data-stu-id="6461f-107">For the user SDO, use the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method to obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface for the object.</span></span> <span data-ttu-id="6461f-108">Для SDO службы используйте **IUnknown:: QueryInterface** для получения интерфейса [**Исдо**](/windows/desktop/api/sdoias/nn-sdoias-isdo) или интерфейса [**исдосервицеконтрол**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) .</span><span class="sxs-lookup"><span data-stu-id="6461f-108">For the service SDO, use **IUnknown::QueryInterface** to obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface or [**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) interface.</span></span>

<span data-ttu-id="6461f-109">Перед вызовом метода [**исдомачине:: жетсервицесдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) или [**Исдомачине:: Жетусерсдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo)вызовите [**исдомачине:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) , чтобы связать объект компьютера с локальным компьютером.</span><span class="sxs-lookup"><span data-stu-id="6461f-109">Before calling either [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) or [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo), call [**ISdoMachine::Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) to associate the machine object with the local computer.</span></span>

<span data-ttu-id="6461f-110">Пример кода, демонстрирующий, как получить эти Сдос, см. в разделе [Получение SDO службы](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) и [Получение пользовательского SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) .</span><span class="sxs-lookup"><span data-stu-id="6461f-110">See [Retrieving a Service SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) and [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) for sample code that demonstrates how to obtain these SDOs.</span></span>

 

 