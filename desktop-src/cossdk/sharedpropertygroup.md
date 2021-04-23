---
description: Создает и обращается к общим свойствам в группе общих свойств.
ms.assetid: 20fd32f0-b2b2-4bed-8c59-1d1fdc8a399e
title: Класс Шаредпропертиграуп (Комсвкс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroup
api_type:
- COM
ms.openlocfilehash: a3fff14043d67b96db99334c7bec1afee2577f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807277"
---
# <a name="sharedpropertygroup-class"></a><span data-ttu-id="908b9-103">Класс Шаредпропертиграуп</span><span class="sxs-lookup"><span data-stu-id="908b9-103">SharedPropertyGroup class</span></span>

<span data-ttu-id="908b9-104">Создает и обращается к общим свойствам в группе общих свойств.</span><span class="sxs-lookup"><span data-stu-id="908b9-104">Creates and accesses the shared properties in a shared property group.</span></span>

<span data-ttu-id="908b9-105">Дополнительные сведения об использовании общих диспетчер свойств в COM+ см. в разделе [com+ shared Диспетчер свойств](com--shared-property-manager.md).</span><span class="sxs-lookup"><span data-stu-id="908b9-105">For more information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="908b9-106">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="908b9-106">When to implement</span></span>

<span data-ttu-id="908b9-107">Этот класс реализуется с помощью COM+.</span><span class="sxs-lookup"><span data-stu-id="908b9-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="908b9-108">Требование</span><span class="sxs-lookup"><span data-stu-id="908b9-108">Requirement</span></span> | <span data-ttu-id="908b9-109">Значение</span><span class="sxs-lookup"><span data-stu-id="908b9-109">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="908b9-110">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="908b9-110">Interfaces</span></span> | [<span data-ttu-id="908b9-111">**ишаредпропертиграуп**</span><span class="sxs-lookup"><span data-stu-id="908b9-111">**ISharedPropertyGroup**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) |



 

## <a name="when-to-use"></a><span data-ttu-id="908b9-112">Назначение</span><span class="sxs-lookup"><span data-stu-id="908b9-112">When to use</span></span>

<span data-ttu-id="908b9-113">Используйте этот класс для доступа к методам [**ишаредпропертиграуп**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span><span class="sxs-lookup"><span data-stu-id="908b9-113">Use this class to access the methods of [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span></span>

## <a name="remarks"></a><span data-ttu-id="908b9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="908b9-114">Remarks</span></span>

<span data-ttu-id="908b9-115">Объект **шаредпропертиграуп** можно создать с помощью метода [**креатепропертиграуп**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) объекта [**ишаредпропертиграупманажер**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span><span class="sxs-lookup"><span data-stu-id="908b9-115">You can create a **SharedPropertyGroup** object using the [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) method of [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span></span>

<span data-ttu-id="908b9-116">Чтобы использовать этот класс из Visual Basic Майкрософт, добавьте ссылку на библиотеку типов служб COM+.</span><span class="sxs-lookup"><span data-stu-id="908b9-116">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="908b9-117">Объект Шаредпропертиграуп создается путем вызова метода [**креатепропертиграуп**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) объекта [**шаредпропертиграупманажер**](sharedpropertygroupmanager.md) .</span><span class="sxs-lookup"><span data-stu-id="908b9-117">A SharedPropertyGroup object is created by calling the [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) method of the [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="908b9-118">Требования</span><span class="sxs-lookup"><span data-stu-id="908b9-118">Requirements</span></span>



| <span data-ttu-id="908b9-119">Требование</span><span class="sxs-lookup"><span data-stu-id="908b9-119">Requirement</span></span> | <span data-ttu-id="908b9-120">Значение</span><span class="sxs-lookup"><span data-stu-id="908b9-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="908b9-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="908b9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="908b9-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="908b9-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="908b9-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="908b9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="908b9-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="908b9-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="908b9-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="908b9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="908b9-126"><dt>Комсвкс. h</dt></span><span class="sxs-lookup"><span data-stu-id="908b9-126"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="908b9-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="908b9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="908b9-128">**ишаредпропертиграуп**</span><span class="sxs-lookup"><span data-stu-id="908b9-128">**ISharedPropertyGroup**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)
</dt> <dt>

[<span data-ttu-id="908b9-129">**шаредпроперти**</span><span class="sxs-lookup"><span data-stu-id="908b9-129">**SharedProperty**</span></span>](sharedproperty.md)
</dt> <dt>

[<span data-ttu-id="908b9-130">**шаредпропертиграупманажер**</span><span class="sxs-lookup"><span data-stu-id="908b9-130">**SharedPropertyGroupManager**</span></span>](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




