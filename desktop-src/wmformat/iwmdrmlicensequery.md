---
title: Интерфейс Ивмдрмлиценсекуери
description: Интерфейс Ивмдрмлиценсекуери позволяет приложениям запрашивать права и состояние лицензии для защищенного файла.
ms.assetid: 4ec8ff9f-0acb-4389-8995-65f24736491b
keywords:
- Формат Windows Media в интерфейсе Ивмдрмлиценсекуери
- Ивмдрмлиценсекуери интерфейса Windows Media Format, описание
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6463f405bf50d4d4ecb037dc542e3af0e5b7df46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792685"
---
# <a name="iwmdrmlicensequery-interface"></a><span data-ttu-id="2e637-105">Интерфейс Ивмдрмлиценсекуери</span><span class="sxs-lookup"><span data-stu-id="2e637-105">IWMDRMLicenseQuery interface</span></span>

<span data-ttu-id="2e637-106">Интерфейс **ивмдрмлиценсекуери** позволяет приложениям запрашивать права и состояние лицензии для защищенного файла.</span><span class="sxs-lookup"><span data-stu-id="2e637-106">The **IWMDRMLicenseQuery** interface enables applications to query the rights and license state for a protected file.</span></span> <span data-ttu-id="2e637-107">Этот интерфейс использует идентификатор ключа для выполнения запросов к локальному хранилищу лицензий.</span><span class="sxs-lookup"><span data-stu-id="2e637-107">This interface uses the Key ID to perform queries on the local license store.</span></span>

<span data-ttu-id="2e637-108">Чтобы получить экземпляр этого интерфейса, вызовите метод [**ивмдрмпровидер:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="2e637-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="2e637-109">Передайте **IID \_ ивмдрмлиценсекуери** в качестве параметра *riid* .</span><span class="sxs-lookup"><span data-stu-id="2e637-109">Pass **IID\_IWMDRMLicenseQuery** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="2e637-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="2e637-110">Members</span></span>

<span data-ttu-id="2e637-111">Интерфейс **ивмдрмлиценсекуери** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2e637-111">The **IWMDRMLicenseQuery** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2e637-112">**Ивмдрмлиценсекуери** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2e637-112">**IWMDRMLicenseQuery** also has these types of members:</span></span>

-   [<span data-ttu-id="2e637-113">Методы</span><span class="sxs-lookup"><span data-stu-id="2e637-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2e637-114">Методы</span><span class="sxs-lookup"><span data-stu-id="2e637-114">Methods</span></span>

<span data-ttu-id="2e637-115">Интерфейс **ивмдрмлиценсекуери** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2e637-115">The **IWMDRMLicenseQuery** interface has these methods.</span></span>



| <span data-ttu-id="2e637-116">Метод</span><span class="sxs-lookup"><span data-stu-id="2e637-116">Method</span></span>                                                                                | <span data-ttu-id="2e637-117">Описание</span><span class="sxs-lookup"><span data-stu-id="2e637-117">Description</span></span>                                                                                      |
|:--------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e637-118">**куеряктионалловед**</span><span class="sxs-lookup"><span data-stu-id="2e637-118">**QueryActionAllowed**</span></span>](iwmdrmlicensequery-queryactionallowed.md)                   | <span data-ttu-id="2e637-119">Запрашивает у локального хранилища лицензий разрешения на выполнение действий по ИДЕНТИФИКАТОРу ключа.</span><span class="sxs-lookup"><span data-stu-id="2e637-119">Queries the local license store for permissions to perform actions by Key ID.</span></span><br/>         |
| [<span data-ttu-id="2e637-120">**куерилиценсестате**</span><span class="sxs-lookup"><span data-stu-id="2e637-120">**QueryLicenseState**</span></span>](iwmdrmlicensequery-querylicensestate.md)                     | <span data-ttu-id="2e637-121">Запрашивает данные о состоянии лицензии в локальном хранилище лицензий по ИДЕНТИФИКАТОРу ключа и специальным правам.</span><span class="sxs-lookup"><span data-stu-id="2e637-121">Queries the local license store for license state data by Key ID and specific rights.</span></span><br/> |
| [<span data-ttu-id="2e637-122">**сетактионалловедкуерипарамс**</span><span class="sxs-lookup"><span data-stu-id="2e637-122">**SetActionAllowedQueryParams**</span></span>](iwmdrmlicensequery-setactionallowedqueryparams.md) | <span data-ttu-id="2e637-123">Задает параметры среды для повышения точности запросов лицензий.</span><span class="sxs-lookup"><span data-stu-id="2e637-123">Sets environmental parameters to improve the accuracy of license queries.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="2e637-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e637-124">Remarks</span></span>

<span data-ttu-id="2e637-125">Методы **ивмдрмлиценсекуери** не предоставляют сведения об отдельных лицензиях.</span><span class="sxs-lookup"><span data-stu-id="2e637-125">The methods of **IWMDRMLicenseQuery** do not provide information about individual licenses.</span></span> <span data-ttu-id="2e637-126">Вместо этого данные лицензии объединяются подсистемой DRM перед возвратом результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="2e637-126">Instead, the license data is aggregated by the DRM subsystem before the query results are returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e637-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e637-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e637-128">**Интерфейсы**</span><span class="sxs-lookup"><span data-stu-id="2e637-128">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

