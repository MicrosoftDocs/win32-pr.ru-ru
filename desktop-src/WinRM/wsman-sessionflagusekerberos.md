---
title: Метод WSMan. Сессионфлагусекерберос (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлагусекерберос для использования в параметре Flags WSMan. CreateSession.
ms.assetid: be005312-1e87-4371-9791-709a9be46f7c
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Сессионфлагусекерберос
- Служба удаленного управления Windows метода Сессионфлагусекерберос, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Сессионфлагусекерберос
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseKerberos
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e7436a5b79480b39c093545a0b579da3d13082
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802363"
---
# <a name="wsmansessionflagusekerberos-method"></a><span data-ttu-id="ece1d-106">Метод WSMan. Сессионфлагусекерберос</span><span class="sxs-lookup"><span data-stu-id="ece1d-106">WSMan.SessionFlagUseKerberos method</span></span>

<span data-ttu-id="ece1d-107">Метод **WSMan. сессионфлагусекерберос** возвращает значение флага проверки подлинности **всманфлагусекерберос** для использования в параметре *flags* [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="ece1d-107">The **WSMan.SessionFlagUseKerberos** method returns the value of the **WSManFlagUseKerberos** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="ece1d-108">Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение.</span><span class="sxs-lookup"><span data-stu-id="ece1d-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="ece1d-109">Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ece1d-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="ece1d-110">**Всманфлагусекерберос** — это константа в перечислении **\_ \_ всмансессионфлагс** .</span><span class="sxs-lookup"><span data-stu-id="ece1d-110">**WSManFlagUseKerberos** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="ece1d-111">Дополнительные сведения см. в разделе [константы проверки подлинности](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ece1d-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ece1d-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ece1d-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseKerberos( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="ece1d-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="ece1d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ece1d-114">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ece1d-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ece1d-115">Значение константы.</span><span class="sxs-lookup"><span data-stu-id="ece1d-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ece1d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ece1d-116">Return value</span></span>

<span data-ttu-id="ece1d-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="ece1d-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ece1d-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ece1d-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ece1d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ece1d-119">Requirements</span></span>



| <span data-ttu-id="ece1d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ece1d-120">Requirement</span></span> | <span data-ttu-id="ece1d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ece1d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece1d-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ece1d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ece1d-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ece1d-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="ece1d-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ece1d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ece1d-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ece1d-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ece1d-126">Header</span><span class="sxs-lookup"><span data-stu-id="ece1d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ece1d-127"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ece1d-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ece1d-128">IDL</span><span class="sxs-lookup"><span data-stu-id="ece1d-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ece1d-129"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ece1d-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="ece1d-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ece1d-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="ece1d-131"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ece1d-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ece1d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ece1d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ece1d-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ece1d-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ece1d-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ece1d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ece1d-135">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="ece1d-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="ece1d-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="ece1d-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





