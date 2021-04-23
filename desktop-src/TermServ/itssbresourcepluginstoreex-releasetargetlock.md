---
title: Итссбресаурцеплугинсторикс Релеасетаржетлокк, метод
description: Снимает блокировку на целевой объект.
ms.assetid: ab2ae9f3-2d38-4b31-9889-58297c574bd4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Релеасетаржетлокк
- Службы удаленных рабочих столов метода Релеасетаржетлокк, интерфейс Итссбресаурцеплугинсторикс
- Службы удаленных рабочих столов интерфейса Итссбресаурцеплугинсторикс, метод Релеасетаржетлокк
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.ReleaseTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc34bdb27e40316ea1271bf0faa5d8c6b0abfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136311"
---
# <a name="itssbresourcepluginstoreexreleasetargetlock-method"></a><span data-ttu-id="3d3d6-106">Метод Итссбресаурцеплугинсторикс:: Релеасетаржетлокк</span><span class="sxs-lookup"><span data-stu-id="3d3d6-106">ITsSbResourcePluginStoreEx::ReleaseTargetLock method</span></span>

<span data-ttu-id="3d3d6-107">Снимает блокировку на целевой объект.</span><span class="sxs-lookup"><span data-stu-id="3d3d6-107">Releases a lock on a target.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d3d6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d3d6-108">Syntax</span></span>


```C++
HRESULT ReleaseTargetLock(
  [in] IUnknown *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="3d3d6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d3d6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d3d6-110">*пконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3d3d6-110">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d3d6-111">Указатель на контекст, возвращенный методом [**аккуиретаржетлокк**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) .</span><span class="sxs-lookup"><span data-stu-id="3d3d6-111">A pointer to the context returned by the [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d3d6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d3d6-112">Return value</span></span>

<span data-ttu-id="3d3d6-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3d3d6-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3d3d6-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3d3d6-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d3d6-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d3d6-115">Remarks</span></span>

<span data-ttu-id="3d3d6-116">Этот метод доступен только в Windows Server 2012 R2 с [KB3091411](https://support.microsoft.com/kb/3091411) , установленным в интерфейсе [**итссбресаурцеплугинсторикс**](itssbresourcepluginstoreex.md) .</span><span class="sxs-lookup"><span data-stu-id="3d3d6-116">This method is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) interface.</span></span> <span data-ttu-id="3d3d6-117">Этот метод доступен в интерфейсе [**итссбресаурцеплугинсторе**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) , начиная с Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="3d3d6-117">This method is available on the [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface starting with Windows Server 2016.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d3d6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="3d3d6-118">Requirements</span></span>



| <span data-ttu-id="3d3d6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="3d3d6-119">Requirement</span></span> | <span data-ttu-id="3d3d6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3d3d6-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d3d6-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d3d6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3d3d6-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3d3d6-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3d3d6-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d3d6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3d3d6-124">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3d3d6-124">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="3d3d6-125">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="3d3d6-125">End of server support</span></span><br/>    | <span data-ttu-id="3d3d6-126">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3d3d6-126">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="3d3d6-127">IDL</span><span class="sxs-lookup"><span data-stu-id="3d3d6-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3d3d6-128"><dt>Сбтсв. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3d3d6-128"><dt>SbTsV.idl</dt></span></span> </dl>          |
| <span data-ttu-id="3d3d6-129">IID</span><span class="sxs-lookup"><span data-stu-id="3d3d6-129">IID</span></span><br/>                      | <span data-ttu-id="3d3d6-130">IID \_ итссбресаурцеплугинсторикс определен как 80b83ffd-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="3d3d6-130">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d3d6-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d3d6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d3d6-132">**итссбресаурцеплугинсторикс**</span><span class="sxs-lookup"><span data-stu-id="3d3d6-132">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





