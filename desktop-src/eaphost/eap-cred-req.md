---
title: Запрос \_ на \_ выеаптипесий EAP
description: Хранит учетные данные безопасности EAP в \_ \_ структуре массива входных полей конфигурации EAP \_ \_ . | Запрос \_ на \_ выеаптипесий EAP
ms.assetid: 537a90fc-4dd2-44d4-93da-949f31130ac4
keywords:
- EAP_CRED_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20da4e6aa8b1ab24dfd9cd791236d1f9b26304f6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694025"
---
# <a name="eap_cred_req"></a><span data-ttu-id="fd915-105">Заявка на для EAP \_ cred \_</span><span class="sxs-lookup"><span data-stu-id="fd915-105">EAP\_CRED\_REQ</span></span>

<span data-ttu-id="fd915-106">В структуре **EAP \_ cred \_ req** хранятся учетные данные безопасности EAP в структуре [**\_ \_ \_ \_ массива входных полей конфигурации EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .</span><span class="sxs-lookup"><span data-stu-id="fd915-106">The **EAP\_CRED\_REQ** structure stores EAP security credentials within a [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_REQ;
```



<dl> <dt>

<span data-ttu-id="fd915-107">**Заявка на для EAP \_ cred \_**</span><span class="sxs-lookup"><span data-stu-id="fd915-107">**EAP\_CRED\_REQ**</span></span>
</dt> <dd>

<span data-ttu-id="fd915-108">В **структуре \_ EAP CRED \_ req** хранятся как старые, так и новые УЧЕТные данные безопасности EAP, на которые указывает параметр *пбуидата* структуры [**\_ данных интерактивного \_ пользовательского интерфейса \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , если параметр *двдататипе* [**\_ \_ \_ \_ типа данных интерактивного пользовательского интерфейса EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) указывает тип запроса учетных данных.</span><span class="sxs-lookup"><span data-stu-id="fd915-108">The **EAP\_CRED\_REQ** structure stores both the old and new EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd915-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd915-109">Remarks</span></span>

<span data-ttu-id="fd915-110">Для поддержки единого входа (SSO) используется структура **EAP \_ cred \_ req** .</span><span class="sxs-lookup"><span data-stu-id="fd915-110">The **EAP\_CRED\_REQ** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="fd915-111">Структура **\_ \_ требования** к назначению EAP идентична структуре [**\_ \_ ОТВ для CRED**](eap-cred-resp.md) .</span><span class="sxs-lookup"><span data-stu-id="fd915-111">The **EAP\_CRED\_REQ** structure is identical to the [**EAP\_CRED\_RESP**](eap-cred-resp.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd915-112">Требования</span><span class="sxs-lookup"><span data-stu-id="fd915-112">Requirements</span></span>



| <span data-ttu-id="fd915-113">Требование</span><span class="sxs-lookup"><span data-stu-id="fd915-113">Requirement</span></span> | <span data-ttu-id="fd915-114">Значение</span><span class="sxs-lookup"><span data-stu-id="fd915-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd915-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd915-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fd915-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd915-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd915-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd915-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fd915-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fd915-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd915-119">Header</span><span class="sxs-lookup"><span data-stu-id="fd915-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd915-120"><dt>Еаптипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd915-120"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd915-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd915-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd915-122">Структуры запрашивающего сторона EAPHost</span><span class="sxs-lookup"><span data-stu-id="fd915-122">EAPHost Supplicant Structures</span></span>](eap-host-supplicant-structures.md)
</dt> <dt>

[<span data-ttu-id="fd915-123">**подотчетное от EAP \_ cred \_**</span><span class="sxs-lookup"><span data-stu-id="fd915-123">**EAP\_CRED\_RESP**</span></span>](eap-cred-resp.md)
</dt> <dt>

[<span data-ttu-id="fd915-124">**запрос \_ на \_ истечение срока действия CRED EAP \_**</span><span class="sxs-lookup"><span data-stu-id="fd915-124">**EAP\_CRED\_EXPIRY\_REQ**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

<span data-ttu-id="fd915-125">[**\_отв. \_ истечение срока действия для истечения EAP \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fd915-125">[**EAP\_CRED\_EXPIRY\_RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fd915-126">**\_Интерактивные \_ данные ПОЛЬЗОВАТЕЛЬСКОГО интерфейса EAP \_**</span><span class="sxs-lookup"><span data-stu-id="fd915-126">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="fd915-127">Единый вход и PLAP</span><span class="sxs-lookup"><span data-stu-id="fd915-127">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

