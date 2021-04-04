---
description: Указывает источник параметров безопасности 802.1 X, используемых компонентом безопасности независимого поставщика оборудования.
ms.assetid: 9c216319-d962-4c68-89a3-116eff3f4376
title: Усемсонекс (IHV), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useMSOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: aa9f2092ac0e76feae89b02f333ae3098288ccef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998734"
---
# <a name="usemsonex-ihv-element"></a><span data-ttu-id="13d59-103">Усемсонекс (IHV), элемент</span><span class="sxs-lookup"><span data-stu-id="13d59-103">useMSOneX (IHV) Element</span></span>

<span data-ttu-id="13d59-104">Элемент **усемсонекс** (IHV) указывает происхождение параметров безопасности 802.1 x, используемых компонентом безопасности IHV.</span><span class="sxs-lookup"><span data-stu-id="13d59-104">The **useMSOneX** (IHV) element specifies the origin of 802.1X security settings used by an IHV security component.</span></span>

<span data-ttu-id="13d59-105">Если **усемсонекс** имеет значение true, компоненты безопасности IHV используют определенные корпорацией Майкрософт параметры 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="13d59-105">When **useMSOneX** is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="13d59-106">Если **усемсонекс** имеет значение false, компоненты безопасности IHV используют предоставленные поставщиком параметры 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="13d59-106">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span>

<span data-ttu-id="13d59-107">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="13d59-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="useMSOneX"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="13d59-108">Элемент определяется элементом [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="13d59-108">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="13d59-109">Требования</span><span class="sxs-lookup"><span data-stu-id="13d59-109">Requirements</span></span>



| <span data-ttu-id="13d59-110">Требование</span><span class="sxs-lookup"><span data-stu-id="13d59-110">Requirement</span></span> | <span data-ttu-id="13d59-111">Значение</span><span class="sxs-lookup"><span data-stu-id="13d59-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="13d59-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13d59-112">Minimum supported client</span></span><br/> | <span data-ttu-id="13d59-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="13d59-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="13d59-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13d59-114">Minimum supported server</span></span><br/> | <span data-ttu-id="13d59-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="13d59-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="13d59-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13d59-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="13d59-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="13d59-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="13d59-118">**АППАРАТ**</span><span class="sxs-lookup"><span data-stu-id="13d59-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="13d59-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="13d59-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="13d59-120">**IHV (Вланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="13d59-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




