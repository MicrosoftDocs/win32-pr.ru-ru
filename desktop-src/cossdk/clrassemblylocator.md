---
description: Извлекает сведения о сборке при использовании управляемого кода в платформа .NET Framework среде CLR.
ms.assetid: 45dcdc6a-74df-4763-ba8b-82f604db78d4
title: Класс Клрассемблилокатор (Комсвкс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClrAssemblyLocator
api_type:
- COM
ms.openlocfilehash: ff5c1d21525a950208c1b919d4dee0e2122d2e50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895646"
---
# <a name="clrassemblylocator-class"></a><span data-ttu-id="bc687-103">Класс Клрассемблилокатор</span><span class="sxs-lookup"><span data-stu-id="bc687-103">ClrAssemblyLocator class</span></span>

<span data-ttu-id="bc687-104">Извлекает сведения о сборке при использовании управляемого кода в платформа .NET Framework среде CLR.</span><span class="sxs-lookup"><span data-stu-id="bc687-104">Retrieves information about an assembly when using managed code in the .NET Framework common language runtime.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="bc687-105">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="bc687-105">When to implement</span></span>

<span data-ttu-id="bc687-106">Этот класс реализуется с помощью COM+.</span><span class="sxs-lookup"><span data-stu-id="bc687-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="bc687-107">Требование</span><span class="sxs-lookup"><span data-stu-id="bc687-107">Requirement</span></span> | <span data-ttu-id="bc687-108">Значение</span><span class="sxs-lookup"><span data-stu-id="bc687-108">Value</span></span> |
|------------|-------------------------------------------------------|
| <span data-ttu-id="bc687-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="bc687-109">CLSID</span></span>      | <span data-ttu-id="bc687-110">GUID \_ ассемблилокатор</span><span class="sxs-lookup"><span data-stu-id="bc687-110">GUID\_AssemblyLocator</span></span>                                 |
| <span data-ttu-id="bc687-111">ProgID:</span><span class="sxs-lookup"><span data-stu-id="bc687-111">ProgID</span></span>     | <span data-ttu-id="bc687-112">L "System. EnterpriseServices. internal. Ассемблилокатор"</span><span class="sxs-lookup"><span data-stu-id="bc687-112">L"System.EnterpriseServices.Internal.AssemblyLocator"</span></span> |
| <span data-ttu-id="bc687-113">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="bc687-113">Interfaces</span></span> | [<span data-ttu-id="bc687-114">**иассемблилокатор**</span><span class="sxs-lookup"><span data-stu-id="bc687-114">**IAssemblyLocator**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)          |



 

## <a name="when-to-use"></a><span data-ttu-id="bc687-115">Назначение</span><span class="sxs-lookup"><span data-stu-id="bc687-115">When to use</span></span>

<span data-ttu-id="bc687-116">Используйте этот класс для доступа к методам [**иассемблилокатор**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator).</span><span class="sxs-lookup"><span data-stu-id="bc687-116">Use this class to access the methods of [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator).</span></span>

## <a name="remarks"></a><span data-ttu-id="bc687-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc687-117">Remarks</span></span>

<span data-ttu-id="bc687-118">Чтобы создать этот объект, вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="bc687-118">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="bc687-119">Чтобы использовать этот класс из Visual Basic Майкрософт, добавьте ссылку на библиотеку типов служб COM+.</span><span class="sxs-lookup"><span data-stu-id="bc687-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="bc687-120">Объект Клрассемблилокатор можно объявить с помощью "Комсвкслиб. Клрассемблилокатор" в качестве имени класса.</span><span class="sxs-lookup"><span data-stu-id="bc687-120">A ClrAssemblyLocator object can be declared using "COMSVCSLib.ClrAssemblyLocator" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc687-121">Требования</span><span class="sxs-lookup"><span data-stu-id="bc687-121">Requirements</span></span>



| <span data-ttu-id="bc687-122">Требование</span><span class="sxs-lookup"><span data-stu-id="bc687-122">Requirement</span></span> | <span data-ttu-id="bc687-123">Значение</span><span class="sxs-lookup"><span data-stu-id="bc687-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bc687-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc687-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bc687-125">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc687-125">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bc687-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc687-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bc687-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bc687-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bc687-128">Header</span><span class="sxs-lookup"><span data-stu-id="bc687-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc687-129"><dt>Комсвкс. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc687-129"><dt>ComSvcs.h</dt></span></span> </dl> |



 

