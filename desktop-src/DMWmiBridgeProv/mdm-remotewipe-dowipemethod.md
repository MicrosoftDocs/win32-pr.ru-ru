---
title: метод Довипемесод класса MDM_RemoteWipe
description: Запускает устройство для запуска удаленной очистки.
ms.assetid: dc25dc09-6a74-4c08-b452-b1d83085bb41
keywords:
- метод Довипемесод
- метод Довипемесод, класс MDM_RemoteWipe
- Класс MDM_RemoteWipe, метод Довипемесод
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipeMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f31dcc9dde2fe51ca0d8677df8b27637edd06c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489177"
---
# <a name="dowipemethod-method-of-the-mdm_remotewipe-class"></a><span data-ttu-id="33828-106">метод Довипемесод \_ класса MDM ремотевипе</span><span class="sxs-lookup"><span data-stu-id="33828-106">doWipeMethod method of the MDM\_RemoteWipe class</span></span>

<span data-ttu-id="33828-107">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="33828-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="33828-108">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="33828-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="33828-109">Запускает устройство для запуска удаленной очистки.</span><span class="sxs-lookup"><span data-stu-id="33828-109">Triggers the device to start the remote wipe.</span></span> <span data-ttu-id="33828-110">См. также [doWipe](/windows/client-management/mdm/remotewipe-csp).</span><span class="sxs-lookup"><span data-stu-id="33828-110">See also, [doWipe](/windows/client-management/mdm/remotewipe-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="33828-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33828-111">Syntax</span></span>


```mof
uint32 doWipeMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="33828-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="33828-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33828-113">*параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="33828-113">*param* \[in\]</span></span>
<span data-ttu-id="33828-114"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="33828-114"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="33828-115">Требования</span><span class="sxs-lookup"><span data-stu-id="33828-115">Requirements</span></span>



| <span data-ttu-id="33828-116">Требование</span><span class="sxs-lookup"><span data-stu-id="33828-116">Requirement</span></span> | <span data-ttu-id="33828-117">Значение</span><span class="sxs-lookup"><span data-stu-id="33828-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33828-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33828-118">Minimum supported client</span></span><br/> | <span data-ttu-id="33828-119">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="33828-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="33828-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33828-120">Minimum supported server</span></span><br/> | <span data-ttu-id="33828-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="33828-121">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="33828-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="33828-122">Namespace</span></span><br/>                | <span data-ttu-id="33828-123">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="33828-123">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="33828-124">MOF</span><span class="sxs-lookup"><span data-stu-id="33828-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33828-125"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33828-125"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="33828-126">DLL</span><span class="sxs-lookup"><span data-stu-id="33828-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33828-127"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33828-127"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33828-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33828-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33828-129">**\_РЕМОТЕВИПЕ MDM**</span><span class="sxs-lookup"><span data-stu-id="33828-129">**MDM\_RemoteWipe**</span></span>](mdm-remotewipe.md)
</dt> <dt>

[<span data-ttu-id="33828-130">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="33828-130">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

