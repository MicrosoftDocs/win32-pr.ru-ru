---
title: Метод Верифихеалсмесод класса MDM_HealthAttestation
description: Способ уведомления устройства о подготовке запроса на проверку сертификата работоспособности. См. также Верифихеалс.
ms.assetid: f5b11081-c664-4525-8f36-5f17c21e7f22
keywords:
- Метод Верифихеалсмесод
- Метод Верифихеалсмесод, класс MDM_HealthAttestation
- Класс MDM_HealthAttestation, метод Верифихеалсмесод
topic_type:
- apiref
api_name:
- MDM_HealthAttestation.VerifyHealthMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d90d71d3758059706d4ea598e7012433220feb27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654465"
---
# <a name="verifyhealthmethod-method-of-the-mdm_healthattestation-class"></a><span data-ttu-id="b996d-107">Метод Верифихеалсмесод \_ класса MDM хеалсаттестатион</span><span class="sxs-lookup"><span data-stu-id="b996d-107">VerifyHealthMethod method of the MDM\_HealthAttestation class</span></span>

<span data-ttu-id="b996d-108">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="b996d-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b996d-109">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="b996d-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b996d-110">Способ уведомления устройства о подготовке запроса на проверку сертификата работоспособности.</span><span class="sxs-lookup"><span data-stu-id="b996d-110">Method to notify the device to prepare a health certificate verification request.</span></span> <span data-ttu-id="b996d-111">См. также [верифихеалс](/windows/client-management/mdm/healthattestation-csp).</span><span class="sxs-lookup"><span data-stu-id="b996d-111">See also, [VerifyHealth](/windows/client-management/mdm/healthattestation-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="b996d-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b996d-112">Syntax</span></span>


```mof
uint32 VerifyHealthMethod();
```



## <a name="parameters"></a><span data-ttu-id="b996d-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="b996d-113">Parameters</span></span>

<span data-ttu-id="b996d-114">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b996d-114">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="b996d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b996d-115">Requirements</span></span>



| <span data-ttu-id="b996d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b996d-116">Requirement</span></span> | <span data-ttu-id="b996d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b996d-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b996d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b996d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b996d-119">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b996d-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b996d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b996d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b996d-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b996d-121">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b996d-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b996d-122">Namespace</span></span><br/>                | <span data-ttu-id="b996d-123">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="b996d-123">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b996d-124">MOF</span><span class="sxs-lookup"><span data-stu-id="b996d-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b996d-125"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b996d-125"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b996d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b996d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b996d-127"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b996d-127"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b996d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b996d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b996d-129">**\_ХЕАЛСАТТЕСТАТИОН MDM**</span><span class="sxs-lookup"><span data-stu-id="b996d-129">**MDM\_HealthAttestation**</span></span>](mdm-healthattestation.md)
</dt> <dt>

[<span data-ttu-id="b996d-130">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="b996d-130">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

