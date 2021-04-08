---
title: Класс MDM_DeviceStatus_Antispyware01
description: Класс MDM \_ девицестатус \_ Antispyware01 используется предприятием для запроса состояния антишпионской совместимости устройств с корпоративными политиками.
ms.assetid: 53275aa1-ff7d-4630-b6c5-aedce3f4665a
keywords:
- Класс MDM_DeviceStatus_Antispyware01
- MDM_DeviceStatus_Antispyware01 класс, описание
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Antispyware01
- MDM_DeviceStatus_Antispyware01.InstanceID
- MDM_DeviceStatus_Antispyware01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91468c98981c93e211b3e3bee99564574f7a56cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892318"
---
# <a name="mdm_devicestatus_antispyware01-class"></a><span data-ttu-id="500af-105">\_Класс MDM девицестатус \_ Antispyware01</span><span class="sxs-lookup"><span data-stu-id="500af-105">MDM\_DeviceStatus\_Antispyware01 class</span></span>

<span data-ttu-id="500af-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="500af-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="500af-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="500af-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="500af-108">Класс **MDM \_ девицестатус \_ Antispyware01** используется предприятием для запроса состояния антишпионской совместимости устройств с корпоративными политиками.</span><span class="sxs-lookup"><span data-stu-id="500af-108">The **MDM\_DeviceStatus\_Antispyware01** class is used by the enterprise to query the state of antispyware compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="500af-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="500af-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="500af-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="500af-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Antispyware01
{
  string InstanceID;
  string ParentID;
  sint32 SignatureStatus;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="500af-111">Члены</span><span class="sxs-lookup"><span data-stu-id="500af-111">Members</span></span>

<span data-ttu-id="500af-112">Класс **MDM \_ девицестатус \_ Antispyware01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="500af-112">The **MDM\_DeviceStatus\_Antispyware01** class has these types of members:</span></span>

-   [<span data-ttu-id="500af-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="500af-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="500af-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="500af-114">Properties</span></span>

<span data-ttu-id="500af-115">Класс **MDM \_ девицестатус \_ Antispyware01** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="500af-115">The **MDM\_DeviceStatus\_Antispyware01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="500af-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="500af-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="500af-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="500af-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="500af-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="500af-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="500af-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="500af-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="500af-120">Узел для запроса защиты от шпионских программ.</span><span class="sxs-lookup"><span data-stu-id="500af-120">Node for the antispyware query.</span></span>

</dd> <dt>

<span data-ttu-id="500af-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="500af-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="500af-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="500af-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="500af-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="500af-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="500af-124">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="500af-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="500af-125">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="500af-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="500af-126">Для этого класса строка имеет значение "./вендор/мсфт/девицестатус"</span><span class="sxs-lookup"><span data-stu-id="500af-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="500af-127">сигнатурестатус</span><span class="sxs-lookup"><span data-stu-id="500af-127">SignatureStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-antivirus-signaturestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="500af-128">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="500af-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="500af-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="500af-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="500af-130">Состояние</span><span class="sxs-lookup"><span data-stu-id="500af-130">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="500af-131">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="500af-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="500af-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="500af-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="500af-133">Требования</span><span class="sxs-lookup"><span data-stu-id="500af-133">Requirements</span></span>



| <span data-ttu-id="500af-134">Требование</span><span class="sxs-lookup"><span data-stu-id="500af-134">Requirement</span></span> | <span data-ttu-id="500af-135">Значение</span><span class="sxs-lookup"><span data-stu-id="500af-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="500af-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="500af-136">Minimum supported client</span></span><br/> | <span data-ttu-id="500af-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="500af-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="500af-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="500af-138">Minimum supported server</span></span><br/> | <span data-ttu-id="500af-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="500af-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="500af-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="500af-140">Namespace</span></span><br/>                | <span data-ttu-id="500af-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="500af-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="500af-142">MOF</span><span class="sxs-lookup"><span data-stu-id="500af-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="500af-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="500af-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="500af-144">DLL</span><span class="sxs-lookup"><span data-stu-id="500af-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="500af-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="500af-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

