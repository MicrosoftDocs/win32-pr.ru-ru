---
description: Метод Сетсекуритиполици класса Msvm_SecurityService — задает предохранитель ключа для виртуальной системы.
ms.assetid: 22496fde-6298-4e9d-bd0c-135dcb4ea5a5
title: Метод Сетсекуритиполици класса Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.SetSecurityPolicy
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31b03ee8a941b0715b85f6a749c4ba59ade032f7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118732"
---
# <a name="setsecuritypolicy-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="77ada-103">Метод Сетсекуритиполици \_ класса SecurityService мсвм</span><span class="sxs-lookup"><span data-stu-id="77ada-103">SetSecurityPolicy method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="77ada-104">Задает предохранитель ключа для виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="77ada-104">Sets the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="77ada-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77ada-105">Syntax</span></span>


```mof
uint32 SetSecurityPolicy(
  [in]  string              SecuritySettingData,
  [in]  uint8               SecurityPolicy[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="77ada-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="77ada-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77ada-107">*Секуритисеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="77ada-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77ada-108">Строка содержит встроенный экземпляр класса [**мсвм \_ секуритисеттингдата**](msvm-securitysettingdata.md) , представляющий параметры безопасности виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="77ada-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="77ada-109">*SecurityPolicy* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="77ada-109">*SecurityPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77ada-110">Массив необработанных байтов, содержащий политику безопасности, которую необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="77ada-110">Raw byte array that contains the security policy to set.</span></span>

</dd> <dt>

<span data-ttu-id="77ada-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="77ada-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77ada-112">Необязательный параметр для отслеживания хода выполнения операции, который используется, если метод не может быть выполнен синхронно.</span><span class="sxs-lookup"><span data-stu-id="77ada-112">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="77ada-113">Если операция выполняется асинхронно, возвращается значение 4096.</span><span class="sxs-lookup"><span data-stu-id="77ada-113">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77ada-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77ada-114">Return value</span></span>

<span data-ttu-id="77ada-115">При успешном выполнении возвращает 0; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="77ada-115">On, success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="77ada-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="77ada-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="77ada-117">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="77ada-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="77ada-118">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="77ada-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="77ada-119">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="77ada-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="77ada-120">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="77ada-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="77ada-121">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="77ada-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="77ada-122">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="77ada-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="77ada-123">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="77ada-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="77ada-124">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="77ada-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="77ada-125">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="77ada-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="77ada-126">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="77ada-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="77ada-127">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="77ada-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="77ada-128">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="77ada-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="77ada-129">Требования</span><span class="sxs-lookup"><span data-stu-id="77ada-129">Requirements</span></span>



| <span data-ttu-id="77ada-130">Требование</span><span class="sxs-lookup"><span data-stu-id="77ada-130">Requirement</span></span> | <span data-ttu-id="77ada-131">Значение</span><span class="sxs-lookup"><span data-stu-id="77ada-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77ada-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77ada-132">Minimum supported client</span></span><br/> | <span data-ttu-id="77ada-133">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="77ada-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="77ada-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77ada-134">Minimum supported server</span></span><br/> | <span data-ttu-id="77ada-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="77ada-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="77ada-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="77ada-136">Namespace</span></span><br/>                | <span data-ttu-id="77ada-137">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="77ada-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="77ada-138">MOF</span><span class="sxs-lookup"><span data-stu-id="77ada-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77ada-139"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77ada-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="77ada-140">DLL</span><span class="sxs-lookup"><span data-stu-id="77ada-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77ada-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="77ada-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="77ada-142">См. также</span><span class="sxs-lookup"><span data-stu-id="77ada-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77ada-143">**Мсвм \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="77ada-143">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




