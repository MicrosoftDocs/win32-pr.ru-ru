---
description: Объект Феатуреинфо содержит сведения о целевом компоненте и создается из объекта Session с помощью метода Феатуреинфо.
ms.assetid: c9c96799-22c7-4e74-947b-3b8d31ebc1f1
title: Объект Феатуреинфо
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1db1bab5b1e55f027bb01eb9eff22484a4e39170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665090"
---
# <a name="featureinfo-object"></a><span data-ttu-id="28e8e-103">Объект Феатуреинфо</span><span class="sxs-lookup"><span data-stu-id="28e8e-103">FeatureInfo object</span></span>

<span data-ttu-id="28e8e-104">Объект **феатуреинфо** содержит сведения о целевом компоненте и создается из объекта [**Session**](session-object.md) с помощью метода [**феатуреинфо**](session-featureinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="28e8e-104">The **FeatureInfo** object contains information regarding the targeted feature and is created from the [**Session**](session-object.md) object using the [**FeatureInfo**](session-featureinfo.md) Method.</span></span>

## <a name="members"></a><span data-ttu-id="28e8e-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="28e8e-105">Members</span></span>

<span data-ttu-id="28e8e-106">Объект **феатуреинфо** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="28e8e-106">The **FeatureInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="28e8e-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="28e8e-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="28e8e-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="28e8e-108">Properties</span></span>

<span data-ttu-id="28e8e-109">Объект **феатуреинфо** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="28e8e-109">The **FeatureInfo** object has these properties.</span></span>



| <span data-ttu-id="28e8e-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="28e8e-110">Property</span></span>                                                  | <span data-ttu-id="28e8e-111">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="28e8e-111">Access type</span></span>           | <span data-ttu-id="28e8e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="28e8e-112">Description</span></span>                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28e8e-113">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="28e8e-113">**Attributes**</span></span>](featureinfo-attributes.md)<br/>   | <span data-ttu-id="28e8e-114">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="28e8e-114">Read/write</span></span><br/> | <span data-ttu-id="28e8e-115">Возвращает значение для функции в столбце Attributes таблицы Feature.</span><span class="sxs-lookup"><span data-stu-id="28e8e-115">Returns the value for the feature in the Attributes column of the Feature table.</span></span><br/> |
| [<span data-ttu-id="28e8e-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="28e8e-116">**Description**</span></span>](featureinfo-description.md)<br/> |                       | <span data-ttu-id="28e8e-117">Возвращает описание компонента.</span><span class="sxs-lookup"><span data-stu-id="28e8e-117">Returns the description of the feature.</span></span><br/>                                          |
| [<span data-ttu-id="28e8e-118">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="28e8e-118">**Title**</span></span>](featureinfo-title.md)<br/>             | <span data-ttu-id="28e8e-119">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="28e8e-119">Read-only</span></span><br/>  | <span data-ttu-id="28e8e-120">Возвращает название компонента.</span><span class="sxs-lookup"><span data-stu-id="28e8e-120">Returns the title of the feature.</span></span><br/>                                                |



 

## <a name="requirements"></a><span data-ttu-id="28e8e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="28e8e-121">Requirements</span></span>



| <span data-ttu-id="28e8e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="28e8e-122">Requirement</span></span> | <span data-ttu-id="28e8e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="28e8e-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28e8e-124">Версия</span><span class="sxs-lookup"><span data-stu-id="28e8e-124">Version</span></span><br/> | <span data-ttu-id="28e8e-125">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="28e8e-125">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="28e8e-126">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="28e8e-126">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="28e8e-127">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="28e8e-127">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="28e8e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="28e8e-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="28e8e-129"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28e8e-129"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="28e8e-130">IID</span><span class="sxs-lookup"><span data-stu-id="28e8e-130">IID</span></span><br/>     | <span data-ttu-id="28e8e-131">IID \_ ифеатуреинфо определяется как 000C109F-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="28e8e-131">IID\_IFeatureInfo is defined as 000C109F-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="28e8e-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28e8e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28e8e-133">Примеры сценариев установщик Windows</span><span class="sxs-lookup"><span data-stu-id="28e8e-133">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




