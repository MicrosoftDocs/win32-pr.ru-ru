---
title: Класс MDM_Policy_Result01_ActiveXControls02
description: '\_Класс политики MDM \_ Result01 \_ ActiveXControls02 представляет доступные политики элементов управления ActiveX.'
ms.assetid: 46778743-59d7-4d37-836c-3f263bb8a083
keywords:
- Класс MDM_Policy_Result01_ActiveXControls02
- MDM_Policy_Result01_ActiveXControls02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ActiveXControls02
- MDM_Policy_Result01_ActiveXControls02.InstanceID
- MDM_Policy_Result01_ActiveXControls02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36ee572cfbbd823ce9e819688d9399b22f5d564c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071674"
---
# <a name="mdm_policy_result01_activexcontrols02-class"></a><span data-ttu-id="52141-105">\_Класс политики MDM \_ Result01 \_ ActiveXControls02</span><span class="sxs-lookup"><span data-stu-id="52141-105">MDM\_Policy\_Result01\_ActiveXControls02 class</span></span>

<span data-ttu-id="52141-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="52141-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="52141-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="52141-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="52141-108">\_Класс политики MDM \_ Result01 \_ ActiveXControls02 представляет доступные политики элементов управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="52141-108">The MDM\_Policy\_Result01\_ActiveXControls02 class represents the available ActiveX Controls policies.</span></span>

<span data-ttu-id="52141-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="52141-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="52141-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52141-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ActiveXControls02
{
  string InstanceID;
  string ParentID;
  string ApprovedInstallationSites;
};
```

## <a name="members"></a><span data-ttu-id="52141-111">Члены</span><span class="sxs-lookup"><span data-stu-id="52141-111">Members</span></span>

<span data-ttu-id="52141-112">Класс **\_ политики MDM \_ Result01 \_ ActiveXControls02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="52141-112">The **MDM\_Policy\_Result01\_ActiveXControls02** class has these types of members:</span></span>

-   [<span data-ttu-id="52141-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="52141-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52141-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="52141-114">Properties</span></span>

<span data-ttu-id="52141-115">Класс **\_ политики MDM \_ Result01 \_ ActiveXControls02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="52141-115">The **MDM\_Policy\_Result01\_ActiveXControls02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="52141-116">аппровединсталлатионситес</span><span class="sxs-lookup"><span data-stu-id="52141-116">ApprovedInstallationSites</span></span>](/windows/client-management/mdm/policy-csp-activexcontrols#activexcontrols-approvedinstallationsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52141-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="52141-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52141-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="52141-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="52141-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="52141-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52141-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="52141-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52141-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="52141-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52141-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="52141-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="52141-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="52141-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52141-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="52141-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52141-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="52141-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52141-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="52141-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52141-127">Требования</span><span class="sxs-lookup"><span data-stu-id="52141-127">Requirements</span></span>



| <span data-ttu-id="52141-128">Требование</span><span class="sxs-lookup"><span data-stu-id="52141-128">Requirement</span></span> | <span data-ttu-id="52141-129">Значение</span><span class="sxs-lookup"><span data-stu-id="52141-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52141-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52141-130">Minimum supported client</span></span><br/> | <span data-ttu-id="52141-131">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="52141-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52141-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52141-132">Minimum supported server</span></span><br/> | <span data-ttu-id="52141-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="52141-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="52141-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="52141-134">Namespace</span></span><br/>                | <span data-ttu-id="52141-135">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="52141-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="52141-136">MOF</span><span class="sxs-lookup"><span data-stu-id="52141-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52141-137"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52141-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="52141-138">DLL</span><span class="sxs-lookup"><span data-stu-id="52141-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52141-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52141-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

