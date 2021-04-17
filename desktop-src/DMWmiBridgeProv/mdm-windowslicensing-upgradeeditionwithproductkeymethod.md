---
title: Метод Упградидитионвиспродукткэймесод класса MDM_WindowsLicensing
description: Вводит ключ продукта для обновления выпусков устройств Windows 10 Desktop. См. также Упградидитионвиспродукткэй.
ms.assetid: 6576fb5c-210c-4979-8c01-ed8f78e72c2c
keywords:
- Метод Упградидитионвиспродукткэймесод
- Метод Упградидитионвиспродукткэймесод, класс MDM_WindowsLicensing
- Класс MDM_WindowsLicensing, метод Упградидитионвиспродукткэймесод
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85824fc6fac9e5a15bf2bc890215afcbd0958680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491934"
---
# <a name="upgradeeditionwithproductkeymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="29cf0-107">Метод Упградидитионвиспродукткэймесод \_ класса MDM виндовслиценсинг</span><span class="sxs-lookup"><span data-stu-id="29cf0-107">UpgradeEditionWithProductKeyMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="29cf0-108">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="29cf0-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="29cf0-109">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="29cf0-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="29cf0-110">Вводит ключ продукта для обновления выпусков устройств Windows 10 Desktop.</span><span class="sxs-lookup"><span data-stu-id="29cf0-110">Enters a product key for an edition upgrade of Windows 10 desktop devices.</span></span> <span data-ttu-id="29cf0-111">См. также [упградидитионвиспродукткэй](/windows/client-management/mdm/windowslicensing-csp).</span><span class="sxs-lookup"><span data-stu-id="29cf0-111">See also, [UpgradeEditionWithProductKey](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="29cf0-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29cf0-112">Syntax</span></span>


```mof
uint32 UpgradeEditionWithProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="29cf0-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="29cf0-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29cf0-114">*параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="29cf0-114">*param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29cf0-115">Ключ продукта.</span><span class="sxs-lookup"><span data-stu-id="29cf0-115">The product key.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29cf0-116">Требования</span><span class="sxs-lookup"><span data-stu-id="29cf0-116">Requirements</span></span>



| <span data-ttu-id="29cf0-117">Требование</span><span class="sxs-lookup"><span data-stu-id="29cf0-117">Requirement</span></span> | <span data-ttu-id="29cf0-118">Значение</span><span class="sxs-lookup"><span data-stu-id="29cf0-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29cf0-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29cf0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="29cf0-120">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="29cf0-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="29cf0-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29cf0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="29cf0-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="29cf0-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="29cf0-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="29cf0-123">Namespace</span></span><br/>                | <span data-ttu-id="29cf0-124">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="29cf0-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="29cf0-125">MOF</span><span class="sxs-lookup"><span data-stu-id="29cf0-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29cf0-126"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29cf0-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="29cf0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="29cf0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29cf0-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29cf0-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29cf0-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29cf0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29cf0-130">**\_ВИНДОВСЛИЦЕНСИНГ MDM**</span><span class="sxs-lookup"><span data-stu-id="29cf0-130">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="29cf0-131">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="29cf0-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

