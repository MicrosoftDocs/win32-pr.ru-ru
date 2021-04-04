---
title: Метод Упградидитионвислиценсемесод класса MDM_WindowsLicensing
description: Способ предоставления лицензии на обновление выпуска устройств Windows 10 Mobile. См. также Упградидитионвислиценсе.
ms.assetid: 1a57fb71-eea6-41bf-bc44-6d3a816096a4
keywords:
- Метод Упградидитионвислиценсемесод
- Метод Упградидитионвислиценсемесод, класс MDM_WindowsLicensing
- Класс MDM_WindowsLicensing, метод Упградидитионвислиценсемесод
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithLicenseMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b336ee4128aa520ecd463c3607254526c7c3dc7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989042"
---
# <a name="upgradeeditionwithlicensemethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="66faa-107">Метод Упградидитионвислиценсемесод \_ класса MDM виндовслиценсинг</span><span class="sxs-lookup"><span data-stu-id="66faa-107">UpgradeEditionWithLicenseMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="66faa-108">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="66faa-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="66faa-109">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="66faa-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="66faa-110">Способ предоставления лицензии на обновление выпуска устройств Windows 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="66faa-110">Method for providing a license for an edition upgrade of Windows 10 mobile devices.</span></span> <span data-ttu-id="66faa-111">См. также [упградидитионвислиценсе](/windows/client-management/mdm/windowslicensing-csp).</span><span class="sxs-lookup"><span data-stu-id="66faa-111">See also, [UpgradeEditionWithLicense](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="66faa-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66faa-112">Syntax</span></span>


```mof
uint32 UpgradeEditionWithLicenseMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="66faa-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="66faa-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66faa-114">*параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66faa-114">*param* \[in\]</span></span>
<span data-ttu-id="66faa-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="66faa-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="66faa-116">Требования</span><span class="sxs-lookup"><span data-stu-id="66faa-116">Requirements</span></span>



| <span data-ttu-id="66faa-117">Требование</span><span class="sxs-lookup"><span data-stu-id="66faa-117">Requirement</span></span> | <span data-ttu-id="66faa-118">Значение</span><span class="sxs-lookup"><span data-stu-id="66faa-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66faa-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66faa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="66faa-120">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="66faa-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="66faa-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66faa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="66faa-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="66faa-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="66faa-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="66faa-123">Namespace</span></span><br/>                | <span data-ttu-id="66faa-124">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="66faa-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="66faa-125">MOF</span><span class="sxs-lookup"><span data-stu-id="66faa-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66faa-126"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66faa-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="66faa-127">DLL</span><span class="sxs-lookup"><span data-stu-id="66faa-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66faa-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66faa-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66faa-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66faa-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66faa-130">**\_ВИНДОВСЛИЦЕНСИНГ MDM**</span><span class="sxs-lookup"><span data-stu-id="66faa-130">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="66faa-131">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="66faa-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

