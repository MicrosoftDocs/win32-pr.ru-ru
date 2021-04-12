---
title: Интерфейс IWMDRMDeviceApp2
description: Интерфейс IWMDRMDeviceApp2 расширяет Ивмдрмдевицеапп, предоставляя новую версию метода Куеридевицестатус.
ms.assetid: a7e28d5a-041f-4102-97db-0c77ca146e26
keywords:
- Интерфейс IWMDRMDeviceApp2 Windows Media диспетчер устройств
- Интерфейс IWMDRMDeviceApp2 Windows Media диспетчер устройств, описание
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df4bfdb023198631b16ffa0e511488fa52423c5e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334808"
---
# <a name="iwmdrmdeviceapp2-interface"></a><span data-ttu-id="f07d8-105">Интерфейс IWMDRMDeviceApp2</span><span class="sxs-lookup"><span data-stu-id="f07d8-105">IWMDRMDeviceApp2 interface</span></span>

<span data-ttu-id="f07d8-106">Интерфейс **IWMDRMDeviceApp2** расширяет [**ивмдрмдевицеапп**](iwmdrmdeviceapp.md) , предоставляя новую версию метода [**куеридевицестатус**](iwmdrmdeviceapp-querydevicestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="f07d8-106">The **IWMDRMDeviceApp2** interface extends [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) by providing a new version of the [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) method.</span></span> <span data-ttu-id="f07d8-107">**QueryDeviceStatus2** позволяет вызывающему объекту запрашивать определенные требования DRM.</span><span class="sxs-lookup"><span data-stu-id="f07d8-107">**QueryDeviceStatus2** enables the caller to query for a specific DRM requirement.</span></span>

<span data-ttu-id="f07d8-108">Чтобы получить этот интерфейс, вызовите **CoCreateInstance** и передайте CLSID \_ вмдрмдевицеапп.</span><span class="sxs-lookup"><span data-stu-id="f07d8-108">To get this interface, call **CoCreateInstance** and pass in CLSID\_WMDRMDeviceApp.</span></span>

> [!Note]  
> <span data-ttu-id="f07d8-109">Этот интерфейс определен в файле заголовка, созданном из Вмдрмдевицеапп. idl.</span><span class="sxs-lookup"><span data-stu-id="f07d8-109">This interface is defined in the header file built from WMDRMDeviceApp.idl.</span></span> <span data-ttu-id="f07d8-110">Этот заголовок **\# содержит** "вмдм. h".</span><span class="sxs-lookup"><span data-stu-id="f07d8-110">This header **\#includes** "wmdm.h".</span></span> <span data-ttu-id="f07d8-111">Может потребоваться изменить это имя файла в соответствии с заголовком, созданным из ВМДМ. idl.</span><span class="sxs-lookup"><span data-stu-id="f07d8-111">You might need to change this file name to match the header built from WMDM.idl.</span></span>

 

## <a name="members"></a><span data-ttu-id="f07d8-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="f07d8-112">Members</span></span>

<span data-ttu-id="f07d8-113">Интерфейс **IWMDRMDeviceApp2** наследует от [**ивмдрмдевицеапп**](iwmdrmdeviceapp.md).</span><span class="sxs-lookup"><span data-stu-id="f07d8-113">The **IWMDRMDeviceApp2** interface inherits from [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md).</span></span> <span data-ttu-id="f07d8-114">**IWMDRMDeviceApp2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f07d8-114">**IWMDRMDeviceApp2** also has these types of members:</span></span>

-   [<span data-ttu-id="f07d8-115">Методы</span><span class="sxs-lookup"><span data-stu-id="f07d8-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f07d8-116">Методы</span><span class="sxs-lookup"><span data-stu-id="f07d8-116">Methods</span></span>

<span data-ttu-id="f07d8-117">Интерфейс **IWMDRMDeviceApp2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f07d8-117">The **IWMDRMDeviceApp2** interface has these methods.</span></span>



| <span data-ttu-id="f07d8-118">Метод</span><span class="sxs-lookup"><span data-stu-id="f07d8-118">Method</span></span>                                                            | <span data-ttu-id="f07d8-119">Описание</span><span class="sxs-lookup"><span data-stu-id="f07d8-119">Description</span></span>                                                          |
|:------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="f07d8-120">**QueryDeviceStatus2**</span><span class="sxs-lookup"><span data-stu-id="f07d8-120">**QueryDeviceStatus2**</span></span>](iwmdrmdeviceapp2-querydevicestatus2.md) | <span data-ttu-id="f07d8-121">Запрашивает устройство для определенного состояния DRM или возможности.</span><span class="sxs-lookup"><span data-stu-id="f07d8-121">Queries a device for a specific DRM status or capability.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="f07d8-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f07d8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f07d8-123">**ивмдрмдевицеапп**</span><span class="sxs-lookup"><span data-stu-id="f07d8-123">**IWMDRMDeviceApp**</span></span>](iwmdrmdeviceapp.md)
</dt> <dt>

[<span data-ttu-id="f07d8-124">**Обработка защищенного содержимого в приложении**</span><span class="sxs-lookup"><span data-stu-id="f07d8-124">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="f07d8-125">**Интерфейсы для приложений**</span><span class="sxs-lookup"><span data-stu-id="f07d8-125">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> <dt>

[<span data-ttu-id="f07d8-126">**Использование содержимого измерения**</span><span class="sxs-lookup"><span data-stu-id="f07d8-126">**Metering Content Usage**</span></span>](metering-content-usage.md)
</dt> </dl>

 

 





