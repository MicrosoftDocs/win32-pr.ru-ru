---
title: Класс MDM_Policy_Config01_ActiveXControls02
description: Этот параметр политики определяет, какие сайты установки ActiveX могут использовать стандартные пользователи в Организации для установки элементов управления ActiveX на своих компьютерах.
ms.assetid: 242888ae-f07a-40b7-9539-29fcca9cfc40
keywords:
- Класс MDM_Policy_Config01_ActiveXControls02
- MDM_Policy_Config01_ActiveXControls02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ActiveXControls02
- MDM_Policy_Config01_ActiveXControls02.InstanceID
- MDM_Policy_Config01_ActiveXControls02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 213edcea47bc0fd3379f753613c5b884963ca781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654459"
---
# <a name="mdm_policy_config01_activexcontrols02-class"></a><span data-ttu-id="a7da4-105">\_Класс политики MDM \_ Config01 \_ ActiveXControls02</span><span class="sxs-lookup"><span data-stu-id="a7da4-105">MDM\_Policy\_Config01\_ActiveXControls02 class</span></span>

<span data-ttu-id="a7da4-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="a7da4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a7da4-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="a7da4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a7da4-108">Этот параметр политики определяет, какие сайты установки ActiveX могут использовать стандартные пользователи в Организации для установки элементов управления ActiveX на своих компьютерах.</span><span class="sxs-lookup"><span data-stu-id="a7da4-108">This policy setting determines which ActiveX installation sites standard users in your organization can use to install ActiveX controls on their computers.</span></span> <span data-ttu-id="a7da4-109">Если этот параметр включен, администратор может создать список утвержденных сайтов установки ActiveX, указанных по URL-адресу узла.</span><span class="sxs-lookup"><span data-stu-id="a7da4-109">When this setting is enabled, the administrator can create a list of approved Activex Install sites specified by host URL.</span></span>

<span data-ttu-id="a7da4-110">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="a7da4-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7da4-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7da4-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ActiveXControls02
{
  string InstanceID;
  string ParentID;
  string ApprovedInstallationSites;
};
```

## <a name="members"></a><span data-ttu-id="a7da4-112">Члены</span><span class="sxs-lookup"><span data-stu-id="a7da4-112">Members</span></span>

<span data-ttu-id="a7da4-113">Класс **\_ политики MDM \_ Config01 \_ ActiveXControls02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a7da4-113">The **MDM\_Policy\_Config01\_ActiveXControls02** class has these types of members:</span></span>

-   [<span data-ttu-id="a7da4-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="a7da4-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a7da4-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="a7da4-115">Properties</span></span>

<span data-ttu-id="a7da4-116">Класс **\_ политики MDM \_ Config01 \_ ActiveXControls02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a7da4-116">The **MDM\_Policy\_Config01\_ActiveXControls02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a7da4-117">аппровединсталлатионситес</span><span class="sxs-lookup"><span data-stu-id="a7da4-117">ApprovedInstallationSites</span></span>](/windows/client-management/mdm/policy-csp-activexcontrols#activexcontrols-approvedinstallationsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7da4-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a7da4-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7da4-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a7da4-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a7da4-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a7da4-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7da4-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a7da4-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7da4-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7da4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7da4-123">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a7da4-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a7da4-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a7da4-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7da4-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a7da4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7da4-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7da4-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7da4-127">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a7da4-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a7da4-128">Требования</span><span class="sxs-lookup"><span data-stu-id="a7da4-128">Requirements</span></span>



| <span data-ttu-id="a7da4-129">Требование</span><span class="sxs-lookup"><span data-stu-id="a7da4-129">Requirement</span></span> | <span data-ttu-id="a7da4-130">Значение</span><span class="sxs-lookup"><span data-stu-id="a7da4-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7da4-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7da4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a7da4-132">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a7da4-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a7da4-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7da4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a7da4-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a7da4-134">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a7da4-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a7da4-135">Namespace</span></span><br/>                | <span data-ttu-id="a7da4-136">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="a7da4-136">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a7da4-137">MOF</span><span class="sxs-lookup"><span data-stu-id="a7da4-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7da4-138"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7da4-138"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7da4-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a7da4-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7da4-140"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7da4-140"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

