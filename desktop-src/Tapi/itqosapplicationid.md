---
description: Интерфейс Иткосаппликатионид предоставляет метод, позволяющий приложению получить идентификатор качества обслуживания для текущего вызова.
ms.assetid: 1df50b3a-bd16-4e9b-afca-b025bfe537a4
title: Интерфейс Иткосаппликатионид (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23df8da80798cc52ecd73b4f29288812f3774d9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680053"
---
# <a name="itqosapplicationid-interface"></a><span data-ttu-id="625de-103">Интерфейс Иткосаппликатионид</span><span class="sxs-lookup"><span data-stu-id="625de-103">ITQOSApplicationID interface</span></span>

<span data-ttu-id="625de-104">\[ Этот интерфейс недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="625de-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="625de-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="625de-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="625de-106">Интерфейс **иткосаппликатионид** предоставляет метод, позволяющий приложению получить идентификатор качества обслуживания для текущего вызова.</span><span class="sxs-lookup"><span data-stu-id="625de-106">The **ITQOSApplicationID** interface exposes a method that allows an application to get the QOS identifier for the current call.</span></span>

<span data-ttu-id="625de-107">Этот интерфейс реализуется с помощью [ИПКОНФ MSP](ipconf-msp.md) и предоставляется только в том случае, если вызов использует конференции IP.</span><span class="sxs-lookup"><span data-stu-id="625de-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and is exposed only when a call uses IP Conferencing.</span></span>

## <a name="members"></a><span data-ttu-id="625de-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="625de-108">Members</span></span>

<span data-ttu-id="625de-109">Интерфейс **иткосаппликатионид** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="625de-109">The **ITQOSApplicationID** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="625de-110">**Иткосаппликатионид** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="625de-110">**ITQOSApplicationID** also has these types of members:</span></span>

-   [<span data-ttu-id="625de-111">Методы</span><span class="sxs-lookup"><span data-stu-id="625de-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="625de-112">Методы</span><span class="sxs-lookup"><span data-stu-id="625de-112">Methods</span></span>

<span data-ttu-id="625de-113">Интерфейс **иткосаппликатионид** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="625de-113">The **ITQOSApplicationID** interface has these methods.</span></span>



| <span data-ttu-id="625de-114">Метод</span><span class="sxs-lookup"><span data-stu-id="625de-114">Method</span></span>                                                                | <span data-ttu-id="625de-115">Описание</span><span class="sxs-lookup"><span data-stu-id="625de-115">Description</span></span>                         |
|:----------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="625de-116">**сеткосаппликатионид**</span><span class="sxs-lookup"><span data-stu-id="625de-116">**SetQOSApplicationID**</span></span>](itqosapplicationid-setqosapplicationid.md) | <span data-ttu-id="625de-117">Задает идентификатор качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="625de-117">Sets the QOS identifier.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="625de-118">Требования</span><span class="sxs-lookup"><span data-stu-id="625de-118">Requirements</span></span>



| <span data-ttu-id="625de-119">Требование</span><span class="sxs-lookup"><span data-stu-id="625de-119">Requirement</span></span> | <span data-ttu-id="625de-120">Значение</span><span class="sxs-lookup"><span data-stu-id="625de-120">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="625de-121">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="625de-121">TAPI version</span></span><br/> | <span data-ttu-id="625de-122">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="625de-122">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="625de-123">Header</span><span class="sxs-lookup"><span data-stu-id="625de-123">Header</span></span><br/>       | <dl> <span data-ttu-id="625de-124"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="625de-124"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="625de-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="625de-125">Library</span></span><br/>      | <dl> <span data-ttu-id="625de-126"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="625de-126"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="625de-127">DLL</span><span class="sxs-lookup"><span data-stu-id="625de-127">DLL</span></span><br/>          | <dl> <span data-ttu-id="625de-128"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="625de-128"><dt>Tapi3.dll</dt></span></span> </dl> |



 

