---
title: Класс MDM_Policy_User_Result01_System02
description: '\_ \_ \_ Класс User RESULT01 System02 политики MDM \_ представляет доступные политики телеметрии.'
ms.assetid: ed16474c-3bbb-41d8-9806-81dbd95c608d
keywords:
- Класс MDM_Policy_User_Result01_System02
- MDM_Policy_User_Result01_System02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_System02
- MDM_Policy_User_Result01_System02.InstanceID
- MDM_Policy_User_Result01_System02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ce5e01429a648d265904d3b3996be9fb7a3faa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414805"
---
# <a name="mdm_policy_user_result01_system02-class"></a><span data-ttu-id="08e2c-105">\_Класс политики MDM \_ user \_ Result01 \_ System02</span><span class="sxs-lookup"><span data-stu-id="08e2c-105">MDM\_Policy\_User\_Result01\_System02 class</span></span>

<span data-ttu-id="08e2c-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="08e2c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="08e2c-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="08e2c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="08e2c-108">\_ \_ \_ Класс User RESULT01 System02 политики MDM \_ представляет доступные политики телеметрии.</span><span class="sxs-lookup"><span data-stu-id="08e2c-108">The MDM\_Policy\_User\_Result01\_System02 class represents the available telemetry policies.</span></span>

<span data-ttu-id="08e2c-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="08e2c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="08e2c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08e2c-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_System02
{
  string InstanceID;
  string ParentID;
  sint32 AllowTelemetry;
};
```

## <a name="members"></a><span data-ttu-id="08e2c-111">Члены</span><span class="sxs-lookup"><span data-stu-id="08e2c-111">Members</span></span>

<span data-ttu-id="08e2c-112">Класс **\_ \_ user \_ Result01 \_ System02 политики MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="08e2c-112">The **MDM\_Policy\_User\_Result01\_System02** class has these types of members:</span></span>

-   [<span data-ttu-id="08e2c-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="08e2c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08e2c-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="08e2c-114">Properties</span></span>

<span data-ttu-id="08e2c-115">Класс **\_ \_ user \_ Result01 \_ System02 политики MDM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="08e2c-115">The **MDM\_Policy\_User\_Result01\_System02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="08e2c-116">AllowTelemetry</span><span class="sxs-lookup"><span data-stu-id="08e2c-116">AllowTelemetry</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowtelemetry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08e2c-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="08e2c-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08e2c-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="08e2c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08e2c-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="08e2c-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08e2c-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08e2c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08e2c-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08e2c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08e2c-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="08e2c-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08e2c-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="08e2c-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08e2c-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08e2c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08e2c-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08e2c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08e2c-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="08e2c-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08e2c-127">Требования</span><span class="sxs-lookup"><span data-stu-id="08e2c-127">Requirements</span></span>



| <span data-ttu-id="08e2c-128">Требование</span><span class="sxs-lookup"><span data-stu-id="08e2c-128">Requirement</span></span> | <span data-ttu-id="08e2c-129">Значение</span><span class="sxs-lookup"><span data-stu-id="08e2c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08e2c-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08e2c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="08e2c-131">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="08e2c-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="08e2c-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08e2c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="08e2c-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="08e2c-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="08e2c-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="08e2c-134">Namespace</span></span><br/>                | <span data-ttu-id="08e2c-135">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="08e2c-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="08e2c-136">MOF</span><span class="sxs-lookup"><span data-stu-id="08e2c-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08e2c-137"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08e2c-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="08e2c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="08e2c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08e2c-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08e2c-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

