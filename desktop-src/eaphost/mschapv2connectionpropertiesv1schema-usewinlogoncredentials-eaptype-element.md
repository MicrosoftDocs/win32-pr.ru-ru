---
title: Усевинлогонкредентиалс (Еаптипе), элемент
description: Сведения об элементе Усевинлогонкредентиалс (Еаптипе). Этот элемент управляет использованием учетных данных винлогин.
ms.assetid: 8ebd87ce-7d2b-4305-b50c-239bb9c7af75
keywords:
- Элемент Усевинлогонкредентиалс EAPHost
topic_type:
- apiref
api_name:
- UseWinLogonCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f17520d4eaee64d3dd9809ecb465ca8e39690fc4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793927"
---
# <a name="usewinlogoncredentials-eaptype-element"></a><span data-ttu-id="c56e0-105">Усевинлогонкредентиалс (Еаптипе), элемент</span><span class="sxs-lookup"><span data-stu-id="c56e0-105">UseWinLogonCredentials (EapType) Element</span></span>

<span data-ttu-id="c56e0-106">Элемент **усевинлогонкредентиалс (еаптипе)** управляет использованием учетных данных винлогин.</span><span class="sxs-lookup"><span data-stu-id="c56e0-106">The **UseWinLogonCredentials (EapType)** element controls use of the winlogin credentials.</span></span>

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

<span data-ttu-id="c56e0-107">Элемент **усевинлогонкредентиалс** определяется элементом [**еаптипе**](mschapv2connectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c56e0-107">The **UseWinLogonCredentials** element is defined by the [**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="c56e0-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c56e0-108">Remarks</span></span>

<span data-ttu-id="c56e0-109">Если значение — TRUE, EAP MS-CHAPv2 получает учетные данные из Winlogon.</span><span class="sxs-lookup"><span data-stu-id="c56e0-109">If TRUE, then EAP MS-CHAPv2 obtains credentials from winlogon.</span></span> <span data-ttu-id="c56e0-110">Если значение равно FALSE, то EAP MS-CHAPv2 получает учетные данные от пользователя.</span><span class="sxs-lookup"><span data-stu-id="c56e0-110">If FALSE, then EAP MS-CHAPv2 obtains credentials from the user.</span></span> <span data-ttu-id="c56e0-111">Элемент **усевинлогонкредентиалс (еаптипе)** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c56e0-111">The **UseWinLogonCredentials (EapType)** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="c56e0-112">Требования</span><span class="sxs-lookup"><span data-stu-id="c56e0-112">Requirements</span></span>



| <span data-ttu-id="c56e0-113">Роль</span><span class="sxs-lookup"><span data-stu-id="c56e0-113">Role</span></span> | <span data-ttu-id="c56e0-114">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="c56e0-114">Minimum supported OS versions</span></span> |
|------|-------------------------------|
| <span data-ttu-id="c56e0-115">Клиент</span><span class="sxs-lookup"><span data-stu-id="c56e0-115">Client</span></span><br/> | <span data-ttu-id="c56e0-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c56e0-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c56e0-117">Сервер</span><span class="sxs-lookup"><span data-stu-id="c56e0-117">Server</span></span><br/> | <span data-ttu-id="c56e0-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c56e0-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c56e0-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c56e0-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="c56e0-120">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="c56e0-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c56e0-121">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="c56e0-121">**EapType**</span></span>](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="c56e0-122">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="c56e0-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c56e0-123">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="c56e0-123">**EapType**</span></span>](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="c56e0-124">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="c56e0-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="c56e0-125">Схема mschapv2connectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c56e0-125">mschapv2connectionpropertiesv1 Schema</span></span>](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





