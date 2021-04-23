---
title: Имсрдпклиенттранспортсеттингс Гатевайдефаултусажемесод, свойство
description: Метод использования по умолчанию для шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 7014538d-550a-4246-ad32-406ef67fb112
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайдефаултусажемесод
- Службы удаленных рабочих столов свойства Гатевайдефаултусажемесод, интерфейс Имсрдпклиенттранспортсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиенттранспортсеттингс, свойство Гатевайдефаултусажемесод
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayDefaultUsageMethod
- IMsRdpClientTransportSettings.get_GatewayDefaultUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8417da30f9a692e6e233174a33f4b03682a5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681804"
---
# <a name="imsrdpclienttransportsettingsgatewaydefaultusagemethod-property"></a><span data-ttu-id="8b83e-106">Свойство Имсрдпклиенттранспортсеттингс:: Гатевайдефаултусажемесод</span><span class="sxs-lookup"><span data-stu-id="8b83e-106">IMsRdpClientTransportSettings::GatewayDefaultUsageMethod property</span></span>

<span data-ttu-id="8b83e-107">Метод использования по умолчанию для шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="8b83e-107">The default usage method for Remote Desktop Gateway (RD Gateway).</span></span>

<span data-ttu-id="8b83e-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8b83e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b83e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b83e-109">Syntax</span></span>


```C++
HRESULT get_GatewayDefaultUsageMethod(
  [out] ULONG *pulProxyDefaultUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="8b83e-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8b83e-110">Property value</span></span>

<span data-ttu-id="8b83e-111">Указатель на метод использования по умолчанию для шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="8b83e-111">A pointer to the default usage method for RD Gateway.</span></span> <span data-ttu-id="8b83e-112">Возвращает объединение пользовательских параметров, заданных параметрами SET [**\_ гатевайусажемесод ()**](imsrdpclienttransportsettings-gatewayusagemethod.md)и групповой политики.</span><span class="sxs-lookup"><span data-stu-id="8b83e-112">Returns a union of the user settings that are set by [**put\_GatewayUsageMethod()**](imsrdpclienttransportsettings-gatewayusagemethod.md), and group policy settings.</span></span> <span data-ttu-id="8b83e-113">Если параметры пользователя не были заданы методом set **\_ гатевайусажемесод ()**, **Get \_ гатевайдефаултусажемесод ()** вернет значение по умолчанию, равное **таймеру TSC для \_ \_ \_ обнаружения в режиме прокси**.</span><span class="sxs-lookup"><span data-stu-id="8b83e-113">If no user settings were set by **put\_GatewayUsageMethod()**, **get\_GatewayDefaultUsageMethod()** will return the default value of **TSC\_PROXY\_MODE\_DETECT**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8b83e-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="8b83e-114">Error codes</span></span>

<span data-ttu-id="8b83e-115">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="8b83e-115">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b83e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8b83e-116">Requirements</span></span>



| <span data-ttu-id="8b83e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8b83e-117">Requirement</span></span> | <span data-ttu-id="8b83e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8b83e-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b83e-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b83e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8b83e-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b83e-120">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="8b83e-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b83e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8b83e-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b83e-122">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="8b83e-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="8b83e-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="8b83e-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b83e-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="8b83e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8b83e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b83e-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b83e-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="8b83e-127">IID</span><span class="sxs-lookup"><span data-stu-id="8b83e-127">IID</span></span><br/>                      | <span data-ttu-id="8b83e-128">IID \_ имсрдпклиенттранспортсеттингс определен как 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="8b83e-128">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8b83e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b83e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b83e-130">**имсрдпклиенттранспортсеттингс**</span><span class="sxs-lookup"><span data-stu-id="8b83e-130">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





