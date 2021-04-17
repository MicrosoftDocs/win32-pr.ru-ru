---
title: Метод Session. Identify (Всмандисп. h)
description: Запрашивает удаленный компьютер, чтобы определить, поддерживает ли он протокол WS-Management.
ms.assetid: b86ec9b8-8fc4-4c3e-aca7-2f7d039749df
ms.tgt_platform: multiple
keywords:
- Выявление служба удаленного управления Windows метода
- Обнаружение служба удаленного управления Windows метода, объект Session
- Объект Session служба удаленного управления Windows, метод Identify
topic_type:
- apiref
api_name:
- Session.Identify
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f1caa5b1e44e4ca65082e33bca4d045e487c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710535"
---
# <a name="sessionidentify-method"></a><span data-ttu-id="a57bb-106">Метод Session. Identify</span><span class="sxs-lookup"><span data-stu-id="a57bb-106">Session.Identify method</span></span>

<span data-ttu-id="a57bb-107">Метод **Session. Identify** запрашивает удаленный компьютер, чтобы определить, поддерживает ли он протокол WS-Management.</span><span class="sxs-lookup"><span data-stu-id="a57bb-107">The **Session.Identify** method queries a remote computer to determine if it supports the WS-Management protocol.</span></span> <span data-ttu-id="a57bb-108">Дополнительные сведения см. [в разделе Определение того, поддерживает ли удаленный компьютер протокол WS-Management](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="a57bb-108">For more information, see [Detecting Whether a Remote Computer Supports WS-Management Protocol](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a57bb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a57bb-109">Syntax</span></span>


```VB
Session.Identify( _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a57bb-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a57bb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a57bb-111">*Флаги* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="a57bb-111">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a57bb-112">Чтобы отправить запрос в режиме с проверкой подлинности, используйте константу проверки подлинности из перечисления **всмансессионфлагс** .</span><span class="sxs-lookup"><span data-stu-id="a57bb-112">To send the request in authenticated mode use authentication constant from the **WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="a57bb-113">Для отправки в режиме без проверки подлинности используйте **всманфлагусеноаусентикатион**.</span><span class="sxs-lookup"><span data-stu-id="a57bb-113">To send in unauthenticated mode, use **WSManFlagUseNoAuthentication**.</span></span> <span data-ttu-id="a57bb-114">Дополнительные сведения см. в разделе [**константы проверки подлинности**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a57bb-114">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a57bb-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a57bb-115">Return value</span></span>

<span data-ttu-id="a57bb-116">XML-строка, указывающая версию протокола WS-Management, поставщика операционной системы и, если запрос был отправлен с проверкой подлинности, версия операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a57bb-116">An XML string that specifies the WS-Management protocol version, the operating system vendor and, if the request was sent authenticated, the operating system version.</span></span>

## <a name="remarks"></a><span data-ttu-id="a57bb-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a57bb-117">Remarks</span></span>

<span data-ttu-id="a57bb-118">**Сеанс. Identify** основан на операции [протокол WS-Management](ws-management-protocol.md) , определенной как всманидентити.</span><span class="sxs-lookup"><span data-stu-id="a57bb-118">**Session.Identify** is based on the [WS-Management Protocol](ws-management-protocol.md) operation defined as wsmanIdentity.</span></span> <span data-ttu-id="a57bb-119">Это указывается в пакете SOAP следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a57bb-119">This is specified in the SOAP packet as follows:</span></span>


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



## <a name="examples"></a><span data-ttu-id="a57bb-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="a57bb-120">Examples</span></span>

<span data-ttu-id="a57bb-121">Следующий пример на языке VBScript отправляет на удаленный компьютер с именем Remote запрос на выявление запроса на проверку без проверки подлинности в том же домене.</span><span class="sxs-lookup"><span data-stu-id="a57bb-121">The following VBScript example sends an unauthenticated Identify request to the remote computer named Remote in the same domain.</span></span>


```VB
set WSMan = CreateObject("Wsman.Automation")
set Session = WSMan.CreateSession("Remote", _
  WSMan.SessionFlagUseNoAuthentication)
WScript.Echo Session.Identify
```



## <a name="requirements"></a><span data-ttu-id="a57bb-122">Требования</span><span class="sxs-lookup"><span data-stu-id="a57bb-122">Requirements</span></span>



| <span data-ttu-id="a57bb-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a57bb-123">Requirement</span></span> | <span data-ttu-id="a57bb-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a57bb-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a57bb-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a57bb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a57bb-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a57bb-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="a57bb-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a57bb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a57bb-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a57bb-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a57bb-129">Header</span><span class="sxs-lookup"><span data-stu-id="a57bb-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a57bb-130"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a57bb-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a57bb-131">IDL</span><span class="sxs-lookup"><span data-stu-id="a57bb-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a57bb-132"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a57bb-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="a57bb-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a57bb-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="a57bb-134"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a57bb-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a57bb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a57bb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a57bb-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a57bb-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a57bb-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a57bb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a57bb-138">**Session**</span><span class="sxs-lookup"><span data-stu-id="a57bb-138">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="a57bb-139">**IWSManSession:: Identify**</span><span class="sxs-lookup"><span data-stu-id="a57bb-139">**IWSManSession::Identify**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify)
</dt> <dt>

[<span data-ttu-id="a57bb-140">Протокол WS-Management</span><span class="sxs-lookup"><span data-stu-id="a57bb-140">WS-Management Protocol</span></span>](ws-management-protocol.md)
</dt> </dl>

 

 





