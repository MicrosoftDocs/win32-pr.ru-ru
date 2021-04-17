---
title: Элемент EAP (свойства соединения)
description: Сведения об элементе EAP. Этот элемент захватывает выбранный тип метода и конфигурацию конкретного метода. | Элемент EAP (свойства соединения)
ms.assetid: 4e9f3869-257e-4b03-93f6-2eec94eaacee
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
ms.openlocfilehash: c39812d00ecf9a1183eb81fc03b09b146d751f0e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693972"
---
# <a name="eap-element-connection-properties"></a><span data-ttu-id="181c5-106">Элемент EAP (свойства соединения)</span><span class="sxs-lookup"><span data-stu-id="181c5-106">Eap Element (connection properties)</span></span>

<span data-ttu-id="181c5-107">Элемент **EAP** захватывает выбранный тип метода и конфигурацию конкретного метода.</span><span class="sxs-lookup"><span data-stu-id="181c5-107">The **Eap** element captures the method type selected and method-specific configuration.</span></span>

``` syntax
<xs:element name="Eap
          
        "
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="181c5-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="181c5-108">Remarks</span></span>

<span data-ttu-id="181c5-109">Метод может определять составные элементы внутри элемента **EAP** .</span><span class="sxs-lookup"><span data-stu-id="181c5-109">The method can define the constituent elements inside the **Eap** element.</span></span> <span data-ttu-id="181c5-110">Метод также выполняет проверку схемы для элементов в **EAP**.</span><span class="sxs-lookup"><span data-stu-id="181c5-110">The method also performs schema validation on the elements in **Eap**.</span></span>

## <a name="requirements"></a><span data-ttu-id="181c5-111">Требования</span><span class="sxs-lookup"><span data-stu-id="181c5-111">Requirements</span></span>



| <span data-ttu-id="181c5-112">Роль</span><span class="sxs-lookup"><span data-stu-id="181c5-112">Role</span></span> | <span data-ttu-id="181c5-113">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="181c5-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="181c5-114">Клиент</span><span class="sxs-lookup"><span data-stu-id="181c5-114">Client</span></span><br/> | <span data-ttu-id="181c5-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="181c5-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="181c5-116">Сервер</span><span class="sxs-lookup"><span data-stu-id="181c5-116">Server</span></span><br/> | <span data-ttu-id="181c5-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="181c5-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="181c5-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="181c5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="181c5-119">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="181c5-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="181c5-120">Схема baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="181c5-120">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





