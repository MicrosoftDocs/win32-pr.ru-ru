---
description: Указывает, используется ли проверка подлинности 802.1 X.
ms.assetid: dbddaf5a-7574-4282-ab4d-f6f697ed94ab
title: Усеонекс (Аусенкриптион), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: cb327be4006e8da0074815a74e49d3ccdc5d3c84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673919"
---
# <a name="useonex-authencryption-element"></a><span data-ttu-id="b6a90-103">Усеонекс (Аусенкриптион), элемент</span><span class="sxs-lookup"><span data-stu-id="b6a90-103">useOneX (authEncryption) Element</span></span>

<span data-ttu-id="b6a90-104">Элемент Усеонекс (Аусенкриптион) указывает, используется ли проверка подлинности 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="b6a90-104">The useOneX (authEncryption) element indicates whether 802.1X authentication is used.</span></span>

``` syntax
<xs:element name="useOneX"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="b6a90-105">Элемент определяется элементом [**аусенкриптион**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b6a90-105">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="b6a90-106">Примеры</span><span class="sxs-lookup"><span data-stu-id="b6a90-106">Examples</span></span>

<span data-ttu-id="b6a90-107">Чтобы просмотреть образцы профилей, использующих элемент **усеонекс** , см. раздел [образцы профиля беспроводной связи](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="b6a90-107">To view sample profiles that use the **useOneX** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6a90-108">Требования</span><span class="sxs-lookup"><span data-stu-id="b6a90-108">Requirements</span></span>



| <span data-ttu-id="b6a90-109">Требование</span><span class="sxs-lookup"><span data-stu-id="b6a90-109">Requirement</span></span> | <span data-ttu-id="b6a90-110">Значение</span><span class="sxs-lookup"><span data-stu-id="b6a90-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b6a90-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6a90-111">Minimum supported client</span></span><br/> | <span data-ttu-id="b6a90-112">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b6a90-112">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b6a90-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6a90-113">Minimum supported server</span></span><br/> | <span data-ttu-id="b6a90-114">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b6a90-114">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="b6a90-115">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="b6a90-115">Redistributable</span></span><br/>          | <span data-ttu-id="b6a90-116">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="b6a90-116">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="b6a90-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6a90-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="b6a90-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="b6a90-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b6a90-119">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="b6a90-119">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="b6a90-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="b6a90-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b6a90-121">**Аусенкриптион (безопасность)**</span><span class="sxs-lookup"><span data-stu-id="b6a90-121">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




