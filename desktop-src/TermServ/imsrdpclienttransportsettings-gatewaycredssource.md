---
title: Имсрдпклиенттранспортсеттингс Гатевайкредссаурце, свойство
description: Указывает или получает метод проверки подлинности шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 3b05edcb-f678-4d80-99fd-b76d27c80c68
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайкредссаурце
- Службы удаленных рабочих столов свойства Гатевайкредссаурце, интерфейс Имсрдпклиенттранспортсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиенттранспортсеттингс, свойство Гатевайкредссаурце
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayCredsSource
- IMsRdpClientTransportSettings.get_GatewayCredsSource
- IMsRdpClientTransportSettings.put_GatewayCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2771998ddc7c53d05c5d0db452f34a734a7c3e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415049"
---
# <a name="imsrdpclienttransportsettingsgatewaycredssource-property"></a><span data-ttu-id="3a5ae-106">Свойство Имсрдпклиенттранспортсеттингс:: Гатевайкредссаурце</span><span class="sxs-lookup"><span data-stu-id="3a5ae-106">IMsRdpClientTransportSettings::GatewayCredsSource property</span></span>

<span data-ttu-id="3a5ae-107">Указывает или получает метод проверки подлинности шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="3a5ae-107">Specifies or retrieves the Remote Desktop Gateway (RD Gateway) authentication method.</span></span>

<span data-ttu-id="3a5ae-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3a5ae-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a5ae-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a5ae-109">Syntax</span></span>


```C++
HRESULT put_GatewayCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a><span data-ttu-id="3a5ae-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3a5ae-110">Property value</span></span>

<span data-ttu-id="3a5ae-111">Переменная **ulong** , указывающая метод проверки подлинности шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3a5ae-111">A **ULONG** variable that specifies the RD Gateway authentication method.</span></span> <span data-ttu-id="3a5ae-112">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="3a5ae-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="3a5ae-113">\_Усерпасс режима прокси-сервера TSC \_ \_ \_ (0)</span><span class="sxs-lookup"><span data-stu-id="3a5ae-113">TSC\_PROXY\_CREDS\_MODE\_USERPASS (0)</span></span>
</dt> <dd>

<span data-ttu-id="3a5ae-114">Используйте пароль (NTLM) в качестве метода проверки подлинности для шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3a5ae-114">Use a password (NTLM) as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="3a5ae-115">\_Смарт-прокси режим учетных записи \_ \_ \_ (1)</span><span class="sxs-lookup"><span data-stu-id="3a5ae-115">TSC\_PROXY\_CREDS\_MODE\_SMARTCARD (1)</span></span>
</dt> <dd>

<span data-ttu-id="3a5ae-116">Используйте смарт-карту в качестве метода проверки подлинности для шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3a5ae-116">Use a smart card as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="3a5ae-117">В \_ режиме прокси-сервера TSC \_ \_ \_ ANY (4)</span><span class="sxs-lookup"><span data-stu-id="3a5ae-117">TSC\_PROXY\_CREDS\_MODE\_ANY (4)</span></span>
</dt> <dd>

<span data-ttu-id="3a5ae-118">Используйте любой метод проверки подлинности для шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3a5ae-118">Use any authentication method for RD Gateway.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="3a5ae-119">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="3a5ae-119">Error codes</span></span>

<span data-ttu-id="3a5ae-120">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="3a5ae-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a5ae-121">Требования</span><span class="sxs-lookup"><span data-stu-id="3a5ae-121">Requirements</span></span>



| <span data-ttu-id="3a5ae-122">Требование</span><span class="sxs-lookup"><span data-stu-id="3a5ae-122">Requirement</span></span> | <span data-ttu-id="3a5ae-123">Значение</span><span class="sxs-lookup"><span data-stu-id="3a5ae-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a5ae-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a5ae-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3a5ae-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a5ae-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="3a5ae-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a5ae-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3a5ae-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a5ae-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="3a5ae-128">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3a5ae-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="3a5ae-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a5ae-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="3a5ae-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3a5ae-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a5ae-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a5ae-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="3a5ae-132">IID</span><span class="sxs-lookup"><span data-stu-id="3a5ae-132">IID</span></span><br/>                      | <span data-ttu-id="3a5ae-133">IID \_ имсрдпклиенттранспортсеттингс определен как 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="3a5ae-133">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a5ae-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a5ae-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a5ae-135">**имсрдпклиенттранспортсеттингс**</span><span class="sxs-lookup"><span data-stu-id="3a5ae-135">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





