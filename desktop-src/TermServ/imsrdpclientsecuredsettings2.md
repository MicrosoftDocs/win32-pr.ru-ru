---
title: Интерфейс IMsRdpClientSecuredSettings2
description: Определяет дополнительные свойства элемента управления ActiveX удаленный рабочий стол, которые ограничены конкретными зонами безопасности URL-адресов Internet Explorer.
ms.assetid: dde9824c-7adf-4783-bb1a-fb2bdbb7aead
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientSecuredSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientSecuredSettings2, описание
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ceaf322b51a4b619f8d73a898c444706d61f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672643"
---
# <a name="imsrdpclientsecuredsettings2-interface"></a><span data-ttu-id="a877d-105">Интерфейс IMsRdpClientSecuredSettings2</span><span class="sxs-lookup"><span data-stu-id="a877d-105">IMsRdpClientSecuredSettings2 interface</span></span>

<span data-ttu-id="a877d-106">Определяет дополнительные свойства элемента управления ActiveX удаленный рабочий стол, которые ограничены конкретными зонами безопасности URL-адресов Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a877d-106">Defines additional properties of the Remote Desktop ActiveX control that are restricted to specific Internet Explorer URL security zones.</span></span>

## <a name="members"></a><span data-ttu-id="a877d-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="a877d-107">Members</span></span>

<span data-ttu-id="a877d-108">Интерфейс **IMsRdpClientSecuredSettings2** наследует от [**имсрдпклиентсекуредсеттингс**](imsrdpclientsecuredsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="a877d-108">The **IMsRdpClientSecuredSettings2** interface inherits from [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md).</span></span> <span data-ttu-id="a877d-109">**IMsRdpClientSecuredSettings2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a877d-109">**IMsRdpClientSecuredSettings2** also has these types of members:</span></span>

-   [<span data-ttu-id="a877d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a877d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a877d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a877d-111">Properties</span></span>

<span data-ttu-id="a877d-112">Интерфейс **IMsRdpClientSecuredSettings2** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a877d-112">The **IMsRdpClientSecuredSettings2** interface has these properties.</span></span>



| <span data-ttu-id="a877d-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="a877d-113">Property</span></span>                                                   | <span data-ttu-id="a877d-114">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="a877d-114">Access type</span></span>           | <span data-ttu-id="a877d-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a877d-115">Description</span></span>                                                                                                          |
|:-----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a877d-116">**пкб**</span><span class="sxs-lookup"><span data-stu-id="a877d-116">**PCB**</span></span>](imsrdpclientsecuredsettings2-pcb.md)<br/> | <span data-ttu-id="a877d-117">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="a877d-117">Read/write</span></span><br/> | <span data-ttu-id="a877d-118">Задает параметр предварительного подключения BLOB-объекта (ПКБ), используемый перед подключением для передачи на сервер.</span><span class="sxs-lookup"><span data-stu-id="a877d-118">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a877d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a877d-119">Requirements</span></span>



| <span data-ttu-id="a877d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a877d-120">Requirement</span></span> | <span data-ttu-id="a877d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a877d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a877d-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a877d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a877d-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a877d-123">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="a877d-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a877d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a877d-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a877d-125">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="a877d-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a877d-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="a877d-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a877d-127"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="a877d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a877d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a877d-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a877d-129"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="a877d-130">IID</span><span class="sxs-lookup"><span data-stu-id="a877d-130">IID</span></span><br/>                      | <span data-ttu-id="a877d-131">IID \_ имсрдпклиентсекуредсеттингс определен как 25f2ce20-8b1d-4971-A7CD-549dae201fc0</span><span class="sxs-lookup"><span data-stu-id="a877d-131">IID\_IMsRdpClientSecuredSettings is defined as 25f2ce20-8b1d-4971-a7cd-549dae201fc0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a877d-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a877d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a877d-133">**имсрдпклиентсекуредсеттингс**</span><span class="sxs-lookup"><span data-stu-id="a877d-133">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





