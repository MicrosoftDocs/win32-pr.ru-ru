---
description: Метод RegistryValue объекта Installer считывает сведения об указанном разделе реестра value.
ms.assetid: 63c258f9-8649-419d-9f79-3681f9f97302
title: Метод Installer. RegistryValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RegistryValue
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6da79ff08eebe62ad177119a35bfc29b21c9350
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651982"
---
# <a name="installerregistryvalue-method"></a><span data-ttu-id="3755d-103">Метод Installer. RegistryValue</span><span class="sxs-lookup"><span data-stu-id="3755d-103">Installer.RegistryValue method</span></span>

<span data-ttu-id="3755d-104">Метод **RegistryValue** объекта [**Installer**](installer-object.md) считывает сведения об указанном разделе реестра value.</span><span class="sxs-lookup"><span data-stu-id="3755d-104">The **RegistryValue** method of the [**Installer**](installer-object.md) object reads information about a specified registry key of value.</span></span> <span data-ttu-id="3755d-105">Если указанный раздел или значение не существует, метод возвращает ошибку 9, «индекс вне диапазона».</span><span class="sxs-lookup"><span data-stu-id="3755d-105">If the key or value specified does not exist, the method returns an error of 9, "Subscript out of Range."</span></span>

## <a name="syntax"></a><span data-ttu-id="3755d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3755d-106">Syntax</span></span>


