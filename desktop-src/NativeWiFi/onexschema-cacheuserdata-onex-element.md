---
description: Указывает, кэшируются ли учетные данные пользователя для последующих подключений.
ms.assetid: 65ed03f1-f61e-46f8-a666-91b393618de3
title: Элемент Качеусердата (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- cacheUserData
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8650bb2e5899e96f921d57460c8ba49ffab0ea66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998412"
---
# <a name="cacheuserdata-onex-element"></a><span data-ttu-id="6209c-103">Элемент Качеусердата (OneX)</span><span class="sxs-lookup"><span data-stu-id="6209c-103">cacheUserData (OneX) Element</span></span>

<span data-ttu-id="6209c-104">Элемент Качеусердата (OneX) указывает, кэшируются ли учетные данные пользователя для последующих соединений.</span><span class="sxs-lookup"><span data-stu-id="6209c-104">The cacheUserData (OneX) element specifies whether the user credentials are cached for subsequent connections.</span></span> <span data-ttu-id="6209c-105">Если Качеусердата имеет значение TRUE, учетные данные кэшируются.</span><span class="sxs-lookup"><span data-stu-id="6209c-105">When cacheUserData is TRUE, the credentials are cached.</span></span> <span data-ttu-id="6209c-106">Если Качеусердата имеет значение FALSE, учетные данные не кэшируются, и пользователь может получить запрос на ввод учетных данных при последующих попытках подключения.</span><span class="sxs-lookup"><span data-stu-id="6209c-106">When cacheUserData is FALSE, the credentials are not cached and the user may be prompted for credentials on subsequent connection attempts.</span></span>

<span data-ttu-id="6209c-107">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6209c-107">This element is optional.</span></span> <span data-ttu-id="6209c-108">Если Качеусердата не указан в профиле, то учетные данные пользователя кэшируются.</span><span class="sxs-lookup"><span data-stu-id="6209c-108">When cacheUserData is not specified in a profile, the user credentials are cached.</span></span>

<span data-ttu-id="6209c-109">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.</span><span class="sxs-lookup"><span data-stu-id="6209c-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="cacheUserData"
    type="boolean"
 />
```

<span data-ttu-id="6209c-110">Элемент **качеусердата** определяется элементом [**OneX**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6209c-110">The **cacheUserData** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="6209c-111">Требования</span><span class="sxs-lookup"><span data-stu-id="6209c-111">Requirements</span></span>



| <span data-ttu-id="6209c-112">Требование</span><span class="sxs-lookup"><span data-stu-id="6209c-112">Requirement</span></span> | <span data-ttu-id="6209c-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6209c-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6209c-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6209c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6209c-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6209c-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6209c-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6209c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6209c-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6209c-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6209c-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6209c-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="6209c-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="6209c-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6209c-120">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="6209c-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="6209c-121">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="6209c-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6209c-122">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="6209c-122">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




