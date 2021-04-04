---
title: Класс MDM_DeviceStatus_Firewall01
description: Класс MDM \_ девицестатус \_ Firewall01 используется предприятием для запроса состояния соответствия брандмауэра устройствам с их политиками предприятия.
ms.assetid: 0f62350c-8c7b-44fb-b163-dedaf4669895
keywords:
- Класс MDM_DeviceStatus_Firewall01
- MDM_DeviceStatus_Firewall01 класс, описание
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Firewall01
- MDM_DeviceStatus_Firewall01.InstanceID
- MDM_DeviceStatus_Firewall01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67166a076b9e6db01d8642d7b1d21e72b8732c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803119"
---
# <a name="mdm_devicestatus_firewall01-class"></a><span data-ttu-id="2540c-105">\_Класс MDM девицестатус \_ Firewall01</span><span class="sxs-lookup"><span data-stu-id="2540c-105">MDM\_DeviceStatus\_Firewall01 class</span></span>

<span data-ttu-id="2540c-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="2540c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2540c-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="2540c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2540c-108">Класс **MDM \_ девицестатус \_ Firewall01** используется предприятием для запроса состояния соответствия брандмауэра устройствам с их политиками предприятия.</span><span class="sxs-lookup"><span data-stu-id="2540c-108">The **MDM\_DeviceStatus\_Firewall01** class is used by the enterprise to query the state of firewall compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="2540c-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="2540c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2540c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2540c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Firewall01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="2540c-111">Члены</span><span class="sxs-lookup"><span data-stu-id="2540c-111">Members</span></span>

<span data-ttu-id="2540c-112">Класс **MDM \_ девицестатус \_ Firewall01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2540c-112">The **MDM\_DeviceStatus\_Firewall01** class has these types of members:</span></span>

-   [<span data-ttu-id="2540c-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="2540c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2540c-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="2540c-114">Properties</span></span>

<span data-ttu-id="2540c-115">Класс **MDM \_ девицестатус \_ Firewall01** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2540c-115">The **MDM\_DeviceStatus\_Firewall01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2540c-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2540c-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2540c-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2540c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2540c-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2540c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2540c-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2540c-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2540c-120">Узел для запроса брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="2540c-120">Node for the firewall query.</span></span>

</dd> <dt>

<span data-ttu-id="2540c-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2540c-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2540c-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2540c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2540c-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2540c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2540c-124">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2540c-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2540c-125">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="2540c-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="2540c-126">Для этого класса строка имеет значение "./вендор/мсфт/девицестатус"</span><span class="sxs-lookup"><span data-stu-id="2540c-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="2540c-127">Состояние</span><span class="sxs-lookup"><span data-stu-id="2540c-127">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2540c-128">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2540c-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2540c-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2540c-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2540c-130">Требования</span><span class="sxs-lookup"><span data-stu-id="2540c-130">Requirements</span></span>



| <span data-ttu-id="2540c-131">Требование</span><span class="sxs-lookup"><span data-stu-id="2540c-131">Requirement</span></span> | <span data-ttu-id="2540c-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2540c-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2540c-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2540c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2540c-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2540c-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2540c-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2540c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2540c-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2540c-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2540c-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2540c-137">Namespace</span></span><br/>                | <span data-ttu-id="2540c-138">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="2540c-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2540c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2540c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2540c-140"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2540c-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2540c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2540c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2540c-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2540c-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

