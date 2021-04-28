---
description: Метод Сеткэйпротектор класса Msvm_SecurityService — задает предохранитель ключа для виртуальной системы.
ms.assetid: 84c114cb-a3a0-44f2-b862-38b05b96bd46
title: Метод Сеткэйпротектор класса Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.SetKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3b5eca7ddcc506d158175782e3e13796e56de267
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111412"
---
# <a name="setkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="dc6c3-103">Метод Сеткэйпротектор \_ класса SecurityService мсвм</span><span class="sxs-lookup"><span data-stu-id="dc6c3-103">SetKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="dc6c3-104">Задает предохранитель ключа для виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="dc6c3-104">Sets the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc6c3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc6c3-105">Syntax</span></span>


```mof
uint32 SetKeyProtector(
  [in]  string              SecuritySettingData,
  [in]  uint8               KeyProtector[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="dc6c3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc6c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc6c3-107">*Секуритисеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc6c3-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc6c3-108">Строка содержит встроенный экземпляр класса [**мсвм \_ секуритисеттингдата**](msvm-securitysettingdata.md) , представляющий параметры безопасности виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="dc6c3-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="dc6c3-109">*Кэйпротектор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc6c3-109">*KeyProtector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc6c3-110">Массив необработанных байтов, содержащий предохранитель ключа, который необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="dc6c3-110">Raw byte array that contains the key protector to set.</span></span>

</dd> <dt>

<span data-ttu-id="dc6c3-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dc6c3-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc6c3-112">Необязательный параметр для отслеживания хода выполнения операции, который используется, если метод не может быть выполнен синхронно.</span><span class="sxs-lookup"><span data-stu-id="dc6c3-112">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="dc6c3-113">Если операция выполняется асинхронно, возвращается значение 4096.</span><span class="sxs-lookup"><span data-stu-id="dc6c3-113">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc6c3-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc6c3-114">Return value</span></span>

<span data-ttu-id="dc6c3-115">При успешном выполнении возвращает 0 или 4096; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="dc6c3-115">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="dc6c3-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="dc6c3-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dc6c3-117">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="dc6c3-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="dc6c3-118">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="dc6c3-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="dc6c3-119">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="dc6c3-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="dc6c3-120">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="dc6c3-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="dc6c3-121">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="dc6c3-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="dc6c3-122">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="dc6c3-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="dc6c3-123">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="dc6c3-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="dc6c3-124">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="dc6c3-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="dc6c3-125">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="dc6c3-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="dc6c3-126">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="dc6c3-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="dc6c3-127">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="dc6c3-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="dc6c3-128">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="dc6c3-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dc6c3-129">Требования</span><span class="sxs-lookup"><span data-stu-id="dc6c3-129">Requirements</span></span>



| <span data-ttu-id="dc6c3-130">Требование</span><span class="sxs-lookup"><span data-stu-id="dc6c3-130">Requirement</span></span> | <span data-ttu-id="dc6c3-131">Значение</span><span class="sxs-lookup"><span data-stu-id="dc6c3-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc6c3-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc6c3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="dc6c3-133">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="dc6c3-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dc6c3-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc6c3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="dc6c3-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="dc6c3-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="dc6c3-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dc6c3-136">Namespace</span></span><br/>                | <span data-ttu-id="dc6c3-137">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="dc6c3-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dc6c3-138">MOF</span><span class="sxs-lookup"><span data-stu-id="dc6c3-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc6c3-139"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc6c3-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc6c3-140">DLL</span><span class="sxs-lookup"><span data-stu-id="dc6c3-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc6c3-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dc6c3-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dc6c3-142">См. также</span><span class="sxs-lookup"><span data-stu-id="dc6c3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc6c3-143">**Мсвм \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="dc6c3-143">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




