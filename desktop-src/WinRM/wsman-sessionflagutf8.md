---
title: Метод WSMan. SessionFlagUTF8 (Всмандисп. h)
description: Возвращает значение флага проверки подлинности WSManFlagUTF8 для использования в параметре Flags WSMan. CreateSession.
ms.assetid: a79e292a-364b-4bf3-ae66-6a15ad51524f
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода SessionFlagUTF8
- Служба удаленного управления Windows метода SessionFlagUTF8, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод SessionFlagUTF8
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUTF8
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 985763131c2f3d4227f1a24af612ea3141237832
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803562"
---
# <a name="wsmansessionflagutf8-method"></a><span data-ttu-id="4178f-106">Метод WSMan. SessionFlagUTF8</span><span class="sxs-lookup"><span data-stu-id="4178f-106">WSMan.SessionFlagUTF8 method</span></span>

<span data-ttu-id="4178f-107">Метод **WSMan. SessionFlagUTF8** возвращает значение флага проверки подлинности **WSManFlagUTF8** для использования в параметре *flags* [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="4178f-107">The **WSMan.SessionFlagUTF8** method returns the value of the **WSManFlagUTF8** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="4178f-108">Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение.</span><span class="sxs-lookup"><span data-stu-id="4178f-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="4178f-109">Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4178f-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="4178f-110">**WSManFlagUTF8** — это константа в перечислении **\_ \_ всмансессионфлагс** .</span><span class="sxs-lookup"><span data-stu-id="4178f-110">**WSManFlagUTF8** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="4178f-111">Дополнительные сведения см. в разделе [другие константы сеанса](other-session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4178f-111">For more information, see [Other Session Constants](other-session-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4178f-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4178f-112">Syntax</span></span>


```VB
WSMan.SessionFlagUTF8( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="4178f-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="4178f-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4178f-114">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4178f-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4178f-115">Значение константы.</span><span class="sxs-lookup"><span data-stu-id="4178f-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4178f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4178f-116">Return value</span></span>

<span data-ttu-id="4178f-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4178f-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4178f-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4178f-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4178f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4178f-119">Requirements</span></span>



| <span data-ttu-id="4178f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4178f-120">Requirement</span></span> | <span data-ttu-id="4178f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4178f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4178f-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4178f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4178f-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4178f-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="4178f-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4178f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4178f-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4178f-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4178f-126">Header</span><span class="sxs-lookup"><span data-stu-id="4178f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4178f-127"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="4178f-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4178f-128">IDL</span><span class="sxs-lookup"><span data-stu-id="4178f-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4178f-129"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4178f-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="4178f-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4178f-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="4178f-131"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4178f-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4178f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4178f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4178f-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4178f-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4178f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4178f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4178f-135">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="4178f-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="4178f-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="4178f-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





