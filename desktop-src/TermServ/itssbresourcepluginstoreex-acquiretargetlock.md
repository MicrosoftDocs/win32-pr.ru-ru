---
title: Итссбресаурцеплугинсторикс Аккуиретаржетлокк, метод
description: Блокирует целевой объект.
ms.assetid: 76707f1d-1f13-4d81-8954-2acf05cda2cd
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Аккуиретаржетлокк
- Службы удаленных рабочих столов метода Аккуиретаржетлокк, интерфейс Итссбресаурцеплугинсторикс
- Службы удаленных рабочих столов интерфейса Итссбресаурцеплугинсторикс, метод Аккуиретаржетлокк
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.AcquireTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c18be0a544ebcea2d2cecb40dcea3a08e4bd35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135390"
---
# <a name="itssbresourcepluginstoreexacquiretargetlock-method"></a><span data-ttu-id="27c9b-106">Метод Итссбресаурцеплугинсторикс:: Аккуиретаржетлокк</span><span class="sxs-lookup"><span data-stu-id="27c9b-106">ITsSbResourcePluginStoreEx::AcquireTargetLock method</span></span>

<span data-ttu-id="27c9b-107">Блокирует целевой объект.</span><span class="sxs-lookup"><span data-stu-id="27c9b-107">Locks a target.</span></span>

## <a name="syntax"></a><span data-ttu-id="27c9b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27c9b-108">Syntax</span></span>


```C++
HRESULT AcquireTargetLock(
  [in]  BSTR     targetName,
  [in]  DWORD    dwTimeout,
  [out] IUnknown **ppContext
);
```



## <a name="parameters"></a><span data-ttu-id="27c9b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="27c9b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27c9b-110">*TargetName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27c9b-110">*targetName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c9b-111">Имя целевого объекта для блокировки.</span><span class="sxs-lookup"><span data-stu-id="27c9b-111">The name of the target to lock.</span></span>

</dd> <dt>

<span data-ttu-id="27c9b-112">*двтимеаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27c9b-112">*dwTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c9b-113">Время ожидания для операции в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="27c9b-113">The timeout for the operation, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="27c9b-114">*ппконтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="27c9b-114">*ppContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27c9b-115">Возвращает указатель на контекст блокировки.</span><span class="sxs-lookup"><span data-stu-id="27c9b-115">Returns a pointer to the context of the lock.</span></span> <span data-ttu-id="27c9b-116">Чтобы снять блокировку, укажите этот указатель на метод [**релеасетаржетлокк**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) .</span><span class="sxs-lookup"><span data-stu-id="27c9b-116">To release the lock, supply this pointer to the [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27c9b-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27c9b-117">Return value</span></span>

<span data-ttu-id="27c9b-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="27c9b-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="27c9b-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="27c9b-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="27c9b-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27c9b-120">Remarks</span></span>

<span data-ttu-id="27c9b-121">После получения блокировки предполагается, что вызывающий поток имеет монопольный доступ к целевому объекту и, следовательно, ни один другой поток (на том же компьютере) не сможет его обновить.</span><span class="sxs-lookup"><span data-stu-id="27c9b-121">After the lock is acquired, the calling thread is assumed to have exclusive access to the target object and therefore no other thread (within the same machine) can update it.</span></span> <span data-ttu-id="27c9b-122">Поэтому вызывающий поток должен вызвать метод [**релеасетаржетлокк**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) , как только он внес необходимые обновления в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="27c9b-122">Therefore the calling thread must call the [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) method as soon as it has made the necessary updates to the target object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="27c9b-123">Эта блокировка не полностью мешает изменению целевых объектов извне, если в развертывании существует несколько посредников подключений.</span><span class="sxs-lookup"><span data-stu-id="27c9b-123">this lock does not completely prevent target objects from being modified externally if more than one Connection Broker exists in the deployment.</span></span> <span data-ttu-id="27c9b-124">Вызывающий поток должен быть подготовлен для корректной обработки ошибки и повторного выполнения целевого обновления.</span><span class="sxs-lookup"><span data-stu-id="27c9b-124">The calling thread must be prepared to handle a failure gracefully and retry the target update.</span></span>

 

<span data-ttu-id="27c9b-125">Этот метод доступен в Windows Server 2012 R2 с [KB3091411](https://support.microsoft.com/kb/3091411) , установленным в интерфейсе [**итссбресаурцеплугинсторикс**](itssbresourcepluginstoreex.md) .</span><span class="sxs-lookup"><span data-stu-id="27c9b-125">This method is available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="27c9b-126">Требования</span><span class="sxs-lookup"><span data-stu-id="27c9b-126">Requirements</span></span>



| <span data-ttu-id="27c9b-127">Требование</span><span class="sxs-lookup"><span data-stu-id="27c9b-127">Requirement</span></span> | <span data-ttu-id="27c9b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="27c9b-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="27c9b-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27c9b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="27c9b-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="27c9b-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="27c9b-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27c9b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="27c9b-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="27c9b-132">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="27c9b-133">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="27c9b-133">End of server support</span></span><br/>    | <span data-ttu-id="27c9b-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="27c9b-134">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="27c9b-135">IDL</span><span class="sxs-lookup"><span data-stu-id="27c9b-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="27c9b-136"><dt>Сбтсв. idl</dt></span><span class="sxs-lookup"><span data-stu-id="27c9b-136"><dt>SbTsV.idl</dt></span></span> </dl>          |
| <span data-ttu-id="27c9b-137">IID</span><span class="sxs-lookup"><span data-stu-id="27c9b-137">IID</span></span><br/>                      | <span data-ttu-id="27c9b-138">IID \_ итссбресаурцеплугинсторикс определен как 80b83ffd-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="27c9b-138">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="27c9b-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27c9b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27c9b-140">**итссбресаурцеплугинсторикс**</span><span class="sxs-lookup"><span data-stu-id="27c9b-140">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





