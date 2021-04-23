---
title: Интерфейс Ивмдрминдивидуализатионстатус
description: Интерфейс Ивмдрминдивидуализатионстатус позволяет получать дополнительные сведения о состоянии процесса индивидуализации. Этот интерфейс поставляется с событиями Мевмдрминдивидуализатионпрогресс.
ms.assetid: 3a148005-22fa-4495-a47c-d9463db16293
keywords:
- Формат Windows Media в интерфейсе Ивмдрминдивидуализатионстатус
- Ивмдрминдивидуализатионстатус интерфейса Windows Media Format, описание
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19a369bf9b70d9a43af8a48f13f1b8bbb87525b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987760"
---
# <a name="iwmdrmindividualizationstatus-interface"></a><span data-ttu-id="d69df-105">Интерфейс Ивмдрминдивидуализатионстатус</span><span class="sxs-lookup"><span data-stu-id="d69df-105">IWMDRMIndividualizationStatus interface</span></span>

<span data-ttu-id="d69df-106">Интерфейс **ивмдрминдивидуализатионстатус** позволяет получать дополнительные сведения о состоянии процесса индивидуализации.</span><span class="sxs-lookup"><span data-stu-id="d69df-106">The **IWMDRMIndividualizationStatus** interface enables retrieval of advanced status information about the progress of individualization.</span></span>

<span data-ttu-id="d69df-107">Этот интерфейс поставляется с событиями Мевмдрминдивидуализатионпрогресс.</span><span class="sxs-lookup"><span data-stu-id="d69df-107">This interface is delivered with MEWMDRMIndividualizationProgress events.</span></span> <span data-ttu-id="d69df-108">Многие такие события создаются между вызовом [**ивмдрмсекурити::P ерформсекуритюпдате**](iwmdrmsecurity-performsecurityupdate.md) и завершением процесса индивидуализации, который оповещается о формировании события **мевмдрминдивидуализатионкомплетед** .</span><span class="sxs-lookup"><span data-stu-id="d69df-108">Many such events are generated between a call to [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) and the completion of the individualization process, which is signaled by the generation of an **MEWMDRMIndividualizationCompleted** event.</span></span>

<span data-ttu-id="d69df-109">Чтобы получить указатель на экземпляр интерфейса **ивмдрминдивидуализатионстатус** , необходимо сначала вызвать метод **Имфмедиаевент:: GetValue** события Progress.</span><span class="sxs-lookup"><span data-stu-id="d69df-109">To retrieve a pointer to an instance of the **IWMDRMIndividualizationStatus** interface, you must first call the **IMFMediaEvent::GetValue** method of the progress event.</span></span> <span data-ttu-id="d69df-110">Значение, получаемое из события, является указателем на интерфейс **IUnknown** объекта, реализующего интерфейс **ивмдрминдивидуализатионстатус** .</span><span class="sxs-lookup"><span data-stu-id="d69df-110">The value you retrieve from the event is a pointer to the **IUnknown** interface of the object that implements the **IWMDRMIndividualizationStatus** interface.</span></span>

## <a name="members"></a><span data-ttu-id="d69df-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="d69df-111">Members</span></span>

<span data-ttu-id="d69df-112">Интерфейс **ивмдрминдивидуализатионстатус** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d69df-112">The **IWMDRMIndividualizationStatus** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d69df-113">**Ивмдрминдивидуализатионстатус** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d69df-113">**IWMDRMIndividualizationStatus** also has these types of members:</span></span>

-   [<span data-ttu-id="d69df-114">Методы</span><span class="sxs-lookup"><span data-stu-id="d69df-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d69df-115">Методы</span><span class="sxs-lookup"><span data-stu-id="d69df-115">Methods</span></span>

<span data-ttu-id="d69df-116">Интерфейс **ивмдрминдивидуализатионстатус** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d69df-116">The **IWMDRMIndividualizationStatus** interface has these methods.</span></span>



| <span data-ttu-id="d69df-117">Метод</span><span class="sxs-lookup"><span data-stu-id="d69df-117">Method</span></span>                                                       | <span data-ttu-id="d69df-118">Описание</span><span class="sxs-lookup"><span data-stu-id="d69df-118">Description</span></span>                                                        |
|:-------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="d69df-119">**GetStatus**</span><span class="sxs-lookup"><span data-stu-id="d69df-119">**GetStatus**</span></span>](iwmdrmindividualizationstatus-getstatus.md) | <span data-ttu-id="d69df-120">Получает подробные сведения о индивидуализации.</span><span class="sxs-lookup"><span data-stu-id="d69df-120">Retrieves detailed information about individualization.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d69df-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d69df-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d69df-122">**Интерфейсы**</span><span class="sxs-lookup"><span data-stu-id="d69df-122">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

