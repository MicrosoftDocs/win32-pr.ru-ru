---
description: Привязывает управляемый объект к домену приложения, который является изолированной средой, в которой выполняются приложения.
ms.assetid: 9357ea5d-6f86-4747-a923-16575ff13122
title: Класс Аппдомаинхелпер (Комсвкс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AppDomainHelper
api_type:
- COM
ms.openlocfilehash: 6b4fbedbca631ec49dc2e416d939abdeb239e5b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538735"
---
# <a name="appdomainhelper-class"></a><span data-ttu-id="1ad55-103">Класс Аппдомаинхелпер</span><span class="sxs-lookup"><span data-stu-id="1ad55-103">AppDomainHelper class</span></span>

<span data-ttu-id="1ad55-104">Привязывает управляемый объект к домену приложения, который является изолированной средой, в которой выполняются приложения.</span><span class="sxs-lookup"><span data-stu-id="1ad55-104">Binds a managed object to an application domain, which is an isolated environment where applications execute.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="1ad55-105">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="1ad55-105">When to implement</span></span>

<span data-ttu-id="1ad55-106">Этот класс реализуется с помощью COM+.</span><span class="sxs-lookup"><span data-stu-id="1ad55-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="1ad55-107">Требование</span><span class="sxs-lookup"><span data-stu-id="1ad55-107">Requirement</span></span> | <span data-ttu-id="1ad55-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1ad55-108">Value</span></span> |
|------------|-------------------------------------------------------|
| <span data-ttu-id="1ad55-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="1ad55-109">CLSID</span></span>      | <span data-ttu-id="1ad55-110">GUID \_ аппдомаинхелпер</span><span class="sxs-lookup"><span data-stu-id="1ad55-110">GUID\_AppDomainHelper</span></span>                                 |
| <span data-ttu-id="1ad55-111">ProgID:</span><span class="sxs-lookup"><span data-stu-id="1ad55-111">ProgID</span></span>     | <span data-ttu-id="1ad55-112">L "System. EnterpriseServices. internal. Аппдомаинхелпер"</span><span class="sxs-lookup"><span data-stu-id="1ad55-112">L"System.EnterpriseServices.Internal.AppDomainHelper"</span></span> |
| <span data-ttu-id="1ad55-113">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="1ad55-113">Interfaces</span></span> | [<span data-ttu-id="1ad55-114">**иаппдомаинхелпер**</span><span class="sxs-lookup"><span data-stu-id="1ad55-114">**IAppDomainHelper**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)          |



 

## <a name="when-to-use"></a><span data-ttu-id="1ad55-115">Назначение</span><span class="sxs-lookup"><span data-stu-id="1ad55-115">When to use</span></span>

<span data-ttu-id="1ad55-116">Используйте этот класс для доступа к методам [**иаппдомаинхелпер**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper).</span><span class="sxs-lookup"><span data-stu-id="1ad55-116">Use this class to access the methods of [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper).</span></span>

## <a name="remarks"></a><span data-ttu-id="1ad55-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ad55-117">Remarks</span></span>

<span data-ttu-id="1ad55-118">Чтобы создать этот объект, вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="1ad55-118">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="1ad55-119">Чтобы использовать этот класс из Visual Basic Майкрософт, добавьте ссылку на библиотеку типов служб COM+.</span><span class="sxs-lookup"><span data-stu-id="1ad55-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="1ad55-120">Объект Аппдомаинхелпер можно объявить с помощью "Комсвкслиб. Аппдомаинхелпер" в качестве имени класса.</span><span class="sxs-lookup"><span data-stu-id="1ad55-120">An AppDomainHelper object can be declared using "COMSVCSLib.AppDomainHelper" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ad55-121">Требования</span><span class="sxs-lookup"><span data-stu-id="1ad55-121">Requirements</span></span>



| <span data-ttu-id="1ad55-122">Требование</span><span class="sxs-lookup"><span data-stu-id="1ad55-122">Requirement</span></span> | <span data-ttu-id="1ad55-123">Значение</span><span class="sxs-lookup"><span data-stu-id="1ad55-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1ad55-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ad55-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1ad55-125">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ad55-125">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1ad55-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ad55-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1ad55-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1ad55-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1ad55-128">Header</span><span class="sxs-lookup"><span data-stu-id="1ad55-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ad55-129"><dt>Комсвкс. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ad55-129"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ad55-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ad55-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ad55-131">**иаппдомаинхелпер**</span><span class="sxs-lookup"><span data-stu-id="1ad55-131">**IAppDomainHelper**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)
</dt> </dl>

 

