---
description: Свойство Context Возвращает контекст этого исправления.
ms.assetid: 09c92b0b-44f3-4355-8171-03da8ba32757
title: Свойство patch. Context
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a6495b199046a361910741545a7178050621ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651637"
---
# <a name="patchcontext-property"></a><span data-ttu-id="68045-103">Свойство patch. Context</span><span class="sxs-lookup"><span data-stu-id="68045-103">Patch.Context property</span></span>

<span data-ttu-id="68045-104">Свойство **context** Возвращает контекст этого исправления.</span><span class="sxs-lookup"><span data-stu-id="68045-104">The **Context** property returns the context of this patch.</span></span>

<span data-ttu-id="68045-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="68045-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="68045-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68045-106">Syntax</span></span>


```JScript
propVal = Patch.Context
```



## <a name="property-value"></a><span data-ttu-id="68045-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="68045-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="68045-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68045-108">Remarks</span></span>

<span data-ttu-id="68045-109">Это свойство возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="68045-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="68045-110">Контекст</span><span class="sxs-lookup"><span data-stu-id="68045-110">Context</span></span>                        | <span data-ttu-id="68045-111">Значение</span><span class="sxs-lookup"><span data-stu-id="68045-111">Value</span></span> | <span data-ttu-id="68045-112">Значение</span><span class="sxs-lookup"><span data-stu-id="68045-112">Meaning</span></span>                        |
|--------------------------------|-------|--------------------------------|
| <span data-ttu-id="68045-113">МСИИНСТАЛЛКОНТЕКСТ \_ усерманажед</span><span class="sxs-lookup"><span data-stu-id="68045-113">MSIINSTALLCONTEXT\_USERMANAGED</span></span> | <span data-ttu-id="68045-114">1</span><span class="sxs-lookup"><span data-stu-id="68045-114">1</span></span>     | <span data-ttu-id="68045-115">Исправление в управляемом контексте.</span><span class="sxs-lookup"><span data-stu-id="68045-115">Patch under managed context.</span></span>   |
| <span data-ttu-id="68045-116">\_пользователь мсиинсталлконтекст</span><span class="sxs-lookup"><span data-stu-id="68045-116">MSIINSTALLCONTEXT\_USER</span></span>        | <span data-ttu-id="68045-117">2</span><span class="sxs-lookup"><span data-stu-id="68045-117">2</span></span>     | <span data-ttu-id="68045-118">Исправление в неуправляемом контексте.</span><span class="sxs-lookup"><span data-stu-id="68045-118">Patch under unmanaged context.</span></span> |
| <span data-ttu-id="68045-119">МСИИНСТАЛЛКОНТЕКСТ \_ компьютер</span><span class="sxs-lookup"><span data-stu-id="68045-119">MSIINSTALLCONTEXT\_MACHINE</span></span>     | <span data-ttu-id="68045-120">4</span><span class="sxs-lookup"><span data-stu-id="68045-120">4</span></span>     | <span data-ttu-id="68045-121">Исправление в контексте компьютера.</span><span class="sxs-lookup"><span data-stu-id="68045-121">Patch under machine context.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="68045-122">Требования</span><span class="sxs-lookup"><span data-stu-id="68045-122">Requirements</span></span>



| <span data-ttu-id="68045-123">Требование</span><span class="sxs-lookup"><span data-stu-id="68045-123">Requirement</span></span> | <span data-ttu-id="68045-124">Значение</span><span class="sxs-lookup"><span data-stu-id="68045-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68045-125">Версия</span><span class="sxs-lookup"><span data-stu-id="68045-125">Version</span></span><br/> | <span data-ttu-id="68045-126">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="68045-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="68045-127">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="68045-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="68045-128">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="68045-128">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="68045-129">DLL</span><span class="sxs-lookup"><span data-stu-id="68045-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="68045-130"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68045-130"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="68045-131">IID</span><span class="sxs-lookup"><span data-stu-id="68045-131">IID</span></span><br/>     | <span data-ttu-id="68045-132">IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="68045-132">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="68045-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68045-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68045-134">**Объект Patch**</span><span class="sxs-lookup"><span data-stu-id="68045-134">**Patch Object**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="68045-135">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="68045-135">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




