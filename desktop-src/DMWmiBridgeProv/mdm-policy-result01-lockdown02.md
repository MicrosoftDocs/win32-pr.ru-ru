---
title: Класс MDM_Policy_Result01_LockDown02
description: '\_Класс политики MDM \_ Result01 \_ Lockdown02 представляет доступные политики блокировки.'
ms.assetid: 78eab50e-b1a7-4b96-a848-b8a86a3b82c3
keywords:
- Класс MDM_Policy_Result01_LockDown02
- MDM_Policy_Result01_LockDown02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_LockDown02
- MDM_Policy_Result01_LockDown02.InstanceID
- MDM_Policy_Result01_LockDown02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 159e2178e3e5600bef4fc366a0cf49b7856ce886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490164"
---
# <a name="mdm_policy_result01_lockdown02-class"></a><span data-ttu-id="3be05-105">\_Класс политики MDM \_ Result01 \_ LockDown02</span><span class="sxs-lookup"><span data-stu-id="3be05-105">MDM\_Policy\_Result01\_LockDown02 class</span></span>

<span data-ttu-id="3be05-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="3be05-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3be05-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="3be05-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3be05-108">Класс **\_ политики MDM \_ Result01 \_ Lockdown02** представляет доступные политики блокировки.</span><span class="sxs-lookup"><span data-stu-id="3be05-108">The **MDM\_Policy\_Result01\_Lockdown02** class represents the lockdown policies available.</span></span>

<span data-ttu-id="3be05-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="3be05-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3be05-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3be05-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_LockDown02
{
  string InstanceID;
  string ParentID;
  sint32 AllowEdgeSwipe;
};
```

## <a name="members"></a><span data-ttu-id="3be05-111">Члены</span><span class="sxs-lookup"><span data-stu-id="3be05-111">Members</span></span>

<span data-ttu-id="3be05-112">Класс **\_ политики MDM \_ Result01 \_ LockDown02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3be05-112">The **MDM\_Policy\_Result01\_LockDown02** class has these types of members:</span></span>

-   [<span data-ttu-id="3be05-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="3be05-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3be05-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="3be05-114">Properties</span></span>

<span data-ttu-id="3be05-115">Класс **\_ политики MDM \_ Result01 \_ LockDown02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3be05-115">The **MDM\_Policy\_Result01\_LockDown02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3be05-116">алловеджесвипе</span><span class="sxs-lookup"><span data-stu-id="3be05-116">AllowEdgeSwipe</span></span>](/windows/client-management/mdm/policy-csp-lockdown#lockdown-allowedgeswipe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3be05-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="3be05-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3be05-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3be05-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3be05-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3be05-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3be05-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3be05-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3be05-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3be05-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3be05-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3be05-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3be05-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="3be05-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="3be05-124">Для этого класса строка имеет значение "Lockdown".</span><span class="sxs-lookup"><span data-stu-id="3be05-124">For this class, the string is "Lockdown".</span></span>

</dd> <dt>

<span data-ttu-id="3be05-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3be05-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3be05-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3be05-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3be05-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3be05-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3be05-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3be05-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3be05-129">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="3be05-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="3be05-130">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="3be05-130">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3be05-131">Требования</span><span class="sxs-lookup"><span data-stu-id="3be05-131">Requirements</span></span>



| <span data-ttu-id="3be05-132">Требование</span><span class="sxs-lookup"><span data-stu-id="3be05-132">Requirement</span></span> | <span data-ttu-id="3be05-133">Значение</span><span class="sxs-lookup"><span data-stu-id="3be05-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3be05-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3be05-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3be05-135">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3be05-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3be05-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3be05-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3be05-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3be05-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="3be05-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3be05-138">Namespace</span></span><br/>                | <span data-ttu-id="3be05-139">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="3be05-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="3be05-140">MOF</span><span class="sxs-lookup"><span data-stu-id="3be05-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3be05-141"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3be05-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="3be05-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3be05-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3be05-143"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3be05-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

