---
description: Указывает тип шифрования данных, используемый для подключения к беспроводной локальной сети.
ms.assetid: 0ba24106-bd6f-465a-af80-ce85501756b9
title: Элемент encryption (Аусенкриптион)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- encryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7efd9e0865cb489a7d033772112b0aaeb8a8fb23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154575"
---
# <a name="encryption-authencryption-element"></a><span data-ttu-id="ac995-103">Элемент encryption (Аусенкриптион)</span><span class="sxs-lookup"><span data-stu-id="ac995-103">encryption (authEncryption) Element</span></span>

<span data-ttu-id="ac995-104">Элемент encryption (Аусенкриптион) указывает тип шифрования данных, используемый для подключения к беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="ac995-104">The encryption (authEncryption) element specifies the type of data encryption to use to connect to a wireless LAN.</span></span>

``` syntax
<xs:element name="encryption">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="none"
             />
            <xs:enumeration
                value="WEP"
             />
            <xs:enumeration
                value="TKIP"
             />
            <xs:enumeration
                value="AES"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="ac995-105">Элемент определяется элементом [**аусенкриптион**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ac995-105">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac995-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac995-106">Remarks</span></span>

<span data-ttu-id="ac995-107">Если элемент **ENCRYPTION** имеет значение WEP, для параметра [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) должен быть задан параметр **нетворккэй**.</span><span class="sxs-lookup"><span data-stu-id="ac995-107">When the **encryption** element has a value of WEP, [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) must be set to **networkKey**.</span></span>

<span data-ttu-id="ac995-108">Метод шифрования AES указан в спецификациях [802.1 x](https://ieeexplore.ieee.org/document/1438730) и [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="ac995-108">The AES encryption method is as specified in the [802.1X](https://ieeexplore.ieee.org/document/1438730) and [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specifications.</span></span>

## <a name="examples"></a><span data-ttu-id="ac995-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="ac995-109">Examples</span></span>

<span data-ttu-id="ac995-110">Чтобы просмотреть образцы профилей, в которых используется элемент **ENCRYPTION** , см. раздел [образцы профилей беспроводной связи](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ac995-110">To view sample profiles that use the **encryption** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac995-111">Требования</span><span class="sxs-lookup"><span data-stu-id="ac995-111">Requirements</span></span>



| <span data-ttu-id="ac995-112">Требование</span><span class="sxs-lookup"><span data-stu-id="ac995-112">Requirement</span></span> | <span data-ttu-id="ac995-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ac995-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ac995-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac995-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ac995-115">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ac995-115">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ac995-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac995-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ac995-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ac995-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="ac995-118">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="ac995-118">Redistributable</span></span><br/>          | <span data-ttu-id="ac995-119">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="ac995-119">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="ac995-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac995-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="ac995-121">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="ac995-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ac995-122">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="ac995-122">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="ac995-123">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="ac995-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ac995-124">**Аусенкриптион (безопасность)**</span><span class="sxs-lookup"><span data-stu-id="ac995-124">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




