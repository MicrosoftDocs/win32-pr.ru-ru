---
title: Сложный тип Басиапмесодусеркредентиалс
description: Сведения о сложном типе Басиапмесодусеркредентиалс. Этот тип является элементом-заполнителем для учетных данных метода.
ms.assetid: ebbf813d-657a-4ff2-acf2-c18ce694b564
keywords:
- Басиапмесодусеркредентиалс сложный тип EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37bc7a91a5d90cde6cba1af12bb0a4784ee21c7f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793783"
---
# <a name="baseeapmethodusercredentials-complex-type"></a><span data-ttu-id="b4d24-105">Сложный тип Басиапмесодусеркредентиалс</span><span class="sxs-lookup"><span data-stu-id="b4d24-105">BaseEapMethodUserCredentials Complex Type</span></span>

<span data-ttu-id="b4d24-106">Сложный тип **басиапмесодусеркредентиалс** — это элемент-заполнитель для учетных данных метода.</span><span class="sxs-lookup"><span data-stu-id="b4d24-106">The **BaseEapMethodUserCredentials** complex type is a placeholder element for method credential data.</span></span>

``` syntax
<xs:complexType name="BaseEapMethodUserCredentials">
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

## <a name="remarks"></a><span data-ttu-id="b4d24-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4d24-107">Remarks</span></span>

<span data-ttu-id="b4d24-108">Метод EAP выполняет проверку схемы содержимого **басиапмесодусеркредентиалс**.</span><span class="sxs-lookup"><span data-stu-id="b4d24-108">The EAP method performs schema validation on the contents of **BaseEapMethodUserCredentials**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4d24-109">Требования</span><span class="sxs-lookup"><span data-stu-id="b4d24-109">Requirements</span></span>



| <span data-ttu-id="b4d24-110">Роль</span><span class="sxs-lookup"><span data-stu-id="b4d24-110">Role</span></span> | <span data-ttu-id="b4d24-111">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="b4d24-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="b4d24-112">Клиент</span><span class="sxs-lookup"><span data-stu-id="b4d24-112">Client</span></span><br/> | <span data-ttu-id="b4d24-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b4d24-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b4d24-114">Сервер</span><span class="sxs-lookup"><span data-stu-id="b4d24-114">Server</span></span><br/> | <span data-ttu-id="b4d24-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b4d24-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4d24-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4d24-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4d24-117">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="b4d24-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b4d24-118">Схема басиапмесодусеркредентиалс</span><span class="sxs-lookup"><span data-stu-id="b4d24-118">baseeapmethodusercredentials Schema</span></span>](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 





