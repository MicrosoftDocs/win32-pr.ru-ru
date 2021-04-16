---
description: Метод Ремовепатчес удаляет один или несколько исправлений для продуктов, которые могут получить исправление. Метод Ремовепатчес вызывает Мсиремовепатчес.
ms.assetid: 09c6ad3a-9f5e-4f9a-82c8-be7e411efd60
title: Метод Installer. Ремовепатчес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RemovePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2130ae2958f03eb16b5145e5eb61e42f869ad775
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651980"
---
# <a name="installerremovepatches-method"></a><span data-ttu-id="676f5-104">Метод Installer. Ремовепатчес</span><span class="sxs-lookup"><span data-stu-id="676f5-104">Installer.RemovePatches method</span></span>

<span data-ttu-id="676f5-105">Метод **ремовепатчес** удаляет один или несколько исправлений для продуктов, которые могут получить исправление.</span><span class="sxs-lookup"><span data-stu-id="676f5-105">The **RemovePatches** method removes one or more patches to products eligible to receive the patch.</span></span> <span data-ttu-id="676f5-106">Метод **ремовепатчес** вызывает [**мсиремовепатчес**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span><span class="sxs-lookup"><span data-stu-id="676f5-106">The **RemovePatches** method calls [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span></span>

## <a name="syntax"></a><span data-ttu-id="676f5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="676f5-107">Syntax</span></span>


```JScript
Installer.RemovePatches(
  PatchList,
  ProductCode,
  UninstallType,
  PropertyList
)
```



## <a name="parameters"></a><span data-ttu-id="676f5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="676f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="676f5-109">*патчлист*</span><span class="sxs-lookup"><span data-stu-id="676f5-109">*PatchList*</span></span> 
</dt> <dd>

<span data-ttu-id="676f5-110">Строка, содержащая разделенный точками с запятой список исправлений для удаления.</span><span class="sxs-lookup"><span data-stu-id="676f5-110">A string that contains a semicolon delimited list of patches to remove.</span></span> <span data-ttu-id="676f5-111">Каждое исправление может быть представлено полным путем к пакету исправлений или идентификатором GUID исправления.</span><span class="sxs-lookup"><span data-stu-id="676f5-111">Each patch can be represented by either the full path to the patch package or by patch GUID.</span></span> <span data-ttu-id="676f5-112">Этот параметр обязателен.</span><span class="sxs-lookup"><span data-stu-id="676f5-112">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="676f5-113">*ProductCode*</span><span class="sxs-lookup"><span data-stu-id="676f5-113">*ProductCode*</span></span> 
</dt> <dd>

<span data-ttu-id="676f5-114">Строка с идентификатором GUID продукта, из которого удаляются исправления.</span><span class="sxs-lookup"><span data-stu-id="676f5-114">A string with the GUID of the product from which the patches are to be removed.</span></span> <span data-ttu-id="676f5-115">Этот параметр обязателен.</span><span class="sxs-lookup"><span data-stu-id="676f5-115">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="676f5-116">*унинсталлтипе*</span><span class="sxs-lookup"><span data-stu-id="676f5-116">*UninstallType*</span></span> 
</dt> <dd>

<span data-ttu-id="676f5-117">Целочисленное значение, указывающее тип удаления исправления.</span><span class="sxs-lookup"><span data-stu-id="676f5-117">An integer value that specifies the type of patch removal.</span></span> <span data-ttu-id="676f5-118">Этот параметр должен быть **мсиинсталлтипесинглеинстанце**.</span><span class="sxs-lookup"><span data-stu-id="676f5-118">This parameter must be **msiInstallTypeSingleInstance**.</span></span>

</dd> <dt>

<span data-ttu-id="676f5-119">*PropertyList*</span><span class="sxs-lookup"><span data-stu-id="676f5-119">*PropertyList*</span></span> 
</dt> <dd>

<span data-ttu-id="676f5-120">Строка, указывающая пары "свойство = значение" для включения.</span><span class="sxs-lookup"><span data-stu-id="676f5-120">A string that specifies the Property=Value pairs to include.</span></span> <span data-ttu-id="676f5-121">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="676f5-121">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="676f5-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="676f5-122">Return value</span></span>

<span data-ttu-id="676f5-123">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="676f5-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="676f5-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="676f5-124">Remarks</span></span>

<span data-ttu-id="676f5-125">Пример, демонстрирующий, как приложение может удалить исправление из всех доступных для пользователя продуктов, см. в разделе Удаление [исправлений](uninstalling-patches.md) .</span><span class="sxs-lookup"><span data-stu-id="676f5-125">See [Uninstalling Patches](uninstalling-patches.md) for an example that demonstrates how an application can remove a patch from all products that are available to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="676f5-126">Требования</span><span class="sxs-lookup"><span data-stu-id="676f5-126">Requirements</span></span>



| <span data-ttu-id="676f5-127">Требование</span><span class="sxs-lookup"><span data-stu-id="676f5-127">Requirement</span></span> | <span data-ttu-id="676f5-128">Значение</span><span class="sxs-lookup"><span data-stu-id="676f5-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="676f5-129">Версия</span><span class="sxs-lookup"><span data-stu-id="676f5-129">Version</span></span><br/> | <span data-ttu-id="676f5-130">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="676f5-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="676f5-131">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="676f5-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="676f5-132">Установщик Windows 3,0 или более поздней версии в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="676f5-132">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="676f5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="676f5-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="676f5-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="676f5-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="676f5-135">IID</span><span class="sxs-lookup"><span data-stu-id="676f5-135">IID</span></span><br/>     | <span data-ttu-id="676f5-136">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="676f5-136">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="676f5-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="676f5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="676f5-138">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="676f5-138">**ProductCode**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="676f5-139">**мсиремовепатчес**</span><span class="sxs-lookup"><span data-stu-id="676f5-139">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[<span data-ttu-id="676f5-140">Удаление исправлений</span><span class="sxs-lookup"><span data-stu-id="676f5-140">Uninstalling Patches</span></span>](uninstalling-patches.md)
</dt> <dt>

[<span data-ttu-id="676f5-141">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="676f5-141">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




