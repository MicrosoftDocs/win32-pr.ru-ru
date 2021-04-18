---
title: Метод Инапсистемхеалсаженткаллбакк Компаресохрекуестс (Напсистемхеалсажент. h)
description: Используется агентом SHA для сравнения запросов SoH.
ms.assetid: 14ba189a-e745-44b0-b729-522087d4e08b
keywords:
- Метод Компаресохрекуестс NAP
- Метод Компаресохрекуестс NAP, интерфейс Инапсистемхеалсаженткаллбакк
- Инапсистемхеалсаженткаллбакк интерфейса NAP, метод Компаресохрекуестс
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.CompareSoHRequests
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6713f3de47cfbde6df67662f89ab3c094d0674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672695"
---
# <a name="inapsystemhealthagentcallbackcomparesohrequests-method"></a><span data-ttu-id="f62f5-106">Метод Инапсистемхеалсаженткаллбакк:: Компаресохрекуестс</span><span class="sxs-lookup"><span data-stu-id="f62f5-106">INapSystemHealthAgentCallback::CompareSoHRequests method</span></span>

> [!Note]  
> <span data-ttu-id="f62f5-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="f62f5-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f62f5-108">Метод **инапсистемхеалсаженткаллбакк:: компаресохрекуестс** используется агентом SHA для сравнения запросов SoH.</span><span class="sxs-lookup"><span data-stu-id="f62f5-108">The **INapSystemHealthAgentCallback::CompareSoHRequests** method is used by the SHA to compare SoH requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="f62f5-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f62f5-109">Syntax</span></span>


```C++
HRESULT CompareSoHRequests(
  [in]  const SoHRequest *lhs,
  [in]  const SoHRequest *rhs,
  [out]       BOOL       *isEqual
);
```



## <a name="parameters"></a><span data-ttu-id="f62f5-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f62f5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f62f5-111">*LHS* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f62f5-111">*lhs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f62f5-112">Указатель на [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) слева от операции сравнения.</span><span class="sxs-lookup"><span data-stu-id="f62f5-112">A pointer to the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the left of the comparison operation.</span></span>

</dd> <dt>

<span data-ttu-id="f62f5-113">*RHS* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f62f5-113">*rhs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f62f5-114">Указатель на [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) справа от операции сравнения.</span><span class="sxs-lookup"><span data-stu-id="f62f5-114">A pointer to the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the right of the comparison operation.</span></span>

</dd> <dt>

<span data-ttu-id="f62f5-115">не *равно* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f62f5-115">*isEqual* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f62f5-116">Указатель на **логическое** **значение true** , если *LHS* и *RHS* семантически равны, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f62f5-116">A pointer to a **BOOL** that is **TRUE** if *lhs* and *rhs* are semantically equal, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f62f5-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f62f5-117">Return value</span></span>

<span data-ttu-id="f62f5-118">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="f62f5-118">This method can return one of these values.</span></span>



| <span data-ttu-id="f62f5-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f62f5-119">Return code</span></span>                                                                               | <span data-ttu-id="f62f5-120">Описание</span><span class="sxs-lookup"><span data-stu-id="f62f5-120">Description</span></span>                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="f62f5-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f62f5-121"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="f62f5-122">Указывает на успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="f62f5-122">Indicates success.</span></span><br/>                         |
| <dl> <span data-ttu-id="f62f5-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="f62f5-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="f62f5-124">Метод не был реализован SHA.</span><span class="sxs-lookup"><span data-stu-id="f62f5-124">The method was not implemented by the SHA.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f62f5-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f62f5-125">Remarks</span></span>

<span data-ttu-id="f62f5-126">Этот метод обратного вызова объявляется системой защиты доступа к сети и реализуется модулем записи SHA.</span><span class="sxs-lookup"><span data-stu-id="f62f5-126">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="f62f5-127">SHA должен сравнить SoH и вернуть **значение true** , если SoH семантически равны.</span><span class="sxs-lookup"><span data-stu-id="f62f5-127">The SHA should compare the SoHs and return **TRUE** if the SoHs are semantically equal.</span></span> <span data-ttu-id="f62f5-128">Напажент использует эти сведения, чтобы определить, следует ли инициировать обмен SoH из-за изменения состояния клиентского компьютера.</span><span class="sxs-lookup"><span data-stu-id="f62f5-128">The NapAgent uses this information to determine if an SoH exchange should be initiated due to change of state of the client machine.</span></span>

<span data-ttu-id="f62f5-129">Если SHA поместит в свое состояние работоспособности добавочные идентификаторы или отметки времени, то SoH может быть семантически равным (т. е. они могут передать одни и те же сведения о работоспособности), но они могут быть неодинаковыми.</span><span class="sxs-lookup"><span data-stu-id="f62f5-129">If SHAs have put incremental IDs or time-stamps into their SoH, then SoHs may be semantically equal (i.e. they may convey the same health information), but they may be byte-wise unequal.</span></span> <span data-ttu-id="f62f5-130">SHA должен реализовать эту функцию, чтобы проверить семантическое равенство SoH.</span><span class="sxs-lookup"><span data-stu-id="f62f5-130">SHAs should implement this function to check for semantic equality of SoHs.</span></span>

<span data-ttu-id="f62f5-131">Если SHA не поместит какие-либо отметки времени или идентификаторы в свои SoH, они могут не реализовывать эту функцию и возвращать **E \_ нотимпл**.</span><span class="sxs-lookup"><span data-stu-id="f62f5-131">If SHAs have not put any time-stamps or Ids into their SoHs, they may choose to not implement this function and return **E\_NOTIMPL**.</span></span> <span data-ttu-id="f62f5-132">В этом случае Напажент выполняет побайтовое сравнение на [**сохрекуестс**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="f62f5-132">In this case, the NapAgent performs a byte-wise comparison on the [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="requirements"></a><span data-ttu-id="f62f5-133">Требования</span><span class="sxs-lookup"><span data-stu-id="f62f5-133">Requirements</span></span>



| <span data-ttu-id="f62f5-134">Требование</span><span class="sxs-lookup"><span data-stu-id="f62f5-134">Requirement</span></span> | <span data-ttu-id="f62f5-135">Значение</span><span class="sxs-lookup"><span data-stu-id="f62f5-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f62f5-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f62f5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f62f5-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f62f5-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f62f5-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f62f5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f62f5-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f62f5-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f62f5-140">Header</span><span class="sxs-lookup"><span data-stu-id="f62f5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f62f5-141"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="f62f5-141"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="f62f5-142">IDL</span><span class="sxs-lookup"><span data-stu-id="f62f5-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f62f5-143"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f62f5-143"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f62f5-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f62f5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f62f5-145">**инапсистемхеалсаженткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="f62f5-145">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> <dt>

[<span data-ttu-id="f62f5-146">**Состояния**</span><span class="sxs-lookup"><span data-stu-id="f62f5-146">**SoH**</span></span>](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> </dl>

 

 





