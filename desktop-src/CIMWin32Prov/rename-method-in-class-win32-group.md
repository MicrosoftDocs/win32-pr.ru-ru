---
description: Позволяет изменить имя группы.
ms.assetid: 7eb1360e-7416-4a90-abc6-c9a85a114316
ms.tgt_platform: multiple
title: Метод Rename класса Win32_Group
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c111a0c12d0fdc1ce3f6d6bcaa0e7b0f57831054
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655639"
---
# <a name="rename-method-of-the-win32_group-class"></a><span data-ttu-id="8a0fa-103">Метод Rename \_ класса группы Win32</span><span class="sxs-lookup"><span data-stu-id="8a0fa-103">Rename method of the Win32\_Group class</span></span>

<span data-ttu-id="8a0fa-104">Метод **переименования** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) позволяет изменить имя группы.</span><span class="sxs-lookup"><span data-stu-id="8a0fa-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method allows the group name to be changed.</span></span>

<span data-ttu-id="8a0fa-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="8a0fa-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8a0fa-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8a0fa-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a0fa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a0fa-107">Syntax</span></span>


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="8a0fa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a0fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a0fa-109">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a0fa-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0fa-110">Имя учетной записи пользователя Windows в домене, указанном свойством **domain** данного класса.</span><span class="sxs-lookup"><span data-stu-id="8a0fa-110">Name of the Windows user account on the domain specified by the **Domain** property of this class.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a0fa-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a0fa-111">Return value</span></span>

<span data-ttu-id="8a0fa-112">Метод **Rename** может возвращать коды ошибок, перечисленные в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="8a0fa-112">The **Rename** method can return the error codes listed in the following list.</span></span> <span data-ttu-id="8a0fa-113">Для целочисленных значений, отличных от перечисленных, см. [ \_ коды возврата WMI](/windows/desktop/WmiSdk/wmi-return-codes).</span><span class="sxs-lookup"><span data-stu-id="8a0fa-113">For integer values other than those listed, refer to [WMI\_Return Codes](/windows/desktop/WmiSdk/wmi-return-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8a0fa-114">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="8a0fa-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="8a0fa-115">0</span><span class="sxs-lookup"><span data-stu-id="8a0fa-115">0</span></span>

<span data-ttu-id="8a0fa-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="8a0fa-116">Success.</span></span>

</dd> <dt>

<span data-ttu-id="8a0fa-117">**Экземпляр не найден**</span><span class="sxs-lookup"><span data-stu-id="8a0fa-117">**Instance not found**</span></span>
</dt> <dd>

<span data-ttu-id="8a0fa-118">1</span><span class="sxs-lookup"><span data-stu-id="8a0fa-118">1</span></span>

</dd> <dt>

<span data-ttu-id="8a0fa-119">**Требуется экземпляр**</span><span class="sxs-lookup"><span data-stu-id="8a0fa-119">**Instance required**</span></span>
</dt> <dd>

<span data-ttu-id="8a0fa-120">2</span><span class="sxs-lookup"><span data-stu-id="8a0fa-120">2</span></span>

</dd> <dt>

<span data-ttu-id="8a0fa-121">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="8a0fa-121">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8a0fa-122">3</span><span class="sxs-lookup"><span data-stu-id="8a0fa-122">3</span></span>

</dd> <dt>

<span data-ttu-id="8a0fa-123">**Группа не найдена**</span><span class="sxs-lookup"><span data-stu-id="8a0fa-123">**Group not found**</span></span>
</dt> <dd>

<span data-ttu-id="8a0fa-124">4</span><span class="sxs-lookup"><span data-stu-id="8a0fa-124">4</span></span>

</dd> <dt>

<span data-ttu-id="8a0fa-125">**Домен не найден**</span><span class="sxs-lookup"><span data-stu-id="8a0fa-125">**Domain not found**</span></span>
</dt> <dd>

<span data-ttu-id="8a0fa-126">5</span><span class="sxs-lookup"><span data-stu-id="8a0fa-126">5</span></span>

</dd> <dt>

<span data-ttu-id="8a0fa-127">**Операция разрешена только на основном контроллере домена**</span><span class="sxs-lookup"><span data-stu-id="8a0fa-127">**Operation is allowed only on the primary domain controller of the domain**</span></span>
</dt> <dd>

<span data-ttu-id="8a0fa-128">6</span><span class="sxs-lookup"><span data-stu-id="8a0fa-128">6</span></span>

</dd> <dt>

<span data-ttu-id="8a0fa-129">**Операция не разрешена для указанных специальных групп. пользователь, администратор, локальный или гость.**</span><span class="sxs-lookup"><span data-stu-id="8a0fa-129">**Operation is not allowed on specified special groups; user, admin, local or guest.**</span></span>
</dt> <dd>

<span data-ttu-id="8a0fa-130">7</span><span class="sxs-lookup"><span data-stu-id="8a0fa-130">7</span></span>

</dd> <dt>

<span data-ttu-id="8a0fa-131">**Другая ошибка API**</span><span class="sxs-lookup"><span data-stu-id="8a0fa-131">**Other API error**</span></span>
</dt> <dd>

<span data-ttu-id="8a0fa-132">8</span><span class="sxs-lookup"><span data-stu-id="8a0fa-132">8</span></span>

</dd> <dt>

<span data-ttu-id="8a0fa-133">**Внутренняя ошибка**</span><span class="sxs-lookup"><span data-stu-id="8a0fa-133">**Internal error**</span></span>
</dt> <dd>

<span data-ttu-id="8a0fa-134">9</span><span class="sxs-lookup"><span data-stu-id="8a0fa-134">9</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a0fa-135">Требования</span><span class="sxs-lookup"><span data-stu-id="8a0fa-135">Requirements</span></span>



| <span data-ttu-id="8a0fa-136">Требование</span><span class="sxs-lookup"><span data-stu-id="8a0fa-136">Requirement</span></span> | <span data-ttu-id="8a0fa-137">Значение</span><span class="sxs-lookup"><span data-stu-id="8a0fa-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a0fa-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a0fa-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8a0fa-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a0fa-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8a0fa-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a0fa-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8a0fa-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a0fa-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a0fa-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8a0fa-142">Namespace</span></span><br/>                | <span data-ttu-id="8a0fa-143">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8a0fa-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8a0fa-144">MOF</span><span class="sxs-lookup"><span data-stu-id="8a0fa-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a0fa-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a0fa-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a0fa-146">DLL</span><span class="sxs-lookup"><span data-stu-id="8a0fa-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a0fa-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a0fa-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a0fa-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a0fa-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="8a0fa-149">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8a0fa-149">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8a0fa-150">**\_Группа Win32**</span><span class="sxs-lookup"><span data-stu-id="8a0fa-150">**Win32\_Group**</span></span>](win32-group.md)
</dt> <dt>

[<span data-ttu-id="8a0fa-151">**\_Логикалфилесекуритисеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="8a0fa-151">**Win32\_LogicalFileSecuritySetting**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)
</dt> </dl>

 