```JScript
Installer.RegistryValue(
  root,
  key,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="3755d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3755d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3755d-108">*root*</span><span class="sxs-lookup"><span data-stu-id="3755d-108">*root*</span></span> 
</dt> <dd>

<span data-ttu-id="3755d-109">В Windows NT 4,0 корень реестра — это либо числовой корневой ключ, либо имя компьютера в виде строки.</span><span class="sxs-lookup"><span data-stu-id="3755d-109">In Windows NT 4.0, the registry root is either a numeric root key or a machine name as a string.</span></span> <span data-ttu-id="3755d-110">Имена компьютеров всегда являются строками.</span><span class="sxs-lookup"><span data-stu-id="3755d-110">Machine names are always strings.</span></span> <span data-ttu-id="3755d-111">В Windows 95, Windows 98 или Windows Me корень реестра является только числовым корневым ключом.</span><span class="sxs-lookup"><span data-stu-id="3755d-111">In Windows 95, Windows 98, or Windows Me, the registry root is a numeric root key only.</span></span> <span data-ttu-id="3755d-112">Доступ к разделу HKLM можно получить только на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="3755d-112">You can only access HKLM on a remote machine.</span></span>



| <span data-ttu-id="3755d-113">Root</span><span class="sxs-lookup"><span data-stu-id="3755d-113">Root</span></span>                                                                                                                                                                                   | <span data-ttu-id="3755d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="3755d-114">Meaning</span></span>      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span id="HKEY_CLASSES_ROOT"></span><span id="hkey_classes_root"></span><dl> <span data-ttu-id="3755d-115"><dt>**\_корневой узел классов hKey \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3755d-115"><dt>**HKEY\_CLASSES\_ROOT**</dt></span></span> </dl>             | <span data-ttu-id="3755d-116">0</span><span class="sxs-lookup"><span data-stu-id="3755d-116">0</span></span><br/> |
| <span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dl> <span data-ttu-id="3755d-117"><dt>**HKEY \_ текущего \_ пользователя**</dt></span><span class="sxs-lookup"><span data-stu-id="3755d-117"><dt>**HKEY\_CURRENT\_USER**</dt></span></span> </dl>             | <span data-ttu-id="3755d-118">1</span><span class="sxs-lookup"><span data-stu-id="3755d-118">1</span></span><br/> |
| <span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dl> <span data-ttu-id="3755d-119"><dt>**HKEY \_ локальный \_ компьютер**</dt></span><span class="sxs-lookup"><span data-stu-id="3755d-119"><dt>**HKEY\_LOCAL\_MACHINE**</dt></span></span> </dl>          | <span data-ttu-id="3755d-120">2</span><span class="sxs-lookup"><span data-stu-id="3755d-120">2</span></span><br/> |
| <span id="HKEY_USERS"></span><span id="hkey_users"></span><dl> <span data-ttu-id="3755d-121"><dt>**\_Пользователи hKey**</dt></span><span class="sxs-lookup"><span data-stu-id="3755d-121"><dt>**HKEY\_USERS**</dt></span></span> </dl>                                   | <span data-ttu-id="3755d-122">3</span><span class="sxs-lookup"><span data-stu-id="3755d-122">3</span></span><br/> |
| <span id="HKEY_PERFORMANCE_DATA"></span><span id="hkey_performance_data"></span><dl> <span data-ttu-id="3755d-123"><dt>**\_данные о производительности hKey \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3755d-123"><dt>**HKEY\_PERFORMANCE\_DATA**</dt></span></span> </dl> | <span data-ttu-id="3755d-124">4</span><span class="sxs-lookup"><span data-stu-id="3755d-124">4</span></span><br/> |
| <span id="HKEY_CURRENT_CONFIG"></span><span id="hkey_current_config"></span><dl> <span data-ttu-id="3755d-125"><dt>**\_Текущая \_ Конфигурация hKey**</dt></span><span class="sxs-lookup"><span data-stu-id="3755d-125"><dt>**HKEY\_CURRENT\_CONFIG**</dt></span></span> </dl>       | <span data-ttu-id="3755d-126">5</span><span class="sxs-lookup"><span data-stu-id="3755d-126">5</span></span><br/> |
| <span id="HKEY_DYN_DATA"></span><span id="hkey_dyn_data"></span><dl> <span data-ttu-id="3755d-127"><dt>**\_данные hKey Дин \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3755d-127"><dt>**HKEY\_DYN\_DATA**</dt></span></span> </dl>                         | <span data-ttu-id="3755d-128">6</span><span class="sxs-lookup"><span data-stu-id="3755d-128">6</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3755d-129">*key*</span><span class="sxs-lookup"><span data-stu-id="3755d-129">*key*</span></span> 
</dt> <dd>

<span data-ttu-id="3755d-130">Строка, содержащая полный путь к ключу из корня.</span><span class="sxs-lookup"><span data-stu-id="3755d-130">A string containing the complete key path from the root.</span></span>

</dd> <dt>

<span data-ttu-id="3755d-131">*value*</span><span class="sxs-lookup"><span data-stu-id="3755d-131">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="3755d-132">Этот необязательный параметр определяет связанное значение, возвращаемое для указанного ключа.</span><span class="sxs-lookup"><span data-stu-id="3755d-132">This optional parameter designates which associated value to return for the specified key.</span></span> <span data-ttu-id="3755d-133">Значением является одно из значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3755d-133">The value is one of the values shown in the following table.</span></span>



| <span data-ttu-id="3755d-134">Значение</span><span class="sxs-lookup"><span data-stu-id="3755d-134">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="3755d-135">Значение</span><span class="sxs-lookup"><span data-stu-id="3755d-135">Meaning</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Missing_or_blank"></span><span id="missing_or_blank"></span><span id="MISSING_OR_BLANK"></span><dl> <span data-ttu-id="3755d-136"><dt>**Отсутствует или пусто**</dt></span><span class="sxs-lookup"><span data-stu-id="3755d-136"><dt>**Missing or blank**</dt></span></span> </dl> | <span data-ttu-id="3755d-137">Возвращает логическое значение, определяющее, существует ли ключ.</span><span class="sxs-lookup"><span data-stu-id="3755d-137">Returns a Boolean designating whether the key exists.</span></span><br/>                                                                                        |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <span data-ttu-id="3755d-138"><dt>**Строка**</dt></span><span class="sxs-lookup"><span data-stu-id="3755d-138"><dt>**String**</dt></span></span> </dl>                                         | <span data-ttu-id="3755d-139">Возвращает данные, связанные с именованным значением, завершается ошибкой, если имя значения не существует.</span><span class="sxs-lookup"><span data-stu-id="3755d-139">Returns the data associated with the named value, fails if the value name is non-existent.</span></span><br/>                                                   |
| <span id="Positive_integer"></span><span id="positive_integer"></span><span id="POSITIVE_INTEGER"></span><dl> <span data-ttu-id="3755d-140"><dt>**Положительное целое число**</dt></span><span class="sxs-lookup"><span data-stu-id="3755d-140"><dt>**Positive integer**</dt></span></span> </dl> | <span data-ttu-id="3755d-141">Возвращает имя перечислимого значения, основанного на 1, оно пустое, если оно не существует.</span><span class="sxs-lookup"><span data-stu-id="3755d-141">Returns the 1-based enumerated value name, it is empty if non-existent.</span></span> <span data-ttu-id="3755d-142">Этот параметр использует функцию [**реженумвалуе**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) .</span><span class="sxs-lookup"><span data-stu-id="3755d-142">This option uses the [**RegEnumValue**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) function.</span></span><br/> |
| <span id="Negative_integer"></span><span id="negative_integer"></span><span id="NEGATIVE_INTEGER"></span><dl> <span data-ttu-id="3755d-143"><dt>**Отрицательное целое число**</dt></span><span class="sxs-lookup"><span data-stu-id="3755d-143"><dt>**Negative integer**</dt></span></span> </dl> | <span data-ttu-id="3755d-144">Возвращает имя подраздела с именем, основанное на 1, пустое, если оно не существует.</span><span class="sxs-lookup"><span data-stu-id="3755d-144">Returns the 1-based enumerated subkey name, this is empty if non-existent.</span></span> <span data-ttu-id="3755d-145">Этот параметр использует функцию [**реженумкэй**](/windows/win32/api/winreg/nf-winreg-regenumkeya) .</span><span class="sxs-lookup"><span data-stu-id="3755d-145">This option uses the [**RegEnumKey**](/windows/win32/api/winreg/nf-winreg-regenumkeya) function.</span></span><br/>  |
| <span id="Zero_integer"></span><span id="zero_integer"></span><span id="ZERO_INTEGER"></span><dl> <span data-ttu-id="3755d-146"><dt>**Нулевое целое число**</dt></span><span class="sxs-lookup"><span data-stu-id="3755d-146"><dt>**Zero integer**</dt></span></span> </dl>                 | <span data-ttu-id="3755d-147">Возвращает имя класса String для назначенного ключа.</span><span class="sxs-lookup"><span data-stu-id="3755d-147">Returns the string class name for the designated key.</span></span><br/>                                                                                        |
| <span id="Empty_string____"></span><span id="empty_string____"></span><span id="EMPTY_STRING____"></span><dl> <span data-ttu-id="3755d-148"><dt>**Пустая строка ""**</dt></span><span class="sxs-lookup"><span data-stu-id="3755d-148"><dt>**Empty string " "**</dt></span></span> </dl> | <span data-ttu-id="3755d-149">Возвращает значение по умолчанию для раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="3755d-149">Returns the default value of the registry key.</span></span><br/>                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3755d-150">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3755d-150">Return value</span></span>

<span data-ttu-id="3755d-151">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3755d-151">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3755d-152">Требования</span><span class="sxs-lookup"><span data-stu-id="3755d-152">Requirements</span></span>



| <span data-ttu-id="3755d-153">Требование</span><span class="sxs-lookup"><span data-stu-id="3755d-153">Requirement</span></span> | <span data-ttu-id="3755d-154">Значение</span><span class="sxs-lookup"><span data-stu-id="3755d-154">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3755d-155">Версия</span><span class="sxs-lookup"><span data-stu-id="3755d-155">Version</span></span><br/> | <span data-ttu-id="3755d-156">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3755d-156">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3755d-157">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3755d-157">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3755d-158">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="3755d-158">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3755d-159">DLL</span><span class="sxs-lookup"><span data-stu-id="3755d-159">DLL</span></span><br/>     | <dl> <span data-ttu-id="3755d-160"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3755d-160"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3755d-161">IID</span><span class="sxs-lookup"><span data-stu-id="3755d-161">IID</span></span><br/>     | <span data-ttu-id="3755d-162">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3755d-162">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 
