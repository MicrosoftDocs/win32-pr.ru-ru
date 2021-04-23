---
description: Интерфейс Иткаллкуалитиконтрол предоставляет методы, позволяющие приложению получать и задавать параметры для контроля качества вызова.
ms.assetid: 8d33e3b2-6af9-4c2d-bc65-905467f4fc6a
title: Интерфейс Иткаллкуалитиконтрол (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 447e2f34db76ba15ecaec9e7bc03a0d2d398c493
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675522"
---
# <a name="itcallqualitycontrol-interface"></a><span data-ttu-id="8a643-103">Интерфейс Иткаллкуалитиконтрол</span><span class="sxs-lookup"><span data-stu-id="8a643-103">ITCallQualityControl interface</span></span>

<span data-ttu-id="8a643-104">\[ Этот интерфейс недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="8a643-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8a643-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="8a643-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8a643-106">Интерфейс **иткаллкуалитиконтрол** предоставляет методы, позволяющие приложению получать и задавать параметры для контроля качества вызова.</span><span class="sxs-lookup"><span data-stu-id="8a643-106">The **ITCallQualityControl** interface exposes methods that allow an application to get and set parameters for call quality control.</span></span>

<span data-ttu-id="8a643-107">Этот интерфейс реализуется с помощью [ИПКОНФ MSP](ipconf-msp.md) и [H323 MSP](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="8a643-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="8a643-108">Он предоставляется только в том случае, если вызов использует эти поставщики служб.</span><span class="sxs-lookup"><span data-stu-id="8a643-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="8a643-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="8a643-109">Members</span></span>

<span data-ttu-id="8a643-110">Интерфейс **иткаллкуалитиконтрол** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8a643-110">The **ITCallQualityControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8a643-111">**Иткаллкуалитиконтрол** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8a643-111">**ITCallQualityControl** also has these types of members:</span></span>

-   [<span data-ttu-id="8a643-112">Методы</span><span class="sxs-lookup"><span data-stu-id="8a643-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8a643-113">Методы</span><span class="sxs-lookup"><span data-stu-id="8a643-113">Methods</span></span>

<span data-ttu-id="8a643-114">Интерфейс **иткаллкуалитиконтрол** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8a643-114">The **ITCallQualityControl** interface has these methods.</span></span>



| <span data-ttu-id="8a643-115">Метод</span><span class="sxs-lookup"><span data-stu-id="8a643-115">Method</span></span>                                            | <span data-ttu-id="8a643-116">Описание</span><span class="sxs-lookup"><span data-stu-id="8a643-116">Description</span></span>                                                                                                     |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a643-117">**Получить**</span><span class="sxs-lookup"><span data-stu-id="8a643-117">**Get**</span></span>](itcallqualitycontrol-get.md)           | <span data-ttu-id="8a643-118">Возвращает значение заданного [Свойства контроля качества вызова](callqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="8a643-118">Gets the value of a given [call quality control property](callqualityproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="8a643-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="8a643-119">**GetRange**</span></span>](itcallqualitycontrol-getrange.md) | <span data-ttu-id="8a643-120">Возвращает диапазон допустимых значений для заданного [Свойства контроля качества вызова](callqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="8a643-120">Gets the range of valid values for a given [call quality control property](callqualityproperty.md).</span></span><br/> |
| [<span data-ttu-id="8a643-121">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="8a643-121">**Set**</span></span>](itcallqualitycontrol-set.md)           | <span data-ttu-id="8a643-122">Задает значение заданного [Свойства контроля качества вызова](callqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="8a643-122">Sets the value of a given [call quality control property](callqualityproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="8a643-123">Требования</span><span class="sxs-lookup"><span data-stu-id="8a643-123">Requirements</span></span>



| <span data-ttu-id="8a643-124">Требование</span><span class="sxs-lookup"><span data-stu-id="8a643-124">Requirement</span></span> | <span data-ttu-id="8a643-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8a643-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8a643-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="8a643-126">TAPI version</span></span><br/> | <span data-ttu-id="8a643-127">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="8a643-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="8a643-128">Header</span><span class="sxs-lookup"><span data-stu-id="8a643-128">Header</span></span><br/>       | <dl> <span data-ttu-id="8a643-129"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a643-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a643-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8a643-130">Library</span></span><br/>      | <dl> <span data-ttu-id="8a643-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a643-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="8a643-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8a643-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="8a643-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a643-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 

