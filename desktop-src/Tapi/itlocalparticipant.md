---
description: Интерфейс ИтлокалпартиЦипант предоставляется в объекте потока, если Ипконф MSP поддерживает вызов.
ms.assetid: 64965ae2-e30b-4353-a502-f96018da71a5
title: Интерфейс ИтлокалпартиЦипант (Конфприв. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4017837a0b970cb791cdf454437fe2d48720028
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689069"
---
# <a name="itlocalparticipant-interface"></a><span data-ttu-id="65100-103">Интерфейс ИтлокалпартиЦипант</span><span class="sxs-lookup"><span data-stu-id="65100-103">ITLocalParticipant interface</span></span>

<span data-ttu-id="65100-104">Интерфейс **итлокалпартиЦипант** предоставляется в объекте потока, если ипконф MSP поддерживает вызов.</span><span class="sxs-lookup"><span data-stu-id="65100-104">The **ITLocalParticipant** interface is exposed on the stream object when the IPConf MSP supports the call.</span></span> <span data-ttu-id="65100-105">MSP реализует методы, позволяющие приложению получать и задавать сведения о участниках.</span><span class="sxs-lookup"><span data-stu-id="65100-105">The MSP implements methods that allow an application to get and set participant information.</span></span> <span data-ttu-id="65100-106">Интерфейс **итлокалпартиЦипант** создается путем вызова **QueryInterface** в [**итстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span><span class="sxs-lookup"><span data-stu-id="65100-106">The **ITLocalParticipant** interface is created by calling **QueryInterface** on [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span></span>

## <a name="members"></a><span data-ttu-id="65100-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="65100-107">Members</span></span>

<span data-ttu-id="65100-108">Интерфейс **итлокалпартиЦипант** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="65100-108">The **ITLocalParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="65100-109">**ИтлокалпартиЦипант** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="65100-109">**ITLocalParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="65100-110">Методы</span><span class="sxs-lookup"><span data-stu-id="65100-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="65100-111">Методы</span><span class="sxs-lookup"><span data-stu-id="65100-111">Methods</span></span>

<span data-ttu-id="65100-112">Интерфейс **итлокалпартиЦипант** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="65100-112">The **ITLocalParticipant** interface has these methods.</span></span>



| <span data-ttu-id="65100-113">Метод</span><span class="sxs-lookup"><span data-stu-id="65100-113">Method</span></span>                                                                                     | <span data-ttu-id="65100-114">Описание</span><span class="sxs-lookup"><span data-stu-id="65100-114">Description</span></span>                                                                            |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="65100-115">**получить \_ локалпартиЦипанттипединфо**</span><span class="sxs-lookup"><span data-stu-id="65100-115">**get\_LocalParticipantTypedInfo**</span></span>](itlocalparticipant-get-localparticipanttypedinfo.md) | <span data-ttu-id="65100-116">Возвращает сведения о участнике, такие как имя электронной почты или географическое расположение.</span><span class="sxs-lookup"><span data-stu-id="65100-116">Gets participant information, such as e-mail name or geographical location.</span></span><br/> |
| [<span data-ttu-id="65100-117">**разместить \_ локалпартиЦипанттипединфо**</span><span class="sxs-lookup"><span data-stu-id="65100-117">**put\_LocalParticipantTypedInfo**</span></span>](itlocalparticipant-put-localparticipanttypedinfo.md) | <span data-ttu-id="65100-118">Задает сведения о участнике.</span><span class="sxs-lookup"><span data-stu-id="65100-118">Sets participant information.</span></span><br/>                                               |



 

## <a name="requirements"></a><span data-ttu-id="65100-119">Требования</span><span class="sxs-lookup"><span data-stu-id="65100-119">Requirements</span></span>



| <span data-ttu-id="65100-120">Требование</span><span class="sxs-lookup"><span data-stu-id="65100-120">Requirement</span></span> | <span data-ttu-id="65100-121">Значение</span><span class="sxs-lookup"><span data-stu-id="65100-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65100-122">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="65100-122">TAPI version</span></span><br/> | <span data-ttu-id="65100-123">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="65100-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="65100-124">Header</span><span class="sxs-lookup"><span data-stu-id="65100-124">Header</span></span><br/>       | <dl> <span data-ttu-id="65100-125"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="65100-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="65100-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="65100-126">Library</span></span><br/>      | <dl> <span data-ttu-id="65100-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65100-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="65100-128">DLL</span><span class="sxs-lookup"><span data-stu-id="65100-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="65100-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65100-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="65100-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65100-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65100-131">**итстреам**</span><span class="sxs-lookup"><span data-stu-id="65100-131">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

