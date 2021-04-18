---
title: Итсремотепрограм Ремотепрограммоде, свойство
description: Режим Windows Server 2008 R2 RemoteApp.
ms.assetid: 9ebdf966-db9c-4a14-8469-f8b153c6ea78
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Ремотепрограммоде
- Службы удаленных рабочих столов свойства Ремотепрограммоде, интерфейс Итсремотепрограм
- Службы удаленных рабочих столов интерфейса Итсремотепрограм, свойство Ремотепрограммоде
- Службы удаленных рабочих столов свойства Ремотепрограммоде, интерфейс ITSRemoteProgram2
- Службы удаленных рабочих столов интерфейса ITSRemoteProgram2, свойство Ремотепрограммоде
- Службы удаленных рабочих столов свойства Ремотепрограммоде, интерфейс ITSRemoteProgram3
- Службы удаленных рабочих столов интерфейса ITSRemoteProgram3, свойство Ремотепрограммоде
topic_type:
- apiref
api_name:
- ITSRemoteProgram.RemoteProgramMode
- ITSRemoteProgram.get_RemoteProgramMode
- ITSRemoteProgram.put_RemoteProgramMode
- ITSRemoteProgram2.RemoteProgramMode
- ITSRemoteProgram2.get_RemoteProgramMode
- ITSRemoteProgram2.put_RemoteProgramMode
- ITSRemoteProgram3.RemoteProgramMode
- ITSRemoteProgram3.get_RemoteProgramMode
- ITSRemoteProgram3.put_RemoteProgramMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8582824e2f6349e37b125ffd974847b602ad6fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681922"
---
# <a name="itsremoteprogramremoteprogrammode-property"></a><span data-ttu-id="f770e-110">Свойство Итсремотепрограм:: Ремотепрограммоде</span><span class="sxs-lookup"><span data-stu-id="f770e-110">ITSRemoteProgram::RemoteProgramMode property</span></span>

<span data-ttu-id="f770e-111">Режим Windows Server 2008 R2 RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="f770e-111">The Windows Server 2008 R2 RemoteApp mode.</span></span>

<span data-ttu-id="f770e-112">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f770e-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f770e-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f770e-113">Syntax</span></span>


```C++
HRESULT put_RemoteProgramMode(
  [in]  VARIANT_BOOL vboolRemoteProgramMode
);

HRESULT get_RemoteProgramMode(
  [out] VARIANT_BOOL *pvboolRemoteProgramMode
);
```



## <a name="property-value"></a><span data-ttu-id="f770e-114">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f770e-114">Property value</span></span>

<span data-ttu-id="f770e-115">Режим RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="f770e-115">The RemoteApp mode.</span></span> <span data-ttu-id="f770e-116">Если задано **значение \_ true**, режим RemoteApp включен, а удаленный сеанс будет размещать программы RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="f770e-116">If set to **VARIANT\_TRUE**, RemoteApp mode is enabled, and the remote session will host RemoteApp programs.</span></span> <span data-ttu-id="f770e-117">Если задано значение " **Variant \_ false** " (по умолчанию), режим RemoteApp не включен.</span><span class="sxs-lookup"><span data-stu-id="f770e-117">If set to **VARIANT\_FALSE** (the default), RemoteApp mode is not enabled.</span></span> <span data-ttu-id="f770e-118">В удаленном сеансе будет размещен удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="f770e-118">The remote session will host a remote desktop.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f770e-119">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="f770e-119">Error codes</span></span>

<span data-ttu-id="f770e-120">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="f770e-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="f770e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f770e-121">Requirements</span></span>



| <span data-ttu-id="f770e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f770e-122">Requirement</span></span> | <span data-ttu-id="f770e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f770e-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f770e-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f770e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f770e-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f770e-125">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f770e-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f770e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f770e-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f770e-127">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f770e-128">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f770e-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="f770e-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f770e-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f770e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f770e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f770e-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f770e-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f770e-132">IID</span><span class="sxs-lookup"><span data-stu-id="f770e-132">IID</span></span><br/>                      | <span data-ttu-id="f770e-133">IID \_ итсремотепрограм определен как FDD029F9-467A-4c49-8529-64B521DBD1B4</span><span class="sxs-lookup"><span data-stu-id="f770e-133">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="f770e-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f770e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f770e-135">**ITSRemoteProgram2**</span><span class="sxs-lookup"><span data-stu-id="f770e-135">**ITSRemoteProgram2**</span></span>](itsremoteprogram2.md)
</dt> <dt>

[<span data-ttu-id="f770e-136">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="f770e-136">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> <dt>

[<span data-ttu-id="f770e-137">**итсремотепрограм**</span><span class="sxs-lookup"><span data-stu-id="f770e-137">**ITSRemoteProgram**</span></span>](itsremoteprogram.md)
</dt> </dl>

 

 





