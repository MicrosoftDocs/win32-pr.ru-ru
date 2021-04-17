---
description: Запрашивает изменение состояния запланированной системы на указанное значение.
ms.assetid: 54ed9514-4f09-458e-8e86-a807ee66df17
title: Метод RequestStateChange класса Msvm_PlannedComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 172ec383473510a30ccde66b2617e8ef02ffdb72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683377"
---
# <a name="requeststatechange-method-of-the-msvm_plannedcomputersystem-class"></a><span data-ttu-id="b7aca-103">Метод RequestStateChange \_ класса мсвм планнедкомпутерсистем</span><span class="sxs-lookup"><span data-stu-id="b7aca-103">RequestStateChange method of the Msvm\_PlannedComputerSystem class</span></span>

<span data-ttu-id="b7aca-104">Запрашивает изменение состояния запланированной системы на указанное значение.</span><span class="sxs-lookup"><span data-stu-id="b7aca-104">Requests that the state of the planned system be changed to the value specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7aca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7aca-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="b7aca-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7aca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7aca-107">*RequestedState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7aca-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7aca-108">Запрошенное состояние для запланированной системы.</span><span class="sxs-lookup"><span data-stu-id="b7aca-108">The requested state for the planned system.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b7aca-109">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="b7aca-109">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b7aca-110">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="b7aca-110">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="b7aca-111">**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="b7aca-111">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="b7aca-112">**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="b7aca-112">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="b7aca-113">**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="b7aca-113">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="b7aca-114">**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="b7aca-114">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="b7aca-115">**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="b7aca-115">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="b7aca-116">**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="b7aca-116">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="b7aca-117">**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="b7aca-117">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b7aca-118">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="b7aca-118">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b7aca-119">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b7aca-119">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="b7aca-120">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b7aca-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7aca-121">Этот параметр не используется и должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b7aca-121">This parameter is not used and should be **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b7aca-122">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7aca-122">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7aca-123">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="b7aca-123">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7aca-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7aca-124">Return value</span></span>

<span data-ttu-id="b7aca-125">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b7aca-125">This method returns one of the following values.</span></span>



| <span data-ttu-id="b7aca-126">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="b7aca-126">Return code/value</span></span>                                                                                                                      | <span data-ttu-id="b7aca-127">Описание</span><span class="sxs-lookup"><span data-stu-id="b7aca-127">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b7aca-128"><dt></dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b7aca-128"><dt></dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="b7aca-129">Успешно</span><span class="sxs-lookup"><span data-stu-id="b7aca-129">Success</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="b7aca-130"><dt></dt><dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="b7aca-130"><dt></dt> <dt>4096</dt></span></span> </dl>  |                                                                                    |
| <dl> <span data-ttu-id="b7aca-131"><dt></dt><dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="b7aca-131"><dt></dt> <dt>32768</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="b7aca-132"><dt></dt><dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="b7aca-132"><dt></dt> <dt>32769</dt></span></span> </dl> | <span data-ttu-id="b7aca-133">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="b7aca-133">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="b7aca-134"><dt></dt><dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="b7aca-134"><dt></dt> <dt>32770</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="b7aca-135"><dt></dt><dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="b7aca-135"><dt></dt> <dt>32771</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="b7aca-136"><dt></dt><dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="b7aca-136"><dt></dt> <dt>32772</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="b7aca-137"><dt></dt><dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="b7aca-137"><dt></dt> <dt>32773</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="b7aca-138"><dt></dt><dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="b7aca-138"><dt></dt> <dt>32774</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="b7aca-139"><dt></dt><dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="b7aca-139"><dt></dt> <dt>32775</dt></span></span> </dl> | <span data-ttu-id="b7aca-140">Значение, указанное в параметре *RequestedState* , не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b7aca-140">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="b7aca-141"><dt></dt><dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="b7aca-141"><dt></dt> <dt>32776</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="b7aca-142"><dt></dt><dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="b7aca-142"><dt></dt> <dt>32777</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="b7aca-143"><dt></dt><dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="b7aca-143"><dt></dt> <dt>32778</dt></span></span> </dl> |                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="b7aca-144">Требования</span><span class="sxs-lookup"><span data-stu-id="b7aca-144">Requirements</span></span>



| <span data-ttu-id="b7aca-145">Требование</span><span class="sxs-lookup"><span data-stu-id="b7aca-145">Requirement</span></span> | <span data-ttu-id="b7aca-146">Значение</span><span class="sxs-lookup"><span data-stu-id="b7aca-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7aca-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7aca-147">Minimum supported client</span></span><br/> | <span data-ttu-id="b7aca-148">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b7aca-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b7aca-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7aca-149">Minimum supported server</span></span><br/> | <span data-ttu-id="b7aca-150">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b7aca-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b7aca-151">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b7aca-151">Namespace</span></span><br/>                | <span data-ttu-id="b7aca-152">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="b7aca-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b7aca-153">MOF</span><span class="sxs-lookup"><span data-stu-id="b7aca-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7aca-154"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7aca-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7aca-155">DLL</span><span class="sxs-lookup"><span data-stu-id="b7aca-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7aca-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b7aca-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b7aca-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7aca-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7aca-158">**Мсвм \_ планнедкомпутерсистем**</span><span class="sxs-lookup"><span data-stu-id="b7aca-158">**Msvm\_PlannedComputerSystem**</span></span>](msvm-plannedcomputersystem.md)
</dt> </dl>

 

 




