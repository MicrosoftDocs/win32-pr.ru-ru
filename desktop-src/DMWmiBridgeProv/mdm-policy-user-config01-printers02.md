---
title: Класс MDM_Policy_User_Config01_Printers02
description: '\_Класс политики MDM \_ user \_ Config01 \_ Printers02 представляет доступные политики принтера.'
ms.assetid: 9faeaa04-92b4-43b0-be17-0f85f2eb493c
keywords:
- Класс MDM_Policy_User_Config01_Printers02
- MDM_Policy_User_Config01_Printers02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Printers02
- MDM_Policy_User_Config01_Printers02.InstanceID
- MDM_Policy_User_Config01_Printers02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04be571473f05d93242c77d02052cf84c335caf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802393"
---
# <a name="mdm_policy_user_config01_printers02-class"></a><span data-ttu-id="b6a8d-105">\_Класс политики MDM \_ user \_ Config01 \_ Printers02</span><span class="sxs-lookup"><span data-stu-id="b6a8d-105">MDM\_Policy\_User\_Config01\_Printers02 class</span></span>

<span data-ttu-id="b6a8d-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="b6a8d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b6a8d-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="b6a8d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b6a8d-108">\_Класс политики MDM \_ user \_ Config01 \_ Printers02 представляет доступные политики принтера.</span><span class="sxs-lookup"><span data-stu-id="b6a8d-108">The MDM\_Policy\_User\_Config01\_Printers02 class represents the available printer policies.</span></span>

<span data-ttu-id="b6a8d-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b6a8d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6a8d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6a8d-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Printers02
{
  string InstanceID;
  string ParentID;
  string PointAndPrintRestrictions_User;
};
```

## <a name="members"></a><span data-ttu-id="b6a8d-111">Члены</span><span class="sxs-lookup"><span data-stu-id="b6a8d-111">Members</span></span>

<span data-ttu-id="b6a8d-112">Класс **\_ \_ user \_ Config01 \_ Printers02 политики MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b6a8d-112">The **MDM\_Policy\_User\_Config01\_Printers02** class has these types of members:</span></span>

-   [<span data-ttu-id="b6a8d-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="b6a8d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6a8d-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="b6a8d-114">Properties</span></span>

<span data-ttu-id="b6a8d-115">Класс **\_ \_ user \_ Config01 \_ Printers02 политики MDM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="b6a8d-115">The **MDM\_Policy\_User\_Config01\_Printers02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6a8d-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b6a8d-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6a8d-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b6a8d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6a8d-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b6a8d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6a8d-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b6a8d-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b6a8d-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b6a8d-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6a8d-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b6a8d-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6a8d-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b6a8d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6a8d-123">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b6a8d-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b6a8d-124">\_Пользователь поинтандпринтрестриктионс</span><span class="sxs-lookup"><span data-stu-id="b6a8d-124">PointAndPrintRestrictions\_User</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-pointandprintrestrictions-user)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6a8d-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b6a8d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6a8d-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b6a8d-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6a8d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="b6a8d-127">Requirements</span></span>



| <span data-ttu-id="b6a8d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="b6a8d-128">Requirement</span></span> | <span data-ttu-id="b6a8d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="b6a8d-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6a8d-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6a8d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b6a8d-131">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b6a8d-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b6a8d-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6a8d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b6a8d-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b6a8d-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b6a8d-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b6a8d-134">Namespace</span></span><br/>                | <span data-ttu-id="b6a8d-135">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="b6a8d-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b6a8d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="b6a8d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6a8d-137"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6a8d-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6a8d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b6a8d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6a8d-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6a8d-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

