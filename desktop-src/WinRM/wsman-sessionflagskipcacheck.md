---
title: Метод WSMan. Сессионфлагскипкачекк (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлагскипкачекк для использования в параметре Flags WSMan. CreateSession.
ms.assetid: a67cadb3-c20a-4a58-a13b-5bbd23c547d1
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Сессионфлагскипкачекк
- Служба удаленного управления Windows метода Сессионфлагскипкачекк, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Сессионфлагскипкачекк
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCACheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e536112b16ad8cbab3cebb2de582a2e0ea8aec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071132"
---
# <a name="wsmansessionflagskipcacheck-method"></a><span data-ttu-id="8d8b7-106">Метод WSMan. Сессионфлагскипкачекк</span><span class="sxs-lookup"><span data-stu-id="8d8b7-106">WSMan.SessionFlagSkipCACheck method</span></span>

<span data-ttu-id="8d8b7-107">Метод **WSMan. сессионфлагскипкачекк** возвращает значение флага проверки подлинности **всманфлагскипкачекк** для использования в параметре *flags* [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="8d8b7-107">The **WSMan.SessionFlagSkipCACheck** method returns the value of the **WSManFlagSkipCACheck** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="8d8b7-108">Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение.</span><span class="sxs-lookup"><span data-stu-id="8d8b7-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="8d8b7-109">Дополнительные сведения о том, как вызывать этот метод и примеры кода, см. в разделе [константы сеанса](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8d8b7-109">For more information about how to call this method and code examples, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="8d8b7-110">**Всманфлагскипкачекк** — это константа в перечислении **\_ \_ всмансессионфлагс** .</span><span class="sxs-lookup"><span data-stu-id="8d8b7-110">**WSManFlagSkipCACheck** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="8d8b7-111">Дополнительные сведения см. в разделе [**константы проверки подлинности**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8d8b7-111">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d8b7-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d8b7-112">Syntax</span></span>


```VB
WSMan.SessionFlagSkipCACheck( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="8d8b7-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d8b7-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d8b7-114">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8d8b7-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d8b7-115">Значение константы.</span><span class="sxs-lookup"><span data-stu-id="8d8b7-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d8b7-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d8b7-116">Return value</span></span>

<span data-ttu-id="8d8b7-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="8d8b7-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8d8b7-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8d8b7-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d8b7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8d8b7-119">Requirements</span></span>



| <span data-ttu-id="8d8b7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8d8b7-120">Requirement</span></span> | <span data-ttu-id="8d8b7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8d8b7-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d8b7-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d8b7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8d8b7-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d8b7-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="8d8b7-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d8b7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8d8b7-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d8b7-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="8d8b7-126">Header</span><span class="sxs-lookup"><span data-stu-id="8d8b7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d8b7-127"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d8b7-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d8b7-128">IDL</span><span class="sxs-lookup"><span data-stu-id="8d8b7-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8d8b7-129"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8d8b7-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="8d8b7-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8d8b7-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="8d8b7-131"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8d8b7-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8d8b7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8d8b7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d8b7-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d8b7-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8d8b7-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d8b7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d8b7-135">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="8d8b7-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="8d8b7-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="8d8b7-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





