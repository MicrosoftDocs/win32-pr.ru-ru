---
description: Установщик задает свойство Мсинтпродукттипе для операционных систем Windows NT, Windows 2000 и более поздних версий.
ms.assetid: 6bbc8283-5911-4fbd-8a0f-09c398280e74
title: Мсинтпродукттипе, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7fef0791f5842163812b62a7314578d480676c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668872"
---
# <a name="msintproducttype-property"></a><span data-ttu-id="6e2fe-103">Мсинтпродукттипе, свойство</span><span class="sxs-lookup"><span data-stu-id="6e2fe-103">MsiNTProductType property</span></span>

<span data-ttu-id="6e2fe-104">Установщик задает свойство **мсинтпродукттипе** для операционных систем Windows NT, Windows 2000 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="6e2fe-104">The installer sets the **MsiNTProductType** property for Windows NT, Windows 2000, and later operating systems.</span></span> <span data-ttu-id="6e2fe-105">Это свойство указывает тип продукта Windows.</span><span class="sxs-lookup"><span data-stu-id="6e2fe-105">This property indicates the Windows product type.</span></span>

<span data-ttu-id="6e2fe-106">Для операционных систем Windows 2000 и более поздних версий установщик устанавливает следующие значения.</span><span class="sxs-lookup"><span data-stu-id="6e2fe-106">For Windows 2000 and later operating systems, the installer sets the following values.</span></span> <span data-ttu-id="6e2fe-107">Обратите внимание, что значения равны значению поля **впродукттипе** структуры [**осверсионинфоекс**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="6e2fe-107">Note that values are the same as of the **wProductType** field of the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span>



| <span data-ttu-id="6e2fe-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6e2fe-108">Value</span></span> | <span data-ttu-id="6e2fe-109">Значение</span><span class="sxs-lookup"><span data-stu-id="6e2fe-109">Meaning</span></span>                                  |
|-------|------------------------------------------|
| <span data-ttu-id="6e2fe-110">1</span><span class="sxs-lookup"><span data-stu-id="6e2fe-110">1</span></span>     | <span data-ttu-id="6e2fe-111">Windows 2000 профессиональная и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="6e2fe-111">Windows 2000 Professional and later</span></span>      |
| <span data-ttu-id="6e2fe-112">2</span><span class="sxs-lookup"><span data-stu-id="6e2fe-112">2</span></span>     | <span data-ttu-id="6e2fe-113">Контроллер домена Windows 2000 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="6e2fe-113">Windows 2000 domain controller and later</span></span> |
| <span data-ttu-id="6e2fe-114">3</span><span class="sxs-lookup"><span data-stu-id="6e2fe-114">3</span></span>     | <span data-ttu-id="6e2fe-115">Windows 2000 Server и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="6e2fe-115">Windows 2000 Server and later</span></span>            |



 

<span data-ttu-id="6e2fe-116">Для операционных систем, предшествующих Windows 2000, установщик устанавливает следующие значения.</span><span class="sxs-lookup"><span data-stu-id="6e2fe-116">For operating systems earlier than Windows 2000, the installer sets the following values.</span></span>



| <span data-ttu-id="6e2fe-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6e2fe-117">Value</span></span> | <span data-ttu-id="6e2fe-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6e2fe-118">Meaning</span></span>                      |
|-------|------------------------------|
| <span data-ttu-id="6e2fe-119">1</span><span class="sxs-lookup"><span data-stu-id="6e2fe-119">1</span></span>     | <span data-ttu-id="6e2fe-120">Рабочая станция Windows NT</span><span class="sxs-lookup"><span data-stu-id="6e2fe-120">Windows NT Workstation</span></span>       |
| <span data-ttu-id="6e2fe-121">2</span><span class="sxs-lookup"><span data-stu-id="6e2fe-121">2</span></span>     | <span data-ttu-id="6e2fe-122">Контроллер домена Windows NT</span><span class="sxs-lookup"><span data-stu-id="6e2fe-122">Windows NT domain controller</span></span> |
| <span data-ttu-id="6e2fe-123">3</span><span class="sxs-lookup"><span data-stu-id="6e2fe-123">3</span></span>     | <span data-ttu-id="6e2fe-124">Windows NT Server</span><span class="sxs-lookup"><span data-stu-id="6e2fe-124">Windows NT Server</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="6e2fe-125">Требования</span><span class="sxs-lookup"><span data-stu-id="6e2fe-125">Requirements</span></span>



| <span data-ttu-id="6e2fe-126">Требование</span><span class="sxs-lookup"><span data-stu-id="6e2fe-126">Requirement</span></span> | <span data-ttu-id="6e2fe-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6e2fe-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e2fe-128">Версия</span><span class="sxs-lookup"><span data-stu-id="6e2fe-128">Version</span></span><br/> | <span data-ttu-id="6e2fe-129">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6e2fe-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6e2fe-130">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6e2fe-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6e2fe-131">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6e2fe-131">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6e2fe-132">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="6e2fe-132">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6e2fe-133">См. также</span><span class="sxs-lookup"><span data-stu-id="6e2fe-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e2fe-134">Свойства</span><span class="sxs-lookup"><span data-stu-id="6e2fe-134">Properties</span></span>](properties.md)
</dt> </dl>

 

 
