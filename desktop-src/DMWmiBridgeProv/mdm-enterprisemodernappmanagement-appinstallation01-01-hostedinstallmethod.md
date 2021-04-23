---
title: Метод Хостединсталлмесод класса MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: Метод для выполнения установки пакета приложения из размещенного расположения, такого как локальный диск, UNC-источник данных или HTTPS. См. также Хостединсталл.
ms.assetid: 1ec16315-75ce-4613-804e-6b587c4071d6
keywords:
- Метод Хостединсталлмесод
- Метод Хостединсталлмесод, класс MDM_EnterpriseModernAppManagement_AppInstallation01_01
- Класс MDM_EnterpriseModernAppManagement_AppInstallation01_01, метод Хостединсталлмесод
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.HostedInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9597f748a2b5695fd2703f187cfe50db7ad0aa85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654592"
---
# <a name="hostedinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="ac837-107">Метод Хостединсталлмесод \_ класса MDM ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="ac837-107">HostedInstallMethod method of the MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="ac837-108">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="ac837-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ac837-109">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="ac837-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ac837-110">Метод для выполнения установки пакета приложения из размещенного расположения, такого как локальный диск, UNC-источник данных или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ac837-110">Method to perform an install of an app package from a hosted location, such as a local drive, a UNC, or HTTPS data source.</span></span> <span data-ttu-id="ac837-111">См. также [хостединсталл](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="ac837-111">See also, [HostedInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="ac837-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac837-112">Syntax</span></span>


```mof
uint32 HostedInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="ac837-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac837-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac837-114">*параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac837-114">*param* \[in\]</span></span>
<span data-ttu-id="ac837-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ac837-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ac837-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ac837-116">Requirements</span></span>



| <span data-ttu-id="ac837-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ac837-117">Requirement</span></span> | <span data-ttu-id="ac837-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ac837-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac837-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac837-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ac837-120">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ac837-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ac837-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac837-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ac837-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ac837-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ac837-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ac837-123">Namespace</span></span><br/>                | <span data-ttu-id="ac837-124">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="ac837-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ac837-125">MOF</span><span class="sxs-lookup"><span data-stu-id="ac837-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac837-126"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac837-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac837-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ac837-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac837-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac837-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac837-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac837-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac837-130">**MDM \_ ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="ac837-130">**MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[<span data-ttu-id="ac837-131">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="ac837-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

