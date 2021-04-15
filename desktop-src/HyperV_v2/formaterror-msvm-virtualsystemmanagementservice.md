---
description: Возвращает отформатированную строку сообщения об ошибке для указанного массива внедренных \_ экземпляров ошибок мсвм.
ms.assetid: 477EF4AE-00A8-4F2D-A335-E41A2EF620BB
title: Метод Форматеррор класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.FormatError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e768a6ea968d428d7809c7c322a80f3ad233aa2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662468"
---
# <a name="formaterror-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="923d0-103">Метод Форматеррор \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="923d0-103">FormatError method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="923d0-104">Возвращает отформатированную строку сообщения об ошибке для указанного массива внедренных экземпляров [**\_ ошибок мсвм**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="923d0-104">Returns a formatted error message string for the specified array of embedded [**Msvm\_Error**](msvm-error.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="923d0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="923d0-105">Syntax</span></span>


```mof
uint32 FormatError(
  [in]  string Errors[],
  [out] string ErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="923d0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="923d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="923d0-107">*Ошибки* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="923d0-107">*Errors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="923d0-108">Тип: **строка \[ \]**</span><span class="sxs-lookup"><span data-stu-id="923d0-108">Type: **string\[\]**</span></span>

<span data-ttu-id="923d0-109">Массив строк, содержащий экземпляры [**\_ ошибок мсвм**](msvm-error.md) , которые используются для создания сообщения об ошибке вывода.</span><span class="sxs-lookup"><span data-stu-id="923d0-109">An array of strings containing [**Msvm\_Error**](msvm-error.md) instances used to generate the output error message.</span></span>

</dd> <dt>

<span data-ttu-id="923d0-110">*ErrorMessage* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="923d0-110">*ErrorMessage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="923d0-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="923d0-111">Type: **string**</span></span>

<span data-ttu-id="923d0-112">На выходе строка, содержащая сцепленные сообщения об ошибках, представленные экземплярами [**\_ ошибок мсвм**](msvm-error.md) , передаваемыми в параметре *Errors* .</span><span class="sxs-lookup"><span data-stu-id="923d0-112">On output, a string that contains the concatenated error messages represented by the [**Msvm\_Error**](msvm-error.md) instances passed in the *Errors* parameter.</span></span> <span data-ttu-id="923d0-113">Каждая строка ошибки отделяется парой символов новой строки (" \\ n").</span><span class="sxs-lookup"><span data-stu-id="923d0-113">Each error string is separated by a pair of newline characters ('\\n').</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="923d0-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="923d0-114">Return value</span></span>

<span data-ttu-id="923d0-115">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="923d0-115">Type: **uint32**</span></span>

<span data-ttu-id="923d0-116">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="923d0-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="923d0-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="923d0-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="923d0-118">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="923d0-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="923d0-119">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="923d0-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="923d0-120">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="923d0-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="923d0-121">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="923d0-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="923d0-122">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="923d0-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="923d0-123">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="923d0-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="923d0-124">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="923d0-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="923d0-125">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="923d0-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="923d0-126">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="923d0-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="923d0-127">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="923d0-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="923d0-128">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="923d0-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="923d0-129">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="923d0-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="923d0-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="923d0-130">Remarks</span></span>

<span data-ttu-id="923d0-131">Доступ к классу [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="923d0-131">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="923d0-132">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="923d0-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="923d0-133">Требования</span><span class="sxs-lookup"><span data-stu-id="923d0-133">Requirements</span></span>



| <span data-ttu-id="923d0-134">Требование</span><span class="sxs-lookup"><span data-stu-id="923d0-134">Requirement</span></span> | <span data-ttu-id="923d0-135">Значение</span><span class="sxs-lookup"><span data-stu-id="923d0-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="923d0-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="923d0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="923d0-137">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="923d0-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="923d0-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="923d0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="923d0-139">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="923d0-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="923d0-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="923d0-140">Namespace</span></span><br/>                | <span data-ttu-id="923d0-141">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="923d0-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="923d0-142">MOF</span><span class="sxs-lookup"><span data-stu-id="923d0-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="923d0-143"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="923d0-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="923d0-144">DLL</span><span class="sxs-lookup"><span data-stu-id="923d0-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="923d0-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="923d0-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="923d0-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="923d0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="923d0-147">**Форматеррор (v1)**</span><span class="sxs-lookup"><span data-stu-id="923d0-147">**FormatError (V1)**</span></span>](/previous-versions/windows/desktop/virtual/formaterror-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="923d0-148">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="923d0-148">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

