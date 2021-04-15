---
title: Метод Ексекутеккк класса MSAD_DomainController
description: Вызывает функцию Дсрепликаконсистенцичекк, которая вызывает средство проверки согласованности знаний (KCC) для проверки топологии репликации.
ms.assetid: 958c9a15-cde2-4c74-bd4c-c2d53551cfb0
ms.tgt_platform: multiple
keywords:
- Active Directory метода Ексекутеккк
- Active Directory метода Ексекутеккк, класс MSAD_DomainController
- Класс MSAD_DomainController Active Directory, метод Ексекутеккк
topic_type:
- apiref
api_name:
- MSAD_DomainController.ExecuteKCC
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce017f86042181d2e80ae3614e3fc1cbccc676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654555"
---
# <a name="executekcc-method-of-the-msad_domaincontroller-class"></a><span data-ttu-id="1129d-106">Метод Ексекутеккк \_ класса DOMAINCONTROLLER МСАД</span><span class="sxs-lookup"><span data-stu-id="1129d-106">ExecuteKCC method of the MSAD\_DomainController class</span></span>

<span data-ttu-id="1129d-107">Вызывает функцию [**дсрепликаконсистенцичекк**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) , которая вызывает средство проверки согласованности знаний (KCC) для проверки топологии репликации.</span><span class="sxs-lookup"><span data-stu-id="1129d-107">Calls the [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) function, which invokes the Knowledge Consistency Checker (KCC) to verify the replication topology.</span></span>

## <a name="syntax"></a><span data-ttu-id="1129d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1129d-108">Syntax</span></span>


```mof
void ExecuteKCC(
  [in] uint32 TaskID,
  [in] uint32 dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="1129d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1129d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1129d-110">*TaskId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1129d-110">*TaskID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1129d-111">Задача, которую должно выполнить KCC.</span><span class="sxs-lookup"><span data-stu-id="1129d-111">The task that the KCC should execute.</span></span> <span data-ttu-id="1129d-112">**Службы каталогов \_ В настоящее время поддерживается только \_ \_ \_ топология обновления KCC TASKID** .</span><span class="sxs-lookup"><span data-stu-id="1129d-112">**DS\_KCC\_TASKID\_UPDATE\_TOPOLOGY** is the only value that is currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="1129d-113">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1129d-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1129d-114">Набор флагов, изменяющих поведение метода **ексекутеккк** .</span><span class="sxs-lookup"><span data-stu-id="1129d-114">A set of flags that modify the behavior of the **ExecuteKCC** method.</span></span> <span data-ttu-id="1129d-115">Этот параметр может иметь значение 0 или быть сочетанием одного или нескольких из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1129d-115">This parameter can be zero or a combination of one or more of the following values.</span></span>

<dt>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>

<span data-ttu-id="1129d-116"><span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**\_флаг проверки согласованности DS, \_ \_ асинхронная \_ операция**</span><span class="sxs-lookup"><span data-stu-id="1129d-116"><span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**DS\_KCC\_FLAG\_ASYNC\_OP**</span></span>


</dt> <dd>

<span data-ttu-id="1129d-117">Задача помещается в очередь, а затем функция возвращается, не дожидаясь завершения задачи.</span><span class="sxs-lookup"><span data-stu-id="1129d-117">The task is queued and then the function returns without waiting for the task to complete.</span></span>

</dd> <dt>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>

<span data-ttu-id="1129d-118"><span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**\_флаг проверки согласованности DS в \_ \_ клапане**</span><span class="sxs-lookup"><span data-stu-id="1129d-118"><span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**DS\_KCC\_FLAG\_DAMPED**</span></span>


</dt> <dd>

<span data-ttu-id="1129d-119">Задача не будет добавлена в очередь, если в ближайшее время будет запущена другая задача из очереди.</span><span class="sxs-lookup"><span data-stu-id="1129d-119">The task will not be added to the queue if another queued task will run soon.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1129d-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1129d-120">Return value</span></span>

<span data-ttu-id="1129d-121">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1129d-121">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1129d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="1129d-122">Requirements</span></span>



| <span data-ttu-id="1129d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="1129d-123">Requirement</span></span> | <span data-ttu-id="1129d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1129d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1129d-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1129d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1129d-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1129d-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1129d-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1129d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1129d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1129d-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1129d-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1129d-129">Namespace</span></span><br/>                | <span data-ttu-id="1129d-130">Корневой \\ микрософтактиведиректори</span><span class="sxs-lookup"><span data-stu-id="1129d-130">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="1129d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="1129d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1129d-132"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1129d-132"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="1129d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1129d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1129d-134"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1129d-134"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1129d-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1129d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1129d-136">**МСАДный \_ DomainController**</span><span class="sxs-lookup"><span data-stu-id="1129d-136">**MSAD\_DomainController**</span></span>](msad-domaincontroller.md)
</dt> </dl>

 

 





