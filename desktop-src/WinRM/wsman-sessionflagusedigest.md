---
title: Метод WSMan. Сессионфлагуседижест (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлагуседижест для использования в параметре flags метода WSMan. CreateSession.
ms.assetid: dba2448a-4f72-4000-8687-4c1be812fc3b
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Сессионфлагуседижест
- Служба удаленного управления Windows метода Сессионфлагуседижест, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Сессионфлагуседижест
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseDigest
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4018428123443836c4f433f3e82f03a93ee9b766
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071662"
---
# <a name="wsmansessionflagusedigest-method"></a><span data-ttu-id="a1122-106">Метод WSMan. Сессионфлагуседижест</span><span class="sxs-lookup"><span data-stu-id="a1122-106">WSMan.SessionFlagUseDigest method</span></span>

<span data-ttu-id="a1122-107">Метод **WSMan. сессионфлагуседижест** возвращает значение флага проверки подлинности **всманфлагуседижест** для использования в параметре *flags* метода [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="a1122-107">The **WSMan.SessionFlagUseDigest** method returns the value of the **WSManFlagUseDigest** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="a1122-108">Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение.</span><span class="sxs-lookup"><span data-stu-id="a1122-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="a1122-109">Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a1122-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="a1122-110">**Всманфлагуседижест** — это значение в перечислении **\_ \_ всмансессионфлагс** .</span><span class="sxs-lookup"><span data-stu-id="a1122-110">**WSManFlagUseDigest** is a value in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="a1122-111">Дополнительные сведения см. в разделе [константы проверки подлинности](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a1122-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a1122-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1122-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseDigest( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="a1122-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1122-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1122-114">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a1122-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1122-115">Значение константы.</span><span class="sxs-lookup"><span data-stu-id="a1122-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1122-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1122-116">Return value</span></span>

<span data-ttu-id="a1122-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a1122-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a1122-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a1122-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1122-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a1122-119">Requirements</span></span>



| <span data-ttu-id="a1122-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a1122-120">Requirement</span></span> | <span data-ttu-id="a1122-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a1122-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1122-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1122-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a1122-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1122-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="a1122-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1122-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a1122-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1122-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a1122-126">Header</span><span class="sxs-lookup"><span data-stu-id="a1122-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1122-127"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1122-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1122-128">IDL</span><span class="sxs-lookup"><span data-stu-id="a1122-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a1122-129"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a1122-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="a1122-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a1122-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="a1122-131"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a1122-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a1122-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a1122-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1122-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1122-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a1122-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1122-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1122-135">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="a1122-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="a1122-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="a1122-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





