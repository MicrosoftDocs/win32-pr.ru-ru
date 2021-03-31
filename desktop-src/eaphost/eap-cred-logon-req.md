---
title: Запрос \_ \_ учетного имени EAP \_ (еаптипес. h)
description: Хранит учетные данные безопасности EAP в \_ \_ структуре массива входных полей конфигурации EAP \_ \_ .
ms.assetid: 1F1A2F77-054D-4FD2-83A5-69C3D77418B3
keywords:
- EAP_CRED_LOGON_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2af29daa9d68e4cd2dd78f101585c2fa14d25200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071392"
---
# <a name="eap_cred_logon_req"></a><span data-ttu-id="ec845-104">запрос \_ \_ учетного имени EAP \_</span><span class="sxs-lookup"><span data-stu-id="ec845-104">EAP\_CRED\_LOGON\_REQ</span></span>

<span data-ttu-id="ec845-105">В структуре **EAP \_ cred \_ logon \_ req** ХРАНЯТСЯ учетные данные безопасности EAP в структуре [**\_ \_ \_ \_ массива входных полей конфигурации EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .</span><span class="sxs-lookup"><span data-stu-id="ec845-105">The **EAP\_CRED\_LOGON\_REQ** structure stores EAP security credentials within an [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_REQ;
```



<dl> <dt>

<span data-ttu-id="ec845-106">**запрос \_ \_ учетного имени EAP \_**</span><span class="sxs-lookup"><span data-stu-id="ec845-106">**EAP\_CRED\_LOGON\_REQ**</span></span>
</dt> <dd>

<span data-ttu-id="ec845-107">В **структуре \_ \_ \_ требования к входу** для удостоверения EAP ХРАНЯТСЯ учетные данные безопасности EAP, на которые указывает параметр *пбуидата* структуры [**\_ \_ \_ данных интерактивного пользовательского интерфейса EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , если параметр *двдататипе* [**\_ \_ \_ \_ типа данных интерактивного пользовательского интерфейса EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) указывает тип запроса учетных данных.</span><span class="sxs-lookup"><span data-stu-id="ec845-107">The **EAP\_CRED\_LOGON\_REQ** structure stores EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span> <span data-ttu-id="ec845-108">Поля ввода в этой структуре совпадают с полями ввода, возвращаемыми функцией [**еафостпиркуерикредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span><span class="sxs-lookup"><span data-stu-id="ec845-108">The input fields in this structure are the same as the input fields returned by [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span></span> <span data-ttu-id="ec845-109">**Протокол EAP \_ Требование \_ к \_ входу** в учетную запись используется в первоначальном запросе Credential, и запрос на удостоверение [**EAP- \_ cred \_**](eap-cred-req.md) используется в запросе на повтор учетных данных во время проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ec845-109">**EAP\_CRED\_LOGON\_REQ** is used in the initial credential request and [**EAP\_CRED\_REQ**](eap-cred-req.md) is used in the credential retry request during an authentication.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec845-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec845-110">Remarks</span></span>

<span data-ttu-id="ec845-111">Для поддержки единого входа (SSO) используется структура **EAP \_ cred \_ logon \_ req** .</span><span class="sxs-lookup"><span data-stu-id="ec845-111">The **EAP\_CRED\_LOGON\_REQ** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="ec845-112">Структура запросов на **\_ Вход в \_ учетную \_ запись EAP-CRED** идентична структуре [**\_ \_ \_ ОТВ для входа в систему**](eap-cred-logon-resp.md) .</span><span class="sxs-lookup"><span data-stu-id="ec845-112">The **EAP\_CRED\_LOGON\_REQ** structure is identical to the [**EAP\_CRED\_LOGON\_RESP**](eap-cred-logon-resp.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec845-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ec845-113">Requirements</span></span>



| <span data-ttu-id="ec845-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ec845-114">Requirement</span></span> | <span data-ttu-id="ec845-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ec845-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec845-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec845-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ec845-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec845-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec845-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec845-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ec845-119">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ec845-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ec845-120">Header</span><span class="sxs-lookup"><span data-stu-id="ec845-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec845-121"><dt>Еаптипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec845-121"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec845-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec845-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec845-123">**\_ \_ массив входных \_ полей \_ конфигурации EAP**</span><span class="sxs-lookup"><span data-stu-id="ec845-123">**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[<span data-ttu-id="ec845-124">**Заявка на для EAP \_ cred \_**</span><span class="sxs-lookup"><span data-stu-id="ec845-124">**EAP\_CRED\_REQ**</span></span>](eap-cred-req.md)
</dt> <dt>

[<span data-ttu-id="ec845-125">**\_Интерактивные \_ данные ПОЛЬЗОВАТЕЛЬСКОГО интерфейса EAP \_**</span><span class="sxs-lookup"><span data-stu-id="ec845-125">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="ec845-126">**\_Интерактивный \_ \_ тип данных пользовательского интерфейса \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="ec845-126">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> <dt>

[<span data-ttu-id="ec845-127">**еафостпиркуерикредентиалинпутфиелдс**</span><span class="sxs-lookup"><span data-stu-id="ec845-127">**EapHostPeerQueryCredentialInputFields**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> </dl>

 

 





