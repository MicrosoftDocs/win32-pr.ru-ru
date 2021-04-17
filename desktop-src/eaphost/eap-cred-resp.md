---
title: '\_ \_ Центр ОТВ для EAP (еаптипес. h)'
description: Хранит учетные данные безопасности EAP в \_ \_ структуре массива входных полей конфигурации EAP \_ \_ . | \_ \_ Центр ОТВ для EAP (еаптипес. h)
ms.assetid: 714c75d8-71c7-4c3f-802a-a5e4f6ca65c2
keywords:
- EAP_CRED_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c2176377dbde0f7c02d2a7d8083ad1bcff9e71
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105713361"
---
# <a name="eap_cred_resp"></a><span data-ttu-id="5eb6b-105">подотчетное от EAP \_ cred \_</span><span class="sxs-lookup"><span data-stu-id="5eb6b-105">EAP\_CRED\_RESP</span></span>

<span data-ttu-id="5eb6b-106">Структура **\_ \_ ОТВ** для удостоверения EAP хранит учетные данные безопасности EAP в структуре [**\_ \_ \_ \_ массива входных полей конфигурации EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .</span><span class="sxs-lookup"><span data-stu-id="5eb6b-106">The **EAP\_CRED\_RESP** structure stores EAP security credentials within a [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_RESP;
```



<dl> <dt>

<span data-ttu-id="5eb6b-107">**подотчетное от EAP \_ cred \_**</span><span class="sxs-lookup"><span data-stu-id="5eb6b-107">**EAP\_CRED\_RESP**</span></span>
</dt> <dd>

<span data-ttu-id="5eb6b-108">В структуре "удостоверение для удостоверения EAP" хранятся как старые, так и новые учетные данные безопасности EAP, на которые указывает параметр *пбуидата* структуры [**\_ данных интерактивного \_ пользовательского интерфейса \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , если параметр *Двдататипе* [**\_ \_ \_ \_ типа данных "интерактивный пользовательский интерфейс EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) " указывает тип ответа учетных данных. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="5eb6b-108">The **EAP\_CRED\_RESP** structure stores both the old and new EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential response type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5eb6b-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5eb6b-109">Remarks</span></span>

<span data-ttu-id="5eb6b-110">Структура **\_ \_ ОТВ** для идентификации EAP используется для поддержки единого входа (SSO).</span><span class="sxs-lookup"><span data-stu-id="5eb6b-110">The **EAP\_CRED\_RESP** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="5eb6b-111">Структура **\_ \_ ОТВ** для правил для EAP идентична структуре запросов на назначение [**EAP \_ \_**](eap-cred-req.md) .</span><span class="sxs-lookup"><span data-stu-id="5eb6b-111">The **EAP\_CRED\_RESP** structure is identical to the [**EAP\_CRED\_REQ**](eap-cred-req.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5eb6b-112">Требования</span><span class="sxs-lookup"><span data-stu-id="5eb6b-112">Requirements</span></span>



| <span data-ttu-id="5eb6b-113">Требование</span><span class="sxs-lookup"><span data-stu-id="5eb6b-113">Requirement</span></span> | <span data-ttu-id="5eb6b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="5eb6b-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5eb6b-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5eb6b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5eb6b-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5eb6b-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5eb6b-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5eb6b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5eb6b-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5eb6b-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5eb6b-119">Header</span><span class="sxs-lookup"><span data-stu-id="5eb6b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="5eb6b-120"><dt>Еаптипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="5eb6b-120"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eb6b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5eb6b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eb6b-122">Структуры запрашивающего сторона EAPHost</span><span class="sxs-lookup"><span data-stu-id="5eb6b-122">EAPHost Supplicant Structures</span></span>](eap-host-supplicant-structures.md)
</dt> <dt>

[<span data-ttu-id="5eb6b-123">**Заявка на для EAP \_ cred \_**</span><span class="sxs-lookup"><span data-stu-id="5eb6b-123">**EAP\_CRED\_REQ**</span></span>](eap-cred-req.md)
</dt> <dt>

[<span data-ttu-id="5eb6b-124">**запрос \_ на \_ истечение срока действия CRED EAP \_**</span><span class="sxs-lookup"><span data-stu-id="5eb6b-124">**EAP\_CRED\_EXPIRY\_REQ**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

<span data-ttu-id="5eb6b-125">[**\_отв. \_ истечение срока действия для истечения EAP \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5eb6b-125">[**EAP\_CRED\_EXPIRY\_RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5eb6b-126">**\_Интерактивные \_ данные ПОЛЬЗОВАТЕЛЬСКОГО интерфейса EAP \_**</span><span class="sxs-lookup"><span data-stu-id="5eb6b-126">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="5eb6b-127">Единый вход и PLAP</span><span class="sxs-lookup"><span data-stu-id="5eb6b-127">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

