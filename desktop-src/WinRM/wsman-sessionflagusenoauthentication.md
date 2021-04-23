---
title: Метод WSMan. Сессионфлагусеноаусентикатион (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлагусеноаусентикатион для использования в параметре flags метода WSMan. CreateSession.
ms.assetid: 22a8107a-8e5e-4636-bf7d-a261f885e074
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Сессионфлагусеноаусентикатион
- Служба удаленного управления Windows метода Сессионфлагусеноаусентикатион, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Сессионфлагусеноаусентикатион
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseNoAuthentication
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9676d3baa9a18ae8a3feb5eb4092c63586a94b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492669"
---
# <a name="wsmansessionflagusenoauthentication-method"></a><span data-ttu-id="c91d4-106">Метод WSMan. Сессионфлагусеноаусентикатион</span><span class="sxs-lookup"><span data-stu-id="c91d4-106">WSMan.SessionFlagUseNoAuthentication method</span></span>

<span data-ttu-id="c91d4-107">Метод **WSMan. сессионфлагусеноаусентикатион** возвращает значение флага проверки подлинности **всманфлагусеноаусентикатион** для использования в параметре *flags* метода [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="c91d4-107">The **WSMan.SessionFlagUseNoAuthentication** method returns the value of the **WSManFlagUseNoAuthentication** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="c91d4-108">Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение.</span><span class="sxs-lookup"><span data-stu-id="c91d4-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="c91d4-109">Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c91d4-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="c91d4-110">**Всманфлагусеноаусентикатион** — это константа в перечислении **\_ \_ всмансессионфлагс** .</span><span class="sxs-lookup"><span data-stu-id="c91d4-110">**WSManFlagUseNoAuthentication** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="c91d4-111">Дополнительные сведения см. в разделе[константы проверки подлинности](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c91d4-111">For more information, see //[Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c91d4-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c91d4-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseNoAuthentication( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="c91d4-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="c91d4-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c91d4-114">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c91d4-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c91d4-115">Значение константы.</span><span class="sxs-lookup"><span data-stu-id="c91d4-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c91d4-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c91d4-116">Return value</span></span>

<span data-ttu-id="c91d4-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c91d4-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c91d4-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c91d4-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c91d4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c91d4-119">Requirements</span></span>



| <span data-ttu-id="c91d4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c91d4-120">Requirement</span></span> | <span data-ttu-id="c91d4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c91d4-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c91d4-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c91d4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c91d4-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c91d4-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c91d4-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c91d4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c91d4-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c91d4-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c91d4-126">Header</span><span class="sxs-lookup"><span data-stu-id="c91d4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c91d4-127"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="c91d4-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c91d4-128">IDL</span><span class="sxs-lookup"><span data-stu-id="c91d4-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c91d4-129"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c91d4-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="c91d4-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c91d4-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="c91d4-131"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c91d4-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c91d4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c91d4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c91d4-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c91d4-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c91d4-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c91d4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c91d4-135">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="c91d4-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="c91d4-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="c91d4-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





