---
title: Метод Стореинсталлмесод класса MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: Метод для выполнения установки приложения и лицензии из Магазина Windows. См. также Стореинсталл.
ms.assetid: 4f8aff47-ad16-4fe5-85be-7ddb55ddff24
keywords:
- Метод Стореинсталлмесод
- Метод Стореинсталлмесод, класс MDM_EnterpriseModernAppManagement_AppInstallation01_01
- Класс MDM_EnterpriseModernAppManagement_AppInstallation01_01, метод Стореинсталлмесод
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.StoreInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4ae34e8502b7d408a7fb4d96fb9c2c4fadb509
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989052"
---
# <a name="storeinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="e2cd5-107">Метод Стореинсталлмесод \_ класса MDM ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="e2cd5-107">StoreInstallMethod method of the MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="e2cd5-108">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="e2cd5-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e2cd5-109">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="e2cd5-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e2cd5-110">Метод для выполнения установки приложения и лицензии из Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="e2cd5-110">Method to perform an install of an app and a license from the Windows Store.</span></span> <span data-ttu-id="e2cd5-111">См. также [стореинсталл](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="e2cd5-111">See also, [StoreInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="e2cd5-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2cd5-112">Syntax</span></span>


```mof
uint32 StoreInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="e2cd5-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2cd5-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2cd5-114">*параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2cd5-114">*param* \[in\]</span></span>
<span data-ttu-id="e2cd5-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e2cd5-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e2cd5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e2cd5-116">Requirements</span></span>



| <span data-ttu-id="e2cd5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e2cd5-117">Requirement</span></span> | <span data-ttu-id="e2cd5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e2cd5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2cd5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2cd5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e2cd5-120">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e2cd5-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e2cd5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2cd5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e2cd5-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e2cd5-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e2cd5-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e2cd5-123">Namespace</span></span><br/>                | <span data-ttu-id="e2cd5-124">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="e2cd5-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e2cd5-125">MOF</span><span class="sxs-lookup"><span data-stu-id="e2cd5-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2cd5-126"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd5-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2cd5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e2cd5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2cd5-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd5-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2cd5-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2cd5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2cd5-130">**MDM \_ ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="e2cd5-130">**MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[<span data-ttu-id="e2cd5-131">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="e2cd5-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

