---
description: 'Интерфейс ИенумпартиЦипант предоставляет стандартные методы перечисления COM для интерфейса ИтпартиЦипант. Метод ИтпартиЦипантконтрол:: ЕнумератепартиЦипантс возвращает указатель на ИенумпартиЦипант.'
ms.assetid: 8534d102-06ce-4e82-8f9c-9ab9f0d14df9
title: Интерфейс ИенумпартиЦипант (Конфприв. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a20a2cd8e72c5c44b054fc4658b304c8b4fa41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676013"
---
# <a name="ienumparticipant-interface"></a><span data-ttu-id="8b6d7-104">Интерфейс ИенумпартиЦипант</span><span class="sxs-lookup"><span data-stu-id="8b6d7-104">IEnumParticipant interface</span></span>

<span data-ttu-id="8b6d7-105">\[**ИенумпартиЦипант** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="8b6d7-105">\[**IEnumParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8b6d7-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="8b6d7-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8b6d7-107">Интерфейс **иенумпартиЦипант** предоставляет стандартные методы перечисления com для интерфейса [**итпартиЦипант**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="8b6d7-107">The **IEnumParticipant** interface provides COM-standard enumeration methods for the [**ITParticipant**](itparticipant.md) interface.</span></span> <span data-ttu-id="8b6d7-108">Метод [**итпартиЦипантконтрол:: енумератепартиЦипантс**](itparticipantcontrol-enumerateparticipants.md) возвращает указатель на **иенумпартиЦипант**.</span><span class="sxs-lookup"><span data-stu-id="8b6d7-108">The [**ITParticipantControl::EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) method returns a pointer to **IEnumParticipant**.</span></span>

<span data-ttu-id="8b6d7-109">Интерфейс **иенумпартиЦипант** скрыт от Visual Basic и языков сценариев.</span><span class="sxs-lookup"><span data-stu-id="8b6d7-109">The **IEnumParticipant** interface is hidden from Visual Basic and scripting languages.</span></span>

## <a name="members"></a><span data-ttu-id="8b6d7-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="8b6d7-110">Members</span></span>

<span data-ttu-id="8b6d7-111">Интерфейс **иенумпартиЦипант** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8b6d7-111">The **IEnumParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8b6d7-112">**ИенумпартиЦипант** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8b6d7-112">**IEnumParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="8b6d7-113">Методы</span><span class="sxs-lookup"><span data-stu-id="8b6d7-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8b6d7-114">Методы</span><span class="sxs-lookup"><span data-stu-id="8b6d7-114">Methods</span></span>

<span data-ttu-id="8b6d7-115">Интерфейс **иенумпартиЦипант** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8b6d7-115">The **IEnumParticipant** interface has these methods.</span></span>



| <span data-ttu-id="8b6d7-116">Метод</span><span class="sxs-lookup"><span data-stu-id="8b6d7-116">Method</span></span>                                  | <span data-ttu-id="8b6d7-117">Описание</span><span class="sxs-lookup"><span data-stu-id="8b6d7-117">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b6d7-118">**Клонировать**</span><span class="sxs-lookup"><span data-stu-id="8b6d7-118">**Clone**</span></span>](ienumparticipant-clone.md) | <span data-ttu-id="8b6d7-119">Создает другой перечислитель с тем же состоянием перечисления, что и текущий.</span><span class="sxs-lookup"><span data-stu-id="8b6d7-119">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="8b6d7-120">**Далее**</span><span class="sxs-lookup"><span data-stu-id="8b6d7-120">**Next**</span></span>](ienumparticipant-next.md)   | <span data-ttu-id="8b6d7-121">Возвращает указанное число следующих элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="8b6d7-121">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="8b6d7-122">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="8b6d7-122">**Reset**</span></span>](ienumparticipant-reset.md) | <span data-ttu-id="8b6d7-123">Выполняет сброс до начала последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="8b6d7-123">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="8b6d7-124">**Пропустить**</span><span class="sxs-lookup"><span data-stu-id="8b6d7-124">**Skip**</span></span>](ienumparticipant-skip.md)   | <span data-ttu-id="8b6d7-125">Пропускает следующее заданное число элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="8b6d7-125">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="8b6d7-126">Требования</span><span class="sxs-lookup"><span data-stu-id="8b6d7-126">Requirements</span></span>



| <span data-ttu-id="8b6d7-127">Требование</span><span class="sxs-lookup"><span data-stu-id="8b6d7-127">Requirement</span></span> | <span data-ttu-id="8b6d7-128">Значение</span><span class="sxs-lookup"><span data-stu-id="8b6d7-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b6d7-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="8b6d7-129">TAPI version</span></span><br/> | <span data-ttu-id="8b6d7-130">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8b6d7-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8b6d7-131">Header</span><span class="sxs-lookup"><span data-stu-id="8b6d7-131">Header</span></span><br/>       | <dl> <span data-ttu-id="8b6d7-132"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b6d7-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="8b6d7-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8b6d7-133">Library</span></span><br/>      | <dl> <span data-ttu-id="8b6d7-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b6d7-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8b6d7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8b6d7-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="8b6d7-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b6d7-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8b6d7-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b6d7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b6d7-138">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="8b6d7-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

