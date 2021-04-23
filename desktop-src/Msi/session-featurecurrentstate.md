---
description: Свойство Феатурекуррентстате объекта Session является свойством только для чтения, которое возвращает текущее установленное состояние указанного компонента. Значения состояния см. в описании свойства Феатуререкуестстате.
ms.assetid: c4c325dc-6e7e-4009-8707-952c04574170
title: Свойство Session. Феатурекуррентстате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 47c834571dd211dd085ed94e9d8c1ff9d5516c9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675721"
---
# <a name="sessionfeaturecurrentstate-property"></a><span data-ttu-id="822f1-104">Свойство Session. Феатурекуррентстате</span><span class="sxs-lookup"><span data-stu-id="822f1-104">Session.FeatureCurrentState property</span></span>

<span data-ttu-id="822f1-105">Свойство **феатурекуррентстате** объекта [**Session**](session-object.md) является свойством только для чтения, которое возвращает текущее установленное состояние указанного компонента.</span><span class="sxs-lookup"><span data-stu-id="822f1-105">The **FeatureCurrentState** property of the [**Session**](session-object.md) object is a read-only property that returns the current installed state of the designated feature.</span></span> <span data-ttu-id="822f1-106">Значения состояния см. в описании свойства [**феатуререкуестстате**](session-featurerequeststate.md) .</span><span class="sxs-lookup"><span data-stu-id="822f1-106">For state values, see the [**FeatureRequestState**](session-featurerequeststate.md) property.</span></span>

<span data-ttu-id="822f1-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="822f1-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="822f1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="822f1-108">Syntax</span></span>


```JScript
propVal = Session.FeatureCurrentState
```



## <a name="property-value"></a><span data-ttu-id="822f1-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="822f1-109">Property value</span></span>

<span data-ttu-id="822f1-110">Обязательное строковое имя запрошенной функции и первичный ключ в [таблице Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="822f1-110">Required string name of the requested feature, and a primary key into the [Feature table](feature-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="822f1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="822f1-111">Remarks</span></span>

<span data-ttu-id="822f1-112">Если свойство завершается неудачно, можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="822f1-112">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="822f1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="822f1-113">Requirements</span></span>



| <span data-ttu-id="822f1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="822f1-114">Requirement</span></span> | <span data-ttu-id="822f1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="822f1-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="822f1-116">Версия</span><span class="sxs-lookup"><span data-stu-id="822f1-116">Version</span></span><br/> | <span data-ttu-id="822f1-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="822f1-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="822f1-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="822f1-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="822f1-119">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="822f1-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="822f1-120">DLL</span><span class="sxs-lookup"><span data-stu-id="822f1-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="822f1-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="822f1-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="822f1-122">IID</span><span class="sxs-lookup"><span data-stu-id="822f1-122">IID</span></span><br/>     | <span data-ttu-id="822f1-123">IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="822f1-123">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="822f1-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="822f1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="822f1-125">**Session**</span><span class="sxs-lookup"><span data-stu-id="822f1-125">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="822f1-126">**Феатуререкуестстате, свойство**</span><span class="sxs-lookup"><span data-stu-id="822f1-126">**FeatureRequestState property**</span></span>](session-featurerequeststate.md)
</dt> </dl>

 

 




