---
title: Класс MDM_Policy_User_Result01_AttachmentManager02
description: '\_Класс политики MDM \_ user \_ Result01 \_ AttachmentManager02 представляет доступные политики диспетчера вложений.'
ms.assetid: c6cfec0d-24f8-4356-a12b-d9b9944776a7
keywords:
- Класс MDM_Policy_User_Result01_AttachmentManager02
- MDM_Policy_User_Result01_AttachmentManager02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_AttachmentManager02
- MDM_Policy_User_Result01_AttachmentManager02.InstanceID
- MDM_Policy_User_Result01_AttachmentManager02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b78eadb9aa320d35d3a8078359a682536fd7e120
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490785"
---
# <a name="mdm_policy_user_result01_attachmentmanager02-class"></a><span data-ttu-id="76ed7-105">\_Класс политики MDM \_ user \_ Result01 \_ AttachmentManager02</span><span class="sxs-lookup"><span data-stu-id="76ed7-105">MDM\_Policy\_User\_Result01\_AttachmentManager02 class</span></span>

<span data-ttu-id="76ed7-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="76ed7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="76ed7-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="76ed7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="76ed7-108">\_Класс политики MDM \_ user \_ Result01 \_ AttachmentManager02 представляет доступные политики диспетчера вложений.</span><span class="sxs-lookup"><span data-stu-id="76ed7-108">The MDM\_Policy\_User\_Result01\_AttachmentManager02 class represents the available attachment manager policies.</span></span>

<span data-ttu-id="76ed7-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="76ed7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="76ed7-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76ed7-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_AttachmentManager02
{
  string InstanceID;
  string ParentID;
  string DoNotPreserveZoneInformation;
  string HideZoneInfoMechanism;
  string NotifyAntivirusPrograms;
};
```

## <a name="members"></a><span data-ttu-id="76ed7-111">Члены</span><span class="sxs-lookup"><span data-stu-id="76ed7-111">Members</span></span>

<span data-ttu-id="76ed7-112">Класс **\_ \_ user \_ Result01 \_ AttachmentManager02 политики MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="76ed7-112">The **MDM\_Policy\_User\_Result01\_AttachmentManager02** class has these types of members:</span></span>

-   [<span data-ttu-id="76ed7-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="76ed7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="76ed7-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="76ed7-114">Properties</span></span>

<span data-ttu-id="76ed7-115">Класс **\_ \_ user \_ Result01 \_ AttachmentManager02 политики MDM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="76ed7-115">The **MDM\_Policy\_User\_Result01\_AttachmentManager02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="76ed7-116">донотпресервезонеинформатион</span><span class="sxs-lookup"><span data-stu-id="76ed7-116">DoNotPreserveZoneInformation</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-donotpreservezoneinformation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76ed7-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="76ed7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76ed7-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="76ed7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76ed7-119">хидезонеинфомечанисм</span><span class="sxs-lookup"><span data-stu-id="76ed7-119">HideZoneInfoMechanism</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-hidezoneinfomechanism)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76ed7-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="76ed7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76ed7-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="76ed7-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76ed7-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="76ed7-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76ed7-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="76ed7-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76ed7-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="76ed7-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76ed7-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="76ed7-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76ed7-126">нотифянтивируспрограмс</span><span class="sxs-lookup"><span data-stu-id="76ed7-126">NotifyAntivirusPrograms</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-notifyantivirusprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76ed7-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="76ed7-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76ed7-128">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="76ed7-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76ed7-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="76ed7-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76ed7-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="76ed7-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76ed7-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="76ed7-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76ed7-132">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="76ed7-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76ed7-133">Требования</span><span class="sxs-lookup"><span data-stu-id="76ed7-133">Requirements</span></span>



| <span data-ttu-id="76ed7-134">Требование</span><span class="sxs-lookup"><span data-stu-id="76ed7-134">Requirement</span></span> | <span data-ttu-id="76ed7-135">Значение</span><span class="sxs-lookup"><span data-stu-id="76ed7-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76ed7-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76ed7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="76ed7-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="76ed7-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="76ed7-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76ed7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="76ed7-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="76ed7-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="76ed7-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="76ed7-140">Namespace</span></span><br/>                | <span data-ttu-id="76ed7-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="76ed7-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="76ed7-142">MOF</span><span class="sxs-lookup"><span data-stu-id="76ed7-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76ed7-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76ed7-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="76ed7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="76ed7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76ed7-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76ed7-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

