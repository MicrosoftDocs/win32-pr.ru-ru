---
title: Метод WSMan. Сессионфлагусекредссп (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлагусекредссп для использования в параметре flags метода WSMan. CreateSession.
ms.assetid: bb167445-91d6-4e06-a976-bf869320784a
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Сессионфлагусекредссп
- Служба удаленного управления Windows метода Сессионфлагусекредссп, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Сессионфлагусекредссп
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseCredSsp
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed5dfbaba3e705f100cdd373e194174f4654a7d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490755"
---
# <a name="wsmansessionflagusecredssp-method"></a><span data-ttu-id="c316b-106">Метод WSMan. Сессионфлагусекредссп</span><span class="sxs-lookup"><span data-stu-id="c316b-106">WSMan.SessionFlagUseCredSsp method</span></span>

<span data-ttu-id="c316b-107">Возвращает значение флага проверки подлинности **всманфлагусекредссп** для использования в параметре *flags* метода [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="c316b-107">Returns the value of the **WSManFlagUseCredSsp** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="c316b-108">Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение.</span><span class="sxs-lookup"><span data-stu-id="c316b-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="c316b-109">Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c316b-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="c316b-110">**Всманфлагусекредссп** — это константа в перечислении **\_ \_ всмансессионфлагс** .</span><span class="sxs-lookup"><span data-stu-id="c316b-110">**WSManFlagUseCredSsp** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="c316b-111">Дополнительные сведения см. в разделе [константы проверки подлинности](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c316b-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c316b-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c316b-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseCredSsp( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="c316b-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="c316b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c316b-114">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c316b-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c316b-115">Значение константы.</span><span class="sxs-lookup"><span data-stu-id="c316b-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c316b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c316b-116">Return value</span></span>

<span data-ttu-id="c316b-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c316b-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c316b-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c316b-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c316b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c316b-119">Requirements</span></span>



| <span data-ttu-id="c316b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c316b-120">Requirement</span></span> | <span data-ttu-id="c316b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c316b-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c316b-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c316b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c316b-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c316b-123">Windows 7</span></span><br/>                                                                                                        |
| <span data-ttu-id="c316b-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c316b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c316b-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c316b-125">Windows Server 2008 R2</span></span><br/>                                                                                           |
| <span data-ttu-id="c316b-126">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="c316b-126">Redistributable</span></span><br/>          | <span data-ttu-id="c316b-127">Windows Management Framework на Windows Server 2008 с пакетом обновления 2 (SP2), Windows Vista с пакетом обновления 1 и Windows Vista с пакетом обновления 2</span><span class="sxs-lookup"><span data-stu-id="c316b-127">Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2</span></span><br/> |
| <span data-ttu-id="c316b-128">Header</span><span class="sxs-lookup"><span data-stu-id="c316b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c316b-129"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="c316b-129"><dt>WSManDisp.h</dt></span></span> </dl>                                      |
| <span data-ttu-id="c316b-130">IDL</span><span class="sxs-lookup"><span data-stu-id="c316b-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c316b-131"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c316b-131"><dt>WSManDisp.idl</dt></span></span> </dl>                                    |
| <span data-ttu-id="c316b-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c316b-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="c316b-133"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c316b-133"><dt>WSManDisp.tlb</dt></span></span> </dl>                                    |
| <span data-ttu-id="c316b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c316b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c316b-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c316b-135"><dt>WSMAuto.dll</dt></span></span> </dl>                                      |



## <a name="see-also"></a><span data-ttu-id="c316b-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c316b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c316b-137">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="c316b-137">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="c316b-138">**Session**</span><span class="sxs-lookup"><span data-stu-id="c316b-138">**Session**</span></span>](session.md)
</dt> </dl>

 

 





