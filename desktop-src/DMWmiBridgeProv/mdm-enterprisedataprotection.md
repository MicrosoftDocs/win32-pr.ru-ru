---
title: Класс MDM_EnterpriseDataProtection
description: Класс MDM \_ ентерприседатапротектион используется для определения текущего состояния Windows Information Protection (WIP) (прежнее название — защита корпоративных данных).
ms.assetid: 2b97de12-76d1-4b74-a979-f0484807b840
keywords:
- Класс MDM_EnterpriseDataProtection
- MDM_EnterpriseDataProtection класс, описание
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection
- MDM_EnterpriseDataProtection.InstanceID
- MDM_EnterpriseDataProtection.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b4a3a1d9d491b6970ee95a081de8bb240d54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491955"
---
# <a name="mdm_enterprisedataprotection-class"></a><span data-ttu-id="0749a-105">\_Класс MDM ентерприседатапротектион</span><span class="sxs-lookup"><span data-stu-id="0749a-105">MDM\_EnterpriseDataProtection class</span></span>

<span data-ttu-id="0749a-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="0749a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0749a-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="0749a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0749a-108">Класс **MDM \_ ентерприседатапротектион** используется для определения текущего состояния Windows Information Protection (WIP) (прежнее название — защита корпоративных данных).</span><span class="sxs-lookup"><span data-stu-id="0749a-108">The **MDM\_EnterpriseDataProtection** class is used to determine the current status of Windows Information Protection (WIP) (formerly known as Enterprise Data Protection) specific settings.</span></span>

<span data-ttu-id="0749a-109">Дополнительные сведения о WIP см. в статье [Защита корпоративных данных с помощью защиты корпоративных данных (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span><span class="sxs-lookup"><span data-stu-id="0749a-109">For more information about WIP, see [Protect your enterprise data using enterprise data protection (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span></span>

<span data-ttu-id="0749a-110">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="0749a-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0749a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0749a-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="0749a-112">Члены</span><span class="sxs-lookup"><span data-stu-id="0749a-112">Members</span></span>

<span data-ttu-id="0749a-113">Класс **MDM \_ ентерприседатапротектион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0749a-113">The **MDM\_EnterpriseDataProtection** class has these types of members:</span></span>

-   [<span data-ttu-id="0749a-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="0749a-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0749a-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="0749a-115">Properties</span></span>

<span data-ttu-id="0749a-116">Класс **MDM \_ ентерприседатапротектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0749a-116">The **MDM\_EnterpriseDataProtection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0749a-117">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0749a-117">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0749a-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0749a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0749a-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0749a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0749a-120">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0749a-120">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0749a-121">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="0749a-121">Identifies the name of the parent node.</span></span> <span data-ttu-id="0749a-122">Для этого класса строка имеет значение "Ентерприседатапротектион".</span><span class="sxs-lookup"><span data-stu-id="0749a-122">For this class, the string is "EnterpriseDataProtection".</span></span>

</dd> <dt>

<span data-ttu-id="0749a-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0749a-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0749a-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0749a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0749a-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0749a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0749a-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0749a-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0749a-127">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="0749a-127">Describes the full path to the parent node.</span></span> <span data-ttu-id="0749a-128">Для этого класса строка имеет значение "./вендор/мсфт/"</span><span class="sxs-lookup"><span data-stu-id="0749a-128">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="0749a-129">Состояние</span><span class="sxs-lookup"><span data-stu-id="0749a-129">Status</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0749a-130">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0749a-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0749a-131">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0749a-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0749a-132">Требования</span><span class="sxs-lookup"><span data-stu-id="0749a-132">Requirements</span></span>



| <span data-ttu-id="0749a-133">Требование</span><span class="sxs-lookup"><span data-stu-id="0749a-133">Requirement</span></span> | <span data-ttu-id="0749a-134">Значение</span><span class="sxs-lookup"><span data-stu-id="0749a-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0749a-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0749a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0749a-136">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0749a-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0749a-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0749a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0749a-138">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0749a-138">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="0749a-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0749a-139">Namespace</span></span><br/>                | <span data-ttu-id="0749a-140">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="0749a-140">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="0749a-141">MOF</span><span class="sxs-lookup"><span data-stu-id="0749a-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0749a-142"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0749a-142"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="0749a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="0749a-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0749a-144"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0749a-144"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

