---
title: Сложный тип Басиапмесодконфиг
description: Сведения о сложном типе Басиапмесодконфиг. Этот тип является элементом-заполнителем для конфигурации метода.
ms.assetid: 9aafd6ad-2342-4882-99d3-2f2e6c3d67b5
keywords:
- Басиапмесодконфиг сложный тип EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac7d628b554696fffd254a45b9b1021d68e2a55e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413765"
---
# <a name="baseeapmethodconfig-complex-type"></a><span data-ttu-id="1b4f9-105">Сложный тип Басиапмесодконфиг</span><span class="sxs-lookup"><span data-stu-id="1b4f9-105">BaseEapMethodConfig Complex Type</span></span>

<span data-ttu-id="1b4f9-106">Сложный тип **басиапмесодконфиг** — это элемент-заполнитель для конфигурации метода.</span><span class="sxs-lookup"><span data-stu-id="1b4f9-106">The **BaseEapMethodConfig** complex type is a placeholder element for the method configuration.</span></span>

``` syntax
<xs:complexType name="BaseEapMethodConfig">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a><span data-ttu-id="1b4f9-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b4f9-107">Remarks</span></span>

<span data-ttu-id="1b4f9-108">Метод EAP выполняет проверку схемы содержимого элемента **басиапмесодконфиг** .</span><span class="sxs-lookup"><span data-stu-id="1b4f9-108">The EAP method performs schema validation on the contents of the **BaseEapMethodConfig** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b4f9-109">Требования</span><span class="sxs-lookup"><span data-stu-id="1b4f9-109">Requirements</span></span>



| <span data-ttu-id="1b4f9-110">Роль</span><span class="sxs-lookup"><span data-stu-id="1b4f9-110">Role</span></span> | <span data-ttu-id="1b4f9-111">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="1b4f9-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="1b4f9-112">Клиент</span><span class="sxs-lookup"><span data-stu-id="1b4f9-112">Client</span></span><br/> | <span data-ttu-id="1b4f9-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b4f9-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1b4f9-114">Сервер</span><span class="sxs-lookup"><span data-stu-id="1b4f9-114">Server</span></span><br/> | <span data-ttu-id="1b4f9-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1b4f9-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b4f9-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b4f9-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b4f9-117">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="1b4f9-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="1b4f9-118">Схема басиапмесодконфиг</span><span class="sxs-lookup"><span data-stu-id="1b4f9-118">baseeapmethodconfig Schema</span></span>](baseeapmethodconfigschema-schema.md)
</dt> </dl>

 

 





