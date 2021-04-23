---
title: Метод WSMan. Сессионфлагноенкриптион (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлагноенкриптион для использования в параметре flags метода WSMan. CreateSession.
ms.assetid: 15c76f0e-85ae-4ee3-bf9f-ba32195d9adc
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Сессионфлагноенкриптион
- Служба удаленного управления Windows метода Сессионфлагноенкриптион, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Сессионфлагноенкриптион
topic_type:
- apiref
api_name:
- WSMan.SessionFlagNoEncryption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4c7a85e97afd67ab6b1114248a9c4b3ee3ebbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701023"
---
# <a name="wsmansessionflagnoencryption-method"></a><span data-ttu-id="d2a47-106">Метод WSMan. Сессионфлагноенкриптион</span><span class="sxs-lookup"><span data-stu-id="d2a47-106">WSMan.SessionFlagNoEncryption method</span></span>

<span data-ttu-id="d2a47-107">Метод **WSMan. сессионфлагноенкриптион** возвращает значение флага проверки подлинности **всманфлагноенкриптион** для использования в параметре *flags* метода [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="d2a47-107">The **WSMan.SessionFlagNoEncryption** method returns the value of the **WSManFlagNoEncryption** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="d2a47-108">Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение.</span><span class="sxs-lookup"><span data-stu-id="d2a47-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="d2a47-109">Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d2a47-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="d2a47-110">**Всманфлагноенкриптион** — это константа в перечислении **\_ \_ всмансессионфлагс** .</span><span class="sxs-lookup"><span data-stu-id="d2a47-110">**WSManFlagNoEncryption** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="d2a47-111">Дополнительные сведения см. в разделе [другие константы сеанса](other-session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d2a47-111">For more information, see [Other Session Constants](other-session-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a47-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2a47-112">Syntax</span></span>


```VB
WSMan.SessionFlagNoEncryption( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="d2a47-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2a47-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a47-114">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d2a47-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a47-115">Значение константы.</span><span class="sxs-lookup"><span data-stu-id="d2a47-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2a47-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2a47-116">Return value</span></span>

<span data-ttu-id="d2a47-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d2a47-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d2a47-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d2a47-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2a47-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d2a47-119">Requirements</span></span>



| <span data-ttu-id="d2a47-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d2a47-120">Requirement</span></span> | <span data-ttu-id="d2a47-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d2a47-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a47-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2a47-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d2a47-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2a47-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="d2a47-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2a47-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d2a47-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2a47-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d2a47-126">Header</span><span class="sxs-lookup"><span data-stu-id="d2a47-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2a47-127"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2a47-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2a47-128">IDL</span><span class="sxs-lookup"><span data-stu-id="d2a47-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d2a47-129"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d2a47-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="d2a47-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d2a47-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="d2a47-131"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d2a47-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d2a47-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d2a47-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2a47-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2a47-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d2a47-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2a47-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2a47-135">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="d2a47-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="d2a47-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="d2a47-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





