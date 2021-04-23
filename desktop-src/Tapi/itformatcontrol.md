---
description: Интерфейс Итформатконтрол предоставляет методы, позволяющие приложению получать сведения о формате приема или передачи для вызова.
ms.assetid: a3d15561-229e-4eb6-a0ac-2d69f170bced
title: Интерфейс Итформатконтрол (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0735e7bfaf5222948cef5e047530a35cb19a125
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689253"
---
# <a name="itformatcontrol-interface"></a><span data-ttu-id="024b9-103">Интерфейс Итформатконтрол</span><span class="sxs-lookup"><span data-stu-id="024b9-103">ITFormatControl interface</span></span>

<span data-ttu-id="024b9-104">\[ Этот интерфейс недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="024b9-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="024b9-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="024b9-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="024b9-106">Интерфейс **итформатконтрол** предоставляет методы, позволяющие приложению получать сведения о формате приема или передачи для вызова.</span><span class="sxs-lookup"><span data-stu-id="024b9-106">The **ITFormatControl** interface exposes methods that allow an application to retrieve information concerning the format of a receive or transmit stream for a call.</span></span>

<span data-ttu-id="024b9-107">Этот интерфейс реализуется с помощью интерфейса [H323 MSP](h323-msp.md) и предоставляется только в том случае, если вызов использует этого поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="024b9-107">This interface is implemented by the [H323 MSP](h323-msp.md) and is exposed only when a call uses this service provider.</span></span>

## <a name="members"></a><span data-ttu-id="024b9-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="024b9-108">Members</span></span>

<span data-ttu-id="024b9-109">Интерфейс **итформатконтрол** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="024b9-109">The **ITFormatControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="024b9-110">**Итформатконтрол** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="024b9-110">**ITFormatControl** also has these types of members:</span></span>

-   [<span data-ttu-id="024b9-111">Методы</span><span class="sxs-lookup"><span data-stu-id="024b9-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="024b9-112">Методы</span><span class="sxs-lookup"><span data-stu-id="024b9-112">Methods</span></span>

<span data-ttu-id="024b9-113">Интерфейс **итформатконтрол** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="024b9-113">The **ITFormatControl** interface has these methods.</span></span>



| <span data-ttu-id="024b9-114">Метод</span><span class="sxs-lookup"><span data-stu-id="024b9-114">Method</span></span>                                                                     | <span data-ttu-id="024b9-115">Описание</span><span class="sxs-lookup"><span data-stu-id="024b9-115">Description</span></span>                                                                    |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="024b9-116">**жеткуррентформат**</span><span class="sxs-lookup"><span data-stu-id="024b9-116">**GetCurrentFormat**</span></span>](itformatcontrol-getcurrentformat.md)               | <span data-ttu-id="024b9-117">Возвращает формат мультимедиа текущего потока.</span><span class="sxs-lookup"><span data-stu-id="024b9-117">Gets the media format of the current stream.</span></span><br/>                        |
| [<span data-ttu-id="024b9-118">**жетнумберофкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="024b9-118">**GetNumberOfCapabilities**</span></span>](itformatcontrol-getnumberofcapabilities.md) | <span data-ttu-id="024b9-119">Возвращает число возможностей, связанных с текущим форматом.</span><span class="sxs-lookup"><span data-stu-id="024b9-119">Gets the number of capabilities associated with the current format.</span></span><br/> |
| [<span data-ttu-id="024b9-120">**жетстреамкапс**</span><span class="sxs-lookup"><span data-stu-id="024b9-120">**GetStreamCaps**</span></span>](itformatcontrol-getstreamcaps.md)                     | <span data-ttu-id="024b9-121">Возвращает возможности, связанные с данным индексом формата.</span><span class="sxs-lookup"><span data-stu-id="024b9-121">Gets the capabilities associated with a given format index.</span></span><br/>         |
| [<span data-ttu-id="024b9-122">**релеасеформат**</span><span class="sxs-lookup"><span data-stu-id="024b9-122">**ReleaseFormat**</span></span>](itformatcontrol-releaseformat.md)                     | <span data-ttu-id="024b9-123">Освобождает структуру, связанную с форматом.</span><span class="sxs-lookup"><span data-stu-id="024b9-123">Releases the structure associated with the format.</span></span><br/>                  |
| [<span data-ttu-id="024b9-124">**реордеркапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="024b9-124">**ReOrderCapabilities**</span></span>](itformatcontrol-reordercapabilities.md)         | <span data-ttu-id="024b9-125">Задает новый порядок для возможностей форматирования.</span><span class="sxs-lookup"><span data-stu-id="024b9-125">Sets a new order for format capabilities.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="024b9-126">Требования</span><span class="sxs-lookup"><span data-stu-id="024b9-126">Requirements</span></span>



| <span data-ttu-id="024b9-127">Требование</span><span class="sxs-lookup"><span data-stu-id="024b9-127">Requirement</span></span> | <span data-ttu-id="024b9-128">Значение</span><span class="sxs-lookup"><span data-stu-id="024b9-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="024b9-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="024b9-129">TAPI version</span></span><br/> | <span data-ttu-id="024b9-130">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="024b9-130">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="024b9-131">Header</span><span class="sxs-lookup"><span data-stu-id="024b9-131">Header</span></span><br/>       | <dl> <span data-ttu-id="024b9-132"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="024b9-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="024b9-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="024b9-133">Library</span></span><br/>      | <dl> <span data-ttu-id="024b9-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="024b9-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="024b9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="024b9-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="024b9-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="024b9-136"><dt>Tapi3.dll</dt></span></span> </dl> |



 

