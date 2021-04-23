---
description: Интерфейс Ипровидепропертибуилдер, реализованный, позволяет объектам указывать объекты построителя свойств для свойств.
ms.assetid: 26557622-4a97-4db0-85ed-3f77fcb769a0
title: Интерфейс Ипровидепропертибуилдер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder:IUnknown
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: b93d05c3c64686b21f19ffe6262ddfd68812dd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648000"
---
# <a name="iprovidepropertybuilder-interface"></a><span data-ttu-id="7ddaa-103">Интерфейс Ипровидепропертибуилдер</span><span class="sxs-lookup"><span data-stu-id="7ddaa-103">IProvidePropertyBuilder interface</span></span>

<span data-ttu-id="7ddaa-104">Интерфейс **ипровидепропертибуилдер** , реализованный, позволяет объектам указывать объекты построителя свойств для свойств.</span><span class="sxs-lookup"><span data-stu-id="7ddaa-104">The **IProvidePropertyBuilder** interface, when implemented, allows objects to specify property builder objects for properties.</span></span> <span data-ttu-id="7ddaa-105">Построители вызываются с помощью кнопки с многоточием ( \[ ... \] ) в обозревателе свойств Microsoft Visual Studio и вызываются через [**ексекутебуилдер**](iprovidepropertybuilder-executebuilder.md) при нажатии кнопки.</span><span class="sxs-lookup"><span data-stu-id="7ddaa-105">Builders are invoked by an ellipsis button (\[...\]) on the Microsoft Visual Studio property browser and is invoked through [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) when the button is pressed.</span></span> <span data-ttu-id="7ddaa-106">Чтобы предоставить конструктор для заданного свойства, возвратите идентификатор GUID для построителя свойств, который должен вызываться для текущего свойства из [**маппропертитобуилдер**](iprovidepropertybuilder-mappropertytobuilder.md).</span><span class="sxs-lookup"><span data-stu-id="7ddaa-106">To supply a builder for a given property, return a GUID for the property builder that should be invoked for the current property from [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span></span> <span data-ttu-id="7ddaa-107">Построители обычно реализуются с помощью модальных диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="7ddaa-107">Builders are generally implemented through modal dialog boxes.</span></span>

<span data-ttu-id="7ddaa-108">Версия этого интерфейса — 1,0.</span><span class="sxs-lookup"><span data-stu-id="7ddaa-108">The version for this interface is 1.0.</span></span> <span data-ttu-id="7ddaa-109">Вызовы методов получаются в динамически назначенной конечной точке (как описано в разделе "двоичная документация MSMQ в сопоставлении конечных точек") и используют UUID (универсальный уникальный идентификатор) "33C0C1D8-33CF-11d3-BFF2-00C04F990235".</span><span class="sxs-lookup"><span data-stu-id="7ddaa-109">Method calls are received at a dynamically assigned endpoint (as described in the MSMQ binary documentation on endpoint mapping) and use the UUID (universally unique identifier) "33C0C1D8-33CF-11d3-BFF2-00C04F990235".</span></span>

## <a name="members"></a><span data-ttu-id="7ddaa-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="7ddaa-110">Members</span></span>

<span data-ttu-id="7ddaa-111">Интерфейс **ипровидепропертибуилдер: IUnknown** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7ddaa-111">The **IProvidePropertyBuilder:IUnknown** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7ddaa-112">**Ипровидепропертибуилдер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7ddaa-112">**IProvidePropertyBuilder** also has these types of members:</span></span>

-   [<span data-ttu-id="7ddaa-113">Методы</span><span class="sxs-lookup"><span data-stu-id="7ddaa-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7ddaa-114">Методы</span><span class="sxs-lookup"><span data-stu-id="7ddaa-114">Methods</span></span>

<span data-ttu-id="7ddaa-115">Интерфейс **ипровидепропертибуилдер: IUnknown** имеет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7ddaa-115">The **IProvidePropertyBuilder:IUnknown** interface has these methods.</span></span>



| <span data-ttu-id="7ddaa-116">Метод</span><span class="sxs-lookup"><span data-stu-id="7ddaa-116">Method</span></span>                                                                       | <span data-ttu-id="7ddaa-117">Описание</span><span class="sxs-lookup"><span data-stu-id="7ddaa-117">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ddaa-118">**ексекутебуилдер**</span><span class="sxs-lookup"><span data-stu-id="7ddaa-118">**ExecuteBuilder**</span></span>](iprovidepropertybuilder-executebuilder.md)             | <span data-ttu-id="7ddaa-119">Уведомляет объект о том, что он должен отобразить его построитель для указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="7ddaa-119">Notifies an object that it should display its builder for the specified property.</span></span><br/> |
| [<span data-ttu-id="7ddaa-120">**маппропертитобуилдер**</span><span class="sxs-lookup"><span data-stu-id="7ddaa-120">**MapPropertyToBuilder**</span></span>](iprovidepropertybuilder-mappropertytobuilder.md) | <span data-ttu-id="7ddaa-121">Проверяет, связан ли конструктор с определенным свойством.</span><span class="sxs-lookup"><span data-stu-id="7ddaa-121">Checks whether a builder should be associated with a particular property.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="7ddaa-122">Требования</span><span class="sxs-lookup"><span data-stu-id="7ddaa-122">Requirements</span></span>



| <span data-ttu-id="7ddaa-123">Требование</span><span class="sxs-lookup"><span data-stu-id="7ddaa-123">Requirement</span></span> | <span data-ttu-id="7ddaa-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7ddaa-124">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7ddaa-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7ddaa-125">DLL</span></span><br/> | <dl> <span data-ttu-id="7ddaa-126"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ddaa-126"><dt>Vsp.dll</dt></span></span> </dl> |



 

 
