---
description: Метод Реинсталлфеатуре объекта Installer переустанавливает компоненты или устраняет проблемы с установленными компонентами.
ms.assetid: cfe2aef4-7742-49cd-b7a3-7d484e1f85e3
title: Метод Installer. Реинсталлфеатуре
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a6bac008ee7121bbcb985b9a8ff5ba02df122266
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652161"
---
# <a name="installerreinstallfeature-method"></a><span data-ttu-id="334a9-103">Метод Installer. Реинсталлфеатуре</span><span class="sxs-lookup"><span data-stu-id="334a9-103">Installer.ReinstallFeature method</span></span>

<span data-ttu-id="334a9-104">Метод **реинсталлфеатуре** объекта [**Installer**](installer-object.md) переустанавливает компоненты или устраняет проблемы с установленными компонентами.</span><span class="sxs-lookup"><span data-stu-id="334a9-104">The **ReinstallFeature** method of the [**Installer**](installer-object.md) object reinstalls features or corrects problems with installed features.</span></span>

## <a name="syntax"></a><span data-ttu-id="334a9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="334a9-105">Syntax</span></span>


```JScript
Installer.ReinstallFeature(
  Product,
  Feature,
  ReinstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="334a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="334a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="334a9-107">*Продукт*</span><span class="sxs-lookup"><span data-stu-id="334a9-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="334a9-108">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="334a9-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="334a9-109">*Компонент*</span><span class="sxs-lookup"><span data-stu-id="334a9-109">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="334a9-110">Указывает компонент для переустановки.</span><span class="sxs-lookup"><span data-stu-id="334a9-110">Specifies the feature to be reinstalled.</span></span> <span data-ttu-id="334a9-111">Родительский компонент или дочерний компонент указанного компонента не переустановлен.</span><span class="sxs-lookup"><span data-stu-id="334a9-111">The parent feature or child feature of the specified feature is not reinstalled.</span></span> <span data-ttu-id="334a9-112">Чтобы переустановить родительскую или дочернюю функцию, необходимо вызвать метод **реинсталлфеатуре** отдельно или использовать метод [**реинсталлпродукт**](installer-reinstallproduct.md) .</span><span class="sxs-lookup"><span data-stu-id="334a9-112">To reinstall the parent or child feature, you must call the **ReinstallFeature** method for each separately or use the [**ReinstallProduct**](installer-reinstallproduct.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="334a9-113">*ReinstallMode*</span><span class="sxs-lookup"><span data-stu-id="334a9-113">*ReinstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="334a9-114">Указывает тип переустановки.</span><span class="sxs-lookup"><span data-stu-id="334a9-114">Specifies the type of reinstallation.</span></span> <span data-ttu-id="334a9-115">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="334a9-115">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="334a9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="334a9-116">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="334a9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="334a9-117">Meaning</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <span data-ttu-id="334a9-118"><dt>**мсиреинсталлмодефилемиссинг**</dt></span><span class="sxs-lookup"><span data-stu-id="334a9-118"><dt>**msiReinstallModeFileMissing**</dt></span></span> </dl>                     | <span data-ttu-id="334a9-119">Переустанавливает только в том случае, если файл отсутствует.</span><span class="sxs-lookup"><span data-stu-id="334a9-119">Reinstalls only if the file is missing.</span></span><br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <span data-ttu-id="334a9-120"><dt>**мсиреинсталлмодефилеолдерверсион**</dt></span><span class="sxs-lookup"><span data-stu-id="334a9-120"><dt>**msiReinstallModeFileOlderVersion**</dt></span></span> </dl> | <span data-ttu-id="334a9-121">Переустанавливает, если файл отсутствует или имеет более раннюю версию.</span><span class="sxs-lookup"><span data-stu-id="334a9-121">Reinstalls if the file is missing or is an older version.</span></span><br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <span data-ttu-id="334a9-122"><dt>**мсиреинсталлмодефиликуалверсион**</dt></span><span class="sxs-lookup"><span data-stu-id="334a9-122"><dt>**msiReinstallModeFileEqualVersion**</dt></span></span> </dl> | <span data-ttu-id="334a9-123">Переустанавливает, если файл отсутствует или имеет такую же или более старую версию.</span><span class="sxs-lookup"><span data-stu-id="334a9-123">Reinstalls if the file is missing or is an equal or older version.</span></span><br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <span data-ttu-id="334a9-124"><dt>**мсиреинсталлмодефиликсакт**</dt></span><span class="sxs-lookup"><span data-stu-id="334a9-124"><dt>**msiReinstallModeFileExact**</dt></span></span> </dl>                             | <span data-ttu-id="334a9-125">Переустанавливает, если файл отсутствует или не является точной версией.</span><span class="sxs-lookup"><span data-stu-id="334a9-125">Reinstalls if the file is missing or is not an exact version.</span></span><br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <span data-ttu-id="334a9-126"><dt>**мсиреинсталлмодефилеверифи**</dt></span><span class="sxs-lookup"><span data-stu-id="334a9-126"><dt>**msiReinstallModeFileVerify**</dt></span></span> </dl>                         | <span data-ttu-id="334a9-127">Проверяет исполняемые файлы и переустанавливает их, если они отсутствуют или повреждены.</span><span class="sxs-lookup"><span data-stu-id="334a9-127">Checks sum executables, and reinstalls if they are missing or corrupt.</span></span><br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <span data-ttu-id="334a9-128"><dt>**мсиреинсталлмодефилереплаце**</dt></span><span class="sxs-lookup"><span data-stu-id="334a9-128"><dt>**msiReinstallModeFileReplace**</dt></span></span> </dl>                     | <span data-ttu-id="334a9-129">Переустанавливает все файлы независимо от версии.</span><span class="sxs-lookup"><span data-stu-id="334a9-129">Reinstalls all files regardless of version.</span></span><br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <span data-ttu-id="334a9-130"><dt>**мсиреинсталлмодеусердата**</dt></span><span class="sxs-lookup"><span data-stu-id="334a9-130"><dt>**msiReinstallModeUserData**</dt></span></span> </dl>                                 | <span data-ttu-id="334a9-131">Проверяет наличие записей реестра, необходимых для пользователя.</span><span class="sxs-lookup"><span data-stu-id="334a9-131">Ensures required per=user registry entries.</span></span><br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <span data-ttu-id="334a9-132"><dt>**мсиреинсталлмодемачинедата**</dt></span><span class="sxs-lookup"><span data-stu-id="334a9-132"><dt>**msiReinstallModeMachineData**</dt></span></span> </dl>                     | <span data-ttu-id="334a9-133">Проверяет наличие записей реестра, необходимых для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="334a9-133">Ensures required per=machine registry entries.</span></span><br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <span data-ttu-id="334a9-134"><dt>**мсиреинсталлмодешорткут**</dt></span><span class="sxs-lookup"><span data-stu-id="334a9-134"><dt>**msiReinstallModeShortcut**</dt></span></span> </dl>                                 | <span data-ttu-id="334a9-135">Проверяет сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="334a9-135">Validates shortcuts.</span></span><br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <span data-ttu-id="334a9-136"><dt>**мсиреинсталлмодепаккаже**</dt></span><span class="sxs-lookup"><span data-stu-id="334a9-136"><dt>**msiReinstallModePackage**</dt></span></span> </dl>                                     | <span data-ttu-id="334a9-137">Использует источник повторного кэширования для установки пакета.</span><span class="sxs-lookup"><span data-stu-id="334a9-137">Uses the recache source to install the package.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="334a9-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="334a9-138">Return value</span></span>

<span data-ttu-id="334a9-139">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="334a9-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="334a9-140">Требования</span><span class="sxs-lookup"><span data-stu-id="334a9-140">Requirements</span></span>



| <span data-ttu-id="334a9-141">Требование</span><span class="sxs-lookup"><span data-stu-id="334a9-141">Requirement</span></span> | <span data-ttu-id="334a9-142">Значение</span><span class="sxs-lookup"><span data-stu-id="334a9-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="334a9-143">Версия</span><span class="sxs-lookup"><span data-stu-id="334a9-143">Version</span></span><br/> | <span data-ttu-id="334a9-144">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="334a9-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="334a9-145">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="334a9-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="334a9-146">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="334a9-146">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="334a9-147">DLL</span><span class="sxs-lookup"><span data-stu-id="334a9-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="334a9-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="334a9-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="334a9-149">IID</span><span class="sxs-lookup"><span data-stu-id="334a9-149">IID</span></span><br/>     | <span data-ttu-id="334a9-150">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="334a9-150">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="334a9-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="334a9-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="334a9-152">**мсиреинсталлфеатуре**</span><span class="sxs-lookup"><span data-stu-id="334a9-152">**MsiReinstallFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
</dt> <dt>

[<span data-ttu-id="334a9-153">Функции установки и настройки</span><span class="sxs-lookup"><span data-stu-id="334a9-153">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




