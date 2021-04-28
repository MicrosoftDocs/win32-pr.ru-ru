---
description: Метод Модифисервицесеттингс класса Msvm_MetricService — изменяет данные настройки для службы.
ms.assetid: E6133DA7-A137-42FA-A523-5B93E9C6DB79
title: Метод Модифисервицесеттингс класса Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 088aec001dd63de7344256fd9e114b6ff73e4425
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112182"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="3b2ba-103">Метод Модифисервицесеттингс \_ класса Метриксервице мсвм</span><span class="sxs-lookup"><span data-stu-id="3b2ba-103">ModifyServiceSettings method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="3b2ba-104">Изменяет данные настройки для службы.</span><span class="sxs-lookup"><span data-stu-id="3b2ba-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b2ba-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b2ba-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3b2ba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b2ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b2ba-107">*SettingData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3b2ba-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b2ba-108">Содержит встроенный экземпляр класса [**мсвм \_ метриксервицесеттингдата**](msvm-metricservicesettingdata.md) , который содержит измененные данные параметров для службы.</span><span class="sxs-lookup"><span data-stu-id="3b2ba-108">Contains an embedded instance of the [**Msvm\_MetricServiceSettingData**](msvm-metricservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="3b2ba-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3b2ba-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b2ba-110">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3b2ba-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b2ba-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b2ba-111">Return value</span></span>

<span data-ttu-id="3b2ba-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3b2ba-112">This method returns one of the following values.</span></span>



| <span data-ttu-id="3b2ba-113">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="3b2ba-113">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="3b2ba-114">Описание</span><span class="sxs-lookup"><span data-stu-id="3b2ba-114">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="3b2ba-115"><dt>**Завершено без ошибки**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3b2ba-115"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="3b2ba-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="3b2ba-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="3b2ba-117"><dt>**Параметры метода проверены — задание запущено**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="3b2ba-117"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="3b2ba-118">Параметры метода проверены, задание запущено.</span><span class="sxs-lookup"><span data-stu-id="3b2ba-118">Method parameters checked, job started.</span></span><br/> |
| <dl> <span data-ttu-id="3b2ba-119"><dt>**Сбой**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="3b2ba-119"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="3b2ba-120">сбой.</span><span class="sxs-lookup"><span data-stu-id="3b2ba-120">Failed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="3b2ba-121"><dt>**Отказано в доступе**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="3b2ba-121"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          | <span data-ttu-id="3b2ba-122">Access denied. (Недопустимое значение {значение_утверждения} для утверждения {имя_утверждения}. Доступ запрещен.)</span><span class="sxs-lookup"><span data-stu-id="3b2ba-122">Access denied.</span></span><br/>                          |
| <dl> <span data-ttu-id="3b2ba-123"><dt>**Не поддерживается**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="3b2ba-123"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          | <span data-ttu-id="3b2ba-124">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3b2ba-124">Not supported.</span></span><br/>                          |
| <dl> <span data-ttu-id="3b2ba-125"><dt>**Состояние неизвестно**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="3b2ba-125"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      | <span data-ttu-id="3b2ba-126">Состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="3b2ba-126">Status is unknown.</span></span><br/>                      |
| <dl> <span data-ttu-id="3b2ba-127"><dt>**Время ожидания**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="3b2ba-127"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                | <span data-ttu-id="3b2ba-128">Время ожидания.</span><span class="sxs-lookup"><span data-stu-id="3b2ba-128">Time-out.</span></span><br/>                               |
| <dl> <span data-ttu-id="3b2ba-129"><dt>**Недопустимый параметр**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="3b2ba-129"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="3b2ba-130">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="3b2ba-130">Invalid parameter.</span></span><br/>                      |
| <dl> <span data-ttu-id="3b2ba-131"><dt>**Система используется**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="3b2ba-131"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       | <span data-ttu-id="3b2ba-132">Система используется.</span><span class="sxs-lookup"><span data-stu-id="3b2ba-132">System is in use.</span></span><br/>                       |
| <dl> <span data-ttu-id="3b2ba-133"><dt>**Недопустимое состояние для этой операции**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="3b2ba-133"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="3b2ba-134">Недопустимое состояние для этой операции.</span><span class="sxs-lookup"><span data-stu-id="3b2ba-134">Invalid state for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="3b2ba-135"><dt>**Недопустимый тип данных**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="3b2ba-135"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    | <span data-ttu-id="3b2ba-136">Неверный тип данных.</span><span class="sxs-lookup"><span data-stu-id="3b2ba-136">Incorrect data type.</span></span><br/>                    |
| <dl> <span data-ttu-id="3b2ba-137"><dt>**Система недоступна**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="3b2ba-137"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                | <span data-ttu-id="3b2ba-138">Система недоступна.</span><span class="sxs-lookup"><span data-stu-id="3b2ba-138">System is not available.</span></span><br/>                |
| <dl> <span data-ttu-id="3b2ba-139"><dt>**Недостаточно памяти**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="3b2ba-139"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          | <span data-ttu-id="3b2ba-140">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="3b2ba-140">Out of memory.</span></span><br/>                          |



 

## <a name="requirements"></a><span data-ttu-id="3b2ba-141">Требования</span><span class="sxs-lookup"><span data-stu-id="3b2ba-141">Requirements</span></span>



| <span data-ttu-id="3b2ba-142">Требование</span><span class="sxs-lookup"><span data-stu-id="3b2ba-142">Requirement</span></span> | <span data-ttu-id="3b2ba-143">Значение</span><span class="sxs-lookup"><span data-stu-id="3b2ba-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b2ba-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b2ba-144">Minimum supported client</span></span><br/> | <span data-ttu-id="3b2ba-145">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3b2ba-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3b2ba-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b2ba-146">Minimum supported server</span></span><br/> | <span data-ttu-id="3b2ba-147">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3b2ba-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3b2ba-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3b2ba-148">Namespace</span></span><br/>                | <span data-ttu-id="3b2ba-149">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3b2ba-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3b2ba-150">MOF</span><span class="sxs-lookup"><span data-stu-id="3b2ba-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b2ba-151"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b2ba-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b2ba-152">DLL</span><span class="sxs-lookup"><span data-stu-id="3b2ba-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b2ba-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3b2ba-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3b2ba-154">См. также</span><span class="sxs-lookup"><span data-stu-id="3b2ba-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b2ba-155">**Мсвм \_ метриксервице**</span><span class="sxs-lookup"><span data-stu-id="3b2ba-155">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

