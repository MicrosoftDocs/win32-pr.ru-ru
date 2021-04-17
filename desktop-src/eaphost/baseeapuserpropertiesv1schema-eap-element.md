---
title: Элемент EAP (свойство User)
description: Сведения об элементе EAP. Этот элемент захватывает выбранный тип метода и конфигурацию конкретного метода. | Элемент EAP (свойство User)
ms.assetid: 4adef133-1d18-444a-baa3-5419b8cbe298
keywords:
- Элемент EAP EAPHost
topic_type:
- apiref
api_name:
- Eap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 23f00b5162ddb42efd9fae759bab1ea47efc04dc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105713400"
---
# <a name="eap-element-user-property"></a><span data-ttu-id="cc92c-106">Элемент EAP (свойство User)</span><span class="sxs-lookup"><span data-stu-id="cc92c-106">Eap element (user property)</span></span>

<span data-ttu-id="cc92c-107">Элемент **EAP** захватывает выбранный тип метода и конфигурацию конкретного метода.</span><span class="sxs-lookup"><span data-stu-id="cc92c-107">The **Eap** element captures the method type selected and method-specific configuration.</span></span>

``` syntax
<xs:element name="Eap"
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="cc92c-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc92c-108">Remarks</span></span>

<span data-ttu-id="cc92c-109">Метод может определять составные элементы внутри элемента **EAP** .</span><span class="sxs-lookup"><span data-stu-id="cc92c-109">The method can define the constituent elements inside the **Eap** element.</span></span> <span data-ttu-id="cc92c-110">Метод также выполняет проверку схемы для элементов в **EAP**.</span><span class="sxs-lookup"><span data-stu-id="cc92c-110">The method also performs schema validation on the elements in **Eap**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc92c-111">Требования</span><span class="sxs-lookup"><span data-stu-id="cc92c-111">Requirements</span></span>



| <span data-ttu-id="cc92c-112">Роль</span><span class="sxs-lookup"><span data-stu-id="cc92c-112">Role</span></span> | <span data-ttu-id="cc92c-113">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="cc92c-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="cc92c-114">Клиент</span><span class="sxs-lookup"><span data-stu-id="cc92c-114">Client</span></span><br/> | <span data-ttu-id="cc92c-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc92c-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cc92c-116">Сервер</span><span class="sxs-lookup"><span data-stu-id="cc92c-116">Server</span></span><br/> | <span data-ttu-id="cc92c-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc92c-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc92c-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc92c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc92c-119">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="cc92c-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="cc92c-120">Схема baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="cc92c-120">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





