---
title: Класс MDM_EnterpriseAPN_Settings01
description: Класс MDM \_ EnterpriseAPN \_ Settings01 используется предприятием для изменения глобальных параметров точки доступа.
ms.assetid: 3f2d3d38-c389-4945-b519-5f2d7dedb86c
keywords:
- Класс MDM_EnterpriseAPN_Settings01
- MDM_EnterpriseAPN_Settings01 класс, описание
topic_type:
- apiref
api_name:
- MDM_EnterpriseAPN_Settings01
- MDM_EnterpriseAPN_Settings01.InstanceID
- MDM_EnterpriseAPN_Settings01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74704451790690df8f9cc11fec8bc1ed80d3c2dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136774"
---
# <a name="mdm_enterpriseapn_settings01-class"></a><span data-ttu-id="6dda8-105">\_ \_ Класс SETTINGS01 для MDM EnterpriseAPN</span><span class="sxs-lookup"><span data-stu-id="6dda8-105">MDM\_EnterpriseAPN\_Settings01 class</span></span>

<span data-ttu-id="6dda8-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="6dda8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6dda8-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="6dda8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6dda8-108">Класс **MDM \_ EnterpriseAPN \_ Settings01** используется предприятием для изменения глобальных параметров точки доступа.</span><span class="sxs-lookup"><span data-stu-id="6dda8-108">The **MDM\_EnterpriseAPN\_Settings01** class is used by the enterprise to change APN global settings.</span></span>

<span data-ttu-id="6dda8-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="6dda8-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dda8-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6dda8-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseAPN_Settings01
{
  string  InstanceID;
  string  ParentID;
  boolean AllowUserControl;
  boolean HideView;
};
```

## <a name="members"></a><span data-ttu-id="6dda8-111">Члены</span><span class="sxs-lookup"><span data-stu-id="6dda8-111">Members</span></span>

<span data-ttu-id="6dda8-112">Класс **MDM \_ EnterpriseAPN \_ Settings01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6dda8-112">The **MDM\_EnterpriseAPN\_Settings01** class has these types of members:</span></span>

-   [<span data-ttu-id="6dda8-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="6dda8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6dda8-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="6dda8-114">Properties</span></span>

<span data-ttu-id="6dda8-115">Класс **MDM \_ EnterpriseAPN \_ Settings01** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6dda8-115">The **MDM\_EnterpriseAPN\_Settings01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6dda8-116">алловусерконтрол</span><span class="sxs-lookup"><span data-stu-id="6dda8-116">AllowUserControl</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-settings-allowusercontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dda8-117">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6dda8-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6dda8-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6dda8-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6dda8-119">хидевиев</span><span class="sxs-lookup"><span data-stu-id="6dda8-119">HideView</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-settings-hideview)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dda8-120">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6dda8-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6dda8-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6dda8-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6dda8-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6dda8-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dda8-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6dda8-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6dda8-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6dda8-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6dda8-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6dda8-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6dda8-126">Узел, содержащий глобальные параметры точки доступа.</span><span class="sxs-lookup"><span data-stu-id="6dda8-126">Node that contains APN global settings.</span></span>

</dd> <dt>

<span data-ttu-id="6dda8-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6dda8-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dda8-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6dda8-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6dda8-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6dda8-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6dda8-130">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6dda8-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6dda8-131">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="6dda8-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="6dda8-132">Для этого класса строка имеет значение "./вендор/мсфт/ентерприсеапн/Сеттингс"</span><span class="sxs-lookup"><span data-stu-id="6dda8-132">For this class, the string is "./Vendor/MSFT/EnterpriseAPN/Settings"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6dda8-133">Требования</span><span class="sxs-lookup"><span data-stu-id="6dda8-133">Requirements</span></span>



| <span data-ttu-id="6dda8-134">Требование</span><span class="sxs-lookup"><span data-stu-id="6dda8-134">Requirement</span></span> | <span data-ttu-id="6dda8-135">Значение</span><span class="sxs-lookup"><span data-stu-id="6dda8-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dda8-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6dda8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6dda8-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6dda8-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6dda8-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6dda8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6dda8-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6dda8-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6dda8-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6dda8-140">Namespace</span></span><br/>                | <span data-ttu-id="6dda8-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="6dda8-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6dda8-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6dda8-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6dda8-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6dda8-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6dda8-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6dda8-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dda8-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dda8-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

