---
title: Метод WSMan. Сессионфлагкредусернамепассворд (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлагкредусернамепассворд для использования в параметре flags метода WSMan. CreateSession.
ms.assetid: 70d12df4-f0ac-499a-8b2f-6ba83b77869e
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Сессионфлагкредусернамепассворд
- Служба удаленного управления Windows метода Сессионфлагкредусернамепассворд, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Сессионфлагкредусернамепассворд
topic_type:
- apiref
api_name:
- WSMan.SessionFlagCredUsernamePassword
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84827f342f70b13f1a2f0192289b34e347f26045
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071793"
---
# <a name="wsmansessionflagcredusernamepassword-method"></a><span data-ttu-id="2d593-106">Метод WSMan. Сессионфлагкредусернамепассворд</span><span class="sxs-lookup"><span data-stu-id="2d593-106">WSMan.SessionFlagCredUsernamePassword method</span></span>

<span data-ttu-id="2d593-107">Метод **WSMan. сессионфлагкредусернамепассворд** возвращает значение флага проверки подлинности **всманфлагкредусернамепассворд** для использования в параметре *flags* метода [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="2d593-107">The **WSMan.SessionFlagCredUsernamePassword** method returns the value of the authentication flag **WSManFlagCredUsernamePassword** for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="2d593-108">Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение.</span><span class="sxs-lookup"><span data-stu-id="2d593-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="2d593-109">Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2d593-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="2d593-110">**Всманфлагкредусернамепассворд** — это константа в перечислении **\_ \_ всмансессионфлагс** .</span><span class="sxs-lookup"><span data-stu-id="2d593-110">**WSManFlagCredUsernamePassword** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="2d593-111">Дополнительные сведения см. в разделе [константы проверки подлинности](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2d593-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d593-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d593-112">Syntax</span></span>


```VB
WSMan.SessionFlagCredUsernamePassword( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="2d593-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d593-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d593-114">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2d593-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d593-115">Значение константы.</span><span class="sxs-lookup"><span data-stu-id="2d593-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d593-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d593-116">Return value</span></span>

<span data-ttu-id="2d593-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="2d593-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2d593-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2d593-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d593-119">Требования</span><span class="sxs-lookup"><span data-stu-id="2d593-119">Requirements</span></span>



| <span data-ttu-id="2d593-120">Требование</span><span class="sxs-lookup"><span data-stu-id="2d593-120">Requirement</span></span> | <span data-ttu-id="2d593-121">Значение</span><span class="sxs-lookup"><span data-stu-id="2d593-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d593-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d593-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2d593-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d593-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="2d593-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d593-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2d593-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d593-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2d593-126">Header</span><span class="sxs-lookup"><span data-stu-id="2d593-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d593-127"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d593-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d593-128">IDL</span><span class="sxs-lookup"><span data-stu-id="2d593-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2d593-129"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2d593-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="2d593-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2d593-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="2d593-131"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2d593-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2d593-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2d593-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d593-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d593-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2d593-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d593-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d593-135">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="2d593-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="2d593-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="2d593-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





