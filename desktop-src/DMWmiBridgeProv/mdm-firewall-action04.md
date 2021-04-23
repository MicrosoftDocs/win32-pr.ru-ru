---
title: Класс MDM_Firewall_Action04
description: '\_ \_ Класс ACTION04 брандмауэра MDM используется для настройки параметров брандмауэра защитника Windows.'
ms.assetid: d0704662-ac2b-4ff5-a2c1-8f2bc7835488
keywords:
- Класс MDM_Firewall_Action04
- MDM_Firewall_Action04 класс, описание
topic_type:
- apiref
api_name:
- MDM_Firewall_Action04
- MDM_Firewall_Action04.InstanceID
- MDM_Firewall_Action04.ParentID
- MDM_Firewall_Action04.Type
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1eede757f6a3e129300e6d81a28d34248dda1f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489945"
---
# <a name="mdm_firewall_action04-class"></a><span data-ttu-id="61998-105">\_ \_ Класс ACTION04 брандмауэра MDM</span><span class="sxs-lookup"><span data-stu-id="61998-105">MDM\_Firewall\_Action04 class</span></span>

<span data-ttu-id="61998-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="61998-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="61998-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="61998-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="61998-108">\_ \_ Класс ACTION04 брандмауэра MDM используется для настройки параметров брандмауэра защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="61998-108">The MDM\_Firewall\_Action04 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="61998-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="61998-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="61998-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61998-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_Action04
{
  string InstanceID;
  string ParentID;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="61998-111">Члены</span><span class="sxs-lookup"><span data-stu-id="61998-111">Members</span></span>

<span data-ttu-id="61998-112">Класс **\_ \_ Action04 брандмауэра MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="61998-112">The **MDM\_Firewall\_Action04** class has these types of members:</span></span>

-   [<span data-ttu-id="61998-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="61998-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61998-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="61998-114">Properties</span></span>

<span data-ttu-id="61998-115">Класс **\_ \_ Action04 брандмауэра MDM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="61998-115">The **MDM\_Firewall\_Action04** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61998-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="61998-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61998-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="61998-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61998-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61998-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61998-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="61998-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="61998-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="61998-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61998-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="61998-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61998-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61998-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61998-123">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="61998-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="61998-124">**Тип**</span><span class="sxs-lookup"><span data-stu-id="61998-124">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61998-125">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="61998-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="61998-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="61998-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61998-127">Требования</span><span class="sxs-lookup"><span data-stu-id="61998-127">Requirements</span></span>



| <span data-ttu-id="61998-128">Требование</span><span class="sxs-lookup"><span data-stu-id="61998-128">Requirement</span></span> | <span data-ttu-id="61998-129">Значение</span><span class="sxs-lookup"><span data-stu-id="61998-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61998-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61998-130">Minimum supported client</span></span><br/> | <span data-ttu-id="61998-131">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="61998-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="61998-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61998-132">Minimum supported server</span></span><br/> | <span data-ttu-id="61998-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="61998-133">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="61998-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="61998-134">Namespace</span></span><br/>                | <span data-ttu-id="61998-135">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="61998-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="61998-136">MOF</span><span class="sxs-lookup"><span data-stu-id="61998-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61998-137"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61998-137"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="61998-138">DLL</span><span class="sxs-lookup"><span data-stu-id="61998-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61998-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61998-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

