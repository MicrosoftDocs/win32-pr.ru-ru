---
description: Метод Реинсталлпродукт объекта Installer переустанавливает продукт или устраняет проблемы установки в установленном продукте.
ms.assetid: ff933cce-9f27-4215-9291-dd860d9c4d08
title: Метод Installer. Реинсталлпродукт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1570f5a0dc607b4a011a5b4276a243c59a64392d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651981"
---
# <a name="installerreinstallproduct-method"></a><span data-ttu-id="29656-103">Метод Installer. Реинсталлпродукт</span><span class="sxs-lookup"><span data-stu-id="29656-103">Installer.ReinstallProduct method</span></span>

<span data-ttu-id="29656-104">Метод **реинсталлпродукт** объекта [**Installer**](installer-object.md) переустанавливает продукт или устраняет проблемы установки в установленном продукте.</span><span class="sxs-lookup"><span data-stu-id="29656-104">The **ReinstallProduct** method of the [**Installer**](installer-object.md) object reinstalls a product or corrects installation problems in an installed product.</span></span>

## <a name="syntax"></a><span data-ttu-id="29656-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29656-105">Syntax</span></span>


```JScript
Installer.ReinstallProduct(
  Product,
  ReinstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="29656-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="29656-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29656-107">*Продукт*</span><span class="sxs-lookup"><span data-stu-id="29656-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="29656-108">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="29656-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="29656-109">*ReinstallMode*</span><span class="sxs-lookup"><span data-stu-id="29656-109">*ReinstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="29656-110">Указывает тип переустановки.</span><span class="sxs-lookup"><span data-stu-id="29656-110">Specifies the type of reinstallation.</span></span> <span data-ttu-id="29656-111">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="29656-111">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="29656-112">Значение</span><span class="sxs-lookup"><span data-stu-id="29656-112">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="29656-113">Значение</span><span class="sxs-lookup"><span data-stu-id="29656-113">Meaning</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <span data-ttu-id="29656-114"><dt>**мсиреинсталлмодефилемиссинг**</dt></span><span class="sxs-lookup"><span data-stu-id="29656-114"><dt>**msiReinstallModeFileMissing**</dt></span></span> </dl>                     | <span data-ttu-id="29656-115">Переустанавливает только в том случае, если файл отсутствует.</span><span class="sxs-lookup"><span data-stu-id="29656-115">Reinstalls only if the file is missing.</span></span><br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <span data-ttu-id="29656-116"><dt>**мсиреинсталлмодефилеолдерверсион**</dt></span><span class="sxs-lookup"><span data-stu-id="29656-116"><dt>**msiReinstallModeFileOlderVersion**</dt></span></span> </dl> | <span data-ttu-id="29656-117">Переустанавливает, если файл отсутствует или имеет более раннюю версию.</span><span class="sxs-lookup"><span data-stu-id="29656-117">Reinstalls if the file is missing or is an older version.</span></span><br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <span data-ttu-id="29656-118"><dt>**мсиреинсталлмодефиликуалверсион**</dt></span><span class="sxs-lookup"><span data-stu-id="29656-118"><dt>**msiReinstallModeFileEqualVersion**</dt></span></span> </dl> | <span data-ttu-id="29656-119">Переустанавливает, если файл отсутствует или имеет такую же или более старую версию.</span><span class="sxs-lookup"><span data-stu-id="29656-119">Reinstalls if the file is missing or is an equal or older version.</span></span><br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <span data-ttu-id="29656-120"><dt>**мсиреинсталлмодефиликсакт**</dt></span><span class="sxs-lookup"><span data-stu-id="29656-120"><dt>**msiReinstallModeFileExact**</dt></span></span> </dl>                             | <span data-ttu-id="29656-121">Переустанавливает, если файл отсутствует или не является точной версией.</span><span class="sxs-lookup"><span data-stu-id="29656-121">Reinstalls if the file is missing or is not an exact version.</span></span><br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <span data-ttu-id="29656-122"><dt>**мсиреинсталлмодефилеверифи**</dt></span><span class="sxs-lookup"><span data-stu-id="29656-122"><dt>**msiReinstallModeFileVerify**</dt></span></span> </dl>                         | <span data-ttu-id="29656-123">Проверяет исполняемые файлы и переустанавливает их, если они отсутствуют или повреждены.</span><span class="sxs-lookup"><span data-stu-id="29656-123">Checks sum executables, and reinstalls if they are missing or corrupt.</span></span><br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <span data-ttu-id="29656-124"><dt>**мсиреинсталлмодефилереплаце**</dt></span><span class="sxs-lookup"><span data-stu-id="29656-124"><dt>**msiReinstallModeFileReplace**</dt></span></span> </dl>                     | <span data-ttu-id="29656-125">Переустанавливает все файлы независимо от версии.</span><span class="sxs-lookup"><span data-stu-id="29656-125">Reinstalls all files regardless of version.</span></span><br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <span data-ttu-id="29656-126"><dt>**мсиреинсталлмодеусердата**</dt></span><span class="sxs-lookup"><span data-stu-id="29656-126"><dt>**msiReinstallModeUserData**</dt></span></span> </dl>                                 | <span data-ttu-id="29656-127">Проверяет наличие записей реестра, необходимых для пользователя.</span><span class="sxs-lookup"><span data-stu-id="29656-127">Ensures required per=user registry entries.</span></span><br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <span data-ttu-id="29656-128"><dt>**мсиреинсталлмодемачинедата**</dt></span><span class="sxs-lookup"><span data-stu-id="29656-128"><dt>**msiReinstallModeMachineData**</dt></span></span> </dl>                     | <span data-ttu-id="29656-129">Проверяет наличие записей реестра, необходимых для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="29656-129">Ensures required per=machine registry entries.</span></span><br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <span data-ttu-id="29656-130"><dt>**мсиреинсталлмодешорткут**</dt></span><span class="sxs-lookup"><span data-stu-id="29656-130"><dt>**msiReinstallModeShortcut**</dt></span></span> </dl>                                 | <span data-ttu-id="29656-131">Проверяет сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="29656-131">Validates shortcuts.</span></span><br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <span data-ttu-id="29656-132"><dt>**мсиреинсталлмодепаккаже**</dt></span><span class="sxs-lookup"><span data-stu-id="29656-132"><dt>**msiReinstallModePackage**</dt></span></span> </dl>                                     | <span data-ttu-id="29656-133">Использует источник повторного кэширования для установки пакета.</span><span class="sxs-lookup"><span data-stu-id="29656-133">Uses the recache source to install the package.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29656-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29656-134">Return value</span></span>

<span data-ttu-id="29656-135">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="29656-135">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="29656-136">Требования</span><span class="sxs-lookup"><span data-stu-id="29656-136">Requirements</span></span>



| <span data-ttu-id="29656-137">Требование</span><span class="sxs-lookup"><span data-stu-id="29656-137">Requirement</span></span> | <span data-ttu-id="29656-138">Значение</span><span class="sxs-lookup"><span data-stu-id="29656-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29656-139">Версия</span><span class="sxs-lookup"><span data-stu-id="29656-139">Version</span></span><br/> | <span data-ttu-id="29656-140">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="29656-140">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="29656-141">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="29656-141">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="29656-142">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="29656-142">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="29656-143">DLL</span><span class="sxs-lookup"><span data-stu-id="29656-143">DLL</span></span><br/>     | <dl> <span data-ttu-id="29656-144"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29656-144"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="29656-145">IID</span><span class="sxs-lookup"><span data-stu-id="29656-145">IID</span></span><br/>     | <span data-ttu-id="29656-146">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="29656-146">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="29656-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29656-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29656-148">**мсиреинсталлпродукт**</span><span class="sxs-lookup"><span data-stu-id="29656-148">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
</dt> <dt>

[<span data-ttu-id="29656-149">Функции установки и настройки</span><span class="sxs-lookup"><span data-stu-id="29656-149">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




