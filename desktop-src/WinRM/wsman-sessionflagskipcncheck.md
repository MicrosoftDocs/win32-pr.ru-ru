---
title: Метод WSMan. Сессионфлагскипкнчекк (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлагскипкнчекк для использования в параметре Flags WSMan. CreateSession.
ms.assetid: 44884a9d-ec5f-4822-945d-2681d214a902
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Сессионфлагскипкнчекк
- Служба удаленного управления Windows метода Сессионфлагскипкнчекк, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Сессионфлагскипкнчекк
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCNCheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c98981ac166ea7b1b76f1ab322db6c48679a4bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988931"
---
# <a name="wsmansessionflagskipcncheck-method"></a><span data-ttu-id="68f57-106">Метод WSMan. Сессионфлагскипкнчекк</span><span class="sxs-lookup"><span data-stu-id="68f57-106">WSMan.SessionFlagSkipCNCheck method</span></span>

<span data-ttu-id="68f57-107">Метод **WSMan. сессионфлагскипкнчекк** возвращает значение флага проверки подлинности **всманфлагскипкнчекк** для использования в параметре *flags* [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="68f57-107">The **WSMan.SessionFlagSkipCNCheck** method returns the value of the **WSManFlagSkipCNCheck** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="68f57-108">Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение.</span><span class="sxs-lookup"><span data-stu-id="68f57-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="68f57-109">Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="68f57-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="68f57-110">**Всманфлагскипкнчекк** — это константа в перечислении **\_ \_ всмансессионфлагс** .</span><span class="sxs-lookup"><span data-stu-id="68f57-110">**WSManFlagSkipCNCheck** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="68f57-111">Дополнительные сведения см. в разделе [**константы проверки подлинности**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="68f57-111">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="68f57-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68f57-112">Syntax</span></span>


```VB
WSMan.SessionFlagSkipCNCheck( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="68f57-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="68f57-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68f57-114">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="68f57-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68f57-115">Значение константы.</span><span class="sxs-lookup"><span data-stu-id="68f57-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68f57-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68f57-116">Return value</span></span>

<span data-ttu-id="68f57-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="68f57-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="68f57-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="68f57-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="68f57-119">Требования</span><span class="sxs-lookup"><span data-stu-id="68f57-119">Requirements</span></span>



| <span data-ttu-id="68f57-120">Требование</span><span class="sxs-lookup"><span data-stu-id="68f57-120">Requirement</span></span> | <span data-ttu-id="68f57-121">Значение</span><span class="sxs-lookup"><span data-stu-id="68f57-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="68f57-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68f57-122">Minimum supported client</span></span><br/> | <span data-ttu-id="68f57-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68f57-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="68f57-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68f57-124">Minimum supported server</span></span><br/> | <span data-ttu-id="68f57-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68f57-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="68f57-126">Header</span><span class="sxs-lookup"><span data-stu-id="68f57-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="68f57-127"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="68f57-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="68f57-128">IDL</span><span class="sxs-lookup"><span data-stu-id="68f57-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="68f57-129"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="68f57-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="68f57-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="68f57-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="68f57-131"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="68f57-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="68f57-132">DLL</span><span class="sxs-lookup"><span data-stu-id="68f57-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68f57-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68f57-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="68f57-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68f57-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68f57-135">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="68f57-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="68f57-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="68f57-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





