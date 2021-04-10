---
description: Задает или получает значение общего свойства.
ms.assetid: 19ed8d50-3ac1-408e-9f25-09f284d025f1
title: Класс Шаредпроперти (Комсвкс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedProperty
api_type:
- COM
ms.openlocfilehash: a7a7857ad280ad722601bdced6c25d04b03dc0b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141371"
---
# <a name="sharedproperty-class"></a><span data-ttu-id="a21bc-103">Класс Шаредпроперти</span><span class="sxs-lookup"><span data-stu-id="a21bc-103">SharedProperty class</span></span>

<span data-ttu-id="a21bc-104">Задает или получает значение общего свойства.</span><span class="sxs-lookup"><span data-stu-id="a21bc-104">Sets or retrieves the value of a shared property.</span></span>

<span data-ttu-id="a21bc-105">Общие сведения об использовании общего диспетчер свойств в COM+ см. в разделе [com+ shared Диспетчер свойств](com--shared-property-manager.md).</span><span class="sxs-lookup"><span data-stu-id="a21bc-105">For general information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="a21bc-106">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="a21bc-106">When to implement</span></span>

<span data-ttu-id="a21bc-107">Этот класс реализуется с помощью COM+.</span><span class="sxs-lookup"><span data-stu-id="a21bc-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="a21bc-108">Требование</span><span class="sxs-lookup"><span data-stu-id="a21bc-108">Requirement</span></span> | <span data-ttu-id="a21bc-109">Значение</span><span class="sxs-lookup"><span data-stu-id="a21bc-109">Value</span></span> |
|------------|--------------------------------------------|
| <span data-ttu-id="a21bc-110">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="a21bc-110">Interfaces</span></span> | [<span data-ttu-id="a21bc-111">**ишаредпроперти**</span><span class="sxs-lookup"><span data-stu-id="a21bc-111">**ISharedProperty**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) |



 

## <a name="when-to-use"></a><span data-ttu-id="a21bc-112">Назначение</span><span class="sxs-lookup"><span data-stu-id="a21bc-112">When to use</span></span>

<span data-ttu-id="a21bc-113">Используйте этот класс для доступа к методам [**ишаредпроперти**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty).</span><span class="sxs-lookup"><span data-stu-id="a21bc-113">Use this class to access the methods of [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty).</span></span>

## <a name="remarks"></a><span data-ttu-id="a21bc-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a21bc-114">Remarks</span></span>

<span data-ttu-id="a21bc-115">Объект **шаредпроперти** можно создать с помощью методов [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) или [**креатепропертибипоситион**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) [**ишаредпропертиграуп**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span><span class="sxs-lookup"><span data-stu-id="a21bc-115">You can create a **SharedProperty** object by using the [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) or [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) methods of [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span></span>

<span data-ttu-id="a21bc-116">Чтобы использовать этот класс из Visual Basic Майкрософт, добавьте ссылку на библиотеку типов служб COM+.</span><span class="sxs-lookup"><span data-stu-id="a21bc-116">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="a21bc-117">Объект Шаредпроперти создается путем вызова методов [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) или [**креатепропертибипоситион**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) объекта [**шаредпропертиграуп**](sharedpropertygroup.md) .</span><span class="sxs-lookup"><span data-stu-id="a21bc-117">A SharedProperty object is created by calling the [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) or [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) methods of the [**SharedPropertyGroup**](sharedpropertygroup.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="a21bc-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a21bc-118">Requirements</span></span>



| <span data-ttu-id="a21bc-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a21bc-119">Requirement</span></span> | <span data-ttu-id="a21bc-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a21bc-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a21bc-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a21bc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a21bc-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a21bc-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a21bc-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a21bc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a21bc-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a21bc-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a21bc-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a21bc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a21bc-126"><dt>Комсвкс. h</dt></span><span class="sxs-lookup"><span data-stu-id="a21bc-126"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a21bc-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a21bc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a21bc-128">**ишаредпроперти**</span><span class="sxs-lookup"><span data-stu-id="a21bc-128">**ISharedProperty**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty)
</dt> <dt>

[<span data-ttu-id="a21bc-129">**шаредпропертиграуп**</span><span class="sxs-lookup"><span data-stu-id="a21bc-129">**SharedPropertyGroup**</span></span>](sharedpropertygroup.md)
</dt> <dt>

[<span data-ttu-id="a21bc-130">**шаредпропертиграупманажер**</span><span class="sxs-lookup"><span data-stu-id="a21bc-130">**SharedPropertyGroupManager**</span></span>](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




