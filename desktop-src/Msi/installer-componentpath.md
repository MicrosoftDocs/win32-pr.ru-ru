---
description: Свойство Компонентпас является свойством только для чтения, которое возвращает полный путь к установленному компоненту. Если путь к разделу для компонента является ключом реестра, то возвращается раздел реестра.
ms.assetid: 6e53419d-f28a-45cd-abc8-0f451177f3fc
title: Свойство Installer. Компонентпас
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e249290af2477d2dfcbc73f80f80b439f1dd3663
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651966"
---
# <a name="installercomponentpath-property"></a><span data-ttu-id="295b0-104">Свойство Installer. Компонентпас</span><span class="sxs-lookup"><span data-stu-id="295b0-104">Installer.ComponentPath property</span></span>

<span data-ttu-id="295b0-105">Свойство **компонентпас** является свойством только для чтения, которое возвращает полный путь к установленному компоненту.</span><span class="sxs-lookup"><span data-stu-id="295b0-105">The **ComponentPath** property is a read-only property that returns the full path to an installed component.</span></span> <span data-ttu-id="295b0-106">Если путь к разделу для компонента является ключом реестра, то возвращается раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="295b0-106">If the key path for the component is a registry key then the registry key is returned.</span></span>

<span data-ttu-id="295b0-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="295b0-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="295b0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="295b0-108">Syntax</span></span>


```JScript
propVal = Installer.ComponentPath
```



## <a name="property-value"></a><span data-ttu-id="295b0-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="295b0-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="295b0-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="295b0-110">Remarks</span></span>

<span data-ttu-id="295b0-111">Если компонент является разделом реестра, то корни реестра представлены в числовом виде.</span><span class="sxs-lookup"><span data-stu-id="295b0-111">If the component is a registry key, the registry roots are represented numerically.</span></span> <span data-ttu-id="295b0-112">Например, путь реестра "HKEY \_ Current \_ user \\ Software \\ Microsoft" будет возвращен как "01: \\ Software \\ Майкрософт".</span><span class="sxs-lookup"><span data-stu-id="295b0-112">For example, a registry path of "HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft" would be returned as "01:\\SOFTWARE\\Microsoft".</span></span> <span data-ttu-id="295b0-113">Возвращаемые корни реестра определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="295b0-113">The registry roots returned are defined as follows:</span></span>



| <span data-ttu-id="295b0-114">Root</span><span class="sxs-lookup"><span data-stu-id="295b0-114">Root</span></span>                    | <span data-ttu-id="295b0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="295b0-115">Returned value</span></span> |
|-------------------------|----------------|
| <span data-ttu-id="295b0-116">\_корневой узел классов hKey \_</span><span class="sxs-lookup"><span data-stu-id="295b0-116">HKEY\_CLASSES\_ROOT</span></span>     | <span data-ttu-id="295b0-117">00</span><span class="sxs-lookup"><span data-stu-id="295b0-117">00</span></span>             |
| <span data-ttu-id="295b0-118">HKEY \_ текущего \_ пользователя</span><span class="sxs-lookup"><span data-stu-id="295b0-118">HKEY\_CURRENT\_USER</span></span>     | <span data-ttu-id="295b0-119">01</span><span class="sxs-lookup"><span data-stu-id="295b0-119">01</span></span>             |
| <span data-ttu-id="295b0-120">HKEY \_ локальный \_ компьютер</span><span class="sxs-lookup"><span data-stu-id="295b0-120">HKEY\_LOCAL\_MACHINE</span></span>    | <span data-ttu-id="295b0-121">02</span><span class="sxs-lookup"><span data-stu-id="295b0-121">02</span></span>             |
| <span data-ttu-id="295b0-122">\_Пользователи hKey</span><span class="sxs-lookup"><span data-stu-id="295b0-122">HKEY\_USERS</span></span>             | <span data-ttu-id="295b0-123">03</span><span class="sxs-lookup"><span data-stu-id="295b0-123">03</span></span>             |
| <span data-ttu-id="295b0-124">\_данные о производительности hKey \_</span><span class="sxs-lookup"><span data-stu-id="295b0-124">HKEY\_PERFORMANCE\_DATA</span></span> | <span data-ttu-id="295b0-125">04</span><span class="sxs-lookup"><span data-stu-id="295b0-125">04</span></span>             |



 

## <a name="requirements"></a><span data-ttu-id="295b0-126">Требования</span><span class="sxs-lookup"><span data-stu-id="295b0-126">Requirements</span></span>



| <span data-ttu-id="295b0-127">Требование</span><span class="sxs-lookup"><span data-stu-id="295b0-127">Requirement</span></span> | <span data-ttu-id="295b0-128">Значение</span><span class="sxs-lookup"><span data-stu-id="295b0-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="295b0-129">Версия</span><span class="sxs-lookup"><span data-stu-id="295b0-129">Version</span></span><br/> | <span data-ttu-id="295b0-130">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="295b0-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="295b0-131">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="295b0-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="295b0-132">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="295b0-132">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="295b0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="295b0-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="295b0-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="295b0-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="295b0-135">IID</span><span class="sxs-lookup"><span data-stu-id="295b0-135">IID</span></span><br/>     | <span data-ttu-id="295b0-136">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="295b0-136">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="295b0-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="295b0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="295b0-138">**мсижеткомпонентпас**</span><span class="sxs-lookup"><span data-stu-id="295b0-138">**MsiGetComponentPath**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 




