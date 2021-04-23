---
title: Метод Чеккаппликабилитимесод класса MDM_WindowsLicensing
description: Проверяет, может ли указанный ключ продукта использоваться для обновления выпуска, активации или изменения ключа продукта Windows 10 для настольных устройств. См. также Чеккаппликабилити.
ms.assetid: b28ea397-72dd-4c10-a9fb-53087c3b654c
keywords:
- Метод Чеккаппликабилитимесод
- Метод Чеккаппликабилитимесод, класс MDM_WindowsLicensing
- Класс MDM_WindowsLicensing, метод Чеккаппликабилитимесод
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.CheckApplicabilityMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eae08c4a13d036a7d1185a3d53dee846ea460e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136739"
---
# <a name="checkapplicabilitymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="7d61e-107">Метод Чеккаппликабилитимесод \_ класса MDM виндовслиценсинг</span><span class="sxs-lookup"><span data-stu-id="7d61e-107">CheckApplicabilityMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="7d61e-108">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="7d61e-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7d61e-109">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="7d61e-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7d61e-110">Проверяет, может ли указанный ключ продукта использоваться для обновления выпуска, активации или изменения ключа продукта Windows 10 для настольных устройств.</span><span class="sxs-lookup"><span data-stu-id="7d61e-110">Checks if the entered product key can be used for an edition upgrade, activation or changing a product key of Windows 10 for desktop devices.</span></span> <span data-ttu-id="7d61e-111">См. также [чеккаппликабилити](/windows/client-management/mdm/windowslicensing-csp).</span><span class="sxs-lookup"><span data-stu-id="7d61e-111">See also, [CheckApplicability](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="7d61e-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d61e-112">Syntax</span></span>


```mof
uint32 CheckApplicabilityMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="7d61e-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d61e-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d61e-114">*параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7d61e-114">*param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d61e-115">Ключ продукта.</span><span class="sxs-lookup"><span data-stu-id="7d61e-115">The product key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d61e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d61e-116">Return value</span></span>

<span data-ttu-id="7d61e-117">TRUE или FALSE</span><span class="sxs-lookup"><span data-stu-id="7d61e-117">TRUE or FALSE</span></span>

## <a name="requirements"></a><span data-ttu-id="7d61e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7d61e-118">Requirements</span></span>



| <span data-ttu-id="7d61e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7d61e-119">Requirement</span></span> | <span data-ttu-id="7d61e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7d61e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d61e-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d61e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7d61e-122">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7d61e-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7d61e-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d61e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7d61e-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7d61e-124">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7d61e-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7d61e-125">Namespace</span></span><br/>                | <span data-ttu-id="7d61e-126">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="7d61e-126">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7d61e-127">MOF</span><span class="sxs-lookup"><span data-stu-id="7d61e-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d61e-128"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d61e-128"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d61e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7d61e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d61e-130"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d61e-130"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d61e-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d61e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d61e-132">**\_ВИНДОВСЛИЦЕНСИНГ MDM**</span><span class="sxs-lookup"><span data-stu-id="7d61e-132">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="7d61e-133">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="7d61e-133">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

