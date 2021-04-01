---
description: Создает общие группы свойств и получает доступ к существующим группам общих свойств.
ms.assetid: 4ba05806-afda-4926-8ca4-abbf15ed8278
title: Класс Шаредпропертиграупманажер (Комсвкс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroupManager
api_type:
- COM
ms.openlocfilehash: 680c5caef996d329e18192193f30841f61f02f27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895745"
---
# <a name="sharedpropertygroupmanager-class"></a><span data-ttu-id="becc7-103">Класс Шаредпропертиграупманажер</span><span class="sxs-lookup"><span data-stu-id="becc7-103">SharedPropertyGroupManager class</span></span>

<span data-ttu-id="becc7-104">Создает общие группы свойств и получает доступ к существующим группам общих свойств.</span><span class="sxs-lookup"><span data-stu-id="becc7-104">Creates shared property groups and to obtain access to existing shared property groups.</span></span>

<span data-ttu-id="becc7-105">Дополнительные сведения об использовании общих диспетчер свойств в COM+ см. в разделе [com+ shared Диспетчер свойств](com--shared-property-manager.md).</span><span class="sxs-lookup"><span data-stu-id="becc7-105">For more information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="becc7-106">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="becc7-106">When to implement</span></span>

<span data-ttu-id="becc7-107">Этот класс реализуется с помощью COM+.</span><span class="sxs-lookup"><span data-stu-id="becc7-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="becc7-108">Требование</span><span class="sxs-lookup"><span data-stu-id="becc7-108">Requirement</span></span> | <span data-ttu-id="becc7-109">Значение</span><span class="sxs-lookup"><span data-stu-id="becc7-109">Value</span></span> |
|------------|--------------------------------------------------------------------|
| <span data-ttu-id="becc7-110">CLSID</span><span class="sxs-lookup"><span data-stu-id="becc7-110">CLSID</span></span>      | <span data-ttu-id="becc7-111">\_ШАРЕДПРОПЕРТИГРАУПМАНАЖЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="becc7-111">CLSID\_SharedPropertyGroupManager</span></span>                                  |
| <span data-ttu-id="becc7-112">ProgID:</span><span class="sxs-lookup"><span data-stu-id="becc7-112">ProgID</span></span>     | <span data-ttu-id="becc7-113">L "Мтксспм. Шаредпропертиграупманажер"</span><span class="sxs-lookup"><span data-stu-id="becc7-113">L"MTxSpm.SharedPropertyGroupManager"</span></span>                               |
| <span data-ttu-id="becc7-114">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="becc7-114">Interfaces</span></span> | [<span data-ttu-id="becc7-115">**ишаредпропертиграупманажер**</span><span class="sxs-lookup"><span data-stu-id="becc7-115">**ISharedPropertyGroupManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) |



 

## <a name="when-to-use"></a><span data-ttu-id="becc7-116">Назначение</span><span class="sxs-lookup"><span data-stu-id="becc7-116">When to use</span></span>

<span data-ttu-id="becc7-117">Используйте этот класс для доступа к методам [**ишаредпропертиграупманажер**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span><span class="sxs-lookup"><span data-stu-id="becc7-117">Use this class to access the methods of [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span></span>

## <a name="remarks"></a><span data-ttu-id="becc7-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="becc7-118">Remarks</span></span>

<span data-ttu-id="becc7-119">Чтобы создать этот объект, вызовите метод [**иобжектконтекст:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span><span class="sxs-lookup"><span data-stu-id="becc7-119">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="becc7-120">Чтобы использовать этот класс из Visual Basic Майкрософт, добавьте ссылку на библиотеку типов служб COM+.</span><span class="sxs-lookup"><span data-stu-id="becc7-120">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="becc7-121">Объект Шаредпропертиграупманажер можно объявить с помощью "Комсвкслиб. Шаредпропертиграупманажер" в качестве имени класса.</span><span class="sxs-lookup"><span data-stu-id="becc7-121">A SharedPropertyGroupManager object can be declared using "COMSVCSLib.SharedPropertyGroupManager" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="becc7-122">Требования</span><span class="sxs-lookup"><span data-stu-id="becc7-122">Requirements</span></span>



| <span data-ttu-id="becc7-123">Требование</span><span class="sxs-lookup"><span data-stu-id="becc7-123">Requirement</span></span> | <span data-ttu-id="becc7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="becc7-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="becc7-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="becc7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="becc7-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="becc7-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="becc7-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="becc7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="becc7-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="becc7-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="becc7-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="becc7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="becc7-130"><dt>Комсвкс. h</dt></span><span class="sxs-lookup"><span data-stu-id="becc7-130"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="becc7-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="becc7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="becc7-132">**ишаредпропертиграупманажер**</span><span class="sxs-lookup"><span data-stu-id="becc7-132">**ISharedPropertyGroupManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)
</dt> <dt>

[<span data-ttu-id="becc7-133">**шаредпроперти**</span><span class="sxs-lookup"><span data-stu-id="becc7-133">**SharedProperty**</span></span>](sharedproperty.md)
</dt> <dt>

[<span data-ttu-id="becc7-134">**шаредпропертиграуп**</span><span class="sxs-lookup"><span data-stu-id="becc7-134">**SharedPropertyGroup**</span></span>](sharedpropertygroup.md)
</dt> </dl>

 

 




