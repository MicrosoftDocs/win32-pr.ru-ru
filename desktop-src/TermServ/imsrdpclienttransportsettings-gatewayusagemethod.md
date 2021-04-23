---
title: Имсрдпклиенттранспортсеттингс Гатевайусажемесод, свойство
description: Указывает, когда следует использовать сервер шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 0644c413-9ff7-42c1-a38e-e1ce546972ff
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайусажемесод
- Службы удаленных рабочих столов свойства Гатевайусажемесод, интерфейс Имсрдпклиенттранспортсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиенттранспортсеттингс, свойство Гатевайусажемесод
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUsageMethod
- IMsRdpClientTransportSettings.get_GatewayUsageMethod
- IMsRdpClientTransportSettings.put_GatewayUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f07bc10c67d01f957e588d1b50085e57b0fa10b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672544"
---
# <a name="imsrdpclienttransportsettingsgatewayusagemethod-property"></a><span data-ttu-id="47f8b-106">Свойство Имсрдпклиенттранспортсеттингс:: Гатевайусажемесод</span><span class="sxs-lookup"><span data-stu-id="47f8b-106">IMsRdpClientTransportSettings::GatewayUsageMethod property</span></span>

<span data-ttu-id="47f8b-107">Указывает, когда следует использовать сервер шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="47f8b-107">Specifies when to use a Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="47f8b-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="47f8b-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f8b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47f8b-109">Syntax</span></span>


```C++
HRESULT put_GatewayUsageMethod(
  [in]  ULONG ulProxyMethod
);

HRESULT get_GatewayUsageMethod(
  [out] ULONG *pulProxyUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="47f8b-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="47f8b-110">Property value</span></span>

<span data-ttu-id="47f8b-111">Переменная **ulong** , указывающая метод использования сервера шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="47f8b-111">A **ULONG** variable that specifies the RD Gateway server usage method.</span></span> <span data-ttu-id="47f8b-112">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="47f8b-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>

<span data-ttu-id="47f8b-113"><span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**Таймер TSC \_ \_Режим прокси \_ None \_ Direct** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="47f8b-113"><span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC\_PROXY\_MODE\_NONE\_DIRECT** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="47f8b-114">Не используйте сервер шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="47f8b-114">Do not use an RD Gateway server.</span></span> <span data-ttu-id="47f8b-115">В пользовательском интерфейсе клиента подключение к удаленному рабочему столу (RDC) флажок не **использовать сервер шлюза удаленных рабочих столов для локальных адресов** снят.</span><span class="sxs-lookup"><span data-stu-id="47f8b-115">In the Remote Desktop Connection (RDC) client UI, the **Bypass RD Gateway server for local addresses** check box is cleared.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>

<span data-ttu-id="47f8b-116"><span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**Таймер TSC \_ \_Режим прокси \_ Direct** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="47f8b-116"><span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC\_PROXY\_MODE\_DIRECT** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="47f8b-117">Всегда используйте сервер шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="47f8b-117">Always use an RD Gateway server.</span></span> <span data-ttu-id="47f8b-118">В пользовательском интерфейсе клиента RDC флажок не **использовать сервер шлюза удаленных рабочих столов для локальных адресов** снят.</span><span class="sxs-lookup"><span data-stu-id="47f8b-118">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is cleared.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>

<span data-ttu-id="47f8b-119"><span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**Таймер TSC \_ \_ \_ Обнаружение режима прокси** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="47f8b-119"><span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC\_PROXY\_MODE\_DETECT** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="47f8b-120">Используйте сервер шлюза удаленных рабочих столов, если не удается выполнить прямое подключение к серверу узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="47f8b-120">Use an RD Gateway server if a direct connection cannot be made to the RD Session Host server.</span></span> <span data-ttu-id="47f8b-121">В пользовательском интерфейсе клиента RDC установлен флажок не **использовать сервер шлюза удаленных рабочих столов для локальных адресов** .</span><span class="sxs-lookup"><span data-stu-id="47f8b-121">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is selected.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>

<span data-ttu-id="47f8b-122"><span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**Таймер TSC \_ \_Режим прокси \_ по умолчанию** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="47f8b-122"><span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC\_PROXY\_MODE\_DEFAULT** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="47f8b-123">Используйте параметры сервера шлюза удаленных рабочих столов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="47f8b-123">Use the default RD Gateway server settings.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>

<span data-ttu-id="47f8b-124"><span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**Таймер TSC \_ \_ \_ \_ Определение режима прокси-сервера** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="47f8b-124"><span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC\_PROXY\_MODE\_NONE\_DETECT** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="47f8b-125">Не используйте сервер шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="47f8b-125">Do not use an RD Gateway server.</span></span> <span data-ttu-id="47f8b-126">В пользовательском интерфейсе клиента RDC установлен флажок не **использовать сервер шлюза удаленных рабочих столов для локальных адресов** .</span><span class="sxs-lookup"><span data-stu-id="47f8b-126">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is selected.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="47f8b-127">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="47f8b-127">Error codes</span></span>

<span data-ttu-id="47f8b-128">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="47f8b-128">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="47f8b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="47f8b-129">Requirements</span></span>



| <span data-ttu-id="47f8b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="47f8b-130">Requirement</span></span> | <span data-ttu-id="47f8b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="47f8b-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47f8b-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47f8b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="47f8b-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47f8b-133">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="47f8b-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47f8b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="47f8b-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47f8b-135">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="47f8b-136">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="47f8b-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="47f8b-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47f8b-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="47f8b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="47f8b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47f8b-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47f8b-139"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="47f8b-140">IID</span><span class="sxs-lookup"><span data-stu-id="47f8b-140">IID</span></span><br/>                      | <span data-ttu-id="47f8b-141">IID \_ имсрдпклиенттранспортсеттингс определен как 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="47f8b-141">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="47f8b-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47f8b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47f8b-143">**имсрдпклиенттранспортсеттингс**</span><span class="sxs-lookup"><span data-stu-id="47f8b-143">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





