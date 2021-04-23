---
description: Изменяет текущие параметры безопасности виртуальной машины.
ms.assetid: b3eedab6-fd69-4c54-a8bf-4e3b77207687
title: Метод Модифисекуритисеттингс класса Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.ModifySecuritySettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4422f04be1833d66280392704630fcb670eba810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664758"
---
# <a name="modifysecuritysettings-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="22cc7-103">Метод Модифисекуритисеттингс \_ класса SecurityService мсвм</span><span class="sxs-lookup"><span data-stu-id="22cc7-103">ModifySecuritySettings method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="22cc7-104">Изменяет текущие параметры безопасности виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="22cc7-104">Modifies the current security settings of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="22cc7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22cc7-105">Syntax</span></span>


```mof
uint32 ModifySecuritySettings(
  [in]  string              SecuritySettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="22cc7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="22cc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22cc7-107">*Секуритисеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22cc7-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22cc7-108">Новые данные параметров безопасности.</span><span class="sxs-lookup"><span data-stu-id="22cc7-108">The new security setting data.</span></span>

</dd> <dt>

<span data-ttu-id="22cc7-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="22cc7-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22cc7-110">Необязательный параметр для отслеживания хода выполнения операции, который используется, если метод не может быть выполнен синхронно.</span><span class="sxs-lookup"><span data-stu-id="22cc7-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="22cc7-111">Если операция выполняется асинхронно, возвращается значение 4096.</span><span class="sxs-lookup"><span data-stu-id="22cc7-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22cc7-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22cc7-112">Return value</span></span>

<span data-ttu-id="22cc7-113">При успешном выполнении возвращает 0; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="22cc7-113">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="22cc7-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="22cc7-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="22cc7-115">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="22cc7-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="22cc7-116">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="22cc7-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22cc7-117">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="22cc7-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22cc7-118">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="22cc7-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="22cc7-119">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="22cc7-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="22cc7-120">**Несовместимые параметры** (6)</span><span class="sxs-lookup"><span data-stu-id="22cc7-120">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="22cc7-121">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="22cc7-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="22cc7-122">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="22cc7-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="22cc7-123">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="22cc7-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="22cc7-124">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="22cc7-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="22cc7-125">Требования</span><span class="sxs-lookup"><span data-stu-id="22cc7-125">Requirements</span></span>



| <span data-ttu-id="22cc7-126">Требование</span><span class="sxs-lookup"><span data-stu-id="22cc7-126">Requirement</span></span> | <span data-ttu-id="22cc7-127">Значение</span><span class="sxs-lookup"><span data-stu-id="22cc7-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22cc7-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22cc7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="22cc7-129">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="22cc7-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="22cc7-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22cc7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="22cc7-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="22cc7-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="22cc7-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="22cc7-132">Namespace</span></span><br/>                | <span data-ttu-id="22cc7-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="22cc7-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="22cc7-134">MOF</span><span class="sxs-lookup"><span data-stu-id="22cc7-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22cc7-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22cc7-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="22cc7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="22cc7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22cc7-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="22cc7-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="22cc7-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22cc7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22cc7-139">**Мсвм \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="22cc7-139">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




