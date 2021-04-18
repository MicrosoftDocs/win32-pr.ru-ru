---
description: Объект Component представляет уникальный экземпляр компонента, доступного для перечисления.
ms.assetid: cdc99bc3-9e2a-49db-8c01-b9634aefac38
title: Объект Component
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Component
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5e31d6a7c3d2422111d0d8c3247e022fa35bdc43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651884"
---
# <a name="component-object"></a><span data-ttu-id="fb88b-103">Объект Component</span><span class="sxs-lookup"><span data-stu-id="fb88b-103">Component object</span></span>

<span data-ttu-id="fb88b-104">Объект Component представляет уникальный экземпляр компонента, доступного для перечисления.</span><span class="sxs-lookup"><span data-stu-id="fb88b-104">The Component object represents a unique instance of a component that is available for enumeration.</span></span>

<span data-ttu-id="fb88b-105">**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fb88b-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="fb88b-106">Этот объект доступен, начиная с установщик Windows 5,0.</span><span class="sxs-lookup"><span data-stu-id="fb88b-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="fb88b-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="fb88b-107">Members</span></span>

<span data-ttu-id="fb88b-108">Объект **компонента** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fb88b-108">The **Component** object has these types of members:</span></span>

-   [<span data-ttu-id="fb88b-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="fb88b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb88b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="fb88b-110">Properties</span></span>

<span data-ttu-id="fb88b-111">Объект **компонента** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fb88b-111">The **Component** object has these properties.</span></span>



| <span data-ttu-id="fb88b-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="fb88b-112">Property</span></span>                                                    | <span data-ttu-id="fb88b-113">Описание</span><span class="sxs-lookup"><span data-stu-id="fb88b-113">Description</span></span>                                                                               |
|:------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb88b-114">**компоненткоде**</span><span class="sxs-lookup"><span data-stu-id="fb88b-114">**ComponentCode**</span></span>](component-componentcode.md)<br/> | <span data-ttu-id="fb88b-115">Код компонента рассматриваемого компонента.</span><span class="sxs-lookup"><span data-stu-id="fb88b-115">The component code of the component in question.</span></span><br/>                               |
| [<span data-ttu-id="fb88b-116">**Локального**</span><span class="sxs-lookup"><span data-stu-id="fb88b-116">**Context**</span></span>](component-context.md)<br/>             | <span data-ttu-id="fb88b-117">Контекст, который был определен как применимый к рассматриваемому компоненту.</span><span class="sxs-lookup"><span data-stu-id="fb88b-117">The context that was determined to be applicable to the component in question.</span></span><br/> |
| [<span data-ttu-id="fb88b-118">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="fb88b-118">**UserSID**</span></span>](component-usersid.md)<br/>             | <span data-ttu-id="fb88b-119">Идентификатор безопасности пользователя для перечисленного компонента.</span><span class="sxs-lookup"><span data-stu-id="fb88b-119">The user SID for the enumerated component.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="fb88b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="fb88b-120">Requirements</span></span>



| <span data-ttu-id="fb88b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="fb88b-121">Requirement</span></span> | <span data-ttu-id="fb88b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="fb88b-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb88b-123">Версия</span><span class="sxs-lookup"><span data-stu-id="fb88b-123">Version</span></span><br/> | <span data-ttu-id="fb88b-124">Установщик Windows 5,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="fb88b-124">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="fb88b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fb88b-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="fb88b-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb88b-126"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="fb88b-127">IID</span><span class="sxs-lookup"><span data-stu-id="fb88b-127">IID</span></span><br/>     | <span data-ttu-id="fb88b-128">IID интерфейса \_ IComponent определяется как 000C1097-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fb88b-128">IID\_IComponent is defined as 000C1097-0000-0000-C000-000000000046</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="fb88b-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb88b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb88b-130">Использование интерфейса автоматизации</span><span class="sxs-lookup"><span data-stu-id="fb88b-130">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="fb88b-131">Примеры сценариев установщик Windows</span><span class="sxs-lookup"><span data-stu-id="fb88b-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




