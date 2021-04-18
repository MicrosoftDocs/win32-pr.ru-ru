---
description: Итстреамкуалитиконтрол предоставляет методы, позволяющие приложению получать и задавать параметры для управления качеством потока.
ms.assetid: b9ecf24a-c87e-44a6-9e20-aa7bf7619314
title: Интерфейс Итстреамкуалитиконтрол (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a85eccc907ef2c8f4c0b67c2a32244004dbdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675763"
---
# <a name="itstreamqualitycontrol-interface"></a><span data-ttu-id="c0fd4-103">Интерфейс Итстреамкуалитиконтрол</span><span class="sxs-lookup"><span data-stu-id="c0fd4-103">ITStreamQualityControl interface</span></span>

<span data-ttu-id="c0fd4-104">\[ Этот интерфейс недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c0fd4-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="c0fd4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c0fd4-106">**Итстреамкуалитиконтрол** предоставляет методы, позволяющие приложению получать и задавать параметры для управления качеством потока.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-106">The **ITStreamQualityControl** exposes methods that allow an application to get and set parameters for stream quality control.</span></span>

<span data-ttu-id="c0fd4-107">Этот интерфейс реализуется с помощью [ИПКОНФ MSP](ipconf-msp.md) и [H323 MSP](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="c0fd4-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="c0fd4-108">Он предоставляется только в том случае, если вызов использует эти поставщики служб.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="c0fd4-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="c0fd4-109">Members</span></span>

<span data-ttu-id="c0fd4-110">Интерфейс **итстреамкуалитиконтрол** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c0fd4-110">The **ITStreamQualityControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c0fd4-111">**Итстреамкуалитиконтрол** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c0fd4-111">**ITStreamQualityControl** also has these types of members:</span></span>

-   [<span data-ttu-id="c0fd4-112">Методы</span><span class="sxs-lookup"><span data-stu-id="c0fd4-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c0fd4-113">Методы</span><span class="sxs-lookup"><span data-stu-id="c0fd4-113">Methods</span></span>

<span data-ttu-id="c0fd4-114">Интерфейс **итстреамкуалитиконтрол** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c0fd4-114">The **ITStreamQualityControl** interface has these methods.</span></span>



| <span data-ttu-id="c0fd4-115">Метод</span><span class="sxs-lookup"><span data-stu-id="c0fd4-115">Method</span></span>                                              | <span data-ttu-id="c0fd4-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c0fd4-116">Description</span></span>                                                                                                 |
|:----------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0fd4-117">**Получить**</span><span class="sxs-lookup"><span data-stu-id="c0fd4-117">**Get**</span></span>](itstreamqualitycontrol-get.md)           | <span data-ttu-id="c0fd4-118">Возвращает значение заданного [свойства качества потока](streamqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="c0fd4-118">Gets the value of a given [stream quality property](streamqualityproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="c0fd4-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="c0fd4-119">**GetRange**</span></span>](itstreamqualitycontrol-getrange.md) | <span data-ttu-id="c0fd4-120">Возвращает диапазон допустимых значений для заданного [свойства качества потока](streamqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="c0fd4-120">Gets the range of valid values for a given [stream quality property](streamqualityproperty.md).</span></span><br/> |
| [<span data-ttu-id="c0fd4-121">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="c0fd4-121">**Set**</span></span>](itstreamqualitycontrol-set.md)           | <span data-ttu-id="c0fd4-122">Задает значение заданного [свойства качества потока](streamqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="c0fd4-122">Sets the value of a given [stream quality property](streamqualityproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="c0fd4-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c0fd4-123">Requirements</span></span>



| <span data-ttu-id="c0fd4-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c0fd4-124">Requirement</span></span> | <span data-ttu-id="c0fd4-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c0fd4-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c0fd4-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="c0fd4-126">TAPI version</span></span><br/> | <span data-ttu-id="c0fd4-127">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="c0fd4-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="c0fd4-128">Header</span><span class="sxs-lookup"><span data-stu-id="c0fd4-128">Header</span></span><br/>       | <dl> <span data-ttu-id="c0fd4-129"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0fd4-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0fd4-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c0fd4-130">Library</span></span><br/>      | <dl> <span data-ttu-id="c0fd4-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0fd4-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="c0fd4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c0fd4-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="c0fd4-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0fd4-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 

