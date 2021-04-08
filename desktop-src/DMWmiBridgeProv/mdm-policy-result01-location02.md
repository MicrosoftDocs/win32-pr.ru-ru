---
title: Класс MDM_Policy_Result01_Location02
description: '\_Класс политики MDM \_ Result01 \_ Location02 получает параметры службы расположения устройства.'
ms.assetid: f6d639db-c9d4-4d7e-b857-54aad602ea29
keywords:
- Класс MDM_Policy_Result01_Location02
- MDM_Policy_Result01_Location02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Location02
- MDM_Policy_Result01_Location02.InstanceID
- MDM_Policy_Result01_Location02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 210fb38e45e600e45590acecb9c647d00ab13995
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891769"
---
# <a name="mdm_policy_result01_location02-class"></a><span data-ttu-id="ebd4c-105">\_Класс политики MDM \_ Result01 \_ Location02</span><span class="sxs-lookup"><span data-stu-id="ebd4c-105">MDM\_Policy\_Result01\_Location02 class</span></span>

<span data-ttu-id="ebd4c-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="ebd4c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ebd4c-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="ebd4c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ebd4c-108">\_Класс политики MDM \_ Result01 \_ Location02 получает параметры службы расположения устройства.</span><span class="sxs-lookup"><span data-stu-id="ebd4c-108">The MDM\_Policy\_Result01\_Location02 class gets the settings of the location service of the device.</span></span>

<span data-ttu-id="ebd4c-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ebd4c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd4c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebd4c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Location02
{
  string InstanceID;
  string ParentID;
  sint32 EnableLocation;
};
```

## <a name="members"></a><span data-ttu-id="ebd4c-111">Члены</span><span class="sxs-lookup"><span data-stu-id="ebd4c-111">Members</span></span>

<span data-ttu-id="ebd4c-112">Класс **\_ политики MDM \_ Result01 \_ Location02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ebd4c-112">The **MDM\_Policy\_Result01\_Location02** class has these types of members:</span></span>

-   [<span data-ttu-id="ebd4c-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="ebd4c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ebd4c-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="ebd4c-114">Properties</span></span>

<span data-ttu-id="ebd4c-115">Класс **\_ политики MDM \_ Result01 \_ Location02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ebd4c-115">The **MDM\_Policy\_Result01\_Location02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ebd4c-116">**EnableLocation**</span><span class="sxs-lookup"><span data-stu-id="ebd4c-116">**EnableLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebd4c-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ebd4c-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ebd4c-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ebd4c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ebd4c-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ebd4c-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebd4c-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ebd4c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ebd4c-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ebd4c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebd4c-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ebd4c-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ebd4c-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ebd4c-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebd4c-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ebd4c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ebd4c-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ebd4c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebd4c-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ebd4c-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ebd4c-127">Требования</span><span class="sxs-lookup"><span data-stu-id="ebd4c-127">Requirements</span></span>



| <span data-ttu-id="ebd4c-128">Требование</span><span class="sxs-lookup"><span data-stu-id="ebd4c-128">Requirement</span></span> | <span data-ttu-id="ebd4c-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ebd4c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd4c-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ebd4c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd4c-131">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ebd4c-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ebd4c-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ebd4c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd4c-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ebd4c-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ebd4c-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ebd4c-134">Namespace</span></span><br/>                | <span data-ttu-id="ebd4c-135">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="ebd4c-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ebd4c-136">MOF</span><span class="sxs-lookup"><span data-stu-id="ebd4c-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ebd4c-137"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ebd4c-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ebd4c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ebd4c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebd4c-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebd4c-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

