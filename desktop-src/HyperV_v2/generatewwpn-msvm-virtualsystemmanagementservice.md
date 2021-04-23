---
description: Формирует набор WWN-имен портов (Ввпнс).
ms.assetid: 36f393eb-6f34-4ae3-a976-c5da60211f3e
title: Метод Женератеввпн класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GenerateWwpn
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b0efba6a24a7e4f7e6826f91930cb69b4b54f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682803"
---
# <a name="generatewwpn-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="7df64-103">Метод Женератеввпн \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="7df64-103">GenerateWwpn method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="7df64-104">Формирует набор WWN-имен портов (Ввпнс).</span><span class="sxs-lookup"><span data-stu-id="7df64-104">Generates a set of World Wide Port Names (WWPNs).</span></span> <span data-ttu-id="7df64-105">Ввпнс создаются в предварительно настроенном диапазоне, определяемом свойствами **минимумввпнаддресс** и **максимумввпнаддресс** класса [**мсвм \_ виртуалсистемманажементсервицесеттингдата**](msvm-virtualsystemmanagementservicesettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="7df64-105">The WWPNs are generated from within the pre-configured range defined by the **MinimumWWPNAddress** and **MaximumWWPNAddress** properties of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class.</span></span> <span data-ttu-id="7df64-106">Если допустимое число Ввпнс меньше запрошенного числа, остальные записи в массиве *женератедввпн* будут иметь недопустимую запись "0000000000000000", и возвращаемое значение будет означать успешность (0).</span><span class="sxs-lookup"><span data-stu-id="7df64-106">If the valid number of WWPNs that can be generated is less than the requested number, then the remaining entries in the *GeneratedWwpn* array will have the invalid entry of "0000000000000000" and the return value will indicate success (0).</span></span>

## <a name="syntax"></a><span data-ttu-id="7df64-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7df64-107">Syntax</span></span>


```mof
uint32 GenerateWwpn(
  [in]  uint32 NumberOfWwpns,
  [out] string GeneratedWwpn[]
);
```



## <a name="parameters"></a><span data-ttu-id="7df64-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7df64-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7df64-109">*Нумберофввпнс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7df64-109">*NumberOfWwpns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7df64-110">Число создаваемых Ввпнс.</span><span class="sxs-lookup"><span data-stu-id="7df64-110">The number of WWPNs to be generated.</span></span>

</dd> <dt>

<span data-ttu-id="7df64-111">*Женератедввпн* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7df64-111">*GeneratedWwpn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7df64-112">Массив строк, каждый из которых будет содержать созданное WWPN.</span><span class="sxs-lookup"><span data-stu-id="7df64-112">An array of strings, each of which will contain a generated WWPN.</span></span> <span data-ttu-id="7df64-113">Он будет отформатирован в виде строки как "01:23:45:67:89: AB: CD: EF".</span><span class="sxs-lookup"><span data-stu-id="7df64-113">It will be formatted in string form as "01:23:45:67:89:ab:cd:ef".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7df64-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7df64-114">Return value</span></span>

<span data-ttu-id="7df64-115">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7df64-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7df64-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="7df64-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7df64-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="7df64-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7df64-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="7df64-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7df64-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="7df64-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7df64-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="7df64-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7df64-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="7df64-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7df64-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="7df64-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7df64-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="7df64-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7df64-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="7df64-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7df64-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="7df64-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7df64-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="7df64-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7df64-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="7df64-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7df64-128">Требования</span><span class="sxs-lookup"><span data-stu-id="7df64-128">Requirements</span></span>



| <span data-ttu-id="7df64-129">Требование</span><span class="sxs-lookup"><span data-stu-id="7df64-129">Requirement</span></span> | <span data-ttu-id="7df64-130">Значение</span><span class="sxs-lookup"><span data-stu-id="7df64-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7df64-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7df64-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7df64-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7df64-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7df64-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7df64-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7df64-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7df64-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7df64-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7df64-135">Namespace</span></span><br/>                | <span data-ttu-id="7df64-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7df64-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7df64-137">MOF</span><span class="sxs-lookup"><span data-stu-id="7df64-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7df64-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7df64-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7df64-139">DLL</span><span class="sxs-lookup"><span data-stu-id="7df64-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7df64-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7df64-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7df64-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7df64-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df64-142">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="7df64-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




