---
description: Клиентский объект представляет связь между компонентом и клиентским продуктом.
ms.assetid: ac1fbd74-fbc4-4f76-8e14-af48443a8528
title: Клиентский объект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Client
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 75cb21a4149d8e6758ab24796949777b8052b120
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668564"
---
# <a name="client-object"></a><span data-ttu-id="3f450-103">Клиентский объект</span><span class="sxs-lookup"><span data-stu-id="3f450-103">Client object</span></span>

<span data-ttu-id="3f450-104">Клиентский объект представляет связь между компонентом и клиентским продуктом.</span><span class="sxs-lookup"><span data-stu-id="3f450-104">The Client object represents a relationship between a component and client product.</span></span>

<span data-ttu-id="3f450-105">**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3f450-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="3f450-106">Этот объект доступен, начиная с установщик Windows 5,0.</span><span class="sxs-lookup"><span data-stu-id="3f450-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="3f450-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="3f450-107">Members</span></span>

<span data-ttu-id="3f450-108">**Клиентский** объект имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3f450-108">The **Client** object has these types of members:</span></span>

-   [<span data-ttu-id="3f450-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="3f450-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3f450-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="3f450-110">Properties</span></span>

<span data-ttu-id="3f450-111">**Клиентский** объект имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="3f450-111">The **Client** object has these properties.</span></span>



| <span data-ttu-id="3f450-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="3f450-112">Property</span></span>                                                 | <span data-ttu-id="3f450-113">Описание</span><span class="sxs-lookup"><span data-stu-id="3f450-113">Description</span></span>                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="3f450-114">**компоненткоде**</span><span class="sxs-lookup"><span data-stu-id="3f450-114">**ComponentCode**</span></span>](client-componentcode.md)<br/> | <span data-ttu-id="3f450-115">Код компонента рассматриваемого компонента.</span><span class="sxs-lookup"><span data-stu-id="3f450-115">The component code of the component in question.</span></span><br/> |
| [<span data-ttu-id="3f450-116">**Локального**</span><span class="sxs-lookup"><span data-stu-id="3f450-116">**Context**</span></span>](client-context.md)<br/>             | <span data-ttu-id="3f450-117">Контекст продукта.</span><span class="sxs-lookup"><span data-stu-id="3f450-117">The context of the product.</span></span><br/>                      |
| [<span data-ttu-id="3f450-118">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="3f450-118">**ProductCode**</span></span>](client-productcode.md)<br/>     | <span data-ttu-id="3f450-119">Клиентское программное произведение рассматриваемого компонента.</span><span class="sxs-lookup"><span data-stu-id="3f450-119">The client product of the component in question.</span></span><br/> |
| [<span data-ttu-id="3f450-120">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="3f450-120">**UserSID**</span></span>](client-usersid.md)<br/>             | <span data-ttu-id="3f450-121">Идентификатор безопасности пользователя для компонента.</span><span class="sxs-lookup"><span data-stu-id="3f450-121">The user SID for the component.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="3f450-122">Требования</span><span class="sxs-lookup"><span data-stu-id="3f450-122">Requirements</span></span>



| <span data-ttu-id="3f450-123">Требование</span><span class="sxs-lookup"><span data-stu-id="3f450-123">Requirement</span></span> | <span data-ttu-id="3f450-124">Значение</span><span class="sxs-lookup"><span data-stu-id="3f450-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3f450-125">Версия</span><span class="sxs-lookup"><span data-stu-id="3f450-125">Version</span></span><br/> | <span data-ttu-id="3f450-126">Установщик Windows 5,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="3f450-126">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="3f450-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3f450-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="3f450-128"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f450-128"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="3f450-129">IID</span><span class="sxs-lookup"><span data-stu-id="3f450-129">IID</span></span><br/>     | <span data-ttu-id="3f450-130">IID \_ иклиент определен как 000C1098-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3f450-130">IID\_IClient is defined as 000C1098-0000-0000-C000-000000000046</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="3f450-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f450-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f450-132">Использование интерфейса автоматизации</span><span class="sxs-lookup"><span data-stu-id="3f450-132">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="3f450-133">Примеры сценариев установщик Windows</span><span class="sxs-lookup"><span data-stu-id="3f450-133">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




