---
title: Класс MDM_DeviceStatus_OS01
description: Класс MDM \_ девицестатус \_ OS01 используется предприятием для запроса операционной системы на устройствах с их политиками предприятия.
ms.assetid: 887dc453-f6b5-4f09-8ce1-b87f71dd8396
keywords:
- Класс MDM_DeviceStatus_OS01
- MDM_DeviceStatus_OS01 класс, описание
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_OS01
- MDM_DeviceStatus_OS01.InstanceID
- MDM_DeviceStatus_OS01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01bff7a57d71b3d651ea2b97a0eac5b2ccd94255
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136779"
---
# <a name="mdm_devicestatus_os01-class"></a><span data-ttu-id="1f7c5-105">\_Класс MDM девицестатус \_ OS01</span><span class="sxs-lookup"><span data-stu-id="1f7c5-105">MDM\_DeviceStatus\_OS01 class</span></span>

<span data-ttu-id="1f7c5-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="1f7c5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1f7c5-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="1f7c5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1f7c5-108">Класс **MDM \_ девицестатус \_ OS01** используется предприятием для запроса операционной системы на устройствах с их политиками предприятия.</span><span class="sxs-lookup"><span data-stu-id="1f7c5-108">The **MDM\_DeviceStatus\_OS01** class is used by the enterprise to query the operating system on devices with their enterprise policies.</span></span>

<span data-ttu-id="1f7c5-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1f7c5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f7c5-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f7c5-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_OS01
{
  string InstanceID;
  string ParentID;
  string Edition;
};
```

## <a name="members"></a><span data-ttu-id="1f7c5-111">Члены</span><span class="sxs-lookup"><span data-stu-id="1f7c5-111">Members</span></span>

<span data-ttu-id="1f7c5-112">Класс **MDM \_ девицестатус \_ OS01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1f7c5-112">The **MDM\_DeviceStatus\_OS01** class has these types of members:</span></span>

-   [<span data-ttu-id="1f7c5-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1f7c5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1f7c5-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="1f7c5-114">Properties</span></span>

<span data-ttu-id="1f7c5-115">Класс **MDM \_ девицестатус \_ OS01** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1f7c5-115">The **MDM\_DeviceStatus\_OS01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1f7c5-116">Выпуск</span><span class="sxs-lookup"><span data-stu-id="1f7c5-116">Edition</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-os-edition)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f7c5-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1f7c5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f7c5-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1f7c5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1f7c5-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1f7c5-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f7c5-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1f7c5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f7c5-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f7c5-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f7c5-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1f7c5-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1f7c5-123">Узел для запроса ОС.</span><span class="sxs-lookup"><span data-stu-id="1f7c5-123">Node for the OS query.</span></span>

</dd> <dt>

<span data-ttu-id="1f7c5-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1f7c5-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f7c5-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1f7c5-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f7c5-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f7c5-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f7c5-127">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1f7c5-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1f7c5-128">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="1f7c5-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="1f7c5-129">Для этого класса строка имеет значение "./вендор/мсфт/девицестатус"</span><span class="sxs-lookup"><span data-stu-id="1f7c5-129">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f7c5-130">Требования</span><span class="sxs-lookup"><span data-stu-id="1f7c5-130">Requirements</span></span>



| <span data-ttu-id="1f7c5-131">Требование</span><span class="sxs-lookup"><span data-stu-id="1f7c5-131">Requirement</span></span> | <span data-ttu-id="1f7c5-132">Значение</span><span class="sxs-lookup"><span data-stu-id="1f7c5-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f7c5-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f7c5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1f7c5-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1f7c5-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1f7c5-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f7c5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1f7c5-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1f7c5-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1f7c5-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1f7c5-137">Namespace</span></span><br/>                | <span data-ttu-id="1f7c5-138">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="1f7c5-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1f7c5-139">MOF</span><span class="sxs-lookup"><span data-stu-id="1f7c5-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f7c5-140"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f7c5-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f7c5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1f7c5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f7c5-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f7c5-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

