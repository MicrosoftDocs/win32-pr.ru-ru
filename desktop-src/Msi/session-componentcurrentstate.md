---
description: Свойство Компоненткуррентстате объекта Session является свойством только для чтения, которое возвращает текущее установленное состояние указанного компонента. Значения состояния см. в описании свойства Компонентрекуестстате.
ms.assetid: c8343e90-8867-462d-9844-e547341a590c
title: Свойство Session. Компоненткуррентстате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8c556dd9656ebced155ef90fe96abd394a32ff1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651976"
---
# <a name="sessioncomponentcurrentstate-property"></a><span data-ttu-id="dff1c-104">Свойство Session. Компоненткуррентстате</span><span class="sxs-lookup"><span data-stu-id="dff1c-104">Session.ComponentCurrentState property</span></span>

<span data-ttu-id="dff1c-105">Свойство **компоненткуррентстате** объекта [**Session**](session-object.md) является свойством только для чтения, которое возвращает текущее установленное состояние указанного компонента.</span><span class="sxs-lookup"><span data-stu-id="dff1c-105">The **ComponentCurrentState** property of the [**Session**](session-object.md) object is a read-only property that returns the current installed state of the designated component.</span></span> <span data-ttu-id="dff1c-106">Значения состояния см. в описании свойства [**компонентрекуестстате**](session-componentrequeststate.md) .</span><span class="sxs-lookup"><span data-stu-id="dff1c-106">For state values, see the [**ComponentRequestState**](session-componentrequeststate.md) property.</span></span>

<span data-ttu-id="dff1c-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dff1c-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dff1c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dff1c-108">Syntax</span></span>


```JScript
propVal = Session.ComponentCurrentState
```



## <a name="property-value"></a><span data-ttu-id="dff1c-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dff1c-109">Property value</span></span>

<span data-ttu-id="dff1c-110">Требуемое строковое имя запрошенного компонента, первичный ключ в таблице Component.</span><span class="sxs-lookup"><span data-stu-id="dff1c-110">Required string name of the requested component, primary key into the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="dff1c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dff1c-111">Remarks</span></span>

<span data-ttu-id="dff1c-112">Если свойство завершается неудачно, можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="dff1c-112">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dff1c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="dff1c-113">Requirements</span></span>



| <span data-ttu-id="dff1c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="dff1c-114">Requirement</span></span> | <span data-ttu-id="dff1c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="dff1c-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dff1c-116">Версия</span><span class="sxs-lookup"><span data-stu-id="dff1c-116">Version</span></span><br/> | <span data-ttu-id="dff1c-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dff1c-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dff1c-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dff1c-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dff1c-119">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="dff1c-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="dff1c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="dff1c-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="dff1c-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dff1c-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="dff1c-122">IID</span><span class="sxs-lookup"><span data-stu-id="dff1c-122">IID</span></span><br/>     | <span data-ttu-id="dff1c-123">IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="dff1c-123">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="dff1c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dff1c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff1c-125">**Session**</span><span class="sxs-lookup"><span data-stu-id="dff1c-125">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="dff1c-126">**Компонентрекуестстате, свойство**</span><span class="sxs-lookup"><span data-stu-id="dff1c-126">**ComponentRequestState property**</span></span>](session-componentrequeststate.md)
</dt> </dl>

 

 




