---
title: Метод WSMan. Сессионфлагусеклиентцертификате (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлагусеклиентцертификате для использования в параметре flags метода WSMan. CreateSession.
ms.assetid: b0ec4dbb-3a98-45e8-8f6b-74b858d6c3fc
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Сессионфлагусеклиентцертификате
- Служба удаленного управления Windows метода Сессионфлагусеклиентцертификате, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Сессионфлагусеклиентцертификате
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseClientCertificate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbbcbc1a920cbd7ce2b58e29c52fc08245b8aa35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340360"
---
# <a name="wsmansessionflaguseclientcertificate-method"></a><span data-ttu-id="639fe-106">Метод WSMan. Сессионфлагусеклиентцертификате</span><span class="sxs-lookup"><span data-stu-id="639fe-106">WSMan.SessionFlagUseClientCertificate method</span></span>

<span data-ttu-id="639fe-107">Метод **WSMan. сессионфлагусеклиентцертификате** возвращает значение флага проверки подлинности **всманфлагусеклиентцертификате** для использования в параметре *flags* метода [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="639fe-107">The **WSMan.SessionFlagUseClientCertificate** method returns the value of the **WSManFlagUseClientCertificate** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="639fe-108">Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение.</span><span class="sxs-lookup"><span data-stu-id="639fe-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="639fe-109">Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="639fe-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="639fe-110">**Всманфлагусеклиентцертификате** — это константа в перечислении **\_ \_ всманаусентикатионфлагс** .</span><span class="sxs-lookup"><span data-stu-id="639fe-110">**WSManFlagUseClientCertificate** is a constant in the **\_\_WSManAuthenticationFlags** enumeration.</span></span> <span data-ttu-id="639fe-111">Дополнительные сведения см. в разделе [константы проверки подлинности](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="639fe-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="639fe-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="639fe-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseClientCertificate( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="639fe-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="639fe-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="639fe-114">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="639fe-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="639fe-115">Значение константы.</span><span class="sxs-lookup"><span data-stu-id="639fe-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="639fe-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="639fe-116">Return value</span></span>

<span data-ttu-id="639fe-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="639fe-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="639fe-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="639fe-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="639fe-119">Требования</span><span class="sxs-lookup"><span data-stu-id="639fe-119">Requirements</span></span>



| <span data-ttu-id="639fe-120">Требование</span><span class="sxs-lookup"><span data-stu-id="639fe-120">Requirement</span></span> | <span data-ttu-id="639fe-121">Значение</span><span class="sxs-lookup"><span data-stu-id="639fe-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="639fe-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="639fe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="639fe-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="639fe-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="639fe-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="639fe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="639fe-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="639fe-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="639fe-126">Header</span><span class="sxs-lookup"><span data-stu-id="639fe-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="639fe-127"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="639fe-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="639fe-128">IDL</span><span class="sxs-lookup"><span data-stu-id="639fe-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="639fe-129"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="639fe-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="639fe-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="639fe-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="639fe-131"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="639fe-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="639fe-132">DLL</span><span class="sxs-lookup"><span data-stu-id="639fe-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="639fe-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="639fe-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="639fe-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="639fe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="639fe-135">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="639fe-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="639fe-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="639fe-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





