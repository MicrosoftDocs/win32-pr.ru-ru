---
title: Имсрдпклиенттранспортсеттингс Гатевайусерселектедкредссаурце, свойство
description: Задает или получает указанный пользователем источник учетных данных шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 0c12ddf6-52c2-40a2-af2b-effd4e8bbdb6
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайусерселектедкредссаурце
- Службы удаленных рабочих столов свойства Гатевайусерселектедкредссаурце, интерфейс Имсрдпклиенттранспортсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиенттранспортсеттингс, свойство Гатевайусерселектедкредссаурце
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.get_GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.put_GatewayUserSelectedCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1556088e62221df7ff91b4b0069bb1ec938ebf23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533875"
---
# <a name="imsrdpclienttransportsettingsgatewayuserselectedcredssource-property"></a><span data-ttu-id="a4b70-106">Свойство Имсрдпклиенттранспортсеттингс:: Гатевайусерселектедкредссаурце</span><span class="sxs-lookup"><span data-stu-id="a4b70-106">IMsRdpClientTransportSettings::GatewayUserSelectedCredsSource property</span></span>

<span data-ttu-id="a4b70-107">Задает или получает указанный пользователем источник учетных данных шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="a4b70-107">Sets or retrieves the user-specified Remote Desktop Gateway (RD Gateway) credential source.</span></span>

<span data-ttu-id="a4b70-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a4b70-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b70-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4b70-109">Syntax</span></span>


```C++
HRESULT put_GatewayUserSelectedCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayUserSelectedCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a><span data-ttu-id="a4b70-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a4b70-110">Property value</span></span>

<span data-ttu-id="a4b70-111">Переменная **ulong** , указывающая метод проверки подлинности шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="a4b70-111">A **ULONG** variable that specifies the RD Gateway authentication method.</span></span> <span data-ttu-id="a4b70-112">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="a4b70-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>

<span data-ttu-id="a4b70-113"><span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**Таймер TSC \_ \_ \_ \_ Усерпасс режима учетных в прокси-сервере** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="a4b70-113"><span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**TSC\_PROXY\_CREDS\_MODE\_USERPASS** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="a4b70-114">Используйте пароль (NTLM) в качестве метода проверки подлинности для шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="a4b70-114">Use a password (NTLM) as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>

<span data-ttu-id="a4b70-115"><span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**Таймер TSC \_ \_ \_ \_ Смарт-прокси режим учетных записи** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="a4b70-115"><span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**TSC\_PROXY\_CREDS\_MODE\_SMARTCARD** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="a4b70-116">Используйте смарт-карту в качестве метода проверки подлинности для шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="a4b70-116">Use a smart card as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>

<span data-ttu-id="a4b70-117"><span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**Таймер TSC \_ Режим учетных и прокси-серверов \_ \_ \_** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="a4b70-117"><span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**TSC\_PROXY\_CREDS\_MODE\_ANY** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="a4b70-118">Используйте любой метод проверки подлинности для шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="a4b70-118">Use any authentication method for RD Gateway.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="a4b70-119">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="a4b70-119">Error codes</span></span>

<span data-ttu-id="a4b70-120">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="a4b70-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b70-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a4b70-121">Requirements</span></span>



| <span data-ttu-id="a4b70-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a4b70-122">Requirement</span></span> | <span data-ttu-id="a4b70-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a4b70-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b70-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4b70-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a4b70-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4b70-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="a4b70-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4b70-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a4b70-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4b70-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="a4b70-128">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a4b70-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="a4b70-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4b70-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a4b70-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a4b70-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4b70-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4b70-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a4b70-132">IID</span><span class="sxs-lookup"><span data-stu-id="a4b70-132">IID</span></span><br/>                      | <span data-ttu-id="a4b70-133">IID \_ имсрдпклиенттранспортсеттингс определен как 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="a4b70-133">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a4b70-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4b70-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4b70-135">**имсрдпклиенттранспортсеттингс**</span><span class="sxs-lookup"><span data-stu-id="a4b70-135">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





