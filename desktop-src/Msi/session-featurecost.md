---
description: Свойство Феатурекост объекта Session возвращает общий объем дискового пространства (в единицах 512 байт), требуемый для указанного компонента и его родительских компонентов (вплоть до корня таблицы функций).
ms.assetid: 5df9912a-2722-41c8-991b-256a009e85df
title: Свойство Session. Феатурекост
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCost
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 25c93ce0b3b4efa91a827217d221546e8bab5744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651975"
---
# <a name="sessionfeaturecost-property"></a><span data-ttu-id="59cad-103">Свойство Session. Феатурекост</span><span class="sxs-lookup"><span data-stu-id="59cad-103">Session.FeatureCost property</span></span>

<span data-ttu-id="59cad-104">Свойство **феатурекост** объекта [**Session**](session-object.md) возвращает общий объем дискового пространства (в единицах 512 байт), требуемый для указанного компонента и его родительских компонентов (вплоть до корня таблицы функций).</span><span class="sxs-lookup"><span data-stu-id="59cad-104">The **FeatureCost** property of the [**Session**](session-object.md) object returns the total amount of disk space (in units of 512 bytes) required by the specified feature and its parent features (up to the root of the Feature table).</span></span> <span data-ttu-id="59cad-105">Для каждого компонента Общая стоимость состоит из затрат на диск, присоединенных к каждому компоненту, связанному с данной функцией.</span><span class="sxs-lookup"><span data-stu-id="59cad-105">For each feature, the total cost is made up of the disk costs attributed to every component linked to the feature.</span></span>

<span data-ttu-id="59cad-106">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="59cad-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="59cad-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59cad-107">Syntax</span></span>


```JScript
propVal = Session.FeatureCost
```



## <a name="property-value"></a><span data-ttu-id="59cad-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="59cad-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="59cad-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59cad-109">Remarks</span></span>

<span data-ttu-id="59cad-110">Если свойство завершается неудачно, можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="59cad-110">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="59cad-111">Требования</span><span class="sxs-lookup"><span data-stu-id="59cad-111">Requirements</span></span>



| <span data-ttu-id="59cad-112">Требование</span><span class="sxs-lookup"><span data-stu-id="59cad-112">Requirement</span></span> | <span data-ttu-id="59cad-113">Значение</span><span class="sxs-lookup"><span data-stu-id="59cad-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59cad-114">Версия</span><span class="sxs-lookup"><span data-stu-id="59cad-114">Version</span></span><br/> | <span data-ttu-id="59cad-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="59cad-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="59cad-116">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="59cad-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="59cad-117">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="59cad-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="59cad-118">DLL</span><span class="sxs-lookup"><span data-stu-id="59cad-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="59cad-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59cad-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="59cad-120">IID</span><span class="sxs-lookup"><span data-stu-id="59cad-120">IID</span></span><br/>     | <span data-ttu-id="59cad-121">IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="59cad-121">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




