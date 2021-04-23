---
title: Подотчетное \_ \_ имя входа EAP \_ (еаптипес. h)
description: Хранит учетные данные безопасности EAP в \_ \_ структуре массива входных полей конфигурации EAP \_ \_ . | Подотчетное \_ \_ имя входа EAP \_ (еаптипес. h)
ms.assetid: 1244A40F-6999-4053-97C4-1C4FB107B2F5
keywords:
- EAP_CRED_LOGON_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1bbabc30918efaed0e286b5df231537ed5543
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694026"
---
# <a name="eap_cred_logon_resp"></a><span data-ttu-id="89a6a-105">\_ \_ центр регистрации имени для EAP \_</span><span class="sxs-lookup"><span data-stu-id="89a6a-105">EAP\_CRED\_LOGON\_RESP</span></span>

<span data-ttu-id="89a6a-106">Структура **\_ ОТВ для \_ входа \_ в систему имени EAP** ХРАНИТ учетные данные безопасности EAP в структуре [**\_ \_ \_ \_ массива входных полей конфигурации EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .</span><span class="sxs-lookup"><span data-stu-id="89a6a-106">The **EAP\_CRED\_LOGON\_RESP** structure stores EAP security credentials within a [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_RESP;
```



<dl> <dt>

<span data-ttu-id="89a6a-107">**\_ \_ центр регистрации имени для EAP \_**</span><span class="sxs-lookup"><span data-stu-id="89a6a-107">**EAP\_CRED\_LOGON\_RESP**</span></span>
</dt> <dd>

<span data-ttu-id="89a6a-108">Структура **\_ ОТВ для \_ входа \_ в систему** удостоверений EAP ХРАНИТ учетные данные безопасности EAP, на которые указывает параметр *пбуидата* структуры [**\_ \_ \_ данных интерактивного пользовательского интерфейса EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , если параметр *двдататипе* [**\_ \_ \_ \_ типа данных интерактивного пользовательского интерфейса EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) указывает тип запроса учетных данных.</span><span class="sxs-lookup"><span data-stu-id="89a6a-108">The **EAP\_CRED\_LOGON\_RESP** structure stores EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span> <span data-ttu-id="89a6a-109">Поля ввода в этой структуре будут совпадать с полями ввода, возвращаемыми функцией [**еафостпиркуерикредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span><span class="sxs-lookup"><span data-stu-id="89a6a-109">The input fields in this structure will be same as the input fields returned by [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span></span> <span data-ttu-id="89a6a-110">**Протокол EAP \_ При первом запросе учетных данных используется \_ регистрационное имя для входа \_ в систему** , а в запросе на повтор учетных данных используется [**протокол EAP \_ cred \_**](eap-cred-resp.md) .</span><span class="sxs-lookup"><span data-stu-id="89a6a-110">**EAP\_CRED\_LOGON\_RESP** is used in the initial credential request and [**EAP\_CRED\_RESP**](eap-cred-resp.md) is used in the credential retry request during an authentication.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89a6a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89a6a-111">Remarks</span></span>

<span data-ttu-id="89a6a-112">Структура **\_ ОТВ для \_ входа \_** в службу EAP используется для поддержки единого входа (SSO).</span><span class="sxs-lookup"><span data-stu-id="89a6a-112">The **EAP\_CRED\_LOGON\_RESP** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="89a6a-113">Структура **\_ ОТВ для \_ входа \_ в систему имени EAP** идентична структуре запросов на [**Вход в \_ \_ учетную \_ запись CRED**](eap-cred-logon-req.md) .</span><span class="sxs-lookup"><span data-stu-id="89a6a-113">The **EAP\_CRED\_LOGON\_RESP** structure is identical to the [**EAP\_CRED\_LOGON\_REQ**](eap-cred-logon-req.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="89a6a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="89a6a-114">Requirements</span></span>



| <span data-ttu-id="89a6a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="89a6a-115">Requirement</span></span> | <span data-ttu-id="89a6a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="89a6a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89a6a-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89a6a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="89a6a-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="89a6a-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89a6a-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89a6a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="89a6a-120">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="89a6a-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="89a6a-121">Header</span><span class="sxs-lookup"><span data-stu-id="89a6a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="89a6a-122"><dt>Еаптипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="89a6a-122"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89a6a-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89a6a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89a6a-124">**еафостпиркуерикредентиалинпутфиелдс**</span><span class="sxs-lookup"><span data-stu-id="89a6a-124">**EapHostPeerQueryCredentialInputFields**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> <dt>

[<span data-ttu-id="89a6a-125">**\_ \_ массив входных \_ полей \_ конфигурации EAP**</span><span class="sxs-lookup"><span data-stu-id="89a6a-125">**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[<span data-ttu-id="89a6a-126">**запрос \_ \_ учетного имени EAP \_**</span><span class="sxs-lookup"><span data-stu-id="89a6a-126">**EAP\_CRED\_LOGON\_REQ**</span></span>](eap-cred-logon-req.md)
</dt> <dt>

[<span data-ttu-id="89a6a-127">**\_Интерактивные \_ данные ПОЛЬЗОВАТЕЛЬСКОГО интерфейса EAP \_**</span><span class="sxs-lookup"><span data-stu-id="89a6a-127">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="89a6a-128">**\_Интерактивный \_ \_ тип данных пользовательского интерфейса \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="89a6a-128">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> </dl>

 

 





