---
title: Сложный тип Чаннеллисттипе
description: Определяет список каналов, к которым поставщики могут регистрировать события. | Сложный тип Чаннеллисттипе
ms.assetid: 01685955-7149-45ce-a47f-6344fcf07826
keywords:
- Журнал событий сложных типов Чаннеллисттипе
topic_type:
- apiref
api_name:
- ChannelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 53293687fd4ab0d87155b86edd026189f6d7c925
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694070"
---
# <a name="channellisttype-complex-type"></a><span data-ttu-id="db13c-105">Сложный тип Чаннеллисттипе</span><span class="sxs-lookup"><span data-stu-id="db13c-105">ChannelListType Complex Type</span></span>

<span data-ttu-id="db13c-106">Определяет список каналов, к которым поставщики могут регистрировать события.</span><span class="sxs-lookup"><span data-stu-id="db13c-106">Defines a list of channels to which providers can log events.</span></span>

``` syntax
<xs:complexType name="ChannelListType">
    <xs:choice
        minOccurs="0"
        maxOccurs="8"
    >
        <xs:element name="importChannel"
            type="ImportChannelType"
         />
        <xs:element name="channel"
            type="ChannelType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="db13c-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="db13c-107">Child elements</span></span>



| <span data-ttu-id="db13c-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="db13c-108">Element</span></span>                                                                            | <span data-ttu-id="db13c-109">Тип</span><span class="sxs-lookup"><span data-stu-id="db13c-109">Type</span></span>                                                                           | <span data-ttu-id="db13c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="db13c-110">Description</span></span>                                                                                                                  |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db13c-111">**маркетинг**</span><span class="sxs-lookup"><span data-stu-id="db13c-111">**channel**</span></span>](eventmanifestschema-channel-channellisttype-element.md)             | [<span data-ttu-id="db13c-112">**чаннелтипе**</span><span class="sxs-lookup"><span data-stu-id="db13c-112">**ChannelType**</span></span>](eventmanifestschema-channeltype-complextype.md)             | <span data-ttu-id="db13c-113">Определяет канал, на который могут регистрироваться события.</span><span class="sxs-lookup"><span data-stu-id="db13c-113">Defines a channel to which events can be logged.</span></span><br/>                                                                  |
| [<span data-ttu-id="db13c-114">**импортчаннел**</span><span class="sxs-lookup"><span data-stu-id="db13c-114">**importChannel**</span></span>](eventmanifestschema-importchannel-channellisttype-element.md) | [<span data-ttu-id="db13c-115">**импортчаннелтипе**</span><span class="sxs-lookup"><span data-stu-id="db13c-115">**ImportChannelType**</span></span>](eventmanifestschema-importchanneltype-complextype.md) | <span data-ttu-id="db13c-116">Определяет канал, который был определен другим поставщиком или манифестом, содержащим раздел метаданных.</span><span class="sxs-lookup"><span data-stu-id="db13c-116">Identifies a channel that has been defined by another provider or in a manifest that contains a metadata section.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="db13c-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db13c-117">Remarks</span></span>

<span data-ttu-id="db13c-118">Можно указать до восьми каналов (любое сочетание импортированных каналов или каналов).</span><span class="sxs-lookup"><span data-stu-id="db13c-118">You can specify up to eight channels (any combination of imported channels or channels that you define).</span></span>

## <a name="requirements"></a><span data-ttu-id="db13c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="db13c-119">Requirements</span></span>



| <span data-ttu-id="db13c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="db13c-120">Requirement</span></span> | <span data-ttu-id="db13c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="db13c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="db13c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db13c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="db13c-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="db13c-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="db13c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db13c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="db13c-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="db13c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





