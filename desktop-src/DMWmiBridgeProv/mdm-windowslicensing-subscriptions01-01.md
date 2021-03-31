---
title: Класс MDM_WindowsLicensing_Subscriptions01_01
description: Класс MDM \_ виндовслиценсинг \_ Subscriptions01 \_ 01 предназначен для сценариев управления лицензированием, связанных с подпиской.
ms.assetid: dc3b7eae-89d3-4e66-a65f-f100e23ea9fd
keywords:
- Класс MDM_WindowsLicensing_Subscriptions01_01
- MDM_WindowsLicensing_Subscriptions01_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing_Subscriptions01_01
- MDM_WindowsLicensing_Subscriptions01_01.InstanceID
- MDM_WindowsLicensing_Subscriptions01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911c578bd0e3cbc56c61f2cf85438660e8f437b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136738"
---
# <a name="mdm_windowslicensing_subscriptions01_01-class"></a><span data-ttu-id="1fec2-105">\_Класс MDM виндовслиценсинг \_ Subscriptions01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="1fec2-105">MDM\_WindowsLicensing\_Subscriptions01\_01 class</span></span>

<span data-ttu-id="1fec2-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="1fec2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1fec2-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="1fec2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1fec2-108">Класс **MDM \_ виндовслиценсинг \_ Subscriptions01 \_ 01** предназначен для сценариев управления лицензированием, связанных с подпиской.</span><span class="sxs-lookup"><span data-stu-id="1fec2-108">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class is designed for subscription-related licensing management scenarios.</span></span>

<span data-ttu-id="1fec2-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1fec2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fec2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fec2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing_Subscriptions01_01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="1fec2-111">Члены</span><span class="sxs-lookup"><span data-stu-id="1fec2-111">Members</span></span>

<span data-ttu-id="1fec2-112">Класс **MDM \_ виндовслиценсинг \_ Subscriptions01 \_ 01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1fec2-112">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="1fec2-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1fec2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1fec2-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="1fec2-114">Properties</span></span>

<span data-ttu-id="1fec2-115">Класс **MDM \_ виндовслиценсинг \_ Subscriptions01 \_ 01** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="1fec2-115">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1fec2-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1fec2-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fec2-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fec2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fec2-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fec2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fec2-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1fec2-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1fec2-120">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="1fec2-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="1fec2-121">Name</span><span class="sxs-lookup"><span data-stu-id="1fec2-121">Name</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fec2-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fec2-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fec2-123">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1fec2-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1fec2-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1fec2-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fec2-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fec2-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fec2-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fec2-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fec2-127">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1fec2-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1fec2-128">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="1fec2-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="1fec2-129">Для этого класса строка имеет значение "./вендор/мсфт/виндовслиценсинг"</span><span class="sxs-lookup"><span data-stu-id="1fec2-129">For this class, the string is "./Vendor/MSFT/WindowsLicensing"</span></span>

</dd> <dt>

[<span data-ttu-id="1fec2-130">Состояние</span><span class="sxs-lookup"><span data-stu-id="1fec2-130">Status</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fec2-131">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1fec2-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fec2-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1fec2-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1fec2-133">Требования</span><span class="sxs-lookup"><span data-stu-id="1fec2-133">Requirements</span></span>



| <span data-ttu-id="1fec2-134">Требование</span><span class="sxs-lookup"><span data-stu-id="1fec2-134">Requirement</span></span> | <span data-ttu-id="1fec2-135">Значение</span><span class="sxs-lookup"><span data-stu-id="1fec2-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fec2-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1fec2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1fec2-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1fec2-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1fec2-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1fec2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1fec2-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1fec2-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1fec2-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1fec2-140">Namespace</span></span><br/>                | <span data-ttu-id="1fec2-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="1fec2-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1fec2-142">MOF</span><span class="sxs-lookup"><span data-stu-id="1fec2-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fec2-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1fec2-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fec2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="1fec2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fec2-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fec2-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

