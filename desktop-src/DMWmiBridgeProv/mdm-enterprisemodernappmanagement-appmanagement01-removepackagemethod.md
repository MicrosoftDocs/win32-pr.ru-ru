---
title: Метод Ремовепаккажемесод класса MDM_EnterpriseModernAppManagement_AppManagement01
description: Метод удаления пакетов. См. также Ремовепаккаже.
ms.assetid: 0f48fd9c-5a3f-48e5-a954-e937e79af049
keywords:
- Метод Ремовепаккажемесод
- Метод Ремовепаккажемесод, класс MDM_EnterpriseModernAppManagement_AppManagement01
- Класс MDM_EnterpriseModernAppManagement_AppManagement01, метод Ремовепаккажемесод
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01.RemovePackageMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2cdeb2c1a8dfaebdde73e52b2910da180b638c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654589"
---
# <a name="removepackagemethod-method-of-the-mdm_enterprisemodernappmanagement_appmanagement01-class"></a><span data-ttu-id="c80ed-107">Метод Ремовепаккажемесод \_ класса MDM ентерприсемодернаппманажемент \_ AppManagement01</span><span class="sxs-lookup"><span data-stu-id="c80ed-107">RemovePackageMethod method of the MDM\_EnterpriseModernAppManagement\_AppManagement01 class</span></span>

<span data-ttu-id="c80ed-108">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="c80ed-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c80ed-109">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="c80ed-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c80ed-110">Метод удаления пакетов.</span><span class="sxs-lookup"><span data-stu-id="c80ed-110">Method for removing packages.</span></span> <span data-ttu-id="c80ed-111">См. также [ремовепаккаже](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="c80ed-111">See also [RemovePackage](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="c80ed-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c80ed-112">Syntax</span></span>


```mof
uint32 RemovePackageMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="c80ed-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="c80ed-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c80ed-114">*параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c80ed-114">*param* \[in\]</span></span>
<span data-ttu-id="c80ed-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c80ed-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="c80ed-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c80ed-116">Requirements</span></span>



| <span data-ttu-id="c80ed-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c80ed-117">Requirement</span></span> | <span data-ttu-id="c80ed-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c80ed-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c80ed-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c80ed-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c80ed-120">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c80ed-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c80ed-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c80ed-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c80ed-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c80ed-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c80ed-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c80ed-123">Namespace</span></span><br/>                | <span data-ttu-id="c80ed-124">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="c80ed-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c80ed-125">MOF</span><span class="sxs-lookup"><span data-stu-id="c80ed-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c80ed-126"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c80ed-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c80ed-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c80ed-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c80ed-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c80ed-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c80ed-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c80ed-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c80ed-130">**MDM \_ ентерприсемодернаппманажемент \_ AppManagement01**</span><span class="sxs-lookup"><span data-stu-id="c80ed-130">**MDM\_EnterpriseModernAppManagement\_AppManagement01**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01.md)
</dt> </dl>

 

