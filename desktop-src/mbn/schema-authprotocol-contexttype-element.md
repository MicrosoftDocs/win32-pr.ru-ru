---
description: Указывает протокол проверки подлинности, используемый для активации контекста протокола данных пакетов (PDP).
ms.assetid: cd3c28d9-8663-4672-94ba-0a53861086cb
title: Ауспротокол (contextType), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthProtocol
api_type:
- Schema
ms.openlocfilehash: 8626d17a234784491c5f186f800943a6ab208bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682660"
---
# <a name="authprotocol-contexttype-element"></a><span data-ttu-id="ac719-103">Ауспротокол (contextType), элемент</span><span class="sxs-lookup"><span data-stu-id="ac719-103">AuthProtocol (contextType) Element</span></span>

<span data-ttu-id="ac719-104">Элемент **ауспротокол (ContextType)** указывает протокол проверки подлинности, используемый для активации контекста протокола данных пакетов (PDP).</span><span class="sxs-lookup"><span data-stu-id="ac719-104">The **AuthProtocol (contextType)** element specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span>

<span data-ttu-id="ac719-105">Элемент может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ac719-105">The element can have one of the following values.</span></span>

| <span data-ttu-id="ac719-106">Значение</span><span class="sxs-lookup"><span data-stu-id="ac719-106">Value</span></span>      | <span data-ttu-id="ac719-107">Значение</span><span class="sxs-lookup"><span data-stu-id="ac719-107">Meaning</span></span>                                                                 |
|------------|-------------------------------------------------------------------------|
| <span data-ttu-id="ac719-108">None</span><span class="sxs-lookup"><span data-stu-id="ac719-108">"NONE"</span></span>     | <span data-ttu-id="ac719-109">Без протокола проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ac719-109">No authentication protocol.</span></span>                                             |
| <span data-ttu-id="ac719-110">PAP</span><span class="sxs-lookup"><span data-stu-id="ac719-110">"PAP"</span></span>      | <span data-ttu-id="ac719-111">Проверка подлинности без шифрования пароля.</span><span class="sxs-lookup"><span data-stu-id="ac719-111">Unencrypted password authentication.</span></span>                                    |
| <span data-ttu-id="ac719-112">ПРОТОКОЛА</span><span class="sxs-lookup"><span data-stu-id="ac719-112">"CHAP"</span></span>     | <span data-ttu-id="ac719-113">Протокол проверки пароля (CHAP).</span><span class="sxs-lookup"><span data-stu-id="ac719-113">Challenge Handshake Authentication Protocol(CHAP).</span></span>                      |
|  <span data-ttu-id="ac719-114">MsCHAPV2</span><span class="sxs-lookup"><span data-stu-id="ac719-114">MsCHAPV2"</span></span> | <span data-ttu-id="ac719-115">Используйте протокол проверки пароля (CHAP) версии 2.0 (Microsoft s).</span><span class="sxs-lookup"><span data-stu-id="ac719-115">Use Microsoft s Challenge Handshake Authentication Protocol(CHAP) v2.0.</span></span> |



 

<span data-ttu-id="ac719-116">Этот элемент является необязательным и используется только для профилей GSM.</span><span class="sxs-lookup"><span data-stu-id="ac719-116">This element is optional and is used only for GSM profiles.</span></span> <span data-ttu-id="ac719-117">Если элемент не указан и профиль предназначен для устройства GSM, то служба мобильной широкополосной связи будет использовать **"нет"**.</span><span class="sxs-lookup"><span data-stu-id="ac719-117">If the element is not specified and the profile is for a GSM device, then the Mobile Broadband service will use **"NONE"**.</span></span>

``` syntax
<xs:element name="AuthProtocol">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="NONE"
             />
            <xs:enumeration
                value="PAP"
             />
            <xs:enumeration
                value="CHAP"
             />
            <xs:enumeration
                value="MsCHAPv2"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="ac719-118">Элемент **ауспротокол** определяется сложным типом [**ContextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ac719-118">The **AuthProtocol** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac719-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ac719-119">Requirements</span></span>



| <span data-ttu-id="ac719-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ac719-120">Requirement</span></span> | <span data-ttu-id="ac719-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ac719-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="ac719-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac719-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ac719-123">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="ac719-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="ac719-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac719-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ac719-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ac719-125">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="ac719-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac719-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="ac719-127">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="ac719-127">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ac719-128">**contextType**</span><span class="sxs-lookup"><span data-stu-id="ac719-128">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="ac719-129">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="ac719-129">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ac719-130">**Контекст (Мбнпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="ac719-130">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




