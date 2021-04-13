---
title: Метод Чанжепродукткэймесод класса MDM_WindowsLicensing
description: Этот метод устанавливает ключ продукта для устройств Windows 10 Desktop. Точка не перезагружена. См. также Чанжепродукткэй.
ms.assetid: 1d9e3243-2ca4-427b-bda2-d33e1e70c80d
keywords:
- Метод Чанжепродукткэймесод
- Метод Чанжепродукткэймесод, класс MDM_WindowsLicensing
- Класс MDM_WindowsLicensing, метод Чанжепродукткэймесод
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.ChangeProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e00345fb0e23655b457e0540c70289a169c54ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491937"
---
# <a name="changeproductkeymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="e2cbb-108">Метод Чанжепродукткэймесод \_ класса MDM виндовслиценсинг</span><span class="sxs-lookup"><span data-stu-id="e2cbb-108">ChangeProductKeyMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="e2cbb-109">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="e2cbb-109">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e2cbb-110">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="e2cbb-110">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e2cbb-111">Этот метод устанавливает ключ продукта для устройств Windows 10 Desktop.</span><span class="sxs-lookup"><span data-stu-id="e2cbb-111">This method installs a product key for Windows 10 desktop devices.</span></span> <span data-ttu-id="e2cbb-112">Точка не перезагружена.</span><span class="sxs-lookup"><span data-stu-id="e2cbb-112">Dot not reboot.</span></span> <span data-ttu-id="e2cbb-113">См. также [чанжепродукткэй](/windows/client-management/mdm/windowslicensing-csp)</span><span class="sxs-lookup"><span data-stu-id="e2cbb-113">See also [ChangeProductKey](/windows/client-management/mdm/windowslicensing-csp)</span></span>

## <a name="syntax"></a><span data-ttu-id="e2cbb-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2cbb-114">Syntax</span></span>


```mof
uint32 ChangeProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="e2cbb-115">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2cbb-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2cbb-116">*параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2cbb-116">*param* \[in\]</span></span>
<span data-ttu-id="e2cbb-117"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e2cbb-117"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e2cbb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e2cbb-118">Requirements</span></span>



| <span data-ttu-id="e2cbb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e2cbb-119">Requirement</span></span> | <span data-ttu-id="e2cbb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e2cbb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2cbb-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2cbb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e2cbb-122">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e2cbb-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e2cbb-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2cbb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e2cbb-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e2cbb-124">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e2cbb-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e2cbb-125">Namespace</span></span><br/>                | <span data-ttu-id="e2cbb-126">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="e2cbb-126">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e2cbb-127">MOF</span><span class="sxs-lookup"><span data-stu-id="e2cbb-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2cbb-128"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2cbb-128"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2cbb-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e2cbb-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2cbb-130"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2cbb-130"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2cbb-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2cbb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2cbb-132">**\_ВИНДОВСЛИЦЕНСИНГ MDM**</span><span class="sxs-lookup"><span data-stu-id="e2cbb-132">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> </dl>

 

