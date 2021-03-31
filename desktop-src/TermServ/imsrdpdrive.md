---
title: Интерфейс Имсрдпдриве
description: Содержит сведения об объекте Drive.
ms.assetid: 25e76657-a898-4581-a866-d66008540f50
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпдриве
- Службы удаленных рабочих столов интерфейса Имсрдпдриве, описание
topic_type:
- apiref
api_name:
- IMsRdpDrive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 032e62ca54d6adccce9b27c8f7e95160c800759b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801144"
---
# <a name="imsrdpdrive-interface"></a><span data-ttu-id="3703a-105">Интерфейс Имсрдпдриве</span><span class="sxs-lookup"><span data-stu-id="3703a-105">IMsRdpDrive interface</span></span>

<span data-ttu-id="3703a-106">Содержит сведения об объекте Drive.</span><span class="sxs-lookup"><span data-stu-id="3703a-106">Contains information about a drive object.</span></span>

## <a name="members"></a><span data-ttu-id="3703a-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="3703a-107">Members</span></span>

<span data-ttu-id="3703a-108">Интерфейс **имсрдпдриве** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3703a-108">The **IMsRdpDrive** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3703a-109">**Имсрдпдриве** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3703a-109">**IMsRdpDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="3703a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="3703a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3703a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="3703a-111">Properties</span></span>

<span data-ttu-id="3703a-112">Интерфейс **имсрдпдриве** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3703a-112">The **IMsRdpDrive** interface has these properties.</span></span>



| <span data-ttu-id="3703a-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="3703a-113">Property</span></span>                                                            | <span data-ttu-id="3703a-114">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="3703a-114">Access type</span></span>           | <span data-ttu-id="3703a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="3703a-115">Description</span></span>                                              |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [<span data-ttu-id="3703a-116">**Имя**</span><span class="sxs-lookup"><span data-stu-id="3703a-116">**Name**</span></span>](imsrdpdrive-name.md)<br/>                         | <span data-ttu-id="3703a-117">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3703a-117">Read-only</span></span><br/>  | <span data-ttu-id="3703a-118">Возвращает имя диска.</span><span class="sxs-lookup"><span data-stu-id="3703a-118">Retrieves the name of the drive.</span></span><br/>              |
| [<span data-ttu-id="3703a-119">**редиректионстате**</span><span class="sxs-lookup"><span data-stu-id="3703a-119">**RedirectionState**</span></span>](imsrdpdrive-redirectionstate.md)<br/> | <span data-ttu-id="3703a-120">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="3703a-120">Read/write</span></span><br/> | <span data-ttu-id="3703a-121">Указывает состояние перенаправления диска.</span><span class="sxs-lookup"><span data-stu-id="3703a-121">Indicates the redirection state of the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3703a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="3703a-122">Requirements</span></span>



| <span data-ttu-id="3703a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="3703a-123">Requirement</span></span> | <span data-ttu-id="3703a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="3703a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3703a-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3703a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3703a-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3703a-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3703a-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3703a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3703a-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3703a-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3703a-129">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3703a-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="3703a-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3703a-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3703a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3703a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3703a-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3703a-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3703a-133">IID</span><span class="sxs-lookup"><span data-stu-id="3703a-133">IID</span></span><br/>                      | <span data-ttu-id="3703a-134">IID \_ имсрдпдриве определен как d28b5458-f694-47a8-8e61-40356a767e46</span><span class="sxs-lookup"><span data-stu-id="3703a-134">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="3703a-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3703a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3703a-136">Справочник по веб-подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="3703a-136">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="3703a-137">**имсрдпдривеколлектион**</span><span class="sxs-lookup"><span data-stu-id="3703a-137">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

