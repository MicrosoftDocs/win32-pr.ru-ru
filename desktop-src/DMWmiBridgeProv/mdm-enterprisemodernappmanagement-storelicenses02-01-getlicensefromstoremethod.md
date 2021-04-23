---
title: Метод Жетлиценсефромсторемесод класса MDM_EnterpriseModernAppManagement_StoreLicenses02_01
description: Метод получения лицензии из магазина. См. также Жетлиценсефромсторе.
ms.assetid: 4cf8a979-60c1-4ec1-968e-5a90cc671ebf
keywords:
- Метод Жетлиценсефромсторемесод
- Метод Жетлиценсефромсторемесод, класс MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- Класс MDM_EnterpriseModernAppManagement_StoreLicenses02_01, метод Жетлиценсефромсторемесод
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.GetLicenseFromStoreMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8751546bfb57e5c9bf34db97ee6b59dd7e1f580
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136762"
---
# <a name="getlicensefromstoremethod-method-of-the-mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a><span data-ttu-id="9e094-107">Метод Жетлиценсефромсторемесод \_ класса MDM ентерприсемодернаппманажемент \_ StoreLicenses02 \_ 01</span><span class="sxs-lookup"><span data-stu-id="9e094-107">GetLicenseFromStoreMethod method of the MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01 class</span></span>

<span data-ttu-id="9e094-108">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="9e094-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9e094-109">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="9e094-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9e094-110">Метод получения лицензии из магазина.</span><span class="sxs-lookup"><span data-stu-id="9e094-110">Method for getting a license from the store.</span></span> <span data-ttu-id="9e094-111">См. также [жетлиценсефромсторе](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="9e094-111">See also, [GetLicenseFromStore](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="9e094-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e094-112">Syntax</span></span>


```mof
uint32 GetLicenseFromStoreMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="9e094-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e094-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e094-114">*параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9e094-114">*param* \[in\]</span></span>
<span data-ttu-id="9e094-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9e094-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="9e094-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9e094-116">Requirements</span></span>



| <span data-ttu-id="9e094-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9e094-117">Requirement</span></span> | <span data-ttu-id="9e094-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9e094-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e094-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e094-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9e094-120">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9e094-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9e094-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e094-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9e094-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9e094-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9e094-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9e094-123">Namespace</span></span><br/>                | <span data-ttu-id="9e094-124">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="9e094-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9e094-125">MOF</span><span class="sxs-lookup"><span data-stu-id="9e094-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e094-126"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e094-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e094-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9e094-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e094-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e094-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e094-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e094-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e094-130">**MDM \_ ентерприсемодернаппманажемент \_ StoreLicenses02 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="9e094-130">**MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01.md)
</dt> <dt>

[<span data-ttu-id="9e094-131">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="9e094-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

