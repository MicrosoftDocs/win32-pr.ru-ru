---
title: Метод WSMan. Сессионфлаженаблеспнсерверпорт (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлаженаблеспнсерверпорт для использования в параметре flags метода WSMan. CreateSession.
ms.assetid: a18a87e6-dcee-4e9f-8e8c-262fef36ab1a
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Сессионфлаженаблеспнсерверпорт
- Служба удаленного управления Windows метода Сессионфлаженаблеспнсерверпорт, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Сессионфлаженаблеспнсерверпорт
topic_type:
- apiref
api_name:
- WSMan.SessionFlagEnableSPNServerPort
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4153f088079b58b3b0e048f2cd8f38b3524754a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534523"
---
# <a name="wsmansessionflagenablespnserverport-method"></a><span data-ttu-id="a8f1c-106">Метод WSMan. Сессионфлаженаблеспнсерверпорт</span><span class="sxs-lookup"><span data-stu-id="a8f1c-106">WSMan.SessionFlagEnableSPNServerPort method</span></span>

<span data-ttu-id="a8f1c-107">Метод **WSMan. сессионфлаженаблеспнсерверпорт** возвращает значение флага проверки подлинности **всманфлаженаблеспнсерверпорт** для использования в параметре *flags* метода [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="a8f1c-107">The **WSMan.SessionFlagEnableSPNServerPort** method returns the value of the authentication flag **WSManFlagEnableSPNServerPort** for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="a8f1c-108">Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение.</span><span class="sxs-lookup"><span data-stu-id="a8f1c-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="a8f1c-109">Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a8f1c-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="a8f1c-110">**Всманфлаженаблеспнсерверпорт** — это константа в перечислении **\_ \_ всмансессионфлагс** .</span><span class="sxs-lookup"><span data-stu-id="a8f1c-110">**WSManFlagEnableSPNServerPort** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="a8f1c-111">Дополнительные сведения см. в разделе [**другие константы сеанса**](other-session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a8f1c-111">For more information, see [**Other Session Constants**](other-session-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f1c-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8f1c-112">Syntax</span></span>


```VB
WSMan.SessionFlagEnableSPNServerPort( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="a8f1c-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8f1c-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8f1c-114">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a8f1c-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f1c-115">Значение константы.</span><span class="sxs-lookup"><span data-stu-id="a8f1c-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8f1c-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8f1c-116">Return value</span></span>

<span data-ttu-id="a8f1c-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a8f1c-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a8f1c-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a8f1c-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8f1c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a8f1c-119">Requirements</span></span>



| <span data-ttu-id="a8f1c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a8f1c-120">Requirement</span></span> | <span data-ttu-id="a8f1c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a8f1c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f1c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8f1c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a8f1c-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8f1c-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="a8f1c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8f1c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a8f1c-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8f1c-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a8f1c-126">Header</span><span class="sxs-lookup"><span data-stu-id="a8f1c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8f1c-127"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8f1c-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8f1c-128">IDL</span><span class="sxs-lookup"><span data-stu-id="a8f1c-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a8f1c-129"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a8f1c-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="a8f1c-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a8f1c-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="a8f1c-131"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a8f1c-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a8f1c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a8f1c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8f1c-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8f1c-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a8f1c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8f1c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f1c-135">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="a8f1c-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="a8f1c-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="a8f1c-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





